---
title: FieldTC.EntryLevel
second_title: Aspose.Words för .NET API Referens
description: FieldTC fast egendom. Hämtar eller ställer in nivån för posten.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldtc/entrylevel/
---
## FieldTC.EntryLevel property

Hämtar eller ställer in nivån för posten.

```csharp
public string EntryLevel { get; set; }
```

### Exempel

Visar hur man infogar ett TOC-fält och filtrerar vilka TC-fält som slutar som poster.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Infoga ett TOC-fält, som kommer att kompilera alla TC-fält till en innehållsförteckning.
    FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Konfigurera fältet endast för att ta upp TC-poster av typen "A" och en ingångsnivå mellan 1 och 3.
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
* namnutrymme [Aspose.Words.Fields](../../fieldtc/)
* hopsättning [Aspose.Words](../../../)


