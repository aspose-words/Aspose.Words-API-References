---
title: FieldOptions.LegacyNumberFormat
linktitle: LegacyNumberFormat
articleTitle: LegacyNumberFormat
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldOptions LegacyNumberFormat لتمكين تنسيقات الأرقام القديمة للحقول أو تعطيلها، مما يعزز التوافق والأداء.
type: docs
weight: 160
url: /ar/net/aspose.words.fields/fieldoptions/legacynumberformat/
---
## FieldOptions.LegacyNumberFormat property

يحصل على القيمة التي تشير إلى ما إذا كان تنسيق الأرقام القديم (الأقدم من AW 13.10) للحقول ممكّنًا أم لا أو يعينها.

```csharp
public bool LegacyNumberFormat { get; set; }
```

## ملاحظات

عندما يتم تعيين هذه الخاصية على`حقيقي`، يعمل رمز القالب "#" كما هو الحال في .net: ويستبدل علامة الجنيه بالرقم المقابل إذا كان موجودًا؛ وإلا فلن تظهر أي رموز في سلسلة النتيجة.

عندما يتم تعيين هذه الخاصية على`خطأ شنيع`رمز القالب "#" يعمل كـ MS Word: يحدد هذا العنصر التنسيقي الخانات الرقمية المطلوبة لعرضها في النتيجة. إذا لم تتضمن النتيجة رقمًا في تلك الخانة، يعرض MS Word مسافة. على سبيل المثال، { = 9 + 6 \# $### } يعرض $ 15.

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
