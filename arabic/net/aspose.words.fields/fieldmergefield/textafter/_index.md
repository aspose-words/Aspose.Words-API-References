---
title: FieldMergeField.TextAfter
second_title: Aspose.Words لمراجع .NET API
description: FieldMergeField ملكية. الحصول على أو تعيين النص المراد إدراجه بعد الحقل إذا لم يكن الحقل فارغًا.
type: docs
weight: 50
url: /ar/net/aspose.words.fields/fieldmergefield/textafter/
---
## FieldMergeField.TextAfter property

الحصول على أو تعيين النص المراد إدراجه بعد الحقل إذا لم يكن الحقل فارغًا.

```csharp
public string TextAfter { get; set; }
```

### أمثلة

يوضح كيفية استخدام حقول MERGEFIELD لإجراء دمج المراسلات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إنشاء جدول بيانات لاستخدامه كمصدر بيانات لدمج المراسلات.
DataTable table = new DataTable("Employees");
table.Columns.Add("Courtesy Title");
table.Columns.Add("First Name");
table.Columns.Add("Last Name");
table.Rows.Add("Mr.", "John", "Doe");
table.Rows.Add("Mrs.", "Jane", "Cardholder");

// أدخل MERGEFIELD مع تعيين خاصية FieldName إلى اسم عمود في مصدر البيانات.
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
* مساحة الاسم [Aspose.Words.Fields](../../fieldmergefield/)
* المجسم [Aspose.Words](../../../)


