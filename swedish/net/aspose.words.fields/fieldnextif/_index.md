---
title: FieldNextIf Class
linktitle: FieldNextIf
articleTitle: FieldNextIf
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.Fields.FieldNextIf – implementera NEXTIF-fält effektivt för att förbättra dokumentautomation och effektivisera dina arbetsflöden.
type: docs
weight: 2600
url: /sv/net/aspose.words.fields/fieldnextif/
---
## FieldNextIf class

Implementerar NEXTIF-fältet.

För att lära dig mer, besök[Arbeta med fält](https://docs.aspose.com/words/net/working-with-fields/) dokumentationsartikel.

```csharp
public class FieldNextIf : Field
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [FieldNextIf](fieldnextif/)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [ComparisonOperator](../../aspose.words.fields/fieldnextif/comparisonoperator/) { get; set; } | Hämtar eller ställer in jämförelseoperatorn. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Hämtar texten som representerar det visade fältresultatet. |
| [End](../../aspose.words.fields/field/end/) { get; } | Hämtar noden som representerar fältets slut. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Får en[`FieldFormat`](../fieldformat/)objekt som ger typad åtkomst till fältets formatering. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Hämtar eller anger om det aktuella resultatet av fältet inte längre är korrekt (inaktuellt) på grund av andra ändringar som gjorts i dokumentet. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Hämtar eller anger om fältet är låst (resultatet ska inte beräknas om). |
| [LeftExpression](../../aspose.words.fields/fieldnextif/leftexpression/) { get; set; } | Hämtar eller anger den vänstra delen av jämförelseuttrycket. |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Hämtar eller ställer in fältets LCID. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Hämtar eller anger text som är mellan fältavgränsaren och fältslutet. |
| [RightExpression](../../aspose.words.fields/fieldnextif/rightexpression/) { get; set; } | Hämtar eller anger den högra delen av jämförelseuttrycket. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Hämtar noden som representerar fältseparatorn. Kan vara`null` . |
| [Start](../../aspose.words.fields/field/start/) { get; } | Hämtar noden som representerar början av fältet. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Hämtar fälttypen Microsoft Word. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). Både fältkod och fältresultat för underfält inkluderas. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Returnerar text mellan fältstart och fältavgränsare (eller fältslut om det inte finns någon avgränsare). |
| [Remove](../../aspose.words.fields/field/remove/)() | Tar bort fältet från dokumentet. Returnerar en nod direkt efter fältet. Om fältets slut är den sista undernoden till dess överordnade nod, returneras dess överordnade stycke. Om fältet redan är borttaget returneras`null` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Utför fältavkopplingen. |
| [Update](../../aspose.words.fields/field/update/)() | Utför fältuppdateringen. Körs om fältet redan uppdateras. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Utför en fältuppdatering. Körs om fältet redan uppdateras. |

## Anmärkningar

Jämför värdena som anges av uttrycken[`LeftExpression`](./leftexpression/) och[`RightExpression`](./rightexpression/) i jämförelse med hjälp av operatorn som anges av[`ComparisonOperator`](./comparisonoperator/) Om jämförelsen är sann, slås nästa datapost samman med det aktuella sammanfogningsdokumentet. (Sammanfogningsfält som följer NEXTIF i huvuddokumentet ersätts med värden från nästa datapost istället för den aktuella dataposten.) Om jämförelsen är falsk slås nästa datapost samman med ett nytt sammanfogningsdokument.

## Exempel

Visar hur man använder NEXT/NEXTIF-fält för att sammanfoga flera rader till en sida under en dokumentkoppling.

```csharp
public void FieldNext()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Skapa en datakälla för vår dokumentkoppling med 3 rader.
    // En dokumentkoppling som använder den här tabellen skulle normalt skapa ett 3-sidigt dokument.
    DataTable table = new DataTable("Employees");
    table.Columns.Add("Courtesy Title");
    table.Columns.Add("First Name");
    table.Columns.Add("Last Name");
    table.Rows.Add("Mr.", "John", "Doe");
    table.Rows.Add("Mrs.", "Jane", "Cardholder");
    table.Rows.Add("Mr.", "Joe", "Bloggs");

    InsertMergeFields(builder, "First row: ");

    // Om vi har flera kopplingsfält med samma fältnamn,
    // de kommer att ta emot data från samma rad i datakällan och visa samma värde efter sammanslagningen.
    // Ett NEXT-fält anger direkt att dokumentkopplingen ska flyttas ner en rad,
    // vilket innebär att alla MERGEFIELD-värden som följer efter NEXT-fältet kommer att ta emot data från nästa rad.
    // Se till att aldrig försöka hoppa till nästa rad medan du redan är på sista raden.
    FieldNext fieldNext = (FieldNext)builder.InsertField(FieldType.FieldNext, true);

    Assert.AreEqual(" NEXT ", fieldNext.GetFieldCode());

    // Efter sammanslagningen, de datakällvärden som dessa MERGEFIELDS accepterar
     // kommer att hamna på samma sida som MERGEFIELDS ovan.
    InsertMergeFields(builder, "Second row: ");

    // Ett NEXTIF-fält har samma funktion som ett NEXT-fält,
    // men den hoppar bara till nästa rad om ett uttalande konstruerat av följande 3 egenskaper är sant.
    FieldNextIf fieldNextIf = (FieldNextIf)builder.InsertField(FieldType.FieldNextIf, true);
    fieldNextIf.LeftExpression = "5";
    fieldNextIf.RightExpression = "2 + 3";
    fieldNextIf.ComparisonOperator = "=";

    Assert.AreEqual(" NEXTIF  5 = \"2 + 3\"", fieldNextIf.GetFieldCode());

    // Om jämförelsen som görs i ovanstående fält är korrekt,
    // följande 3 mergefält kommer att ta data från den tredje raden.
    // Annars kommer dessa fält att ta data från rad 2 igen.
    InsertMergeFields(builder, "Third row: ");

    doc.MailMerge.Execute(table);

     // Vår datakälla har 3 rader, och vi hoppade över rader två gånger.
    // Vårt utdatadokument kommer att ha 1 sida med data från alla 3 rader.
    doc.Save(ArtifactsDir + "Field.NEXT.NEXTIF.docx");
}

/// <summary>
/// Använder en dokumentbyggare för att infoga MERGEFIELDS för en datakälla som innehåller kolumner med namnen "Courtesy Title", "First Name" och "Last Name".
/// </summary>
public void InsertMergeFields(DocumentBuilder builder, string firstFieldTextBefore)
{
    InsertMergeField(builder, "Courtesy Title", firstFieldTextBefore, " ");
    InsertMergeField(builder, "First Name", null, " ");
    InsertMergeField(builder, "Last Name", null, null);
    builder.InsertParagraph();
}

/// <summary>
/// Använder en dokumentbyggare för att infoga ett MERRGEFIELD med angivna egenskaper.
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
