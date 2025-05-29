---
title: FieldOptions.UseInvariantCultureNumberFormat
linktitle: UseInvariantCultureNumberFormat
articleTitle: UseInvariantCultureNumberFormat
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldOptions UseInvariantCultureNumberFormat لإدارة تنسيق الأرقام بسهولة باستخدام الثقافة الثابتة للتعامل مع البيانات بشكل متسق.
type: docs
weight: 210
url: /ar/net/aspose.words.fields/fieldoptions/useinvariantculturenumberformat/
---
## FieldOptions.UseInvariantCultureNumberFormat property

يحصل على القيمة أو يعينها للإشارة إلى أن تنسيق الرقم يتم تحليله باستخدام ثقافة ثابتة أم لا

```csharp
public bool UseInvariantCultureNumberFormat { get; set; }
```

## ملاحظات

عندما يتم تعيين هذه الخاصية على`حقيقي`، يتم أخذ تنسيق الرقم من ثقافة ثابتة.

عندما يتم تعيين هذه الخاصية على`خطأ شنيع` ، يتم أخذ تنسيق الرقم من ثقافة الخيط الحالي.

القيمة الافتراضية هي`خطأ شنيع`.

## أمثلة

يوضح كيفية تنسيق الأرقام وفقًا للثقافة الثابتة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Thread.CurrentThread.CurrentCulture = new CultureInfo("de-DE");
Field field = builder.InsertField(" = 1234567,89 \\# $#,###,###.##");
field.Update();

 // في بعض الأحيان، قد لا تقوم الحقول بتنسيق أرقامها بشكل صحيح في بعض الثقافات.
Assert.IsFalse(doc.FieldOptions.UseInvariantCultureNumberFormat);
Assert.AreEqual("$1.234.567,89 ,     ", field.Result);

// لإصلاح ذلك، يمكننا تغيير الثقافة للموضوع بأكمله.
// هناك طريقة أخرى لإصلاح ذلك وهي تعيين هذا العلم،
// الذي يجعل جميع الحقول تستخدم الثقافة الثابتة عند تنسيق الأرقام.
// تسمح لنا هذه الطريقة بتجنب تغيير الثقافة للموضوع بأكمله.
doc.FieldOptions.UseInvariantCultureNumberFormat = true;
field.Update();
Assert.AreEqual("$1.234.567,89", field.Result);
```

### أنظر أيضا

* class [FieldOptions](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
