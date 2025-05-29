---
title: FieldNextIf.LeftExpression
linktitle: LeftExpression
articleTitle: LeftExpression
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldNextIf LeftExpression. Hantera enkelt vänster sida av dina jämförelseuttryck för förbättrad datahantering och analys.
type: docs
weight: 30
url: /sv/net/aspose.words.fields/fieldnextif/leftexpression/
---
## FieldNextIf.LeftExpression property

Hämtar eller anger den vänstra delen av jämförelseuttrycket.

```csharp
public string LeftExpression { get; set; }
```

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

* class [FieldNextIf](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
