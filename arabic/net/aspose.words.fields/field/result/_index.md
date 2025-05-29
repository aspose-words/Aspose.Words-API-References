---
title: Field.Result
linktitle: Result
articleTitle: Result
second_title: Aspose.Words لـ .NET
description: أدر خصائص نتائج الحقول بسهولة. تمكّن من الوصول إلى النصوص بين فواصل الحقول أو تعديلها لتسهيل معالجة البيانات وزيادة الكفاءة.
type: docs
weight: 70
url: /ar/net/aspose.words.fields/field/result/
---
## Field.Result property

يحصل على النص الموجود بين فاصل الحقل ونهاية الحقل أو يعينه.

```csharp
public string Result { get; set; }
```

## أمثلة

يوضح كيفية إدراج حقل في مستند باستخدام رمز الحقل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("DATE \\@ \"dddd, MMMM dd, yyyy\"");

Assert.AreEqual(FieldType.FieldDate, field.Type);
Assert.AreEqual("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// يؤدي هذا التحميل الزائد لطريقة InsertField إلى تحديث الحقول المدرجة تلقائيًا.
Assert.True((DateTime.Today - DateTime.Parse(field.Result)).Days <= 1);
```

### أنظر أيضا

* class [Field](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
