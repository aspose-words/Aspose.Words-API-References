---
title: FieldMergeField.FieldNameNoPrefix
linktitle: FieldNameNoPrefix
articleTitle: FieldNameNoPrefix
second_title: Aspose.Words لـ .NET
description: FieldMergeField FieldNameNoPrefix ملكية. يقوم بإرجاع اسم حقل البيانات فقط. يتم تجريد أي بادئة من خاصية البادئة في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldmergefield/fieldnamenoprefix/
---
## FieldMergeField.FieldNameNoPrefix property

يقوم بإرجاع اسم حقل البيانات فقط. يتم تجريد أي بادئة من خاصية البادئة.

```csharp
public string FieldNameNoPrefix { get; }
```

## أمثلة

يوضح كيفية استخدام حقول MERGEFIELD لإجراء عملية دمج البريد.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء جدول بيانات لاستخدامه كمصدر بيانات لدمج المراسلات.
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// قم بإدراج MERGEFIELD مع تعيين خاصية FieldName على اسم عمود في مصدر البيانات.
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Courtesy Title";
fieldMergeField.IsMapped = true;
fieldMergeField.IsVerticalFormatting = false;

// يمكننا تطبيق النص قبل وبعد القيمة التي يقبلها هذا الحقل عند حدوث الدمج.
fieldMergeField.TextBefore = "Dear ";
fieldMergeField.TextAfter = " ";

Assert.AreEqual(" MERGEFIELD  \"Courtesy Title\" \\m \\b \"Dear \" \\f \" \"", fieldMergeField.GetFieldCode());

// أدخل MERGEFIELD آخر لعمود مختلف في مصدر البيانات.
fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Last Name";
fieldMergeField.TextAfter = ":";

doc.UpdateFields();
doc.MailMerge.Execute(table);

Assert.AreEqual("Dear Mr. Doe:\u000cDear Mrs. Cardholder:", doc.GetText().Trim());
```

### أنظر أيضا

* class [FieldMergeField](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
