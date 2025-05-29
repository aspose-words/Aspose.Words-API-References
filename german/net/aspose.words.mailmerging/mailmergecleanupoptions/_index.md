---
title: MailMergeCleanupOptions Enum
linktitle: MailMergeCleanupOptions
articleTitle: MailMergeCleanupOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.MailMergeCleanupOptions, um die Serienbriefbereinigung effizient zu verwalten. Optimieren Sie Ihre Dokumente durch die nahtlose Steuerung der Elemententfernung.
type: docs
weight: 4540
url: /de/net/aspose.words.mailmerging/mailmergecleanupoptions/
---
## MailMergeCleanupOptions enumeration

Gibt Optionen an, die bestimmen, welche Elemente beim Seriendruck entfernt werden.

```csharp
[Flags]
public enum MailMergeCleanupOptions
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Gibt einen Standardwert an. |
| RemoveEmptyParagraphs | `1` | Gibt an, ob Absätze, die Serienbrieffelder ohne Daten enthalten, aus dem Dokument entfernt werden sollen. Wenn diese Option aktiviert ist, werden auch Absätze entfernt, die ansonsten leere Serienbrieffelder für den Bereichsanfang und das Bereichsende enthalten. |
| RemoveUnusedRegions | `2` | Gibt an, ob nicht verwendete Serienbriefbereiche aus dem Dokument entfernt werden sollen. |
| RemoveUnusedFields | `4` | Gibt an, ob nicht verwendete Seriendruckfelder aus dem Dokument entfernt werden sollen. |
| RemoveContainingFields | `8` | Gibt an, ob Felder, die Seriendruckfelder enthalten (z. B. IFs), aus dem Dokument entfernt werden sollen , wenn die verschachtelten Seriendruckfelder entfernt werden. |
| RemoveStaticFields | `10` | Gibt an, ob statische Felder aus dem Dokument entfernt werden sollen. Statische Felder sind Felder, deren Ergebnisse bei jeder Dokumentänderung unverändert bleiben. Felder, deren Ergebnisse nicht in einem Dokument gespeichert werden und die direkt berechnet werden (wieFieldListNum , FieldSymbol , usw.) werden nicht als statisch betrachtet. |
| RemoveEmptyTableRows | `20` | Gibt an, ob leere Zeilen, die Seriendruckbereiche enthalten, aus dem Dokument entfernt werden sollen. |
| RemoveEmptyTables | `40` | Gibt an, ob aus dem Dokument Tabellen entfernt werden sollen, die Serienbriefbereiche enthalten, die mit entfernt wurden, entwederRemoveUnusedRegions oder dieRemoveEmptyTableRows option. |

## Beispiele

Zeigt, wie beim Seriendruck die gesamte leere Tabelle entfernt wird.

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

Zeigt, wie leere Absätze, die bei einer Seriendruckverarbeitung entstehen können, aus dem Seriendruck-Ausgabedokument entfernt werden.

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

Zeigt, wie MERGEFIELDs, die während der Serienbrieferstellung nicht verwendet werden, automatisch entfernt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Erstellen Sie ein Dokument mit MERGEFIELDs für drei Spalten einer Serienbrief-Datenquellentabelle,
// und erstellen Sie dann eine Tabelle mit nur zwei Spalten, deren Namen mit unseren MERGEFIELDs übereinstimmen.
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
// Der Seriendruck lässt Felder wie dieses in ihrem Zustand vor dem Seriendruck unverändert.
// Wenn Sie die Eigenschaft „CleanupOptions“ auf „RemoveUnusedFields“ setzen, werden alle MERGEFIELDs entfernt
// die während eines Seriendrucks nicht verwendet werden, um die Seriendruckdokumente zu bereinigen.
doc.MailMerge.CleanupOptions = mailMergeCleanupOptions;
doc.MailMerge.Execute(dataTable);

if (mailMergeCleanupOptions == MailMergeCleanupOptions.RemoveUnusedFields || 
    mailMergeCleanupOptions == MailMergeCleanupOptions.RemoveStaticFields)
    Assert.AreEqual(0, doc.Range.Fields.Count);
else
    Assert.AreEqual(2, doc.Range.Fields.Count);
```

### Siehe auch

* namensraum [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../)
