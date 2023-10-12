---
title: FieldSkipIf.LeftExpression
second_title: Aspose.Words för .NET API Referens
description: FieldSkipIf fast egendom. Hämtar eller ställer in den vänstra delen av jämförelseuttrycket.
type: docs
weight: 30
url: /sv/net/aspose.words.fields/fieldskipif/leftexpression/
---
## FieldSkipIf.LeftExpression property

Hämtar eller ställer in den vänstra delen av jämförelseuttrycket.

```csharp
public string LeftExpression { get; set; }
```

### Exempel

Visar hur man hoppar över sidor i en sammanfogning med hjälp av SKIPIF-fältet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga ett SKIPIF-fält. Om den aktuella raden i en kopplingsoperation uppfyller villkoret
// som uttrycken i det här fältet anger, avbryter åtgärden för sammankoppling av den aktuella raden,
// kasserar det aktuella sammanslagningsdokumentet och flyttar sedan omedelbart till nästa rad för att påbörja nästa sammanslagningsdokument.
FieldSkipIf fieldSkipIf = (FieldSkipIf) builder.InsertField(FieldType.FieldSkipIf, true);

// Flytta byggaren till SKIPIF-fältets separator så att vi kan placera ett MERGEFIELD inuti SKIPIF-fältet.
builder.MoveTo(fieldSkipIf.Separator);
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Department";

// MERGEFIELD hänvisar till kolumnen "Avdelning" i vår datatabell. Om en rad från den tabellen
// har värdet "HR" i kolumnen "Avdelning", då kommer den här raden att uppfylla villkoret.
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "HR";

// Lägg till innehåll i vårt dokument, skapa datakällan och kör sammankopplingen.
builder.MoveToDocumentEnd();
builder.Write("Dear ");
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
builder.Writeln(", ");

 // Den här tabellen har tre rader, och en av dem uppfyller villkoret för vårt SKIPIF-fält.
// Brevkopplingen kommer att producera två sidor.
DataTable table = new DataTable("Employees");
table.Columns.Add("Name");
table.Columns.Add("Department");
table.Rows.Add("John Doe", "Sales");
table.Rows.Add("Jane Doe", "Accounting");
table.Rows.Add("John Cardholder", "HR");

doc.MailMerge.Execute(table);
doc.Save(ArtifactsDir + "Field.SKIPIF.docx");
```

Visar hur man använder MERGEREC- och MERGESEQ-fälten för att antalet och räkna sammanslagningsposter i en sammankopplings utdatadokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
builder.Writeln(",");

// Ett MERGEREC-fält kommer att skriva ut radnumret för de data som slås samman i varje sammanslagningsutdatadokument.
builder.Write("\nRow number of record in data source: ");
FieldMergeRec fieldMergeRec = (FieldMergeRec)builder.InsertField(FieldType.FieldMergeRec, true);

Assert.AreEqual(" MERGEREC ", fieldMergeRec.GetFieldCode());

// Ett MERGESEQ-fält kommer att räkna antalet lyckade sammanslagningar och skriva ut det aktuella värdet på varje sida.
// Om en sammanslagning inte hoppar över några rader och inte anropar några SKIP/SKIPIF/NEXT/NEXTIF-fält, så lyckas alla sammanslagningar.
// Fälten MERGESEQ och MERGEREC kommer att visa samma resultat om deras sammanslagning lyckades.
builder.Write("\nSuccessful merge number: ");
FieldMergeSeq fieldMergeSeq = (FieldMergeSeq)builder.InsertField(FieldType.FieldMergeSeq, true);

Assert.AreEqual(" MERGESEQ ", fieldMergeSeq.GetFieldCode());

// Infoga ett SKIPIF-fält, vilket kommer att hoppa över en sammanslagning om namnet är "John Doe".
FieldSkipIf fieldSkipIf = (FieldSkipIf)builder.InsertField(FieldType.FieldSkipIf, true);
builder.MoveTo(fieldSkipIf.Separator);
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Name";
fieldSkipIf.LeftExpression = "=";
fieldSkipIf.RightExpression = "John Doe";

// Skapa en datakälla med 3 rader, en av dem har "John Doe" som ett värde för kolumnen "Namn".
// Eftersom ett SKIPIF-fält kommer att triggas en gång av det värdet, kommer utdata från vår sammanslagning att ha 2 sidor istället för 3.
// På sidan 1 kommer både MERGESEQ och MERGEREC fälten att visa "1".
// På sidan 2 kommer MERGEREC-fältet att visa "3" och MERGESEQ-fältet kommer att visa "2".
DataTable table = new DataTable("Employees");
table.Columns.Add("Name");
table.Rows.Add(new[] { "Jane Doe" });
table.Rows.Add(new[] { "John Doe" });
table.Rows.Add(new[] { "Joe Bloggs" });

doc.MailMerge.Execute(table);            
doc.Save(ArtifactsDir + "Field.MERGEREC.MERGESEQ.docx");
```

### Se även

* class [FieldSkipIf](../)
* namnutrymme [Aspose.Words.Fields](../../fieldskipif/)
* hopsättning [Aspose.Words](../../../)


