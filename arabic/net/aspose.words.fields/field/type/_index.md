---
title: Field.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words لـ .NET
description: اكتشف نوع حقل مايكروسوفت وورد باستخدام خاصية "نوع الحقل". حسّن مستنداتك بتنسيق دقيق ومحتوى ديناميكي.
type: docs
weight: 100
url: /ar/net/aspose.words.fields/field/type/
---
## Field.Type property

يحصل على نوع حقل Microsoft Word.

```csharp
public virtual FieldType Type { get; }
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

* enum [FieldType](../../fieldtype/)
* class [Field](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
