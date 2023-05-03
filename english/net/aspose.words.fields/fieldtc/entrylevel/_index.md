---
title: FieldTC.EntryLevel
linktitle: EntryLevel
second_title: Aspose.Words for .NET API Reference
description: FieldTC EntryLevel property. Gets or sets the level of the entry in C#.
type: docs
weight: 20
url: /net/aspose.words.fields/fieldtc/entrylevel/
---
## FieldTC.EntryLevel property

Gets or sets the level of the entry.

```csharp
public string EntryLevel { get; set; }
```

## Examples

Shows how to insert a TOC field, and filter which TC fields end up as entries.

```csharp
public void FieldTocEntryIdentifier()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Insert a TOC field, which will compile all TC fields into a table of contents.
    FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Configure the field only to pick up TC entries of the "A" type, and an entry-level between 1 and 3.
    fieldToc.EntryIdentifier = "A";
    fieldToc.EntryLevelRange = "1-3";

    Assert.AreEqual(" TOC  \\f A \\l 1-3", fieldToc.GetFieldCode());

    // These two entries will appear in the table.
    builder.InsertBreak(BreakType.PageBreak);
    InsertTocEntry(builder, "TC field 1", "A", "1");
    InsertTocEntry(builder, "TC field 2", "A", "2");

    Assert.AreEqual(" TC  \"TC field 1\" \\n \\f A \\l 1", doc.Range.Fields[1].GetFieldCode());

    // This entry will be omitted from the table because it has a different type from "A".
    InsertTocEntry(builder, "TC field 3", "B", "1");

    // This entry will be omitted from the table because it has an entry-level outside of the 1-3 range.
    InsertTocEntry(builder, "TC field 4", "A", "5");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TC.docx");
}

/// <summary>
/// Use a document builder to insert a TC field.
/// </summary>
public void InsertTocEntry(DocumentBuilder builder, string text, string typeIdentifier, string entryLevel)
{
    FieldTC fieldTc = (FieldTC)builder.InsertField(FieldType.FieldTOCEntry, true);
    fieldTc.OmitPageNumber = true;
    fieldTc.Text = text;
    fieldTc.TypeIdentifier = typeIdentifier;
    fieldTc.EntryLevel = entryLevel;
}
```

### See Also

* class [FieldTC](../)
* namespace [Aspose.Words.Fields](../../fieldtc/)
* assembly [Aspose.Words](../../../)
