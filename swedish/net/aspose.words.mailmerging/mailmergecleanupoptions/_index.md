---
title: Enum MailMergeCleanupOptions
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.MailMerging.MailMergeCleanupOptions uppräkning. Anger alternativ som bestämmer vilka objekt som tas bort under kopplingen.
type: docs
weight: 3850
url: /sv/net/aspose.words.mailmerging/mailmergecleanupoptions/
---
## MailMergeCleanupOptions enumeration

Anger alternativ som bestämmer vilka objekt som tas bort under kopplingen.

```csharp
[Flags]
public enum MailMergeCleanupOptions
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Anger ett standardvärde. |
| RemoveEmptyParagraphs | `1` | Anger om stycken som innehöll kopplingsfält utan data ska tas bort från dokumentet. När detta alternativ är inställt tas också stycken som innehåller regionstart- och slutkopplingsfält som annars är tomma bort. |
| RemoveUnusedRegions | `2` | Anger om oanvända kopplingsregioner ska tas bort från dokumentet. |
| RemoveUnusedFields | `4` | Anger om oanvända sammanslagningsfält ska tas bort från dokumentet. |
| RemoveContainingFields | `8` | Anger om fält som innehåller sammanslagningsfält (till exempel IF) ska tas bort från document om de kapslade sammanslagningsfälten tas bort. |
| RemoveStaticFields | `10` | Anger om statiska fält ska tas bort från dokumentet. Statiska fält är fält, som resultat förblir desamma vid alla dokumentändringar. Fält, som inte lagrar sina resultat i ett document och som beräknas i farten (somFieldListNum , FieldSymbol , etc.) anses inte vara statiska. |
| RemoveEmptyTableRows | `20` | Anger om tomma rader som innehåller kopplingsregioner ska tas bort från dokumentet. |

### Exempel

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

* namnutrymme [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../)


