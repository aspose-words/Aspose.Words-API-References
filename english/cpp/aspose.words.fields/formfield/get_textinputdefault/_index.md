---
title: Aspose::Words::Fields::FormField::get_TextInputDefault method
linktitle: get_TextInputDefault
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FormField::get_TextInputDefault method. Gets or sets the default string or a calculation expression of a text form field in C++.'
type: docs
weight: 21000
url: /cpp/aspose.words.fields/formfield/get_textinputdefault/
---
## FormField::get_TextInputDefault method


Gets or sets the default string or a calculation expression of a text form field.

```cpp
System::String Aspose::Words::Fields::FormField::get_TextInputDefault()
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
