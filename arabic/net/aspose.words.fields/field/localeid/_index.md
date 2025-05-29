---
title: Field.LocaleId
linktitle: LocaleId
articleTitle: LocaleId
second_title: Aspose.Words لـ .NET
description: أدر خاصية LocaleId لحقلك بسهولة. احصل على أو عيّن LCID لتحسين الترجمة وتجربة المستخدم في تطبيقاتك.
type: docs
weight: 60
url: /ar/net/aspose.words.fields/field/localeid/
---
## Field.LocaleId property

يحصل على أو يعين LCID للحقل.

```csharp
public int LocaleId { get; set; }
```

## أمثلة

يوضح كيفية إدراج حقل والعمل مع إعداداته المحلية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل حقل التاريخ، ثم اطبع التاريخ الذي سيعرضه.
// تحدد ثقافة موضوعك الحالية تنسيق التاريخ.
Field field = builder.InsertField(@"DATE");
Console.WriteLine($"Today's date, as displayed in the \"{CultureInfo.CurrentCulture.EnglishName}\" culture: {field.Result}");

Assert.AreEqual(1033, field.LocaleId);
// سيؤدي تغيير ثقافة موضوعنا إلى التأثير على نتيجة حقل التاريخ.
// هناك طريقة أخرى لجعل حقل DATE يعرض تاريخًا في ثقافة مختلفة وهي استخدام خاصية LocaleId الخاصة به.
//هذه الطريقة تسمح لنا بتجنب تغيير ثقافة الخيط للحصول على هذا التأثير.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
CultureInfo de = new CultureInfo("de-DE");
field.LocaleId = de.LCID;
field.Update();

Console.WriteLine($"Today's date, as displayed according to the \"{CultureInfo.GetCultureInfo(field.LocaleId).EnglishName}\" culture: {field.Result}");
```

### أنظر أيضا

* class [Field](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
