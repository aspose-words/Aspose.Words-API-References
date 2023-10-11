---
title: FieldChar.IsLocked
second_title: Aspose.Words لمراجع .NET API
description: FieldChar ملكية. الحصول على أو تعيين ما إذا كان الحقل الأصلي مقفلاً لا ينبغي إعادة حساب النتيجة.
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fieldchar/islocked/
---
## FieldChar.IsLocked property

الحصول على أو تعيين ما إذا كان الحقل الأصلي مقفلاً (لا ينبغي إعادة حساب النتيجة).

```csharp
public bool IsLocked { get; set; }
```

### أمثلة

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

// استرداد كائن الواجهة الذي يمثل الحقل الموجود في المستند.
field = (FieldDate)fieldStart.GetField();

Assert.AreEqual(false, field.IsLocked);
Assert.AreEqual(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// قم بتحديث الحقل لإظهار التاريخ الحالي.
field.Update();
```

### أنظر أيضا

* class [FieldChar](../)
* مساحة الاسم [Aspose.Words.Fields](../../fieldchar/)
* المجسم [Aspose.Words](../../../)


