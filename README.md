# Dotdigital ChatGraphQl
[![Packagist Version](https://img.shields.io/packagist/v/dotdigital/dotdigital-magento2-extension-chat-graph-ql?color=green&label=stable)](https://github.com/dotmailer/dotmailer-magento2-extension-chat-graph-ql/releases)
[![license](https://img.shields.io/github/license/mashape/apistatus.svg)](LICENSE.md)

## About this module
**Dotdigitalgroup_ChatGraphQl** supports our [Dotdigital Chat](https://github.com/dotmailer/dotmailer-magento2-extension-chat) module.
It provides type and resolver information for Magento to generate endpoints for:
- fetching chat configuration data from the instance
- sending customer data to update the chat profile

## Requirements
- This module requires the `Dotdigitalgroup_Chat` module v1.6.0+

## Installation
- This module is included in our core extension. Please refer to [these instructions](https://github.com/dotmailer/dotmailer-magento2-extension#installation) to install via the Magento Marketplace.

## Endpoints

**Queries**
```
query GetChatData {
        chatData {
            is_enabled
            api_space_id
            cookie_name
        }
    }
```

**Mutations**
```
mutation UpdateChatProfile(
        $profileId: String!,
        $email: String,
        $firstname: String,
        $lastname: String
    ) {
        updateChatProfile(
            profileId: $profileId,
            email: $email,
            firstname: $firstname,
            lastname: $lastname
        )
    }
```

## Changelog

### 1.1.4

##### Improvements
- We updated a dependency on the parent Chat module.

### 1.1.3

##### Improvements
- We updated our code for compatibility with PHP 8.4.

### 1.1.2

##### Improvements
- We've updated the module's dependencies. The module now requires PHP 7.4+ and Magento 2.3.7+.

### 1.1.1

##### Improvements
- We updated our installation instructions.

### 1.1.0

##### What's new
- This module has been renamed `dotdigital/dotdigital-magento2-extension-chat-graph-ql`.

##### Improvements
- `setup_version` has been removed from module.xml.

### 1.0.0
- Initial release
