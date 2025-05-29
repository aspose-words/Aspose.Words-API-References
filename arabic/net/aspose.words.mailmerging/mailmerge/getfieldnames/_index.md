---
title: MailMerge.GetFieldNames
linktitle: GetFieldNames
articleTitle: GetFieldNames
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة MailMerge GetFieldNames للوصول بسهولة إلى جميع أسماء حقول دمج البريد في مستندك واستخدامها لأتمتة المستندات بشكل مبسط.
type: docs
weight: 220
url: /ar/net/aspose.words.mailmerging/mailmerge/getfieldnames/
---
## MailMerge.GetFieldNames method

يقوم بإرجاع مجموعة من أسماء حقول دمج البريد المتوفرة في المستند.

```csharp
public string[] GetFieldNames()
```

## ملاحظات

يُرجع أسماء حقول الدمج كاملةً، بما في ذلك البادئة الاختيارية. لا يُلغي أسماء الحقول المكررة.

يتم إنشاء مجموعة سلسلة جديدة في كل مكالمة.

يتضمن أسماء حقول "الشارب" إذا[`UseNonMergeFields`](../usenonmergefields/) يكون`حقيقي`.

## أمثلة

يُظهر كيفية الحصول على أسماء جميع حقول الدمج في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD FirstName ");
builder.Write(" ");
builder.InsertField(" MERGEFIELD LastName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Columns.Add("City");
dataTable.Rows.Add(new object[] { "John", "Doe", "New York" });
dataTable.Rows.Add(new object[] { "Joe", "Bloggs", "Washington" });

// لكل اسم MERGEFIELD في المستند، تأكد من أن جدول البيانات يحتوي على عمود
 // بنفس الاسم، ثم قم بتنفيذ دمج البريد.
string[] fieldNames = doc.MailMerge.GetFieldNames();

Assert.AreEqual(3, fieldNames.Length);

foreach (string fieldName in fieldNames)
    Assert.True(dataTable.Columns.Contains(fieldName));

doc.MailMerge.Execute(dataTable);
```

### أنظر أيضا

* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* المجسم [Aspose.Words](../../../)
