---
title: FieldMergeField.IsMapped
linktitle: IsMapped
articleTitle: IsMapped
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldMergeField IsMapped لإدارة الحقول المرسومة بسهولة، مما يعزز تكامل البيانات وكفاءة سير العمل لديك.
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fieldmergefield/ismapped/
---
## FieldMergeField.IsMapped property

يحصل على أو يحدد ما إذا كان هذا الحقل حقلًا معينًا.

```csharp
public bool IsMapped { get; set; }
```

## أمثلة

يوضح كيفية استخدام حقول MERGEFIELD لإجراء دمج البريد.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بإنشاء جدول بيانات لاستخدامه كمصدر بيانات لدمج البريد.
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// إدراج MERGEFIELD مع تعيين خاصية FieldName إلى اسم عمود في مصدر البيانات.
FieldMergeField fieldMergeField = (FieldMergeField)builder.InsertField(FieldType.FieldMergeField, true);
fieldMergeField.FieldName = "Courtesy Title";
fieldMergeField.IsMapped = true;
fieldMergeField.IsVerticalFormatting = false;

//يمكننا تطبيق النص قبل وبعد القيمة التي يقبلها هذا الحقل عند حدوث الدمج.
fieldMergeField.TextBefore = "Dear ";
fieldMergeField.TextAfter = " ";

Assert.AreEqual(" MERGEFIELD  \"Courtesy Title\" \\m \\b \"Dear \" \\f \" \"", fieldMergeField.GetFieldCode());
Assert.AreEqual(FieldType.FieldMergeField, fieldMergeField.Type);

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
