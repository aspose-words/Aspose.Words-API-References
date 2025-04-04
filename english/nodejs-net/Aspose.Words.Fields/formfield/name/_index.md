---
title: FormField.name property
linktitle: name property
articleTitle: name property
second_title: Aspose.Words for Node.js
description: "FormField.name property. Gets or sets the form field name."
type: docs
weight: 130
url: /nodejs-net/aspose.words.fields/formfield/name/
---

## FormField.name property

Gets or sets the form field name.


```js
get name(): string
```

### Remarks

Microsoft Word allows strings with at most 20 characters.


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

