---
title: FieldOptions.LegacyNumberFormat
linktitle: LegacyNumberFormat
articleTitle: LegacyNumberFormat
second_title: Aspose.Words لـ .NET
description: FieldOptions LegacyNumberFormat ملكية. الحصول على القيمة التي تشير إلى ما إذا كان تنسيق الأرقام القديم أقدم من AW 13.10 للحقول أو تعيينه ممكنًا أم لا في C#.
type: docs
weight: 160
url: /ar/net/aspose.words.fields/fieldoptions/legacynumberformat/
---
## FieldOptions.LegacyNumberFormat property

الحصول على القيمة التي تشير إلى ما إذا كان تنسيق الأرقام القديم (أقدم من AW 13.10) للحقول أو تعيينه ممكنًا أم لا.

```csharp
public bool LegacyNumberFormat { get; set; }
```

## ملاحظات

عندما يتم تعيين هذه الخاصية إلى`حقيقي`، رمز القالب "#" يعمل كما هو الحال في .net: يستبدل علامة الجنيه بالرقم المقابل إذا كان موجودًا؛ وإلا، فلن تظهر أي رموز في السلسلة الناتجة.

عندما يتم تعيين هذه الخاصية إلى`خطأ شنيع`، رمز القالب "#" يعمل مثل MS Word: يحدد عنصر التنسيق هذا الأماكن الرقمية المطلوبة لعرضها في النتيجة. إذا كانت النتيجة لا تتضمن رقمًا في ذلك المكان، فسيعرض MS Word مسافة. على سبيل المثال، يعرض { = 9 + 6 \# $### } 15 دولارًا.

القيمة الافتراضية هي`خطأ شنيع`.

## أمثلة

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
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
