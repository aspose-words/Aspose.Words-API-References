---
title: FieldOptions.FieldUpdateCultureSource
linktitle: FieldUpdateCultureSource
articleTitle: FieldUpdateCultureSource
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية FieldUpdateCultureSource على تعزيز تنسيق نتيجة الحقل من خلال تحديد الثقافة المطلوبة لتحقيق الوضوح وسهولة الاستخدام بشكل مثالي.
type: docs
weight: 110
url: /ar/net/aspose.words.fields/fieldoptions/fieldupdateculturesource/
---
## FieldOptions.FieldUpdateCultureSource property

يحدد الثقافة التي سيتم استخدامها لتنسيق نتيجة الحقل.

```csharp
public FieldUpdateCultureSource FieldUpdateCultureSource { get; set; }
```

## ملاحظات

بشكل افتراضي، يتم استخدام ثقافة الخيط الحالي.

يؤثر الإعداد فقط على حقول التاريخ/الوقت التي تحتوي على مفتاح التنسيق \\@.

## أمثلة

يوضح كيفية تحديد مصدر الثقافة المستخدمة لتنسيق التاريخ أثناء تحديث الحقل أو دمج البريد.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل حقلي دمج باللغة الألمانية.
builder.Font.LocaleId = new CultureInfo("de-DE").LCID;
builder.InsertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
builder.Write(" - ");
builder.InsertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");

// قم بتعيين الثقافة الحالية إلى اللغة الإنجليزية الأمريكية بعد الحفاظ على قيمتها الأصلية في المتغير.
CultureInfo currentCulture = Thread.CurrentThread.CurrentCulture;
Thread.CurrentThread.CurrentCulture = new CultureInfo("en-US");

// سيستخدم هذا الدمج ثقافة الموضوع الحالي لتنسيق التاريخ، باللغة الإنجليزية الأمريكية.
doc.MailMerge.Execute(new[] { "Date1" }, new object[] { new DateTime(2020, 1, 01) });

// قم بتكوين الدمج التالي للحصول على قيمة ثقافته من رمز الحقل. ستكون قيمة هذه الثقافة بالألمانية.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
doc.MailMerge.Execute(new[] { "Date2" }, new object[] { new DateTime(2020, 1, 01) });

// تحتوي نتيجة الدمج الأولى على تاريخ بتنسيق اللغة الإنجليزية، بينما النتيجة الثانية باللغة الألمانية.
Assert.AreEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020", doc.Range.Text.Trim());

//استعادة ثقافة الموضوع الأصلية.
Thread.CurrentThread.CurrentCulture = currentCulture;
```

### أنظر أيضا

* enum [FieldUpdateCultureSource](../../fieldupdateculturesource/)
* class [FieldOptions](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
