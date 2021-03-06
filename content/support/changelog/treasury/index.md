---
layout: layout-sidebar
name: Treasury (Beta)
description: Information on additions and changes for the Treasury API (Beta).
order: 225
published: true
showInNav: true
icon: fa fa-money
back_to_top: true
title: Treasury (Beta) Changelog
---

# {{ name }}

Monitor this page to keep up with the [Treasury API (Beta)]({{ stache.config.portal_endpoints_treasury }}) latest changes and {{ stache.config.api_type_name }} service releases.

## 2018-04-26

### Changed

- For the  [Bank account (List)]({{ stache.config.portal_endpoints_bank_account_list }}) endpoint, the `bank_name` field is now included in the list of returned objects separate from `account_name`.
- The  [Bank account register (List)]({{ stache.config.portal_endpoints_bank_account_register_list }}), [Checks (List)]({{ stache.config.portal_endpoints_checks_list }}), [Deposits (List)]({{ stache.config.portal_endpoints_deposits_list }}), and [Adjustments (List)]({{ stache.config.portal_endpoints_adjustments_list }}) endpoints now return the `transaction_id` field. This field helps to ensure that "register" items correctly map to checks, deposits, and adjustments.

## January 2018

### 2018-01-17

#### Changed

For the  [Checks (List)]({{ stache.config.portal_endpoints_checks_list }}) endpoint, we made the following changes:

- The new `payee` field is now returned in the listed objects.
- The list is now sorted by check number (ascending).
- We added the `starting_check_number` and `ending_check_number` variables to the check filter. When only `starting_check_number` is provided, a list of checks (starting with that number and higher) is returned. When only `ending_check_number` is provided, a list of checks (less than or equal to that number) is returned. When both variables are provided, a range of checks is returned.

## April 2017

### 2017-04-25

#### New

The Treasury API has been released for a public beta. This API handles information related to bank accounts, including related entities such as adjustments, checks, and deposits.

The initial release contains endpoints to retrieve a list of all bank accounts and all bank account transactions, and to manage deposits, cash receipts, and adjustments. For more information, check out the [entity]({{ stache.config.treasury_entity_reference }}) and [endpoint]({{ stache.config.portal_endpoints_treasury }}) references.
