---
title: FormField.help_text property
linktitle: help_text property
articleTitle: help_text property
second_title: Aspose.Words for Python
description: "FormField.help_text property. Returns or sets the text that's displayed in a message box when the form field has the focus and the user presses F1."
type: docs
weight: 100
url: /python-net/aspose.words.fields/formfield/help_text/
---

## FormField.help_text property

Returns or sets the text that's displayed in a message box when the form field has the focus and the user presses F1.


```python
@property
def help_text(self) -> str:
    ...

@help_text.setter
def help_text(self, value: str):
    ...

```

### Remarks

If the [FormField.own_help](../own_help/) property is set to ``True``, [FormField.help_text](./) specifies the text string value.
If [FormField.own_help](../own_help/) is set to ``False``, [FormField.help_text](./) specifies the name of an AutoText entry that contains help
text for the form field.

Microsoft Word allows strings with at most 255 characters.




### See Also

* module [aspose.words.fields](../../)
* class [FormField](../)

