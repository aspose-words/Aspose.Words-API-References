---
title: IFieldUserPromptRespondent
second_title: Aspose.Words for Java API Reference
description: Represents the respondent to user prompts during field update.
type: docs
weight: 649
url: /java/com.aspose.words/ifielduserpromptrespondent/
---
```
public interface IFieldUserPromptRespondent
```

Represents the respondent to user prompts during field update. The ASK and FILLIN fields are the examples of fields that prompt the user for some response. Implement this interface and assign it to the [FieldOptions.getUserPromptRespondent()](../../com.aspose.words/fieldoptions\#getUserPromptRespondent) / [FieldOptions.setUserPromptRespondent(com.aspose.words.IFieldUserPromptRespondent)](../../com.aspose.words/fieldoptions\#setUserPromptRespondent-com.aspose.words.IFieldUserPromptRespondent) property to establish interaction between field update and the user.
## Methods

| Method | Description |
| --- | --- |
| [respond(String promptText, String defaultResponse)](#respond-java.lang.String-java.lang.String) | When implemented, returns a response from the user on prompting. |
### respond(String promptText, String defaultResponse) {#respond-java.lang.String-java.lang.String}
```
public abstract String respond(String promptText, String defaultResponse)
```


When implemented, returns a response from the user on prompting. Your implementation should return  null  to indicate that the user has not responded to the prompt (i.e. the user has pressed the Cancel button in the prompt window).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| promptText | java.lang.String | Prompt text (i.e. title of the prompt window). |
| defaultResponse | java.lang.String | Default user response (i.e. initial value contained in the prompt window). |

**Returns:**
java.lang.String - User response (i.e. confirmed value contained in the prompt window).
