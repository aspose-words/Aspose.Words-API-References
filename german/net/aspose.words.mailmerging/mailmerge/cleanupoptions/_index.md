---
title: MailMerge.CleanupOptions
second_title: Aspose.Words für .NET-API-Referenz
description: MailMerge eigendom. Ruft eine Reihe von Flags ab die angeben welche Elemente beim Seriendruck entfernt werden sollen oder legt diese fest.
type: docs
weight: 10
url: /de/net/aspose.words.mailmerging/mailmerge/cleanupoptions/
---
## MailMerge.CleanupOptions property

Ruft eine Reihe von Flags ab, die angeben, welche Elemente beim Seriendruck entfernt werden sollen, oder legt diese fest.

```csharp
public MailMergeCleanupOptions CleanupOptions { get; set; }
```

### Beispiele

Zeigt, wie leere Absätze, die bei einem Seriendruck entstehen könnten, aus dem Seriendruck-Ausgabedokument entfernt werden.

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

Zeigt, wie MERGEFIELDs, die beim Seriendruck nicht verwendet werden, automatisch entfernt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie ein Dokument mit MERGEFIELDs für drei Spalten einer Serienbrief-Datenquellentabelle.
// und dann eine Tabelle mit nur zwei Spalten erstellen, deren Namen mit unseren MERGEFIELDs übereinstimmen.
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

// Unser drittes MERGEFIELD verweist auf eine Spalte „Stadt“, die in unserer Datenquelle nicht vorhanden ist.
// Beim Seriendruck bleiben Felder wie dieses in ihrem Zustand vor dem Seriendruck erhalten.
// Wenn Sie die Eigenschaft „CleanupOptions“ auf „RemoveUnusedFields“ setzen, werden alle MERGEFIELDs entfernt
// die während eines Seriendrucks nicht verwendet werden, um die Seriendokumente zu bereinigen.
doc.MailMerge.CleanupOptions = mailMergeCleanupOptions;
doc.MailMerge.Execute(dataTable);

if (mailMergeCleanupOptions == MailMergeCleanupOptions.RemoveUnusedFields || 
    mailMergeCleanupOptions == MailMergeCleanupOptions.RemoveStaticFields)
    Assert.AreEqual(0, doc.Range.Fields.Count);
else
    Assert.AreEqual(2, doc.Range.Fields.Count);
```

### Siehe auch

* enum [MailMergeCleanupOptions](../../mailmergecleanupoptions/)
* class [MailMerge](../)
* namensraum [Aspose.Words.MailMerging](../../mailmerge/)
* Montage [Aspose.Words](../../../)


