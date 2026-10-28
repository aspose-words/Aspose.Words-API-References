---
title: Aspose::Words::Fields::FormField::set_TextInputDefault method
linktitle: set_TextInputDefault
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FormField::set_TextInputDefault method. Sets the default string or a calculation expression of a text form field in C++.'
type: docs
weight: 87000
url: /cpp/aspose.words.fields/formfield/set_textinputdefault/
---
## FormField::set_TextInputDefault method


Sets the default string or a calculation expression of a text form field.

```cpp
void Aspose::Words::Fields::FormField::set_TextInputDefault(const System::String & value)
```

## Remarks


The meaning of this property depends on the value of the [TextInputType](../get_textinputtype/) property.

When [TextInputType](../get_textinputtype/) is [Regular](../../textformfieldtype/) or [Number](../../textformfieldtype/), this string specifies the default string for the text form field. This string is the content that Microsoft Word will display in the document when the form field is empty.

When [TextInputType](../get_textinputtype/) is [Calculated](../../textformfieldtype/), then this string holds the expression to be calculated. The expression needs to be a formula valid according to Microsoft Word formula field requirements. When you set a new expression using this property, Aspose.Words calculates the formula result automatically and inserts it into the form field.

Microsoft Word allows strings with at most 255 characters.
## See Also

* Class [FormField](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
