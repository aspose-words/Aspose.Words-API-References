---
title: Class FieldNext
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Fields.FieldNext klass. Implementerar fältet NÄSTA.
type: docs
weight: 2180
url: /sv/net/aspose.words.fields/fieldnext/
---
## FieldNext class

Implementerar fältet NÄSTA.

För att lära dig mer, besök[Arbeta med Fields](https://docs.aspose.com/words/net/working-with-fields/) dokumentationsartikel.

```csharp
public class FieldNext : Field
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FieldNext](fieldnext/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [End](../../aspose.words.fields/field/end/) { get; } | Hämtar noden som representerar fältänden. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Får en[`FieldFormat`](../fieldformat/) objekt som ger maskinskriven åtkomst till fältets formatering. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Hämtar eller ställer in om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Hämtar eller ställer in om fältet är låst (ska inte räkna om resultatet). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Hämtar eller ställer in LCID för fältet. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Hämtar eller ställer in text som är mellan fältavgränsaren och fältslutet. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Hämtar noden som representerar fältseparatorn. Kan vara`null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Hämtar noden som representerar början av fältet. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Hämtar fälttypen Microsoft Word. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). Både fältkod och fältresultat för underordnade fält ingår. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). |
| [Remove](../../aspose.words.fields/field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod direkt efter fältet. Om fältets slut är den sista child av dess överordnade nod, returnerar dess överordnade stycke. Om fältet redan är borttaget, returneras`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Utför fältavlänkningen. |
| [Update](../../aspose.words.fields/field/update/)() | Utför fältuppdateringen. Kastar om fältet redan uppdateras. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Utför en fältuppdatering. Kastar om fältet redan uppdateras. |

### Anmärkningar

Slår ihop nästa datapost i det aktuella resulterande sammanslagna dokumentet, istället för att starta ett nytt sammanfogat dokument.

### Exempel

Visar hur du använder NEXT/NEXTIF-fält för att slå samman flera rader till en sida under en e-postkoppling.

```csharp
public void FieldNext()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Skapa en datakälla för vår brevkoppling med 3 rader.
    // En sammanslagning som använder den här tabellen skulle normalt skapa ett 3-sidigt dokument.
    DataTable table = new DataTable("Employees");
    table.Columns.Add("Courtesy Title");
    table.Columns.Add("First Name");
    table.Columns.Add("Last Name");
    table.Rows.Add("Mr.", "John", "Doe");
    table.Rows.Add("Mrs.", "Jane", "Cardholder");
    table.Rows.Add("Mr.", "Joe", "Bloggs");

    InsertMergeFields(builder, "First row: ");

    // Om vi har flera sammanslagningsfält med samma fältnamn,
    // de kommer att ta emot data från samma rad i datakällan och visa samma värde efter sammanslagningen.
    // Ett NÄSTA fält talar om för brevkopplingen omedelbart att flytta ned en rad,
    // vilket betyder att alla MERGEFIELDs som följer fältet NÄSTA kommer att ta emot data från nästa rad.
    // Se till att aldrig försöka hoppa till nästa rad medan du redan är på den sista raden.
    FieldNext fieldNext = (FieldNext)builder.InsertField(FieldType.FieldNext, true);

    Assert.AreEqual(" NEXT ", fieldNext.GetFieldCode());

    // Efter sammanslagning, datakällans värden som dessa MERGEFIELDs accepterar
     // kommer att hamna på samma sida som MERGEFIELDs ovan.
    InsertMergeFields(builder, "Second row: ");

    // Ett NEXTIF-fält har samma funktion som ett NEXT-fält,
    // men den hoppar till nästa rad endast om ett påstående som konstruerats av följande 3 egenskaper är sant.
    FieldNextIf fieldNextIf = (FieldNextIf)builder.InsertField(FieldType.FieldNextIf, true);
    fieldNextIf.LeftExpression = "5";
    fieldNextIf.RightExpression = "2 + 3";
    fieldNextIf.ComparisonOperator = "=";

    Assert.AreEqual(" NEXTIF  5 = \"2 + 3\"", fieldNextIf.GetFieldCode());

    // Om jämförelsen i fältet ovan är korrekt,
    // följande 3 sammanslagningsfält tar data från den tredje raden.
    // Annars kommer dessa fält att ta data från rad 2 igen.
    InsertMergeFields(builder, "Third row: ");

    doc.MailMerge.Execute(table);

     // Vår datakälla har 3 rader, och vi hoppade över rader två gånger.
    // Vårt utdatadokument kommer att ha 1 sida med data från alla tre raderna.
    doc.Save(ArtifactsDir + "Field.NEXT.NEXTIF.docx");
}

/// <summary>
/// Använder en dokumentbyggare för att infoga MERGEFIELDs för en datakälla som innehåller kolumner med namnet "Courtesy Title", "First Name" och "Last Name".
/// </summary>
public void InsertMergeFields(DocumentBuilder builder, string firstFieldTextBefore)
{
    InsertMergeField(builder, "Courtesy Title", firstFieldTextBefore, " ");
    InsertMergeField(builder, "First Name", null, " ");
    InsertMergeField(builder, "Last Name", null, null);
    builder.InsertParagraph();
}

/// <summary>
/// Använder en dokumentbyggare för att infoga ett MERRGEFIELD med specificerade egenskaper.
/// </summary>
public void InsertMergeField(DocumentBuilder builder, string fieldName, string textBefore, string textAfter)
{
    FieldMergeField field = (FieldMergeField) builder.InsertField(FieldType.FieldMergeField, true);
    field.FieldName = fieldName;
    field.TextBefore = textBefore;
    field.TextAfter = textAfter;
}
```

### Se även

* class [Field](../field/)
* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)


