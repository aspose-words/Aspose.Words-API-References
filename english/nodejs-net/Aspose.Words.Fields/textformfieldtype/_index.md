---
title: TextFormFieldType enumeration
linktitle: TextFormFieldType enumeration
articleTitle: TextFormFieldType enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Fields.TextFormFieldType enumeration. Specifies the type of a text form field."
type: docs
weight: 1290
url: /nodejs-net/Aspose.Words.Fields/textformfieldtype/
---

## TextFormFieldType enumeration

Specifies the type of a text form field.


### Members

| Name | Description |
| --- | --- |
| Regular | The text form field can contain any text. |
| Number | The text form field can contain only numbers. |
| Date | The text form field can contain only a valid date value. |
| CurrentDate | The text form field value is the current date when the field is updated. |
| CurrentTime | The text form field value is the current time when the field is updated. |
| Calculated | The text form field value is calculated from the expression specified in the [FormField.textInputDefault](../formfield/textInputDefault/) property. |

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

### See Also

* module [Aspose.Words.Fields](../)

