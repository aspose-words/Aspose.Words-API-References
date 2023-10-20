---
title: MailMerge.CleanupOptions
linktitle: CleanupOptions
articleTitle: CleanupOptions
second_title: Aspose.Words för .NET
description: MailMerge CleanupOptions fast egendom. Hämtar eller ställer in en uppsättning flaggor som anger vilka objekt som ska tas bort under kopplingen i C#.
type: docs
weight: 10
url: /sv/net/aspose.words.mailmerging/mailmerge/cleanupoptions/
---
## MailMerge.CleanupOptions property

Hämtar eller ställer in en uppsättning flaggor som anger vilka objekt som ska tas bort under kopplingen.

```csharp
public MailMergeCleanupOptions CleanupOptions { get; set; }
```

## Exempel

Visar hur man tar bort tomma stycken som en sammankoppling kan skapa från sammanslagningsutdatadokumentet.

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

Visar hur man automatiskt tar bort MERGEFIELDs som blir oanvända under kopplingen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Skapa ett dokument med MERGEFIELDs för tre kolumner i en tabell för kopplingsdatakäll,
// och skapa sedan en tabell med endast två kolumner vars namn matchar våra MERGEFIELDs.
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

// Vår tredje MERGEFIELD refererar till en "Stad"-kolumn, som inte finns i vår datakälla.
// Brevkopplingen kommer att lämna fält som detta intakta i tillståndet före sammanslagningen.
// Om du ställer in "CleanupOptions"-egenskapen till "RemoveUusedFields" kommer alla MERGEFIELDs att tas bort
// som förblir oanvända under en sammankoppling för att rensa upp sammanslagningsdokumenten.
doc.MailMerge.CleanupOptions = mailMergeCleanupOptions;
doc.MailMerge.Execute(dataTable);

if (mailMergeCleanupOptions == MailMergeCleanupOptions.RemoveUnusedFields || 
    mailMergeCleanupOptions == MailMergeCleanupOptions.RemoveStaticFields)
    Assert.AreEqual(0, doc.Range.Fields.Count);
else
    Assert.AreEqual(2, doc.Range.Fields.Count);
```

### Se även

* enum [MailMergeCleanupOptions](../../mailmergecleanupoptions/)
* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)
