---
title: FormField.result property
linktitle: result property
articleTitle: result property
second_title: Aspose.Words for NodeJs
description: "FormField.result property. Gets or sets a string that represents the result of this form field."
type: docs
weight: 170
url: /nodejs-net/Aspose.Words.Fields/formfield/result/
---

## FormField.result property

Gets or sets a string that represents the result of this form field.


```js
get result(): string
```

### Remarks

For a text form field the result is the text that is in the field.

For a checkbox form field the result can be "1" or "0" to indicate checked or unchecked.

For a dropdown form field the result is the string selected in the dropdown.

Setting [FormField.result](./) for a text form field does not apply the text format
specified in [FormField.textInputFormat](../textInputFormat/). If you want to set a value and apply the
format, use the [FormField.setTextInputValue()](../setTextInputValue/#object) method.

For a text form field the [FormField.textInputDefault](../textInputDefault/) value is applied
if *value* is``null``.




### Examples

Shows how to insert a combo box.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.write("Please select a fruit: ");

// Insert a combo box which will allow a user to choose an option from a collection of strings.
let comboBox = builder.insertComboBox("MyComboBox", ["Apple", "Banana", "Cherry"], 0);

expect(comboBox.name).toEqual("MyComboBox");
expect(comboBox.type).toEqual(aw.Fields.FieldType.FieldFormDropDown);
expect(comboBox.result).toEqual("Apple");

// The form field will appear in the form of a "select" html tag.
doc.save(base.artifactsDir + "FormFields.create.html");
```

### See Also

* module [Aspose.Words.Fields](../../)
* class [FormField](../)

