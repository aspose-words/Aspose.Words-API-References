---
title: DocumentBuilder.InsertField
linktitle: InsertField
articleTitle: InsertField
second_title: Aspose.Words för .NET
description: DocumentBuilder InsertField metod. Infogar ett Wordfält i ett dokument och uppdaterar eventuellt fältresultatet i C#.
type: docs
weight: 320
url: /sv/net/aspose.words/documentbuilder/insertfield/
---
## InsertField(*[FieldType](../../../aspose.words.fields/fieldtype/), bool*) {#insertfield}

Infogar ett Word-fält i ett dokument och uppdaterar eventuellt fältresultatet.

```csharp
public Field InsertField(FieldType fieldType, bool updateField)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fieldType | FieldType | Typen av fält som ska läggas till. |
| updateField | Boolean | Anger om fältet ska uppdateras omedelbart. |

### Returvärde

A[`Field`](../../../aspose.words.fields/field/) objekt som representerar det infogade fältet.

## Anmärkningar

Denna metod infogar ett fält i ett dokument. Aspose.Words kan uppdatera fält av de flesta typer, men inte alla. För mer information se the `InsertField` överbelastning.

## Exempel

Visar hur man infogar ett fält i ett dokument med hjälp av FieldType.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga två fält samtidigt som du skickar en flagga som avgör om de ska uppdateras när byggaren infogar dem.
// I vissa fall kan det vara beräkningsdyrt att uppdatera fält och det kan vara en bra idé att skjuta upp uppdateringen.
doc.BuiltInDocumentProperties.Author = "John Doe";
builder.Write("This document was written by ");
builder.InsertField(FieldType.FieldAuthor, updateInsertedFieldsImmediately);

builder.InsertParagraph();
builder.Write("\nThis is page ");
builder.InsertField(FieldType.FieldPage, updateInsertedFieldsImmediately);

Assert.AreEqual(" AUTHOR ", doc.Range.Fields[0].GetFieldCode());
Assert.AreEqual(" PAGE ", doc.Range.Fields[1].GetFieldCode());

if (updateInsertedFieldsImmediately)
{
    Assert.AreEqual("John Doe", doc.Range.Fields[0].Result);
    Assert.AreEqual("1", doc.Range.Fields[1].Result);
}
else
{
    Assert.AreEqual(string.Empty, doc.Range.Fields[0].Result);
    Assert.AreEqual(string.Empty, doc.Range.Fields[1].Result);

    // Vi kommer att behöva uppdatera dessa fält med uppdateringsmetoderna manuellt.
    doc.Range.Fields[0].Update();

    Assert.AreEqual("John Doe", doc.Range.Fields[0].Result);

    doc.UpdateFields();

    Assert.AreEqual("1", doc.Range.Fields[1].Result);
}
```

### Se även

