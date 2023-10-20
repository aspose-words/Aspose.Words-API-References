---
title: MailMergeCleanupOptions Enum
linktitle: MailMergeCleanupOptions
articleTitle: MailMergeCleanupOptions
second_title: Aspose.Words für .NET
description: Aspose.Words.MailMerging.MailMergeCleanupOptions opsomming. Gibt Optionen an die bestimmen welche Elemente beim Seriendruck entfernt werden in C#.
type: docs
weight: 3850
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
| RemoveEmptyParagraphs | `1` | Gibt an, ob Absätze, die Serienbrieffelder ohne Daten enthielten, aus dem Dokument entfernt werden sollen. Wenn diese Option festgelegt ist, werden Absätze, die ansonsten leere Serienanfangs- und -endfelder enthalten, ebenfalls entfernt. |
| RemoveUnusedRegions | `2` | Gibt an, ob nicht verwendete Seriendruckbereiche aus dem Dokument entfernt werden sollen. |
| RemoveUnusedFields | `4` | Gibt an, ob nicht verwendete Zusammenführungsfelder aus dem Dokument entfernt werden sollen. |
| RemoveContainingFields | `8` | Gibt an, ob Felder, die Zusammenführungsfelder (z. B. IFs) enthalten, aus dem Dokument entfernt werden sollen , wenn die verschachtelten Zusammenführungsfelder entfernt werden. |
| RemoveStaticFields | `10` | Gibt an, ob statische Felder aus dem Dokument entfernt werden sollen. Statische Felder sind Felder, deren Ergebnisse bei jeder Dokumentänderung gleich bleiben. Felder, deren Ergebnisse nicht in einem document gespeichert werden und im laufenden Betrieb berechnet werden (z. BFieldListNum , FieldSymbol usw.) gelten nicht als statisch. |
| RemoveEmptyTableRows | `20` | Gibt an, ob leere Zeilen, die Seriendruckbereiche enthalten, aus dem Dokument entfernt werden sollen. |

## Beispiele

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

* namensraum [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../)
