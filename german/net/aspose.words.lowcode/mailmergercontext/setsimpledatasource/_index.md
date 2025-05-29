---
title: MailMergerContext.SetSimpleDataSource
linktitle: SetSimpleDataSource
articleTitle: SetSimpleDataSource
second_title: Aspose.Words für .NET
description: Verbessern Sie die Effizienz Ihrer Serienbriefe mit der SetSimpleDataSource-Methode von MailMergerContext und optimieren Sie die Einrichtung der Datenquelle für eine nahtlose Ausführung.
type: docs
weight: 40
url: /de/net/aspose.words.lowcode/mailmergercontext/setsimpledatasource/
---
## SetSimpleDataSource(*string[], object[]*) {#setsimpledatasource_2}

Legt die Datenquelle fest, die zum Ausführen eines einfachen Serienbriefs verwendet wird.

```csharp
public void SetSimpleDataSource(string[] fieldNames, object[] fieldValues)
```

## Bemerkungen

Wenn sowohl die Datenquelle für den einfachen Serienbrief als auch die Datenquelle für den Serienbrief mit Regionen angegeben sind, wird zuerst der Serienbrief mit Regionen und dann der einfache Serienbrief ausgeführt.

## Beispiele

Zeigt, wie Sie mithilfe des Kontexts einen Serienbriefvorgang für einen einzelnen Datensatz durchführen.

```csharp
// Es gibt mehrere Möglichkeiten, Serienbriefe zu erstellen:
string doc = MyDir + "Mail merge.doc";

string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

MailMergerContext mailMergerContext = new MailMergerContext();
mailMergerContext.SetSimpleDataSource(fieldNames, fieldValues);
mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

MailMerger.Create(mailMergerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.MailMergeContext.docx")
    .Execute();
```

Zeigt, wie Sie mithilfe des Kontexts einen Serienbriefvorgang für einen einzelnen Datensatz aus dem Stream durchführen.

```csharp
// Es gibt mehrere Möglichkeiten, Serienbriefvorgänge mit Dokumenten aus dem Stream durchzuführen:
string[] fieldNames = new string[] { "FirstName", "Location", "SpecialCharsInName()" };
string[] fieldValues = new string[] { "James Bond", "London", "Classified" };

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    MailMergerContext mailMergerContext = new MailMergerContext();
    mailMergerContext.SetSimpleDataSource(fieldNames, fieldValues);
    mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeContextStream.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Create(mailMergerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### Siehe auch

* class [MailMergerContext](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## SetSimpleDataSource(*DataRow*) {#setsimpledatasource}

Legt die Datenquelle fest, die zum Ausführen eines einfachen Serienbriefs verwendet wird.

```csharp
public void SetSimpleDataSource(DataRow dataRow)
```

## Bemerkungen

Wenn sowohl die Datenquelle für den einfachen Serienbrief als auch die Datenquelle für den Serienbrief mit Regionen angegeben sind, wird zuerst der Serienbrief mit Regionen und dann der einfache Serienbrief ausgeführt.

## Beispiele

Zeigt, wie Sie mithilfe des Kontexts einen Serienbriefvorgang aus einer DataRow durchführen.

```csharp
// Es gibt mehrere Möglichkeiten, einen Serienbriefvorgang aus einer DataRow heraus durchzuführen:
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

MailMergerContext mailMergerContext = new MailMergerContext();
mailMergerContext.SetSimpleDataSource(dataRow);
mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

MailMerger.Create(mailMergerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.MailMergeContextDataRow.docx")
    .Execute();
```

Zeigt, wie Sie einen Serienbriefvorgang aus einer DataRow mithilfe von Dokumenten aus dem Stream unter Verwendung des Kontexts durchführen.

```csharp
// Es gibt mehrere Möglichkeiten, einen Serienbriefvorgang aus einer DataRow unter Verwendung von Dokumenten aus dem Stream durchzuführen:
DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    MailMergerContext mailMergerContext = new MailMergerContext();
    mailMergerContext.SetSimpleDataSource(dataRow);
    mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeContextStreamDataRow.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Create(mailMergerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### Siehe auch

* class [MailMergerContext](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## SetSimpleDataSource(*DataTable*) {#setsimpledatasource_1}

Legt die Datenquelle fest, die zum Ausführen eines einfachen Serienbriefs verwendet wird.

```csharp
public void SetSimpleDataSource(DataTable dataTable)
```

## Bemerkungen

Wenn sowohl die Datenquelle für den einfachen Serienbrief als auch die Datenquelle für den Serienbrief mit Regionen angegeben sind, wird zuerst der Serienbrief mit Regionen und dann der einfache Serienbrief ausgeführt.

## Beispiele

Zeigt, wie Sie mithilfe des Kontexts einen Seriendruckvorgang aus einer DataTable durchführen.

```csharp
// Es gibt mehrere Möglichkeiten, Serienbriefvorgänge aus einer DataTable heraus durchzuführen:
string doc = MyDir + "Mail merge.doc";

DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

MailMergerContext mailMergerContext = new MailMergerContext();
mailMergerContext.SetSimpleDataSource(dataTable);
mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

MailMerger.Create(mailMergerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.MailMergeContextDataTable.docx")
    .Execute();
```

Zeigt, wie Sie einen Serienbriefvorgang aus einer DataTable mithilfe von Dokumenten aus dem Stream unter Verwendung des Kontexts durchführen.

```csharp
// Es gibt mehrere Möglichkeiten, Serienbriefvorgänge aus einer DataTable mithilfe von Dokumenten aus dem Stream durchzuführen:
DataTable dataTable = new DataTable();
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("Location");
dataTable.Columns.Add("SpecialCharsInName()");

DataRow dataRow = dataTable.Rows.Add(new string[] { "James Bond", "London", "Classified" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    MailMergerContext mailMergerContext = new MailMergerContext();
    mailMergerContext.SetSimpleDataSource(dataTable);
    mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeContextStreamDataTable.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Create(mailMergerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### Siehe auch

* class [MailMergerContext](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)
