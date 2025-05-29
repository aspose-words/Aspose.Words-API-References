---
title: FieldTC.OmitPageNumber
linktitle: OmitPageNumber
articleTitle: OmitPageNumber
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldTC OmitPageNumber – styr synligheten av sidnumret i innehållsförteckningen för förbättrad dokumenttydlighet och professionalism.
type: docs
weight: 30
url: /sv/net/aspose.words.fields/fieldtc/omitpagenumber/
---
## FieldTC.OmitPageNumber property

Hämtar eller anger om sidnumret i innehållsförteckningen ska utelämnas för detta fält.

```csharp
public bool OmitPageNumber { get; set; }
```

## Exempel

Visar hur man infogar ett innehållsförteckningsfält och filtrerar vilka innehållsförteckningsfält som slutar som poster.

```csharp
public void FieldTocEntryIdentifier()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Infoga ett innehållsförteckningsfält, vilket sammanställer alla TC-fält till en innehållsförteckning.
    FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Konfigurera fältet för att endast hämta TC-poster av typen "A" och en ingångsnivå mellan 1 och 3.
    fieldToc.EntryIdentifier = "A";
    fieldToc.EntryLevelRange = "1-3";

    Assert.AreEqual(" TOC  \\f A \\l 1-3", fieldToc.GetFieldCode());

    // Dessa två poster kommer att visas i tabellen.
    builder.InsertBreak(BreakType.PageBreak);
    InsertTocEntry(builder, "TC field 1", "A", "1");
    InsertTocEntry(builder, "TC field 2", "A", "2");

    Assert.AreEqual(" TC  \"TC field 1\" \\n \\f A \\l 1", doc.Range.Fields[1].GetFieldCode());

    // Denna post kommer att utelämnas från tabellen eftersom den har en annan typ än "A".
    InsertTocEntry(builder, "TC field 3", "B", "1");

    // Denna post kommer att utelämnas från tabellen eftersom den har en ingångsnivå utanför intervallet 1-3.
    InsertTocEntry(builder, "TC field 4", "A", "5");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TC.docx");
}

/// <summary>
/// Använd en dokumentbyggare för att infoga ett TC-fält.
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

### Se även

* class [FieldTC](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
