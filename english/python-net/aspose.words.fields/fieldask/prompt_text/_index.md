---
title: FieldAsk.prompt_text property
linktitle: prompt_text property
articleTitle: prompt_text property
second_title: Aspose.Words for Python
description: "FieldAsk.prompt_text property. Gets or sets the prompt text (the title of the prompt window)."
type: docs
weight: 50
url: /python-net/aspose.words.fields/fieldask/prompt_text/
---

## FieldAsk.prompt_text property

Gets or sets the prompt text (the title of the prompt window).


```python
@property
def prompt_text(self) -> str:
    ...

@prompt_text.setter
def prompt_text(self, value: str):
    ...

```

### Examples

Shows how to create an ASK field, and set its properties (MyPromptRespondent).

```python
class MyPromptRespondent(aw.fields.IFieldUserPromptRespondent):

    def respond(self, prompt_text, default_response):
        return 'Response from MyPromptRespondent. ' + default_response
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldAsk](../)

