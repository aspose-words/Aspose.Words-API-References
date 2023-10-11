---
title: MailMerge.GetFieldNames
second_title: Aspose.Words لمراجع .NET API
description: MailMerge طريقة. إرجاع مجموعة من أسماء حقول دمج المراسلات المتوفرة في المستند.
type: docs
weight: 220
url: /ar/net/aspose.words.mailmerging/mailmerge/getfieldnames/
---
## MailMerge.GetFieldNames method

إرجاع مجموعة من أسماء حقول دمج المراسلات المتوفرة في المستند.

```csharp
public string[] GetFieldNames()
```

### ملاحظات

إرجاع أسماء حقول الدمج الكاملة بما في ذلك البادئة الاختيارية. لا يزيل أسماء الحقول المكررة.

يتم إنشاء مصفوفة سلسلة جديدة في كل مكالمة.

يتضمن أسماء الحقول "شارب" إذا[`UseNonMergeFields`](../usenonmergefields/) يكون`حقيقي`.

### أمثلة

يوضح كيفية الحصول على أسماء جميع حقول الدمج في المستند.

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
 // بنفس الاسم، ثم قم بتنفيذ عملية دمج المراسلات.
string[] fieldNames = doc.MailMerge.GetFieldNames();

Assert.AreEqual(3, fieldNames.Length);

foreach (string fieldName in fieldNames)
    Assert.True(dataTable.Columns.Contains(fieldName));

doc.MailMerge.Execute(dataTable);
```

### أنظر أيضا

* class [MailMerge](../)
* مساحة الاسم [Aspose.Words.MailMerging](../../mailmerge/)
* المجسم [Aspose.Words](../../../)


