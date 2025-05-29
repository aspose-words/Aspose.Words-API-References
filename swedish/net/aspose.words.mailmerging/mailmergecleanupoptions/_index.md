---
title: MailMergeCleanupOptions Enum
linktitle: MailMergeCleanupOptions
articleTitle: MailMergeCleanupOptions
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.MailMergeCleanupOptions-enum för att effektivt hantera rensning av dokumentkopplingar. Optimera dina dokument genom att sömlöst kontrollera borttagning av objekt.
type: docs
weight: 4540
url: /sv/net/aspose.words.mailmerging/mailmergecleanupoptions/
---
## MailMergeCleanupOptions enumeration

Anger alternativ som avgör vilka objekt som tas bort under dokumentkoppling.

```csharp
[Flags]
public enum MailMergeCleanupOptions
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Anger ett standardvärde. |
| RemoveEmptyParagraphs | `1` | Anger om stycken som innehöll fält för koppling av dokument utan data ska tas bort från dokumentet. När det här alternativet är aktiverat tas även stycken bort som innehåller start- och slutfält för regionskoppling, vilka annars är tomma. |
| RemoveUnusedRegions | `2` | Anger om oanvända områden för koppling av dokument ska tas bort från dokumentet. |
| RemoveUnusedFields | `4` | Anger om oanvända kopplingsfält ska tas bort från dokumentet. |
| RemoveContainingFields | `8` | Anger om fält som innehåller kopplingsfält (till exempel IF) ska tas bort från dokumentet. om de kapslade kopplingsfälten tas bort. |
| RemoveStaticFields | `10` | Anger om statiska fält ska tas bort från dokumentet. Statiska fält är fält vars resultat förblir desamma vid dokumentändringar. Fält vars resultat inte lagras i ett dokument och beräknas direkt (somFieldListNum , FieldSymbol , etc.) anses inte vara statiska. |
| RemoveEmptyTableRows | `20` | Anger om tomma rader som innehåller områden för koppling av dokument ska tas bort från dokumentet. |
| RemoveEmptyTables | `40` | Anger om tabeller som innehåller kopplade dokumentregioner som togs bort med ska tas bort från dokumentet.RemoveUnusedRegions eller denRemoveEmptyTableRows alternativ. |

## Exempel

Visar hur man tar bort en hel tom tabell under en dokumentkoppling.

```csharp
DataTable tableCustomers = new DataTable("A");
tableCustomers.Columns.Add("CustomerID");
tableCustomers.Columns.Add("CustomerName");
tableCustomers.Rows.Add(new object[] { 1, "John Doe" });
tableCustomers.Rows.Add(new object[] { 2, "Jane Doe" });

DataSet ds = new DataSet();
ds.Tables.Add(tableCustomers);

Document doc = new Document(MyDir + "Mail merge tables.docx");
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Table, true).Count);

doc.MailMerge.MergeDuplicateRegions = false;
doc.MailMerge.CleanupOptions = MailMergeCleanupOptions.RemoveEmptyTables | MailMergeCleanupOptions.RemoveUnusedRegions;
doc.MailMerge.ExecuteWithRegions(ds.Tables["A"]);

doc.Save(ArtifactsDir + "MailMerge.RemoveEmptyTables.docx");

doc = new Document(ArtifactsDir + "MailMerge.RemoveEmptyTables.docx");
Assert.AreEqual(1, doc.GetChildNodes(NodeType.Table, true).Count);
```

Visar hur man tar bort tomma stycken som en dokumentkoppling kan skapa från det sammanfogade utdatadokumentet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD TableStart:MyTable");
builder.InsertField(" MERGEFIELD FirstName ");
builder.Write(" ");
builder.InsertField(" MERGEFIELD LastName ");
builder.InsertField(" MERGEFIELD TableEnd:MyTable");

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "", "" });
dataTable.Rows.Add(new object[] { "Jane", "Doe" });

doc.MailMerge.CleanupOptions = mailMergeCleanupOptions;
doc.MailMerge.ExecuteWithRegions(dataTable);

if (doc.MailMerge.CleanupOptions == MailMergeCleanupOptions.RemoveEmptyParagraphs) 
    Assert.AreEqual(
        "John Doe\r" +
        "Jane Doe", doc.GetText().Trim());
else
    Assert.AreEqual(
        "John Doe\r" +
        " \r" +
        "Jane Doe", doc.GetText().Trim());
```

Visar hur man automatiskt tar bort MERGEFIELDS som inte används under dokumentkoppling.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa ett dokument med MERGEFIELDS för tre kolumner i en datakällstabell för dokumentkoppling,
// och skapa sedan en tabell med endast två kolumner vars namn matchar våra MERGEFIELDS.
builder.InsertField(" MERGEFIELD FirstName ");
builder.Write(" ");
builder.InsertField(" MERGEFIELD LastName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "Joe", "Bloggs" });

// Vårt tredje MERGEFIELD refererar till en "Stad"-kolumn, som inte finns i vår datakälla.
// Kopplningen av dokument lämnar fält som detta intakta i sitt tillstånd före sammanslagningen.
// Om egenskapen "CleanupOptions" ställs in på "RemoveUnusedFields" tas alla MERGEFIELDS bort.
// som inte används under en dokumentkoppling för att rensa upp i de sammanslagna dokumenten.
doc.MailMerge.CleanupOptions = mailMergeCleanupOptions;
doc.MailMerge.Execute(dataTable);

if (mailMergeCleanupOptions == MailMergeCleanupOptions.RemoveUnusedFields || 
    mailMergeCleanupOptions == MailMergeCleanupOptions.RemoveStaticFields)
    Assert.AreEqual(0, doc.Range.Fields.Count);
else
    Assert.AreEqual(2, doc.Range.Fields.Count);
```

### Se även

* namnutrymme [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../)
