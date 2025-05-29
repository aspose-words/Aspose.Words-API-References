---
title: MailMergerContext Class
linktitle: MailMergerContext
articleTitle: MailMergerContext
second_title: Aspose.Words per .NET
description: Scopri la potente classe Aspose.Words.LowCode.MailMergerContext per unire la posta in modo fluido, migliorando l'automazione dei tuoi documenti con facilità ed efficienza.
type: docs
weight: 4280
url: /it/net/aspose.words.lowcode/mailmergercontext/
---
## MailMergerContext class

Contesto di unione di posta.

```csharp
public class MailMergerContext : ProcessorContext
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [MailMergerContext](mailmergercontext/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | Impostazioni del font utilizzate dal processore. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | Opzioni di layout del documento utilizzate dal processore. |
| [MailMergeOptions](../../aspose.words.lowcode/mailmergercontext/mailmergeoptions/) { get; } | Opzioni di unione posta. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | Callback di avviso utilizzato dal processore. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [SetRegionsDataSource](../../aspose.words.lowcode/mailmergercontext/setregionsdatasource/#setregionsdatasource)(*DataSet*) | Imposta l'origine dati utilizzata per eseguire la stampa unione con le regioni. |
| [SetRegionsDataSource](../../aspose.words.lowcode/mailmergercontext/setregionsdatasource/#setregionsdatasource_1)(*DataTable*) | Imposta l'origine dati utilizzata per eseguire la stampa unione con le regioni. |
| [SetSimpleDataSource](../../aspose.words.lowcode/mailmergercontext/setsimpledatasource/#setsimpledatasource)(*DataRow*) | Imposta l'origine dati utilizzata per eseguire una semplice unione di posta. |
| [SetSimpleDataSource](../../aspose.words.lowcode/mailmergercontext/setsimpledatasource/#setsimpledatasource_1)(*DataTable*) | Imposta l'origine dati utilizzata per eseguire una semplice unione di posta. |
| [SetSimpleDataSource](../../aspose.words.lowcode/mailmergercontext/setsimpledatasource/#setsimpledatasource_2)(*string[], object[]*) | Imposta l'origine dati utilizzata per eseguire una semplice unione di posta. |

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

Mostra come eseguire un'operazione di stampa unione con regioni da una DataTable utilizzando il contesto.

```csharp
// Esistono diversi modi per eseguire un'operazione di stampa unione con regioni da una DataTable:
string doc = MyDir + "Mail merge with regions.docx";

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "", "" });
dataTable.Rows.Add(new object[] { "Jane", "Doe" });

MailMergerContext mailMergerContext = new MailMergerContext();
mailMergerContext.SetRegionsDataSource(dataTable);
mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

MailMerger.Create(mailMergerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.MailMergeContextWithRegionsDataTable.docx")
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

Mostra come eseguire un'operazione di unione di posta con regioni da una DataTable utilizzando documenti dal flusso mediante il contesto.

```csharp
// Esistono diversi modi per eseguire un'operazione di unione di posta con regioni da una DataTable utilizzando i documenti dal flusso:
DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "", "" });
dataTable.Rows.Add(new object[] { "Jane", "Doe" });

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    MailMergerContext mailMergerContext = new MailMergerContext();
    mailMergerContext.SetRegionsDataSource(dataTable);
    mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeContextStreamWithRegionsDataTable.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Create(mailMergerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

Mostra come eseguire un'operazione di stampa unione con regioni da un DataSet utilizzando il contesto.

```csharp
// Esistono diversi modi per eseguire un'operazione di unione di posta con regioni da un DataSet:
string doc = MyDir + "Mail merge with regions data set.docx";

DataTable tableCustomers = new DataTable("Customers");
tableCustomers.Columns.Add("CustomerID");
tableCustomers.Columns.Add("CustomerName");
tableCustomers.Rows.Add(new object[] { 1, "John Doe" });
tableCustomers.Rows.Add(new object[] { 2, "Jane Doe" });

DataTable tableOrders = new DataTable("Orders");
tableOrders.Columns.Add("CustomerID");
tableOrders.Columns.Add("ItemName");
tableOrders.Columns.Add("Quantity");
tableOrders.Rows.Add(new object[] { 1, "Hawaiian", 2 });
tableOrders.Rows.Add(new object[] { 2, "Pepperoni", 1 });
tableOrders.Rows.Add(new object[] { 2, "Chicago", 1 });

DataSet dataSet = new DataSet();
dataSet.Tables.Add(tableCustomers);
dataSet.Tables.Add(tableOrders);
dataSet.Relations.Add(tableCustomers.Columns["CustomerID"], tableOrders.Columns["CustomerID"]);

MailMergerContext mailMergerContext = new MailMergerContext();
mailMergerContext.SetRegionsDataSource(dataSet);
mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

MailMerger.Create(mailMergerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.MailMergeContextWithRegionsDataTable.docx")
    .Execute();
```

Mostra come eseguire un'operazione di unione di posta con regioni da un DataSet utilizzando documenti dal flusso mediante il contesto.

```csharp
// Esistono diversi modi per eseguire un'operazione di unione di posta con regioni da un DataSet utilizzando i documenti dal flusso:
DataTable tableCustomers = new DataTable("Customers");
tableCustomers.Columns.Add("CustomerID");
tableCustomers.Columns.Add("CustomerName");
tableCustomers.Rows.Add(new object[] { 1, "John Doe" });
tableCustomers.Rows.Add(new object[] { 2, "Jane Doe" });

DataTable tableOrders = new DataTable("Orders");
tableOrders.Columns.Add("CustomerID");
tableOrders.Columns.Add("ItemName");
tableOrders.Columns.Add("Quantity");
tableOrders.Rows.Add(new object[] { 1, "Hawaiian", 2 });
tableOrders.Rows.Add(new object[] { 2, "Pepperoni", 1 });
tableOrders.Rows.Add(new object[] { 2, "Chicago", 1 });

DataSet dataSet = new DataSet();
dataSet.Tables.Add(tableCustomers);
dataSet.Tables.Add(tableOrders);
dataSet.Relations.Add(tableCustomers.Columns["CustomerID"], tableOrders.Columns["CustomerID"]);

using (FileStream streamIn = new FileStream(MyDir + "Mail merge.doc", FileMode.Open, FileAccess.Read))
{
    MailMergerContext mailMergerContext = new MailMergerContext();
    mailMergerContext.SetRegionsDataSource(dataSet);
    mailMergerContext.MailMergeOptions.TrimWhitespaces = true;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.MailMergeContextStreamWithRegionsDataSet.docx", FileMode.Create, FileAccess.ReadWrite))
        MailMerger.Create(mailMergerContext)
        .From(streamIn)
        .To(streamOut, SaveFormat.Docx)
        .Execute();
}
```

### Guarda anche

* class [ProcessorContext](../processorcontext/)
* spazio dei nomi [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../)
