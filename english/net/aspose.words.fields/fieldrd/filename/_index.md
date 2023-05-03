---
title: FieldRD.FileName
linktitle: FileName
articleTitle: FileName
second_title: Aspose.Words for .NET API Reference
description: FieldRD FileName property. Gets or sets the name of the file to include when generating a table of contents table of authorities or index in C#.
type: docs
weight: 20
url: /net/aspose.words.fields/fieldrd/filename/
---
## FieldRD.FileName property

Gets or sets the name of the file to include when generating a table of contents, table of authorities, or index.

```csharp
public string FileName { get; set; }
```

## Examples

Shows to use the RD field to create a table of contents entries from headings in other documents.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Use a document builder to insert a table of contents,
// and then add one entry for the table of contents on the following page.
builder.InsertField(FieldType.FieldTOC, true);
builder.InsertBreak(BreakType.PageBreak);
builder.CurrentParagraph.ParagraphFormat.StyleName = "Heading 1";
builder.Writeln("TOC entry from within this document");

// Insert an RD field, which references another local file system document in its FileName property.
// The TOC will also now accept all headings from the referenced document as entries for its table.
FieldRD field = (FieldRD)builder.InsertField(FieldType.FieldRefDoc, true);
field.FileName = ArtifactsDir + "ReferencedDocument.docx";

Assert.AreEqual($" RD  {ArtifactsDir.Replace(@"\",@"\\")}ReferencedDocument.docx", field.GetFieldCode());

// Create the document that the RD field is referencing and insert a heading. 
// This heading will show up as an entry in the TOC field in our first document.
Document referencedDoc = new Document();
DocumentBuilder refDocBuilder = new DocumentBuilder(referencedDoc);
refDocBuilder.CurrentParagraph.ParagraphFormat.StyleName = "Heading 1";
refDocBuilder.Writeln("TOC entry from referenced document");
referencedDoc.Save(ArtifactsDir + "ReferencedDocument.docx");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.RD.docx");
```

### See Also

* class [FieldRD](../)
* namespace [Aspose.Words.Fields](../../fieldrd/)
* assembly [Aspose.Words](../../../)
