---
title: FormField.text_input_format property
linktitle: text_input_format property
articleTitle: text_input_format property
second_title: Aspose.Words for Python
description: "FormField.text_input_format property. Returns or sets the text formatting for a text form field."
type: docs
weight: 200
url: /python-net/aspose.words.fields/formfield/text_input_format/
---

## FormField.text_input_format property

Returns or sets the text formatting for a text form field.


```python
@property
def text_input_format(self) -> str:
    ...

@text_input_format.setter
def text_input_format(self, value: str):
    ...

```

### Remarks

If the text form field contains regular text, then valid format strings are
"", "UPPERCASE", "LOWERCASE", "FIRST CAPITAL" and "TITLE CASE". The strings
are case-insensitive.

If the text form field contains a number or a date/time value, then valid
format strings are number or date and time format strings.

Microsoft Word allows strings with at most 64 characters.




### See Also

* module [aspose.words.fields](../../)
* class [FormField](../)

