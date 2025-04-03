---
title: IFieldUserPromptRespondent.respond method
linktitle: respond method
articleTitle: respond method
second_title: Aspose.Words for NodeJs
description: "IFieldUserPromptRespondent.respond method. When implemented, returns a response from the user on prompting"
type: docs
weight: 10
url: /nodejs-net/Aspose.Words.Fields/ifielduserpromptrespondent/respond/
---

## respond(promptText, defaultResponse) {#string_string}

When implemented, returns a response from the user on prompting.
Your implementation should return ``null`` to indicate that the user has not responded to the prompt
(i.e. the user has pressed the Cancel button in the prompt window).



```js
respond(promptText: stringdefaultResponse: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| promptText | string | Prompt text (i.e. title of the prompt window). |
| defaultResponse | string | Default user response (i.e. initial value contained in the prompt window). |

### Returns

User response (i.e. confirmed value contained in the prompt window).


### See Also

* module [Aspose.Words.Fields](../../)
* class [IFieldUserPromptRespondent](../)

