---
title: IFieldUserPromptRespondent.respond method
linktitle: respond method
articleTitle: respond method
second_title: Aspose.Words for Python
description: "IFieldUserPromptRespondent.respond method. When implemented, returns a response from the user on prompting"
type: docs
weight: 10
url: /python-net/aspose.words.fields/ifielduserpromptrespondent/respond/
---

## respond(prompt_text, default_response) {#str_str}

When implemented, returns a response from the user on prompting.
Your implementation should return ``None`` to indicate that the user has not responded to the prompt
(i.e. the user has pressed the Cancel button in the prompt window).



```python
def respond(self, prompt_text: str, default_response: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| prompt_text | str | Prompt text (i.e. title of the prompt window). |
| default_response | str | Default user response (i.e. initial value contained in the prompt window). |

### Returns

User response (i.e. confirmed value contained in the prompt window).


### See Also

* module [aspose.words.fields](../../)
* class [IFieldUserPromptRespondent](../)

