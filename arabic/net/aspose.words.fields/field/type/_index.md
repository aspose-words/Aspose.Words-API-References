---
title: Field.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words لـ .NET
description: Field Type ملكية. الحصول على نوع حقل Microsoft Word في C#.
type: docs
weight: 100
url: /ar/net/aspose.words.fields/field/type/
---
## Field.Type property

الحصول على نوع حقل Microsoft Word.

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

// هذا التحميل الزائد لطريقة InsertField يقوم تلقائيًا بتحديث الحقول المدرجة.
Assert.That(DateTime.Parse(field.Result), Is.EqualTo(DateTime.Today).Within(1).Days);
```

### أنظر أيضا

* enum [FieldType](../../fieldtype/)
* class [Field](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
