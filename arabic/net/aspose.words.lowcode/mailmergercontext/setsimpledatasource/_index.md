---
title: MailMergerContext.SetSimpleDataSource
linktitle: SetSimpleDataSource
articleTitle: SetSimpleDataSource
second_title: Aspose.Words لـ .NET
description: قم بتعزيز كفاءة دمج البريد الخاص بك باستخدام طريقة MailMergerContext SetSimpleDataSource، مما يعمل على تبسيط إعداد مصدر البيانات لضمان التنفيذ السلس.
type: docs
weight: 40
url: /ar/net/aspose.words.lowcode/mailmergercontext/setsimpledatasource/
---
## SetSimpleDataSource(*string[], object[]*) {#setsimpledatasource_2}

يحدد مصدر البيانات المستخدم لتنفيذ دمج البريد البسيط.

```csharp
public void SetSimpleDataSource(string[] fieldNames, object[] fieldValues)
```

## ملاحظات

إذا تم تحديد كل من مصدر بيانات دمج البريد البسيط ومصدر البيانات لدمج البريد مع المناطق، فسيتم تنفيذ دمج البريد مع المناطق أولاً ثم يتم تنفيذ دمج البريد البسيط.

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

### أنظر أيضا

* class [MailMergerContext](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## SetSimpleDataSource(*DataRow*) {#setsimpledatasource}

يحدد مصدر البيانات المستخدم لتنفيذ دمج البريد البسيط.

```csharp
public void SetSimpleDataSource(DataRow dataRow)
```

## ملاحظات

إذا تم تحديد كل من مصدر بيانات دمج البريد البسيط ومصدر البيانات لدمج البريد مع المناطق، فسيتم تنفيذ دمج البريد مع المناطق أولاً ثم يتم تنفيذ دمج البريد البسيط.

## أمثلة

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

### أنظر أيضا

* class [MailMergerContext](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)

---

## SetSimpleDataSource(*DataTable*) {#setsimpledatasource_1}

يحدد مصدر البيانات المستخدم لتنفيذ دمج البريد البسيط.

```csharp
public void SetSimpleDataSource(DataTable dataTable)
```

## ملاحظات

إذا تم تحديد كل من مصدر بيانات دمج البريد البسيط ومصدر البيانات لدمج البريد مع المناطق، فسيتم تنفيذ دمج البريد مع المناطق أولاً ثم يتم تنفيذ دمج البريد البسيط.

## أمثلة

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

### أنظر أيضا

* class [MailMergerContext](../)
* مساحة الاسم [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../../)
