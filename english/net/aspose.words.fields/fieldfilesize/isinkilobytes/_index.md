---
title: FieldFileSize.IsInKilobytes
linktitle: IsInKilobytes
articleTitle: IsInKilobytes
second_title: Aspose.Words for .NET
description: Control file size display with FieldFileSize IsInKilobytes. Easily toggle size visibility in kilobytes for enhanced data management.
type: docs
weight: 20
url: /net/aspose.words.fields/fieldfilesize/isinkilobytes/
---
## FieldFileSize.IsInKilobytes property

Gets or sets whether to display the file size in kilobytes.

```csharp
public bool IsInKilobytes { get; set; }
```

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

* class [FieldFileSize](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
