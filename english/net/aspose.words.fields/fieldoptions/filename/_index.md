---
title: FieldOptions.FileName
linktitle: FileName
articleTitle: FileName
second_title: Aspose.Words for .NET
description: Discover the FieldOptions FileName property to easily manage and customize your document's file name for enhanced organization and efficiency.
type: docs
weight: 140
url: /net/aspose.words.fields/fieldoptions/filename/
---
## FieldOptions.FileName property

Gets or sets the file name of the document.

```csharp
public string FileName { get; set; }
```

## Remarks

This property is used by the [`FieldFileName`](../../fieldfilename/) field with higher priority than the [`OriginalFileName`](../../../aspose.words/document/originalfilename/) property.

## Examples

Shows how to use FieldOptions to override the default value for the FILENAME field.

```csharp
Document doc = new Document(MyDir + "Document.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToDocumentEnd();
builder.Writeln();

// This FILENAME field will display the local system file name of the document we loaded.
FieldFileName field = (FieldFileName)builder.InsertField(FieldType.FieldFileName, true);
field.Update();

Assert.That(field.GetFieldCode(), Is.EqualTo(" FILENAME "));
Assert.That(field.Result, Is.EqualTo("Document.docx"));

builder.Writeln();

// By default, the FILENAME field shows the file's name, but not its full local file system path.
// We can set a flag to make it show the full file path.
field = (FieldFileName)builder.InsertField(FieldType.FieldFileName, true);
field.IncludeFullPath = true;
field.Update();

Assert.That(field.Result, Is.EqualTo(MyDir + "Document.docx"));

// We can also set a value for this property to
// override the value that the FILENAME field displays.
doc.FieldOptions.FileName = "FieldOptions.FILENAME.docx";
field.Update();

Assert.That(field.GetFieldCode(), Is.EqualTo(" FILENAME  \\p"));
Assert.That(field.Result, Is.EqualTo("FieldOptions.FILENAME.docx"));

doc.UpdateFields();
doc.Save(ArtifactsDir + doc.FieldOptions.FileName);
```

### See Also

* class [FieldOptions](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
