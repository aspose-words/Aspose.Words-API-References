---
title: MailMergerContext Class
linktitle: MailMergerContext
articleTitle: MailMergerContext
second_title: .NET için Aspose.Words
description: Sorunsuz e-posta birleştirme için güçlü Aspose.Words.LowCode.MailMergerContext sınıfını keşfedin, belge otomasyonunuzu kolaylıkla ve verimli bir şekilde geliştirin.
type: docs
weight: 4280
url: /tr/net/aspose.words.lowcode/mailmergercontext/
---
## MailMergerContext class

Posta birleştirme bağlamı.

```csharp
public class MailMergerContext : ProcessorContext
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [MailMergerContext](mailmergercontext/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | İşlemci tarafından kullanılan yazı tipi ayarları. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | İşlemci tarafından kullanılan belge düzeni seçenekleri. |
| [MailMergeOptions](../../aspose.words.lowcode/mailmergercontext/mailmergeoptions/) { get; } | Posta birleştirme seçenekleri. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | İşlemci tarafından kullanılan uyarı geri araması. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [SetRegionsDataSource](../../aspose.words.lowcode/mailmergercontext/setregionsdatasource/#setregionsdatasource)(*DataSet*) | Bölgelerle posta birleştirmeyi yürütmek için kullanılan veri kaynağını ayarlar. |
| [SetRegionsDataSource](../../aspose.words.lowcode/mailmergercontext/setregionsdatasource/#setregionsdatasource_1)(*DataTable*) | Bölgelerle posta birleştirmeyi yürütmek için kullanılan veri kaynağını ayarlar. |
| [SetSimpleDataSource](../../aspose.words.lowcode/mailmergercontext/setsimpledatasource/#setsimpledatasource)(*DataRow*) | Basit posta birleştirmeyi yürütmek için kullanılan veri kaynağını ayarlar. |
| [SetSimpleDataSource](../../aspose.words.lowcode/mailmergercontext/setsimpledatasource/#setsimpledatasource_1)(*DataTable*) | Basit posta birleştirmeyi yürütmek için kullanılan veri kaynağını ayarlar. |
| [SetSimpleDataSource](../../aspose.words.lowcode/mailmergercontext/setsimpledatasource/#setsimpledatasource_2)(*string[], object[]*) | Basit posta birleştirmeyi yürütmek için kullanılan veri kaynağını ayarlar. |

## Örnekler

Bağlam kullanılarak tek bir kayıt için posta birleştirme işleminin nasıl yapılacağını gösterir.

```csharp
// Posta birleştirme işlemini yapmanın birkaç yolu vardır:
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

Bağlam kullanılarak DataRow'dan posta birleştirme işleminin nasıl yapılacağını gösterir.

```csharp
// DataRow'dan posta birleştirme işlemini yapmanın birkaç yolu vardır:
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

Bir DataTable'dan bağlam kullanarak posta birleştirme işleminin nasıl yapılacağını gösterir.

```csharp
// DataTable'dan posta birleştirme işlemini yapmanın birkaç yolu vardır:
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

Bir DataTable'dan bağlam kullanarak bölgelerle posta birleştirme işleminin nasıl yapılacağını gösterir.

```csharp
// DataTable'dan bölgelerle posta birleştirme işlemini yapmanın birkaç yolu vardır:
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

Akıştaki tek bir kayıt için bağlam kullanılarak posta birleştirme işleminin nasıl yapılacağını gösterir.

```csharp
// Akıştaki belgeleri kullanarak posta birleştirme işlemini yapmanın birkaç yolu vardır:
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

Bağlam kullanılarak akıştaki belgeler kullanılarak bir DataRow'dan posta birleştirme işleminin nasıl yapılacağını gösterir.

```csharp
// Akıştaki belgeleri kullanarak bir DataRow'dan posta birleştirme işlemi yapmanın birkaç yolu vardır:
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

Akıştaki belgeleri kullanarak bir DataTable'dan posta birleştirme işleminin nasıl yapılacağını gösterir.

```csharp
// Akıştaki belgeleri kullanarak bir DataTable'dan posta birleştirme işlemi yapmanın birkaç yolu vardır:
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

Akıştaki belgeleri kullanarak bir DataTable'dan bölgelerle posta birleştirme işleminin nasıl yapılacağını gösterir.

```csharp
// Akıştaki belgeleri kullanarak bir DataTable'dan bölgelerle posta birleştirme işlemini yapmanın birkaç yolu vardır:
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

Bir DataSet'ten bağlam kullanarak bölgelerle posta birleştirme işleminin nasıl yapılacağını gösterir.

```csharp
// Bir DataSet'ten bölgelerle posta birleştirme işlemini yapmanın birkaç yolu vardır:
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

Akıştaki belgeleri kullanarak bir DataSet'ten bölgelerle posta birleştirme işleminin nasıl yapılacağını gösterir.

```csharp
// Akıştaki belgeleri kullanarak bir DataSet'ten bölgelerle posta birleştirme işlemini yapmanın birkaç yolu vardır:
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

### Ayrıca bakınız

* class [ProcessorContext](../processorcontext/)
* ad alanı [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../)
