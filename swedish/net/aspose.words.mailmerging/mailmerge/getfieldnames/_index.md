---
title: MailMerge.GetFieldNames
second_title: Aspose.Words för .NET API Referens
description: MailMerge metod. Returnerar en samling av kopplingsfältnamn som är tillgängliga i dokumentet.
type: docs
weight: 220
url: /sv/net/aspose.words.mailmerging/mailmerge/getfieldnames/
---
## MailMerge.GetFieldNames method

Returnerar en samling av kopplingsfältnamn som är tillgängliga i dokumentet.

```csharp
public string[] GetFieldNames()
```

### Anmärkningar

Returnerar fullständiga sammanslagningsfältsnamn inklusive valfritt prefix. Eliminerar inte dubbletter av fältnamn.

En ny sträng[]-array skapas vid varje samtal.

Inkluderar "mustasch" fältnamn if[`UseNonMergeFields`](../usenonmergefields/) är **Sann**.

### Exempel

Visar hur man får namn på alla sammanslagningsfält i ett dokument.

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
// med samma namn, och kör sedan sammanslagningen. 
string[] fieldNames = doc.MailMerge.GetFieldNames();

Assert.AreEqual(3, fieldNames.Length);

foreach (string fieldName in fieldNames)
    Assert.True(dataTable.Columns.Contains(fieldName));

doc.MailMerge.Execute(dataTable);
```

### Se även

* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../mailmerge/)
* hopsättning [Aspose.Words](../../../)


