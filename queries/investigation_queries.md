# Investigation Queries

# Spear Phishing Detection Queries

## View Suspicious Email Events

index=email

| table _time, sender, recipient, subject, url, attachment

| sort _time

## Detect Suspicious Sender Domains

index=email

| eval sender_domain=mvindex(split(sender,"@"),1)

| stats count by sender_domain

| sort -count

## Identify Potential Spoofed Emails

index=email

| eval sender_domain=mvindex(split(sender,"@"),1)

| eval display_name=sender

| table _time, sender, sender_domain, subject

## Detect Emails Containing URLs

index=email

| search url="http*"

| table _time, sender, recipient, url, subject

## Detect Emails with Attachments

index=email

| search attachment="*"

| table _time, sender, recipient, attachment, subject

