---
title: MailMergerContext.SetRegionsDataSource
linktitle: SetRegionsDataSource
articleTitle: SetRegionsDataSource
second_title: Aspose.Words لـ .NET
description: قم بتعزيز كفاءة دمج البريد الخاص بك باستخدام طريقة MailMergerContext SetRegionsDataSource لتعيين مصدر البيانات للمناطق بسلاسة.
type: docs
weight: 30
url: /ar/net/aspose.words.lowcode/mailmergercontext/setregionsdatasource/
---
## SetRegionsDataSource(*DataTable*) {#setregionsdatasource_1}

تعيين مصدر البيانات المستخدم لتنفيذ دمج البريد مع المناطق.

```csharp
public void SetRegionsDataSource(DataTable dataTable)
```

## ملاحظات

إذا تم تحديد كل من مصدر بيانات دمج البريد البسيط ومصدر البيانات لدمج البريد مع المناطق، فسيتم تنفيذ دمج البريد مع المناطق أولاً ثم يتم تنفيذ دمج البريد البسيط.

## أمثلة

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

### أنظر أيضا

* class [MailMergerContext](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## SetRegionsDataSource(*DataSet*) {#setregionsdatasource}

تعيين مصدر البيانات المستخدم لتنفيذ دمج البريد مع المناطق.

```csharp
public void SetRegionsDataSource(DataSet dataSet)
```

## ملاحظات

إذا تم تحديد كل من مصدر بيانات دمج البريد البسيط ومصدر البيانات لدمج البريد مع المناطق، فسيتم تنفيذ دمج البريد مع المناطق أولاً ثم يتم تنفيذ دمج البريد البسيط.

## أمثلة

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

* class [MailMergerContext](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)
