---
title: DocumentBuilder.insertComboBox method
linktitle: insertComboBox method
articleTitle: insertComboBox method
second_title: Aspose.Words for Node.js
description: "DocumentBuilder.insertComboBox method. Inserts a combobox form field at the current position."
type: docs
weight: 300
url: /nodejs-net/aspose.words/documentbuilder/insertComboBox/
---

## insertComboBox(name, items, selectedIndex) {#string_string[]_number}

Inserts a combobox form field at the current position.


```js
insertComboBox(name: string, items: string[], selectedIndex: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | string | The name of the form field. Can be an empty string. The value longer than 20 characters will be truncated. |
| items | string[] | The items of the ComboBox. Maximum is 25 items. |
| selectedIndex | number | The index of the selected item in the ComboBox. |

### Remarks

If you specify a name for the form field, then a bookmark is automatically created with the same name.




### Returns

The form field node that was just inserted.


### Examples

Shows how to create form fields.

```js
let builder = new aw.DocumentBuilder();

// Form fields are objects in the document that the user can interact with by being prompted to enter values.
// We can create them using a document builder, and below are two ways of doing so.
// 1 -  Basic text input:
builder.insertTextInput("My text input", aw.Fields.TextFormFieldType.Regular, 
  "", "Enter your name here", 30);

// 2 -  Combo box with prompt text, and a range of possible values:
let items =
[
  "-- Select your favorite footwear --", "Sneakers", "Oxfords", "Flip-flops", "Other"
];

builder.insertParagraph();
builder.insertComboBox("My combo box", items, 0);

builder.document.save(base.artifactsDir + "DocumentBuilder.CreateForm.docx");
```

Shows how to insert a combo box form field into a document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert a form that prompts the user to pick one of the items from the menu.
builder.write("Pick a fruit: ");
let items = [ "Apple", "Banana", "Cherry" ];
builder.insertComboBox("DropDown", items, 0);

doc.save(base.artifactsDir + "DocumentBuilder.insertComboBox.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

