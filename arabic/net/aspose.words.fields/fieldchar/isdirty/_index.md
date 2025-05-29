---
title: FieldChar.IsDirty
linktitle: IsDirty
articleTitle: IsDirty
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تساعد خاصية FieldChar IsDirty في الحفاظ على دقة المستند من خلال تتبع التغييرات، مما يضمن أن تعكس حقولك دائمًا أحدث التحديثات.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldchar/isdirty/
---
## FieldChar.IsDirty property

يحصل على أو يعين ما إذا كانت النتيجة الحالية للحقل لم تعد صحيحة (قديمة) بسبب التعديلات الأخرى التي تم إجراؤها على المستند.

```csharp
public bool IsDirty { get; set; }
```

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

* class [FieldChar](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
