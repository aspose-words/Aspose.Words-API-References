---
title: Document.FieldOptions
linktitle: FieldOptions
articleTitle: FieldOptions
second_title: Aspose.Words لـ .NET
description: استكشف خاصية "خيارات حقل المستند" لإدارة معالجة الحقول بفعالية. اكتشف خيارات فريدة لتحسين التحكم في المستندات وتخصيصها.
type: docs
weight: 130
url: /ar/net/aspose.words/document/fieldoptions/
---
## Document.FieldOptions property

يحصل على[`FieldOptions`](../../../aspose.words.fields/fieldoptions/) كائن يمثل خيارات للتحكم في التعامل مع الحقول في المستند.

```csharp
public FieldOptions FieldOptions { get; }
```

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

* class [FieldOptions](../../../aspose.words.fields/fieldoptions/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
