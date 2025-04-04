---
title: FormField.textInputDefault property
linktitle: textInputDefault property
articleTitle: textInputDefault property
second_title: Aspose.Words for Node.js
description: "FormField.textInputDefault property. Gets or sets the default string or a calculation expression of a text form field."
type: docs
weight: 190
url: /nodejs-net/aspose.words.fields/formfield/textInputDefault/
---

## FormField.textInputDefault property

Gets or sets the default string or a calculation expression of a text form field.


```js
get textInputDefault(): string
```

### Remarks

The meaning of this property depends on the value of the [FormField.textInputType](../textInputType/) property.

When [FormField.textInputType](../textInputType/) is [TextFormFieldType.Regular](../../textformfieldtype/#Regular) or
[TextFormFieldType.Number](../../textformfieldtype/#Number), this string specifies the default string for the text form field.
This string is the content that Microsoft Word will display in the document when the form field is empty.

When [FormField.textInputType](../textInputType/) is [TextFormFieldType.Calculated](../../textformfieldtype/#Calculated), then this string holds
the expression to be calculated. The expression needs to be a formula valid according to Microsoft Word formula field
requirements. When you set a new expression using this property, Aspose.Words calculates the formula result
automatically and inserts it into the form field.

Microsoft Word allows strings with at most 255 characters.




### See Also

* module [Aspose.Words.Fields](../../)
* class [FormField](../)

