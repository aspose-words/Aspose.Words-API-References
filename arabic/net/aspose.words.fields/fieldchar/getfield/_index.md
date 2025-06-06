---
title: FieldChar.GetField
linktitle: GetField
articleTitle: GetField
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة GetField في FieldChar، واسترد الحقول بسهولة لإدارة البيانات بشكل مثالي وتحسين الأداء في تطبيقاتك.
type: docs
weight: 40
url: /ar/net/aspose.words.fields/fieldchar/getfield/
---
## FieldChar.GetField method

يعيد حقلًا لحقل char.

```csharp
public Field GetField()
```

### قيمة الإرجاع

حقل لحقل الحرف.

## ملاحظات

جديد[`Field`](../../field/) يتم إنشاء الكائن في كل مرة يتم فيها استدعاء الطريقة.

## أمثلة

يوضح كيفية العمل مع عقدة FieldStart.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldDate field = (FieldDate)builder.InsertField(FieldType.FieldDate, true);
field.Format.DateTimeFormat = "dddd, MMMM dd, yyyy";
field.Update();

FieldChar fieldStart = field.Start;

Assert.AreEqual(FieldType.FieldDate, fieldStart.FieldType);
Assert.AreEqual(false, fieldStart.IsDirty);
Assert.AreEqual(false, fieldStart.IsLocked);

// استرداد كائن الواجهة الذي يمثل الحقل في المستند.
field = (FieldDate)fieldStart.GetField();

Assert.AreEqual(false, field.IsLocked);
Assert.AreEqual(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

//تحديث الحقل لإظهار التاريخ الحالي.
field.Update();
```

### أنظر أيضا

* class [Field](../../field/)
* class [FieldChar](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
