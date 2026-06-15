---
title: FieldAsk.prompt_once_on_mail_merge property
linktitle: prompt_once_on_mail_merge property
articleTitle: prompt_once_on_mail_merge property
second_title: Aspose.Words for Python
description: "FieldAsk.prompt_once_on_mail_merge property. Gets or sets whether the user response should be recieved once per a mail merge operation."
type: docs
weight: 40
url: /python-net/aspose.words.fields/fieldask/prompt_once_on_mail_merge/
---

## FieldAsk.prompt_once_on_mail_merge property

Gets or sets whether the user response should be recieved once per a mail merge operation.


```python
@property
def prompt_once_on_mail_merge(self) -> bool:
    ...

@prompt_once_on_mail_merge.setter
def prompt_once_on_mail_merge(self, value: bool):
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

