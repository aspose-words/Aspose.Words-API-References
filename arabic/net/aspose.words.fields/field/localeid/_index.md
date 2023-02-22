---
title: Field.LocaleId
second_title: Aspose.Words لمراجع .NET API
description: Field ملكية. الحصول على أو تحديد LCID للحقل.
type: docs
weight: 60
url: /ar/net/aspose.words.fields/field/localeid/
---
## Field.LocaleId property

الحصول على أو تحديد LCID للحقل.

```csharp
public int LocaleId { get; set; }
```

### أمثلة

يوضح كيفية إدراج حقل والعمل باستخدام الإعدادات المحلية الخاصة به.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل حقل التاريخ ، ثم اطبع التاريخ الذي سيعرضه.
// تحدد الثقافة الحالية لمؤشر الترابط الخاص بك تنسيق التاريخ.
Field field = builder.InsertField(@"DATE");
Console.WriteLine($"Today's date, as displayed in the \"{CultureInfo.CurrentCulture.EnglishName}\" culture: {field.Result}");

Assert.AreEqual(1033, field.LocaleId);
// تغيير ثقافة موضوعنا سيؤثر على نتيجة حقل التاريخ.
// هناك طريقة أخرى لجعل حقل التاريخ يعرض تاريخًا في ثقافة مختلفة وهي استخدام خاصية LocaleId الخاصة به.
// تتيح لنا هذه الطريقة تجنب تغيير ثقافة الخيط للحصول على هذا التأثير.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
CultureInfo de = new CultureInfo("de-DE");
field.LocaleId = de.LCID;
field.Update();

Console.WriteLine($"Today's date, as displayed according to the \"{CultureInfo.GetCultureInfo(field.LocaleId).EnglishName}\" culture: {field.Result}");
```

### أنظر أيضا

* class [Field](../)
* مساحة الاسم [Aspose.Words.Fields](../../field/)
* المجسم [Aspose.Words](../../../)


