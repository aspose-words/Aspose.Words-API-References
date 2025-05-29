---
title: MailMergerContext.SetRegionsDataSource
linktitle: SetRegionsDataSource
articleTitle: SetRegionsDataSource
second_title: Aspose.Words för .NET
description: Förbättra effektiviteten i din dokumentkoppling med metoden MailMergerContext SetRegionsDataSource för att sömlöst ställa in din datakälla för regioner.
type: docs
weight: 30
url: /sv/net/aspose.words.lowcode/mailmergercontext/setregionsdatasource/
---
## SetRegionsDataSource(*DataTable*) {#setregionsdatasource_1}

Anger datakällan som används för att köra dokumentkoppling med regioner.

```csharp
public void SetRegionsDataSource(DataTable dataTable)
```

## Anmärkningar

Om både datakällan för enkel dokumentkoppling och datakällan för dokumentkoppling med regioner anges, körs först dokumentkoppling med regioner och sedan körs enkel dokumentkoppling.

## Exempel

Visar hur man utför dokumentkoppling med regioner från en datatabell med hjälp av kontext.

```csharp
// Det finns flera sätt att göra dokumentkoppling med regioner från en datatabell:
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

Visar hur man utför dokumentkoppling med regioner från en datatabell med hjälp av dokument från strömmen med hjälp av kontext.

```csharp
// Det finns flera sätt att göra dokumentkoppling med regioner från en datatabell med hjälp av dokument från strömmen:
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

### Se även

* class [MailMergerContext](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## SetRegionsDataSource(*DataSet*) {#setregionsdatasource}

Anger datakällan som används för att köra dokumentkoppling med regioner.

```csharp
public void SetRegionsDataSource(DataSet dataSet)
```

## Anmärkningar

Om både datakällan för enkel dokumentkoppling och datakällan för dokumentkoppling med regioner anges, körs först dokumentkoppling med regioner och sedan körs enkel dokumentkoppling.

## Exempel

Visar hur man gör en dokumentkoppling med regioner från en datauppsättning med hjälp av kontext.

```csharp
// Det finns flera sätt att göra dokumentkoppling med regioner från en datauppsättning:
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

Visar hur man gör en dokumentkoppling med regioner från en datauppsättning med hjälp av dokument från strömmen med hjälp av kontext.

```csharp
// Det finns flera sätt att göra dokumentkoppling med regioner från en datauppsättning med hjälp av dokument från dataströmmen:
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

### Se även

* class [MailMergerContext](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)
