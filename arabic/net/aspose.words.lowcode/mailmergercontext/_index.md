---
title: MailMergerContext Class
linktitle: MailMergerContext
articleTitle: MailMergerContext
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.LowCode.MailMergerContext القوية لدمج البريد بسلاسة، وتعزيز أتمتة المستندات الخاصة بك بسهولة وكفاءة.
type: docs
weight: 4280
url: /ar/net/aspose.words.lowcode/mailmergercontext/
---
## MailMergerContext class

سياق دمج البريد.

```csharp
public class MailMergerContext : ProcessorContext
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [MailMergerContext](mailmergercontext/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [FontSettings](../../aspose.words.lowcode/processorcontext/fontsettings/) { get; set; } | إعدادات الخط المستخدمة بواسطة المعالج. |
| [LayoutOptions](../../aspose.words.lowcode/processorcontext/layoutoptions/) { get; } | خيارات تخطيط المستند التي يستخدمها المعالج. |
| [MailMergeOptions](../../aspose.words.lowcode/mailmergercontext/mailmergeoptions/) { get; } | خيارات دمج البريد. |
| [WarningCallback](../../aspose.words.lowcode/processorcontext/warningcallback/) { get; set; } | استدعاء تحذيري يستخدمه المعالج. |

## طُرق

| اسم | وصف |
| --- | --- |
| [SetRegionsDataSource](../../aspose.words.lowcode/mailmergercontext/setregionsdatasource/#setregionsdatasource)(*DataSet*) | تعيين مصدر البيانات المستخدم لتنفيذ دمج البريد مع المناطق. |
| [SetRegionsDataSource](../../aspose.words.lowcode/mailmergercontext/setregionsdatasource/#setregionsdatasource_1)(*DataTable*) | تعيين مصدر البيانات المستخدم لتنفيذ دمج البريد مع المناطق. |
| [SetSimpleDataSource](../../aspose.words.lowcode/mailmergercontext/setsimpledatasource/#setsimpledatasource)(*DataRow*) | يحدد مصدر البيانات المستخدم لتنفيذ دمج البريد البسيط. |
| [SetSimpleDataSource](../../aspose.words.lowcode/mailmergercontext/setsimpledatasource/#setsimpledatasource_1)(*DataTable*) | يحدد مصدر البيانات المستخدم لتنفيذ دمج البريد البسيط. |
| [SetSimpleDataSource](../../aspose.words.lowcode/mailmergercontext/setsimpledatasource/#setsimpledatasource_2)(*string[], object[]*) | يحدد مصدر البيانات المستخدم لتنفيذ دمج البريد البسيط. |

## أمثلة

يوضح كيفية إجراء عملية دمج البريد لسجل واحد باستخدام السياق.

```csharp
// هناك عدة طرق لإجراء عملية دمج البريد:
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

يوضح كيفية إجراء عملية دمج البريد من DataRow باستخدام السياق.

```csharp
// هناك عدة طرق لإجراء عملية دمج البريد من DataRow:
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

يوضح كيفية إجراء عملية دمج البريد من جدول بيانات باستخدام السياق.

```csharp
// هناك عدة طرق لإجراء عملية دمج البريد من جدول البيانات:
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

يوضح كيفية القيام بعملية دمج البريد مع المناطق من جدول بيانات باستخدام السياق.

```csharp
// هناك عدة طرق لإجراء عملية دمج البريد مع المناطق من جدول البيانات:
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

يوضح كيفية إجراء عملية دمج البريد لسجل واحد من التدفق باستخدام السياق.

```csharp
// هناك عدة طرق لإجراء عملية دمج البريد باستخدام المستندات من التدفق:
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

يوضح كيفية إجراء عملية دمج البريد من DataRow باستخدام المستندات من التدفق باستخدام السياق.

```csharp
// هناك عدة طرق لإجراء عملية دمج البريد من DataRow باستخدام المستندات من التدفق:
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

يوضح كيفية إجراء عملية دمج البريد من جدول بيانات باستخدام المستندات من التدفق باستخدام السياق.

```csharp
// هناك عدة طرق لإجراء عملية دمج البريد من جدول بيانات باستخدام المستندات من التدفق:
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

يوضح كيفية القيام بعملية دمج البريد مع المناطق من جدول بيانات باستخدام المستندات من التدفق باستخدام السياق.

```csharp
// هناك عدة طرق لإجراء عملية دمج البريد مع المناطق من جدول بيانات باستخدام المستندات من التدفق:
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

يوضح كيفية القيام بعملية دمج البريد باستخدام المناطق من مجموعة بيانات باستخدام السياق.

```csharp
// هناك عدة طرق لإجراء عملية دمج البريد مع المناطق من مجموعة البيانات:
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

يوضح كيفية القيام بعملية دمج البريد مع المناطق من مجموعة بيانات باستخدام المستندات من التدفق باستخدام السياق.

```csharp
// هناك عدة طرق لإجراء عملية دمج البريد مع المناطق من مجموعة بيانات باستخدام المستندات من التدفق:
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

### أنظر أيضا

* class [ProcessorContext](../processorcontext/)
* مساحة الاسم [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../)
