---
title: MailMergerContext Class
linktitle: MailMergerContext
articleTitle: MailMergerContext
second_title: Aspose.Words pour .NET
description: Découvrez la puissante classe Aspose.Words.LowCode.MailMergerContext pour une fusion de courrier transparente, améliorant l'automatisation de vos documents avec facilité et efficacité.
type: docs
weight: 4280
url: /fr/net/aspose.words.lowcode/mailmergercontext/
---
## MailMergerContext class

Contexte de publipostage.

```csharp
public class MailMergerContext : ProcessorContext
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [MailMergerContext](mailmergercontext/)() | Default_Constructor |

## Propriétés

| Nom | La description |
| --- | --- |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | Paramètres de police utilisés par le processeur. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | Options de mise en page du document utilisées par le processeur. |
| [MailMergeOptions](../../aspose.words.lowcode/mailmergercontext/mailmergeoptions/) { get; } | Options de publipostage. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | Rappel d'avertissement utilisé par le processeur. |

## Méthodes

| Nom | La description |
| --- | --- |
| [SetRegionsDataSource](../../aspose.words.lowcode/mailmergercontext/setregionsdatasource/#setregionsdatasource)(*DataSet*) | Définit la source de données utilisée pour exécuter le publipostage avec les régions. |
| [SetRegionsDataSource](../../aspose.words.lowcode/mailmergercontext/setregionsdatasource/#setregionsdatasource_1)(*DataTable*) | Définit la source de données utilisée pour exécuter le publipostage avec les régions. |
| [SetSimpleDataSource](../../aspose.words.lowcode/mailmergercontext/setsimpledatasource/#setsimpledatasource)(*DataRow*) | Définit la source de données utilisée pour exécuter un simple publipostage. |
| [SetSimpleDataSource](../../aspose.words.lowcode/mailmergercontext/setsimpledatasource/#setsimpledatasource_1)(*DataTable*) | Définit la source de données utilisée pour exécuter un simple publipostage. |
| [SetSimpleDataSource](../../aspose.words.lowcode/mailmergercontext/setsimpledatasource/#setsimpledatasource_2)(*string[], object[]*) | Définit la source de données utilisée pour exécuter un simple publipostage. |

## Exemples

Montre comment effectuer une opération de publipostage pour un seul enregistrement à l'aide du contexte.

```csharp
// Il existe plusieurs façons d'effectuer une opération de publipostage :
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

Montre comment effectuer une opération de publipostage à partir d'un DataRow à l'aide du contexte.

```csharp
// Il existe plusieurs façons d'effectuer une opération de publipostage à partir d'un DataRow :
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

Montre comment effectuer une opération de publipostage à partir d'un DataTable à l'aide du contexte.

```csharp
// Il existe plusieurs façons d'effectuer une opération de publipostage à partir d'une table de données :
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

Montre comment effectuer une opération de fusion et de publipostage avec des régions à partir d'un DataTable en utilisant le contexte.

```csharp
// Il existe plusieurs façons d'effectuer une opération de fusion et de publipostage avec des régions à partir d'une DataTable :
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

Montre comment effectuer une opération de publipostage pour un seul enregistrement du flux à l'aide du contexte.

```csharp
// Il existe plusieurs façons d'effectuer une opération de publipostage à l'aide de documents du flux :
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

Montre comment effectuer une opération de publipostage à partir d'un DataRow en utilisant des documents du flux à l'aide du contexte.

```csharp
// Il existe plusieurs façons d'effectuer une opération de publipostage à partir d'un DataRow en utilisant des documents du flux :
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

Montre comment effectuer une opération de publipostage à partir d'un DataTable à l'aide de documents du flux à l'aide du contexte.

```csharp
// Il existe plusieurs façons d'effectuer une opération de publipostage à partir d'un DataTable en utilisant des documents du flux :
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

Montre comment effectuer une opération de fusion et de publipostage avec des régions à partir d'un DataTable en utilisant des documents du flux en utilisant le contexte.

```csharp
// Il existe plusieurs façons d'effectuer une opération de fusion et de publipostage avec des régions à partir d'une DataTable en utilisant des documents du flux :
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

Montre comment effectuer une opération de fusion et de publipostage avec des régions à partir d'un DataSet à l'aide du contexte.

```csharp
// Il existe plusieurs façons d'effectuer une opération de fusion et de publipostage avec des régions à partir d'un DataSet :
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

Montre comment effectuer une opération de fusion et de publipostage avec des régions à partir d'un ensemble de données à l'aide de documents du flux à l'aide du contexte.

```csharp
// Il existe plusieurs façons d'effectuer une opération de fusion et de publipostage avec des régions à partir d'un DataSet en utilisant des documents du flux :
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

### Voir également

* class [ProcessorContext](../processorcontext/)
* espace de noms [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../)
