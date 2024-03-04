---
title: DocumentBuilder.InsertComboBox
linktitle: InsertComboBox
articleTitle: InsertComboBox
second_title: Aspose.Words for .NET
description: DocumentBuilder InsertComboBox method. Inserts a combobox form field at the current position in C#.
type: docs
weight: 300
url: /net/aspose.words/documentbuilder/insertcombobox/
---
## DocumentBuilder.InsertComboBox method

Inserts a combobox form field at the current position.

```csharp
public FormField InsertComboBox(string name, string[] items, int selectedIndex)
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | String | The name of the form field. Can be an empty string. The value longer than 20 characters will be truncated. |
| items | String[] | The items of the ComboBox. Maximum is 25 items. |
| selectedIndex | Int32 | The index of the selected item in the ComboBox. |

### Return Value

The form field node that was just inserted.

## Remarks

If you specify a name for the form field, then a bookmark is automatically created with the same name.

## Examples

Shows how to insert a combo box form field into a document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert a form that prompts the user to pick one of the items from the menu.
builder.Write("Pick a fruit: ");
string[] items = { "Apple", "Banana", "Cherry" };
builder.InsertComboBox("DropDown", items, 0);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertComboBox.docx");
```

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

* class [FormField](../../../aspose.words.fields/formfield/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
