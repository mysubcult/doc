---
id: multiple-languages
title: Multiple Languages
---

## Introduction

You can create a single bot that supports multiple languages by translating all the messages within the bot-building interface. To achieve this, you need to follow a few simple guidelines.

## Translating Bot Messages

To start translating bot messages, you must first write the messages in a specific format. Refer to the [Text Messages](text.md#text-message) section for more details.

For example, if your message is `{welcome_message__Welcome message}`, the message identifier would be `welcome_message`.

## Translation Groups

The next step is to create a translation group. Navigate to:
> **System Configuration -> Translation Groups**

Here, you can create a new translation group.

:::tip
In addition to creating a translation group, you can also customize the bot's photo and nickname for each language.
:::

## Setting a Translation Group

To assign a translation group, edit the `Department` settings and, under the `Bot Configuration` tab, select the desired translation group.

## Translating Messages

Once you click on a translation group, you will see a list of `Translation Items`. The window should look like this:

![](/img/bot/translations-groups.png)

From here, you can create a new translated message:

![](/img/bot/translation-item.png)

## Automatic Translation of Translation Items

This feature allows you to automatically translate items if a translation for the user's language is not found in the `Translation Items`. It provides fine-grained control over which messages should use automatic translations.

To enable automatic translations for specific messages within `Translation Items`, check the following option:
> **If translation is not found, use translation service**

![](/img/bot/translation-auto.png)

For this to work, you must define the default language in the `Bot Individualization` group:
> **For automatic translations, we need to know the bot's main language. This will be the source language for translating bot messages.**

![](/img/bot/bot-translation-group.png)

Additionally, the automatic translation service must be properly configured.

## Automatic Translation of All Triggers

Most common triggers used to send information to users have an `Automatic Translation` option. Only triggers with this option enabled will be automatically translated.

![](/img/bot/translate-trigger.png)

For this feature to work, the automatic translation service must be configured.

:::note
- **If you are translating all trigger responses, you should not use translation identifiers.**
- To improve performance, enable caching in the `Automatic Translations` configuration window.
:::

## Required Permissions

The only permission required to work with bot translations is:
> **'lhbot', 'use'**
