---
title: FieldChar.IsLocked
linktitle: IsLocked
articleTitle: IsLocked
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldChar IsLocked، وتحكّم في إعادة حساب الحقول بسهولة. حسّن دقة وكفاءة مستندك اليوم!
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fieldchar/islocked/
---
## FieldChar.IsLocked property

يحصل على أو يحدد ما إذا كان الحقل الرئيسي مقفلاً (لا ينبغي إعادة حساب نتيجته).

```csharp
public bool IsLocked { get; set; }
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
