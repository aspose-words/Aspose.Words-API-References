---
title: FieldChar.FieldType
linktitle: FieldType
articleTitle: FieldType
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldChar FieldType، التي تكشف عن نوع الحقل، مما يُحسّن كفاءة إدارة البيانات والبرمجة لديك. تعرّف على المزيد الآن!
type: docs
weight: 10
url: /ar/net/aspose.words.fields/fieldchar/fieldtype/
---
## FieldChar.FieldType property

يعيد نوع الحقل.

```csharp
public FieldType FieldType { get; }
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

* enum [FieldType](../../fieldtype/)
* class [FieldChar](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
