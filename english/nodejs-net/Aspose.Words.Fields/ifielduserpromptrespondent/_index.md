---
title: IFieldUserPromptRespondent class
linktitle: IFieldUserPromptRespondent class
articleTitle: IFieldUserPromptRespondent class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Fields.IFieldUserPromptRespondent class. Represents the respondent to user prompts during field update."
type: docs
weight: 1260
url: /nodejs-net/Aspose.Words.Fields/ifielduserpromptrespondent/
---

## IFieldUserPromptRespondent class

Represents the respondent to user prompts during field update.


### Remarks

The ASK and FILLIN fields are the examples of fields that prompt the user for some response. Implement this interface
and assign it to the [FieldOptions.userPromptRespondent](../fieldoptions/userPromptRespondent/) property to establish interaction between field update
and the user.



### Methods

| Name | Description |
| --- | --- |
|[ respond(promptText, defaultResponse)](./respond/#string_string) | When implemented, returns a response from the user on prompting. Your implementation should return ``None`` to indicate that the user has not responded to the prompt (i.e. the user has pressed the Cancel button in the prompt window). |

### See Also

* module [Aspose.Words.Fields](../)

