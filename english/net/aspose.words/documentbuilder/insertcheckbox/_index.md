---
title: DocumentBuilder.InsertCheckBox
second_title: Aspose.Words for .NET API Reference
description: DocumentBuilder method. Inserts a checkbox form field at the current position in C#.
type: docs
weight: 290
url: /net/aspose.words/documentbuilder/insertcheckbox/
---
## InsertCheckBox(string, bool, int) {#insertcheckbox_1}

Inserts a checkbox form field at the current position.

```csharp
public FormField InsertCheckBox(string name, bool checkedValue, int size)
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | String | The name of the form field. Can be an empty string. The value longer than 20 characters will be truncated. |
| checkedValue | Boolean | Checked status of the checkbox form field. |
| size | Int32 | Specifies the size of the checkbox in points. Specify 0 for MS Word to calculate the size of the checkbox automatically. |

### Return Value

The form field node that was just inserted.

## Remarks

If you specify a name for the form field, then a bookmark is automatically created with the same name.

## Examples

Shows how to insert checkboxes into the document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert checkboxes of varying sizes and default checked statuses.
builder.Write("Unchecked check box of a default size: ");
builder.InsertCheckBox(string.Empty, false, false, 0);
builder.InsertParagraph();

builder.Write("Large checked check box: ");
builder.InsertCheckBox("CheckBox_Default", true, true, 50);
builder.InsertParagraph();

// Form fields have a name length limit of 20 characters.
builder.Write("Very large checked check box: ");
builder.InsertCheckBox("CheckBox_OnlyCheckedValue", true, 100);

Assert.AreEqual("CheckBox_OnlyChecked", doc.Range.FormFields[2].Name);

// We can interact with these check boxes in Microsoft Word by double clicking them.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertCheckBox.docx");
```

### See Also

* class [FormField](../../../aspose.words.fields/formfield/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../documentbuilder/)
* assembly [Aspose.Words](../../../)

---

## InsertCheckBox(string, bool, bool, int) {#insertcheckbox}

Inserts a checkbox form field at the current position.

```csharp
public FormField InsertCheckBox(string name, bool defaultValue, bool checkedValue, int size)
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | String | The name of the form field. Can be an empty string. The value longer than 20 characters will be truncated. |
| defaultValue | Boolean | Default value of the checkbox form field. |
| checkedValue | Boolean | Current checked status of the checkbox form field. |
| size | Int32 | Specifies the size of the checkbox in points. Specify 0 for MS Word to calculate the size of the checkbox automatically. |

### Return Value

The form field node that was just inserted.

## Remarks

If you specify a name for the form field, then a bookmark is automatically created with the same name.

## Examples

Shows how to insert checkboxes into the document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insert checkboxes of varying sizes and default checked statuses.
builder.Write("Unchecked check box of a default size: ");
builder.InsertCheckBox(string.Empty, false, false, 0);
builder.InsertParagraph();

builder.Write("Large checked check box: ");
builder.InsertCheckBox("CheckBox_Default", true, true, 50);
builder.InsertParagraph();

// Form fields have a name length limit of 20 characters.
builder.Write("Very large checked check box: ");
builder.InsertCheckBox("CheckBox_OnlyCheckedValue", true, 100);

Assert.AreEqual("CheckBox_OnlyChecked", doc.Range.FormFields[2].Name);

// We can interact with these check boxes in Microsoft Word by double clicking them.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertCheckBox.docx");
```

### See Also

* class [FormField](../../../aspose.words.fields/formfield/)
* class [DocumentBuilder](../)
* namespace [Aspose.Words](../../documentbuilder/)
* assembly [Aspose.Words](../../../)
