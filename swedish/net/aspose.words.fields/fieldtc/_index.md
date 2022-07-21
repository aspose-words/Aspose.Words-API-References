---
title: FieldTC
second_title: Aspose.Words för .NET API Referens
description: Implementerar TC-fältet.
type: docs
weight: 2330
url: /sv/net/aspose.words.fields/fieldtc/
---
## FieldTC class

Implementerar TC-fältet.

```csharp
public sealed class FieldTC : Field
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FieldTC](fieldtc)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [End](../../aspose.words.fields/field/end) { get; } | Hämtar noden som representerar fältänden. |
| [EntryLevel](../../aspose.words.fields/fieldtc/entrylevel) { get; set; } | Hämtar eller ställer in nivån för posten. |
| [Format](../../aspose.words.fields/field/format) { get; } | Får en[`FieldFormat`](../fieldformat) objekt som ger maskinskriven åtkomst till fältets formatering. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Hämtar eller ställer in om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Hämtar eller ställer in om fältet är låst (ska inte räkna om resultatet). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Hämtar eller ställer in LCID för fältet. |
| [OmitPageNumber](../../aspose.words.fields/fieldtc/omitpagenumber) { get; set; } | Hämtar eller ställer in om sidnummer i innehållsförteckningen ska utelämnas för detta fält. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Hämtar eller ställer in text som är mellan fältavgränsaren och fältslutet. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Hämtar noden som representerar fältseparatorn. Kan vara null. |
| [Start](../../aspose.words.fields/field/start) { get; } | Hämtar noden som representerar början av fältet. |
| [Text](../../aspose.words.fields/fieldtc/text) { get; set; } | Hämtar eller ställer in texten i posten. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Hämtar fälttypen Microsoft Word. |
| [TypeIdentifier](../../aspose.words.fields/fieldtc/typeidentifier) { get; set; } | Hämtar eller ställer in en typidentifierare för detta fält (som vanligtvis är en bokstav). |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). Både fältkod och fältresultat för underordnade fält ingår. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). |
| [Remove](../../aspose.words.fields/field/remove)() | Tar bort fältet från dokumentet. Returnerar en nod direkt efter fältet. Om fältets slut är den sista child av dess överordnade nod, returnerar dess överordnade stycke. Om fältet redan är borttaget, returneras **null** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Utför fältavlänkningen. |
| [Update](../../aspose.words.fields/field/update)() | Utför fältuppdateringen. Kastar om fältet redan uppdateras. |
| [Update](../../aspose.words.fields/field/update)(bool) | Utför en fältuppdatering. Kastar om fältet redan uppdateras. |

### Anmärkningar

Definierar texten och sidnumret för en innehållsförteckning (inklusive en figurtabell), vilken används av ett TOC-fält.

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

* class [Field](../field)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