* class [Field](../../../aspose.words.fields/field/)
* enum [FieldType](../../../aspose.words.fields/fieldtype/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## InsertField(*string*) {#insertfield_1}

Infogar ett Word-fält i ett dokument och uppdaterar fältresultatet.

```csharp
public Field InsertField(string fieldCode)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fieldCode | String | Fältkoden som ska infogas (utan hängslen). |

### Returvärde

A[`Field`](../../../aspose.words.fields/field/) objekt som representerar det infogade fältet.

## Anmärkningar

Denna metod infogar ett fält i ett dokument och uppdaterar fältresultatet omedelbart. Aspose.Words kan uppdatera fält av de flesta typer, men inte alla. För mer information se the `InsertField` överbelastning.

## Exempel

Visar hur man infogar ett fält i ett dokument med hjälp av en fältkod.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// Denna överbelastning av InsertField-metoden uppdaterar automatiskt infogade fält.
Assert.That(DateTime.Parse(field.Result), Is.EqualTo(DateTime.Today).Within(1).Days);
```

Visar hur man infogar fält och flyttar dokumentbyggarens markör till dem.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField(@"MERGEFIELD MyMergeField1 \* MERGEFORMAT");
builder.InsertField(@"MERGEFIELD MyMergeField2 \* MERGEFORMAT");

// Flytta markören till det första MERGEFIELD.
builder.MoveToMergeField("MyMergeField1", true, false);

// Observera att markören placeras omedelbart efter det första MERGEFIELD, och före det andra.
Assert.AreEqual(doc.Range.Fields[1].Start, builder.CurrentNode);
Assert.AreEqual(doc.Range.Fields[0].End, builder.CurrentNode.PreviousSibling);

// Om vi vill redigera fältets fältkod eller innehåll med hjälp av byggaren,
// dess markör måste vara inuti ett fält.
// För att placera den i ett fält, skulle vi behöva anropa dokumentbyggarens MoveTo-metod
// och skicka fältets start- eller separatornod som ett argument.
builder.Write(" Text between our merge fields. ");

doc.Save(ArtifactsDir + "DocumentBuilder.MergeFields.docx");
```

### Se även

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## InsertField(*string, string*) {#insertfield_2}

Infogar ett Word-fält i ett dokument utan att uppdatera fältresultatet.

```csharp
public Field InsertField(string fieldCode, string fieldValue)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fieldCode | String | Fältkoden som ska infogas (utan hängslen). |
| fieldValue | String | Fältvärdet som ska infogas. Passera`null` för fält som inte har ett värde. |

### Returvärde

A[`Field`](../../../aspose.words.fields/field/) objekt som representerar det infogade fältet.

## Anmärkningar

Fält i Microsoft Word-dokument består av en fältkod och ett fältresultat. Fältkoden är som en formel och fältresultatet är som det värde som formeln ger. Fältkoden kan också innehålla fältomkopplare som är som ytterligare instruktioner för att utföra en specifik åtgärd.

Du kan växla mellan att visa fältkoder och resultat i ditt dokument i Microsoft Word med kortkommandot Alt+F9. Fältkoder visas mellan klammerparenteser ( { } ).

För att skapa ett fält måste du ange en fälttyp, fältkod och ett "platshållare"-fältvärde. Om du inte är säker på en viss fältkodssyntax, skapa fältet i Microsoft Word first och växla för att se dess fältkod .

Aspose.Words kan beräkna fältresultat för de flesta fälttyper, men denna metod uppdaterar inte fältresultatet automatiskt. Eftersom fältresultatet inte beräknas automatiskt, förväntas du skicka något strängvärde (eller till och med en tom sträng) som kommer att infogas i fältresultatet. Detta värde kommer att finnas kvar i fältresultatet som en platshållare tills fältet är updated. För att uppdatera fältresultatet kan du ringa[`Update`](../../../aspose.words.fields/field/update/)på fältobjektet returned till dig eller[`UpdateFields`](../../document/updatefields/) för att uppdatera fält i hela dokumentet.

## Exempel

Visar hur man ställer in sidnumrering i ett avsnitt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Section 1, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 1, page 3.");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("Section 2, page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Section 2, page 3.");

// Flytta dokumentbyggaren till det första avsnittets primära rubrik,
// som varje sida i det avsnittet kommer att visa.
builder.MoveToSection(0);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

// Infoga ett PAGE-fält som visar numret på den aktuella sidan.
builder.Write("Page ");
builder.InsertField("PAGE", "");

// Konfigurera avsnittet så att sidräkningen som PAGE-fälten visar börjar från 5.
// Konfigurera också alla PAGE-fält för att visa deras sidnummer med stora romerska siffror.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.RestartPageNumbering = true;
pageSetup.PageStartingNumber = 5;
pageSetup.PageNumberStyle = NumberStyle.UppercaseRoman;

// Skapa en annan primär rubrik för den andra sektionen, med ett annat PAGE-fält.
builder.MoveToSection(1);
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write(" - ");
builder.InsertField("PAGE", "");
builder.Write(" - ");

// Konfigurera avsnittet så att sidantal som PAGE-fält visar börjar från 10.
// Konfigurera också alla PAGE-fält för att visa deras sidnummer med arabiska siffror.
pageSetup = doc.Sections[1].PageSetup;
pageSetup.PageStartingNumber = 10;
pageSetup.RestartPageNumbering = true;
pageSetup.PageNumberStyle = NumberStyle.Arabic;

doc.Save(ArtifactsDir + "PageSetup.PageNumbering.docx");
```

### Se även

* class [Field](../../../aspose.words.fields/field/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
