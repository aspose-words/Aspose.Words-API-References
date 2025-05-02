---
title: TextFormFieldType Enum
linktitle: TextFormFieldType
articleTitle: TextFormFieldType
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Fields.TextFormFieldType enum, defining various text form field types for enhanced document automation and customization.
type: docs
weight: 3180
url: /net/aspose.words.fields/textformfieldtype/
---
## TextFormFieldType enumeration

Specifies the type of a text form field.

```csharp
public enum TextFormFieldType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Regular | `0` | The text form field can contain any text. |
| Number | `1` | The text form field can contain only numbers. |
| Date | `2` | The text form field can contain only a valid date value. |
| CurrentDate | `3` | The text form field value is the current date when the field is updated. |
| CurrentTime | `4` | The text form field value is the current time when the field is updated. |
| Calculated | `5` | The text form field value is calculated from the expression specified in the [`TextInputDefault`](../formfield/textinputdefault/) property. |

## Examples

Shows how to create form fields.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Form fields are objects in the document that the user can interact with by being prompted to enter values.
// We can create them using a document builder, and below are two ways of doing so.
// 1 -  Basic text input:
builder.InsertTextInput("My text input", TextFormFieldType.Regular, 
    "", "Enter your name here", 30);

// 2 -  Combo box with prompt text, and a range of possible values:
string[] items =
{
    "-- Select your favorite footwear --", "Sneakers", "Oxfords", "Flip-flops", "Other"
};

builder.InsertParagraph();
builder.InsertComboBox("My combo box", items, 0);

builder.Document.Save(ArtifactsDir + "DocumentBuilder.CreateForm.docx");
```

### See Also

* namespace [Aspose.Words.Fields](../../aspose.words.fields/)
* assembly [Aspose.Words](../../)
