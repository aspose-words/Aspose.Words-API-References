---
title: MailMerge.GetFieldNames
linktitle: GetFieldNames
articleTitle: GetFieldNames
second_title: Aspose.Words für .NET
description: Entdecken Sie die MailMerge GetFieldNames-Methode, um mühelos auf alle Serienbrief-Feldnamen in Ihrem Dokument zuzugreifen und diese für eine optimierte Dokumentautomatisierung zu verwenden.
type: docs
weight: 220
url: /de/net/aspose.words.mailmerging/mailmerge/getfieldnames/
---
## MailMerge.GetFieldNames method

Gibt eine Sammlung der im Dokument verfügbaren Seriendruckfeldnamen zurück.

```csharp
public string[] GetFieldNames()
```

## Bemerkungen

Gibt vollständige Seriendruckfeldnamen inklusive optionalem Präfix zurück. Doppelte Feldnamen werden nicht eliminiert.

Bei jedem Aufruf wird ein neues String-Array erstellt.

Enthält „Mustache“-Feldnamen, wenn[`UseNonMergeFields`](../usenonmergefields/) Ist`WAHR`.

## Beispiele

Zeigt, wie die Namen aller Seriendruckfelder in einem Dokument abgerufen werden.

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

// Stellen Sie für jeden MERGEFIELD-Namen im Dokument sicher, dass die Datentabelle eine Spalte enthält
    // mit demselben Namen und führen Sie dann den Serienbrief aus.
string[] fieldNames = doc.MailMerge.GetFieldNames();

Assert.AreEqual(3, fieldNames.Length);

foreach (string fieldName in fieldNames)
    Assert.True(dataTable.Columns.Contains(fieldName));

doc.MailMerge.Execute(dataTable);
```

### Siehe auch

* class [MailMerge](../)
* namensraum [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../../)
