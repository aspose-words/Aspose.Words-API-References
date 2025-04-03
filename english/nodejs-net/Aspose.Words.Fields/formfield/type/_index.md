---
title: FormField.type property
linktitle: type property
articleTitle: type property
second_title: Aspose.Words for NodeJs
description: "FormField.type property. Returns the form field type."
type: docs
weight: 220
url: /nodejs-net/aspose.words.fields/formfield/type/
---

## FormField.type property

Returns the form field type.


```js
get type(): Aspose.Words.Fields.FieldType
```

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

