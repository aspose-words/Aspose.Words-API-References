---
title: FieldSkipIf.ComparisonOperator
linktitle: ComparisonOperator
articleTitle: ComparisonOperator
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldSkipIf ComparisonOperator och hantera och anpassa enkelt dina jämförelseoperatorer för förbättrad datahantering.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldskipif/comparisonoperator/
---
## FieldSkipIf.ComparisonOperator property

Hämtar eller ställer in jämförelseoperatorn.

```csharp
public string ComparisonOperator { get; set; }
```

## Exempel

Visar hur man hoppar över sidor i en dokumentkoppling med hjälp av SKIPIF-fältet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga ett SKIPIF-fält. Om den aktuella raden i en dokumentkoppling uppfyller villkoret
// vilket uttrycken i detta fält anger, då avbryter dokumentkopplingen den aktuella raden,
// kasserar det aktuella sammanfogade dokumentet och går sedan omedelbart till nästa rad för att påbörja nästa sammanfogade dokument.
FieldSkipIf fieldSkipIf = (FieldSkipIf) builder.InsertField(FieldType.FieldSkipIf, true);

// Flytta byggaren till SKIPIF-fältets avgränsare så att vi kan placera ett MERGEFIELD inuti SKIPIF-fältet.
builder.MoveTo(fieldSkipIf.Separator);
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Department";

// MERGEFIELD refererar till kolumnen "Avdelning" i vår datatabell. Om en rad från den tabellen
// har värdet "HR" i kolumnen "Avdelning", så uppfyller den här raden villkoret.
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "HR";

// Lägg till innehåll i vårt dokument, skapa datakällan och kör dokumentkopplingen.
builder.MoveToDocumentEnd();
builder.Write("Dear ");
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
builder.Writeln(", ");

 // Den här tabellen har tre rader, och en av dem uppfyller villkoret för vårt SKIPIF-fält.
// Kopplad dokument kommer att producera två sidor.
DataTable table = new DataTable("Employees");
table.Columns.Add("Name");
table.Columns.Add("Department");
table.Rows.Add("John Doe", "Sales");
table.Rows.Add("Jane Doe", "Accounting");
table.Rows.Add("John Cardholder", "HR");

doc.MailMerge.Execute(table);
doc.Save(ArtifactsDir + "Field.SKIPIF.docx");
```

Visar hur man använder fälten MERGEREC och MERGESEQ för att numrera och räkna kopplade dokument i utdatadokumenten för en kopplad dokumenthantering.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
builder.Writeln(",");

// Ett MERGEREC-fält skriver ut radnumret för den data som sammanfogas i varje sammanfogningsdokument.
builder.Write("\nRow number of record in data source: ");
FieldMergeRec fieldMergeRec = (FieldMergeRec)builder.InsertField(FieldType.FieldMergeRec, true);

Assert.AreEqual(" MERGEREC ", fieldMergeRec.GetFieldCode());

// Ett MERGESEQ-fält räknar antalet lyckade sammanslagningar och skriver ut det aktuella värdet på varje sida.
// Om en dokumentkoppling inte hoppar över några rader och inte anropar några SKIP/SKIPIF/NEXT/NEXTIF-fält, då lyckas alla sammanslagningar.
// Fälten MERGESEQ och MERGEREC kommer att visa samma resultat om deras dokumentkoppling lyckades.
builder.Write("\nSuccessful merge number: ");
FieldMergeSeq fieldMergeSeq = (FieldMergeSeq)builder.InsertField(FieldType.FieldMergeSeq, true);

Assert.AreEqual(" MERGESEQ ", fieldMergeSeq.GetFieldCode());

// Infoga ett SKIPIF-fält, vilket hoppar över en sammanslagning om namnet är "John Doe".
FieldSkipIf fieldSkipIf = (FieldSkipIf)builder.InsertField(FieldType.FieldSkipIf, true);
builder.MoveTo(fieldSkipIf.Separator);
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "John Doe";

// Skapa en datakälla med 3 rader, varav en har "John Doe" som värde för kolumnen "Namn".
// Eftersom ett SKIPIF-fält utlöses en gång av det värdet, kommer resultatet av vår dokumentkoppling att ha 2 sidor istället för 3.
// På sidan 1 kommer fälten MERGESEQ och MERGEREC båda att visa "1".
// På sidan 2 kommer MERGEREC-fältet att visa "3" och MERGESEQ-fältet kommer att visa "2".
DataTable table = new DataTable("Employees");
table.Columns.Add("Name");
table.Rows.Add("Jane Doe");
table.Rows.Add("John Doe");
table.Rows.Add("Joe Bloggs");

doc.MailMerge.Execute(table);
doc.Save(ArtifactsDir + "Field.MERGEREC.MERGESEQ.docx");
```

### Se även

* class [FieldSkipIf](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
