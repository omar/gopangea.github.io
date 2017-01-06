---
title: Copy Editing
---

To manage copy in the applications, we use [POEditor](https://poeditor.com) to track the values of our copy keys.

## Naming Convention

- Case 1: Static Text on the screen
  - [ScreenName].[FirstTwoWordsOrMoreIfNeeded]

- Case 2: Pop Up messages
  - Title: [ScreenName].[PopUpName].Title (Optional)
  - Text: [ScreenName].[PopUpName].Text

- Case 3: Text to be used as property (ex. Facebook share message)
  - Title: [ScreenName].[PropertyName].Title (Optional)
  - Text: [ScreenName].[PropertyName].Text

- Case 4: Locally generated error messages:
  - [ScreenName].Error.[FirstTwoWordsOrMoreIfNeeded]

- Case 5: API Error Message:
  - Look for message with Group_Code key in Data field
  - If Data field null, look for message with Group_Key for the API  Exception 
  - If Group code is null, look for message in message field
  - Finally default Generic message label - “api_exception_generic”

- Case 6: Unique key for each app:
  - If key is unique for ios, android or web, add the new key still to  -  commons project and add app suffix. Here are the steps
  - Key - Create a POEditor key based on above naming convention
  - Add app suffix - .ios, .andorid, .web
  - So the final format is {{KEY}}.{{APP_SUFFIX}}

- Case 7: Macro
    - If a key needs a value inject into it, then denote that with double curly braces.
      For example, to inject a value into the key, create a key with the value
      > `You have {% raw %}{{ ReferralAmount }}{% endraw %}`
    - If the macro value can be represented as an object, use dot notation instead to denote the property.
      For example, to inject the name of a `Receiver` into the key, create a key with hte value:
      > `Send again to {% raw %}{{ Receiver.FirstName }}`{% endraw %}.  


## Creating or Updating Keys

As a rule, **never update copy keys that are already in use**, only add new keys. This rule ensures that engineers can pull the latest copy keys used in the apps with confidence that the keys that they're using are not still under review or are still a work in progress. This becomes more relevant when doing a hotfix release that doesn't have any copy updates.

### New Keys

1. Add the key in POEditor.
2. Add the values for each language.
3. Include the new keys in the relevant product tickets.

### Updating Existing Keys

As an example, let's assume we want to update the key `FX.RepeatLastTransfer.CallToAction` value from `Repeat your Transfer!` to `Send again!`. Given this key is already in use, we must: 

1. Create the new key in POEditor using the same name but an increment to the version: `FX.RepeatLastTransfer.CallToAction.1`.
2. Add the values for each language.
3. Include the new keys in the relevant product tickets.

The engineer(s) working on the feature will then implement the new key in the code and publish the changes.

