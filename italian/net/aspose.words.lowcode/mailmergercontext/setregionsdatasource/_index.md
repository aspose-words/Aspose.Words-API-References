---
title: MailMergerContext.SetRegionsDataSource
linktitle: SetRegionsDataSource
articleTitle: SetRegionsDataSource
second_title: Aspose.Words per .NET
description: Migliora l'efficienza della tua operazione di stampa unione con il metodo MailMergerContext SetRegionsDataSource per impostare senza problemi l'origine dati per le regioni.
type: docs
weight: 30
url: /it/net/aspose.words.lowcode/mailmergercontext/setregionsdatasource/
---
## SetRegionsDataSource(*DataTable*) {#setregionsdatasource_1}

Imposta l'origine dati utilizzata per eseguire la stampa unione con le regioni.

```csharp
public void SetRegionsDataSource(DataTable dataTable)
```

## Osservazioni

Se vengono specificate sia l'origine dati per la stampa unione semplice sia l'origine dati per la stampa unione con regioni, verrà eseguita prima la stampa unione con regioni e poi verrà eseguita la stampa unione semplice.

## Esempi

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

### Guarda anche

* class [MailMergerContext](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)

---

## SetRegionsDataSource(*DataSet*) {#setregionsdatasource}

Imposta l'origine dati utilizzata per eseguire la stampa unione con le regioni.

```csharp
public void SetRegionsDataSource(DataSet dataSet)
```

## Osservazioni

Se vengono specificate sia l'origine dati per la stampa unione semplice sia l'origine dati per la stampa unione con regioni, verrà eseguita prima la stampa unione con regioni e poi verrà eseguita la stampa unione semplice.

## Esempi

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

* class [MailMergerContext](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)
