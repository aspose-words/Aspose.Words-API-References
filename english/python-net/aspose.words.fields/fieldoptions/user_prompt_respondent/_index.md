---
title: FieldOptions.user_prompt_respondent property
linktitle: user_prompt_respondent property
articleTitle: user_prompt_respondent property
second_title: Aspose.Words for Python
description: "FieldOptions.user_prompt_respondent property. Gets or sets the respondent to user prompts during field update."
type: docs
weight: 210
url: /python-net/aspose.words.fields/fieldoptions/user_prompt_respondent/
---

## FieldOptions.user_prompt_respondent property

Gets or sets the respondent to user prompts during field update.


```python
@property
def user_prompt_respondent(self) -> aspose.words.fields.IFieldUserPromptRespondent:
    ...

@user_prompt_respondent.setter
def user_prompt_respondent(self, value: aspose.words.fields.IFieldUserPromptRespondent):
    ...

```

### Remarks

If the value of this property is set to ``None``, the fields that require user response on prompting
(such as [FieldAsk](../../fieldask/) or [FieldFillIn](../../fieldfillin/)) are not updated.

The default value is ``None``.




### See Also

* module [aspose.words.fields](../../)
* class [FieldOptions](../)

