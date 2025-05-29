---
title: MailMergerContext.SetRegionsDataSource
linktitle: SetRegionsDataSource
articleTitle: SetRegionsDataSource
second_title: Aspose.Words für .NET
description: Verbessern Sie die Effizienz Ihres Serienbriefs mit der Methode „MailMergerContext SetRegionsDataSource“, um Ihre Datenquelle für Regionen nahtlos festzulegen.
type: docs
weight: 30
url: /de/net/aspose.words.lowcode/mailmergercontext/setregionsdatasource/
---
## SetRegionsDataSource(*DataTable*) {#setregionsdatasource_1}

Legt die Datenquelle fest, die zum Ausführen des Serienbriefs mit Regionen verwendet wird.

```csharp
public void SetRegionsDataSource(DataTable dataTable)
```

## Bemerkungen

Wenn sowohl die Datenquelle für den einfachen Serienbrief als auch die Datenquelle für den Serienbrief mit Regionen angegeben sind, wird zuerst der Serienbrief mit Regionen und dann der einfache Serienbrief ausgeführt.

## Beispiele

Zeigt, wie Sie mithilfe des Kontexts einen Serienbrief mit Regionen-Operation aus einer DataTable heraus durchführen.

```csharp
// Es gibt mehrere Möglichkeiten, Serienbriefe mit Regionen aus einer DataTable heraus zu erstellen:
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

Zeigt, wie Sie mithilfe von Dokumenten aus dem Stream und Kontext einen Serienbrief mit Regionen-Operation aus einer DataTable heraus durchführen.

```csharp
// Es gibt mehrere Möglichkeiten, Serienbriefe mit Regionen aus einer DataTable unter Verwendung von Dokumenten aus dem Stream auszuführen:
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

### Siehe auch

* class [MailMergerContext](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)

---

## SetRegionsDataSource(*DataSet*) {#setregionsdatasource}

Legt die Datenquelle fest, die zum Ausführen des Serienbriefs mit Regionen verwendet wird.

```csharp
public void SetRegionsDataSource(DataSet dataSet)
```

## Bemerkungen

Wenn sowohl die Datenquelle für den einfachen Serienbrief als auch die Datenquelle für den Serienbrief mit Regionen angegeben sind, wird zuerst der Serienbrief mit Regionen und dann der einfache Serienbrief ausgeführt.

## Beispiele

Zeigt, wie Sie mithilfe des Kontexts einen Serienbrief mit Regionen-Operation aus einem DataSet heraus durchführen.

```csharp
// Es gibt mehrere Möglichkeiten, Serienbriefe mit Regionen aus einem DataSet heraus durchzuführen:
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

Zeigt, wie Sie mithilfe von Dokumenten aus dem Stream und Kontext einen Serienbriefvorgang mit Regionen aus einem DataSet durchführen.

```csharp
// Es gibt mehrere Möglichkeiten, Serienbriefe mit Regionen aus einem DataSet unter Verwendung von Dokumenten aus dem Stream auszuführen:
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

### Siehe auch

* class [MailMergerContext](../)
* namensraum [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Montage [Aspose.Words](../../../)
