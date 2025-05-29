---
title: MailMerge.GetFieldNames
linktitle: GetFieldNames
articleTitle: GetFieldNames
second_title: Aspose.Words för .NET
description: Upptäck MailMerge GetFieldNames-metoden för att enkelt komma åt och använda alla fältnamn för kopplingar i ditt dokument för effektiv dokumentautomation.
type: docs
weight: 220
url: /sv/net/aspose.words.mailmerging/mailmerge/getfieldnames/
---
## MailMerge.GetFieldNames method

Returnerar en samling namn på fält för kopplingsmeddelanden som finns tillgängliga i dokumentet.

```csharp
public string[] GetFieldNames()
```

## Anmärkningar

Returnerar fullständiga kopplingsfältnamn inklusive valfritt prefix. Tar inte bort dubbletter av fältnamn.

En ny strängmatris skapas vid varje anrop.

Inkluderar fältnamn för "mustasch" om[`UseNonMergeFields`](../usenonmergefields/) är`sann`.

## Exempel

Visar hur man hämtar namnen på alla kopplingsfält i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD FirstName ");
builder.Write(" ");
builder.InsertField(" MERGEFIELD LastName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Columns.Add("City");
dataTable.Rows.Add(new object[] { "John", "Doe", "New York" });
dataTable.Rows.Add(new object[] { "Joe", "Bloggs", "Washington" });

// För varje MERGEFIELD-namn i dokumentet, se till att datatabellen innehåller en kolumn
 // med samma namn och sedan köra dokumentkopplingen.
string[] fieldNames = doc.MailMerge.GetFieldNames();

Assert.AreEqual(3, fieldNames.Length);

foreach (string fieldName in fieldNames)
    Assert.True(dataTable.Columns.Contains(fieldName));

doc.MailMerge.Execute(dataTable);
```

### Se även

* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)
