---
title: respond method
second_title: Aspose.Words for Python via .NET API Reference
description: "When implemented, returns a response from the user on prompting"
type: docs
weight: 10
url: /python-net/aspose.words.fields/ifielduserpromptrespondent/respond/
---

## respond(prompt_text, default_response) {#str_str}

When implemented, returns a response from the user on prompting.
Your implementation should return **null** to indicate that the user has not responded to the prompt
(i.e. the user has pressed the Cancel button in the prompt window).



```python
def respond(self, prompt_text: str, default_response: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| prompt_text | str |  |
| default_response | str |  |

### Returns

User response (i.e. confirmed value contained in the prompt window).


### See Also

* module [aspose.words.fields](../../)
* class [IFieldUserPromptRespondent](../)

