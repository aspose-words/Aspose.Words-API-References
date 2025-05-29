---
title: MailMergerContext.SetSimpleDataSource
linktitle: SetSimpleDataSource
articleTitle: SetSimpleDataSource
second_title: Aspose.Words per .NET
description: Migliora l'efficienza della tua operazione di unione dati con il metodo MailMergerContext SetSimpleDataSource, semplificando la configurazione dell'origine dati per un'esecuzione senza intoppi.
type: docs
weight: 40
url: /it/net/aspose.words.lowcode/mailmergercontext/setsimpledatasource/
---
## SetSimpleDataSource(*string[], object[]*) {#setsimpledatasource_2}

Imposta l'origine dati utilizzata per eseguire una semplice unione di posta.

```csharp
public void SetSimpleDataSource(string[] fieldNames, object[] fieldValues)
```

## Osservazioni

Se vengono specificate sia l'origine dati per la stampa unione semplice sia l'origine dati per la stampa unione con regioni, verrà eseguita prima la stampa unione con regioni e poi verrà eseguita la stampa unione semplice.

## Esempi

Mostra come eseguire un'operazione di stampa unione per un singolo record utilizzando il contesto.

```csharp
// Esistono diversi modi per eseguire un'operazione di unione di posta:
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

Mostra come eseguire un'operazione di stampa unione per un singolo record dal flusso utilizzando il contesto.

```csharp
// Esistono diversi modi per eseguire un'operazione di unione di posta utilizzando i documenti dal flusso:
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

### Guarda anche

* class [MailMergerContext](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## SetSimpleDataSource(*DataRow*) {#setsimpledatasource}

Imposta l'origine dati utilizzata per eseguire una semplice unione di posta.

```csharp
public void SetSimpleDataSource(DataRow dataRow)
```

## Osservazioni

Se vengono specificate sia l'origine dati per la stampa unione semplice sia l'origine dati per la stampa unione con regioni, verrà eseguita prima la stampa unione con regioni e poi verrà eseguita la stampa unione semplice.

## Esempi

Mostra come eseguire un'operazione di stampa unione da un DataRow utilizzando il contesto.

```csharp
// Esistono diversi modi per eseguire un'operazione di stampa unione da un DataRow:
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

Mostra come eseguire un'operazione di unione di posta da un DataRow utilizzando documenti dal flusso mediante il contesto.

```csharp
// Esistono diversi modi per eseguire un'operazione di unione di posta da un DataRow utilizzando i documenti dal flusso:
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

### Guarda anche

* class [MailMergerContext](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## SetSimpleDataSource(*DataTable*) {#setsimpledatasource_1}

Imposta l'origine dati utilizzata per eseguire una semplice unione di posta.

```csharp
public void SetSimpleDataSource(DataTable dataTable)
```

## Osservazioni

Se vengono specificate sia l'origine dati per la stampa unione semplice sia l'origine dati per la stampa unione con regioni, verrà eseguita prima la stampa unione con regioni e poi verrà eseguita la stampa unione semplice.

## Esempi

Mostra come eseguire un'operazione di stampa unione da una tabella dati utilizzando il contesto.

```csharp
// Esistono diversi modi per eseguire un'operazione di stampa unione da una tabella dati:
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

Mostra come eseguire un'operazione di stampa unione da una tabella dati utilizzando documenti dal flusso mediante il contesto.

```csharp
// Esistono diversi modi per eseguire un'operazione di unione di posta da una DataTable utilizzando i documenti dal flusso:
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

### Guarda anche

* class [MailMergerContext](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)
