---
title: FieldChar.FieldType
linktitle: FieldType
articleTitle: FieldType
second_title: Aspose.Words لـ .NET
description: FieldChar FieldType ملكية. إرجاع نوع الحقل في C#.
type: docs
weight: 10
url: /ar/net/aspose.words.fields/fieldchar/fieldtype/
---
## FieldChar.FieldType property

إرجاع نوع الحقل.

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

// استرداد كائن الواجهة الذي يمثل الحقل الموجود في المستند.
field = (FieldDate)fieldStart.GetField();

Assert.AreEqual(false, field.IsLocked);
Assert.AreEqual(" DATE  \\@ \"dddd, MMMM dd, yyyy\"", field.GetFieldCode());

// قم بتحديث الحقل لإظهار التاريخ الحالي.
field.Update();
```

### أنظر أيضا

* enum [FieldType](../../fieldtype/)
* class [FieldChar](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
