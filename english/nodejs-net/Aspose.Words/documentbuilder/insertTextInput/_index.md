---
title: DocumentBuilder.insertTextInput method
linktitle: insertTextInput method
articleTitle: insertTextInput method
second_title: Aspose.Words for Node.js
description: "DocumentBuilder.insertTextInput method. Inserts a text form field at the current position."
type: docs
weight: 510
url: /nodejs-net/aspose.words/documentbuilder/insertTextInput/
---

## insertTextInput(name, type, format, fieldValue, maxLength) {#string_textformfieldtype_string_string_number}

Inserts a text form field at the current position.


```js
insertTextInput(name: string, type: Aspose.Words.Fields.TextFormFieldType, format: string, fieldValue: string, maxLength: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | string | The name of the form field. Can be an empty string. |
| type | [TextFormFieldType](../../../aspose.words.fields/textformfieldtype/) | Specifies the type of the text form field. |
| format | string | Format string used to format the value of the form field. |
| fieldValue | string | Text that will be shown in the field. |
| maxLength | number | Maximum length the user can enter into the form field. Set to zero for unlimited length. |

### Remarks

If you specify a name for the form field, then a bookmark is automatically created with the same name.




### Returns

The form field node that was just inserted.


### Examples

Shows how to insert a text input form field.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.write("Please enter text here: ");

// Insert a text input field, which will allow the user to click it and enter text.
// Assign some placeholder text that the user may overwrite and pass
// a maximum text length of 0 to apply no limit on the form field's contents.
builder.insertTextInput("TextInput1", aw.Fields.TextFormFieldType.Regular, "", "Placeholder text", 0);

// The form field will appear in the form of an "input" html tag, with a type of "text".
doc.save(base.artifactsDir + "FormFields.textInput.html");
```

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

Shows how to insert a text input form field into a document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert a form that prompts the user to enter text.
builder.insertTextInput("TextInput", aw.Fields.TextFormFieldType.Regular, "", "Enter your text here", 0);

doc.save(base.artifactsDir + "DocumentBuilder.insertTextInput.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

