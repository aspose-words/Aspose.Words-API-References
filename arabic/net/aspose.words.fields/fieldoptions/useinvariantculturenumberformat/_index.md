---
title: FieldOptions.UseInvariantCultureNumberFormat
linktitle: UseInvariantCultureNumberFormat
articleTitle: UseInvariantCultureNumberFormat
second_title: Aspose.Words لـ .NET
description: FieldOptions UseInvariantCultureNumberFormat ملكية. الحصول على أو تعيين القيمة التي تشير إلى أنه تم تحليل تنسيق الأرقام باستخدام الثقافة الثابتة أو not في C#.
type: docs
weight: 210
url: /ar/net/aspose.words.fields/fieldoptions/useinvariantculturenumberformat/
---
## FieldOptions.UseInvariantCultureNumberFormat property

الحصول على أو تعيين القيمة التي تشير إلى أنه تم تحليل تنسيق الأرقام باستخدام الثقافة الثابتة أو not

```csharp
public bool UseInvariantCultureNumberFormat { get; set; }
```

## ملاحظات

عند تعيين هذه الخاصية على`حقيقي` ، تنسيق الأرقام مأخوذ من ثقافة ثابتة.

عند تعيين هذه الخاصية على`خطأ شنيع` تنسيق الرقم مأخوذ من ثقافة الموضوع الحالي.

القيمة الافتراضية هي`خطأ شنيع`.

## أمثلة

يوضح كيفية تنسيق الأرقام وفقًا للثقافة الثابتة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Thread.CurrentThread.CurrentCulture = new CultureInfo("de-DE");
Field field = builder.InsertField(" = 1234567,89 \\# $#,###,###.##");
field.Update();

 // في بعض الأحيان، قد لا تقوم الحقول بتنسيق أرقامها بشكل صحيح في ظل ثقافات معينة.
Assert.IsFalse(doc.FieldOptions.UseInvariantCultureNumberFormat);
Assert.AreEqual("$1234567,89 .     ", field.Result);

// لإصلاح ذلك، يمكننا تغيير ثقافة الموضوع بأكمله.
// هناك طريقة أخرى لإصلاح ذلك وهي تعيين هذه العلامة،
// الذي يحصل على جميع الحقول لاستخدام الثقافة الثابتة عند تنسيق الأرقام.
// تتيح لنا هذه الطريقة تجنب تغيير ثقافة الموضوع بأكمله.
doc.FieldOptions.UseInvariantCultureNumberFormat = true;
field.Update();
Assert.AreEqual("$1.234.567,89", field.Result);
```

### أنظر أيضا

* class [FieldOptions](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
