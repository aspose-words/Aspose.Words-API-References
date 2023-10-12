---
title: FieldChar.IsDirty
second_title: Aspose.Words لمراجع .NET API
description: FieldChar ملكية. الحصول على أو تعيين ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة قديمة بسبب تعديلات أخرى تم إجراؤها على المستند.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldchar/isdirty/
---
## FieldChar.IsDirty property

الحصول على أو تعيين ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب تعديلات أخرى تم إجراؤها على المستند.

```csharp
public bool IsDirty { get; set; }
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


