---
title: FieldCitation.SuppressYear
linktitle: SuppressYear
second_title: Aspose.Words for .NET API Reference
description: FieldCitation SuppressYear property. Gets or sets whether the year information is suppressed from the citation in C#.
type: docs
weight: 100
url: /net/aspose.words.fields/fieldcitation/suppressyear/
---
## SuppressYear property

Gets or sets whether the year information is suppressed from the citation.

```csharp
public bool SuppressYear { get; set; }
```

## Examples

Shows how to work with CITATION and BIBLIOGRAPHY fields.

```csharp
// Open a document containing bibliographical sources that we can find in
// Microsoft Word via References -> Citations & Bibliography -> Manage Sources.
Document doc = new Document(MyDir + "Bibliography.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Text to be cited with one source.");

// Create a citation with just the page number and the author of the referenced book.
FieldCitation fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);

// We refer to sources using their tag names.
fieldCitation.SourceTag = "Book1";
fieldCitation.PageNumber = "85";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = true;
fieldCitation.SuppressYear = true;

Assert.AreEqual(" CITATION  Book1 \\p 85 \\t \\y", fieldCitation.GetFieldCode());

// Create a more detailed citation which cites two sources.
builder.InsertParagraph();
builder.Write("Text to be cited with two sources.");
fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);
fieldCitation.SourceTag = "Book1";
fieldCitation.AnotherSourceTag = "Book2";
fieldCitation.FormatLanguageId = "en-US";
fieldCitation.PageNumber = "19";
fieldCitation.Prefix = "Prefix ";
fieldCitation.Suffix = " Suffix";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = false;
fieldCitation.SuppressYear = false;
fieldCitation.VolumeNumber = "VII";

Assert.AreEqual(" CITATION  Book1 \\m Book2 \\l en-US \\p 19 \\f \"Prefix \" \\s \" Suffix\" \\v VII", fieldCitation.GetFieldCode());

// We can use a BIBLIOGRAPHY field to display all the sources within the document.
builder.InsertBreak(BreakType.PageBreak);
FieldBibliography fieldBibliography = (FieldBibliography)builder.InsertField(FieldType.FieldBibliography, true);
fieldBibliography.FormatLanguageId = "1124";

Assert.AreEqual(" BIBLIOGRAPHY  \\l 1124", fieldBibliography.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CITATION.docx");
```

### See Also

* class [FieldCitation](../)
* namespace [Aspose.Words.Fields](../../fieldcitation/)
* assembly [Aspose.Words](../../../)
