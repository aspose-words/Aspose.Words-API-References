---
title: FormField.text_input_default property
linktitle: text_input_default property
articleTitle: text_input_default property
second_title: Aspose.Words for Python
description: "FormField.text_input_default property. Gets or sets the default string or a calculation expression of a text form field."
type: docs
weight: 190
url: /python-net/aspose.words.fields/formfield/text_input_default/
---

## FormField.text_input_default property

Gets or sets the default string or a calculation expression of a text form field.

The meaning of this property depends on the value of the [FormField.text_input_type](../text_input_type/) property.

When [FormField.text_input_type](../text_input_type/) is [TextFormFieldType.REGULAR](../../textformfieldtype/#REGULAR) or
[TextFormFieldType.NUMBER](../../textformfieldtype/#NUMBER), this string specifies the default string for the text form field.
This string is the content that Microsoft Word will display in the document when the form field is empty.

When [FormField.text_input_type](../text_input_type/) is [TextFormFieldType.CALCULATED](../../textformfieldtype/#CALCULATED), then this string holds
the expression to be calculated. The expression needs to be a formula valid according to Microsoft Word formula field
requirements. When you set a new expression using this property, Aspose.Words calculates the formula result
automatically and inserts it into the form field.

Microsoft Word allows strings with at most 255 characters.




### See Also

* module [aspose.words.fields](../../)
* class [FormField](../)

