# Investigation Queries

This section contains the Splunk queries used to investigate the spear phishing activity.

---

## 1. Identify Suspicious Senders

This query identifies the most active email senders and their source IPs.

index=email

| stats count by sender src_ip

| sort -count

## 2. Detect Emails Containing URLs (Phishing Indicator)

This query filters emails that contain links, which are common in phishing attacks.

index=email url=*

| table _time sender recipient url src_ip

## 3. Identify Users Who Clicked Malicious Links

This query shows users who interacted with phishing emails.

index=email status="Clicked"

| table _time recipient src_ip url

## 4. Extract Domain from Suspicious URLs

This query extracts domains from URLs using rex for analysis.

index=email url=*

| rex field=url "http://(?<domain>[^/]+)"

| stats count by domain

## 5. Investigate Attacker Activity Timeline

This query reconstructs activity from the suspected malicious IP.

index=email src_ip="185.23.45.2"

| sort _time
