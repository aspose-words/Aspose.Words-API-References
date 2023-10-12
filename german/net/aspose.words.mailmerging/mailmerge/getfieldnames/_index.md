---
title: MailMerge.GetFieldNames
second_title: Aspose.Words für .NET-API-Referenz
description: MailMerge methode. Gibt eine Sammlung von im Dokument verfügbaren Serienbrieffeldnamen zurück.
type: docs
weight: 220
url: /de/net/aspose.words.mailmerging/mailmerge/getfieldnames/
---
## MailMerge.GetFieldNames method

Gibt eine Sammlung von im Dokument verfügbaren Serienbrieffeldnamen zurück.

```csharp
public string[] GetFieldNames()
```

### Bemerkungen

Gibt vollständige Briefvorlagenfeldnamen einschließlich optionalem Präfix zurück. Eliminiert keine doppelten Feldnamen.

Bei jedem Aufruf wird ein neues String-Array erstellt.

Enthält „Schnurrbart“-Feldnamen, wenn[`UseNonMergeFields`](../usenonmergefields/) Ist`WAHR`.

### Beispiele

Zeigt, wie man Namen aller Zusammenführungsfelder in einem Dokument erhält.

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
* namensraum [Aspose.Words.MailMerging](../../mailmerge/)
* Montage [Aspose.Words](../../../)


