---
title: FieldFileSize Class
linktitle: FieldFileSize
articleTitle: FieldFileSize
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Fields.FieldFileSize class for effortlessly implementing the FILESIZE field, enhancing document management with ease.
type: docs
weight: 2280
url: /net/aspose.words.fields/fieldfilesize/
---
## FieldFileSize class

Implements the FILESIZE field.

To learn more, visit the [Working with Fields](https://docs.aspose.com/words/net/working-with-fields/) documentation article.

```csharp
public class FieldFileSize : Field
```

## Constructors

| Name | Description |
| --- | --- |
| [FieldFileSize](fieldfilesize/)() | The default constructor. |

## Properties

| Name | Description |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Gets the text that represents the displayed field result. |
| [End](../../aspose.words.fields/field/end/) { get; } | Gets the node that represents the field end. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Gets a [`FieldFormat`](../fieldformat/) object that provides typed access to field's formatting. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document. |
| [IsInKilobytes](../../aspose.words.fields/fieldfilesize/isinkilobytes/) { get; set; } | Gets or sets whether to display the file size in kilobytes. |
| [IsInMegabytes](../../aspose.words.fields/fieldfilesize/isinmegabytes/) { get; set; } | Gets or sets whether to display the file size in megabytes. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Gets or sets whether the field is locked (should not recalculate its result). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Gets or sets the LCID of the field. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Gets or sets text that is between the field separator and field end. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Gets the node that represents the field separator. Can be `null`. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Gets the node that represents the start of the field. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Gets the Microsoft Word field type. |

## Methods

| Name | Description |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Returns text between field start and field separator (or field end if there is no separator). |
| [Remove](../../aspose.words.fields/field/remove/)() | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns `null`. |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Performs the field unlink. |
| [Update](../../aspose.words.fields/field/update/)() | Performs the field update. Throws if the field is being updated already. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Performs a field update. Throws if the field is being updated already. |

## Remarks

Retrieves the size of the current document's file or 0 if the size cannot be determined.

In the current implementation, uses the [`OriginalFileName`](../../aspose.words/document/originalfilename/) property to retrieve the file name used to determine the file size.

## Examples

Shows how to display the file size of a document with a FILESIZE field.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.That(doc.BuiltInDocumentProperties.Bytes, Is.EqualTo(18105));

DocumentBuilder builder = new DocumentBuilder(doc);
builder.MoveToDocumentEnd();
builder.InsertParagraph();

// Below are three different units of measure
// with which FILESIZE fields can display the document's file size.
// 1 -  Bytes:
FieldFileSize field = (FieldFileSize)builder.InsertField(FieldType.FieldFileSize, true);
field.Update();

Assert.That(field.GetFieldCode(), Is.EqualTo(" FILESIZE "));
Assert.That(field.Result, Is.EqualTo("18105"));

// 2 -  Kilobytes:
builder.InsertParagraph();
field = (FieldFileSize)builder.InsertField(FieldType.FieldFileSize, true);
field.IsInKilobytes = true;
field.Update();

Assert.That(field.GetFieldCode(), Is.EqualTo(" FILESIZE  \\k"));
Assert.That(field.Result, Is.EqualTo("18"));

// 3 -  Megabytes:
builder.InsertParagraph();
field = (FieldFileSize)builder.InsertField(FieldType.FieldFileSize, true);
field.IsInMegabytes = true;
field.Update();

Assert.That(field.GetFieldCode(), Is.EqualTo(" FILESIZE  \\m"));
Assert.That(field.Result, Is.EqualTo("0"));

// To update the values of these fields while editing in Microsoft Word,
// we must first save the changes, and then manually update these fields.
doc.Save(ArtifactsDir + "Field.FILESIZE.docx");
```

### See Also

* class [Field](../field/)
* namespace [Aspose.Words.Fields](../../aspose.words.fields/)
* assembly [Aspose.Words](../../)
