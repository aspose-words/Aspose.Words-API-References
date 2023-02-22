---
title: FieldOptions.LegacyNumberFormat
second_title: Aspose.Words لمراجع .NET API
description: FieldOptions ملكية. الحصول على القيمة أو تعيينها للإشارة إلى ما إذا كان تنسيق الأرقام القديم أقدم من AW 13.10 للحقول ممكّنًا أم لا.
type: docs
weight: 140
url: /ar/net/aspose.words.fields/fieldoptions/legacynumberformat/
---
## FieldOptions.LegacyNumberFormat property

الحصول على القيمة أو تعيينها للإشارة إلى ما إذا كان تنسيق الأرقام القديم (أقدم من AW 13.10) للحقول ممكّنًا أم لا.

```csharp
public bool LegacyNumberFormat { get; set; }
```

### ملاحظات

عندما يتم تعيين هذه الخاصية على **حقيقي**، رمز القالب "#" يعمل كما في .net: يستبدل علامة الجنيه بالرقم المقابل إذا كان هناك واحد ؛ وبخلاف ذلك ، لا تظهر أي رموز في سلسلة النتائج.

عندما يتم تعيين هذه الخاصية على **خاطئة**، رمز القالب "#" يعمل مثل MS Word: يحدد عنصر التنسيق هذا الأماكن الرقمية المطلوبة لعرضها في النتيجة. إذا لم تتضمن النتيجة رقمًا في ذلك المكان ، يعرض MS Word مسافة. على سبيل المثال ، {= 9 + 6 \ # $ ###} يعرض 15 دولارًا.

النظام الأساسي **خاطئة**.

### أمثلة

يوضح كيفية تمكين تنسيق الأرقام القديم للحقول.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Field field = builder.InsertField("= 2 + 3 \\# $##");

Assert.AreEqual("$ 5", field.Result);

doc.FieldOptions.LegacyNumberFormat = true;
field.Update();

Assert.AreEqual("$5", field.Result);
```

### أنظر أيضا

* class [FieldOptions](../)
* مساحة الاسم [Aspose.Words.Fields](../../fieldoptions/)
* المجسم [Aspose.Words](../../../)


