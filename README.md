# Starbucks Rewards Program Analysis

## Overview

As a means to attract and retain customers, Starbucks uses a rewards program that honors regular customers with special offers not available to the standard customer. For this project, I'll be combing through some fabricated customer and offer data provided by Udacity to understand how Starbucks may choose to alter its rewards program to better suit specific customer segments.

## Datasets and Inputs
- **Buy-One-Get-One (BOGO)**: In this particular offer, a customer is given a reward that enables them to receive an extra, equal product at no cost. The customer must spend a certain threshold in order to make this reward available.
- **Discount**: With this offer, a customer is given a reward that knocks a certain percentage off the original cost of the product they are choosing to purchase, subject to limitations.
- **Informational**: With this final offer, there isn’t necessarily a reward but rather an opportunity for a customer to purchase a certain object given a requisite amount of money. (This might be something like letting customers know that Pumpkin Spice Latte is coming available again toward the beginning of autumn.)

The three provided JSON files and their respective elements:

**profile.json**
This file contains dummy information about Rewards program users. This will serve as the basis for basic customer information.
(17000 users x 5 fields)
  - gender: (categorical) M, F, O, or null
  - age: (numeric) missing value encoded as 118
  - id: (string / hash)
  - became_member_on: (date) format YYYYMMDD
  - income: (numeric)

**portfolio.json**
This file contains offers sent during a 30-day test period. This will serve as the basis to understand our customers’ purchasing patterns.
(10 offers x 6 fields)
  - reward: (numeric) money awarded for the amount spent
  - channels: (list) web, email, mobile, social
  - difficulty: (numeric) money required to be spent to receive reward
  - duration: (numeric) time for offer to be open, in days
  - offer_type: (string) bogo, discount, informational
  - id: (string / hash)

**transcript.json**
This file contains event log information. Complementing the file above, this file will serve as a more granular look into customer behavior.
(306648 events x 4 fields)
  - person: (string / hash)
  - event: (string) offer received, offer viewed, transaction, offer completed
  - value: (dictionary) different values depending on the event type
  - offer id : (string / hash) not associated with any “transaction”
  - amount: (numeric) money spent in “transaction”
  - reward: (numeric) money gained from “offer completed”
  - time: (numeric) hours after start of test

## Acknowledgements

Special thanks again to Starbucks and Udacity for providing the data utilized in this project!
