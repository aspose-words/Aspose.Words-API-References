---
title: HtmlSaveOptions.NavigationMapLevel
linktitle: NavigationMapLevel
articleTitle: NavigationMapLevel
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية NavigationMapLevel في HtmlSaveOptions، للتحكم في مستويات العناوين في صيغ EPUB وMOBI وAZW3. حسّن ظهور محتواك!
type: docs
weight: 390
url: /ar/net/aspose.words.saving/htmlsaveoptions/navigationmaplevel/
---
## HtmlSaveOptions.NavigationMapLevel property

يُحدد الحد الأقصى لعدد العناوين المُضافة إلى خريطة التنقل عند التصدير إلى تنسيقات EPUB أو MOBI أو AZW3 . القيمة الافتراضية هي`3` .

```csharp
public int NavigationMapLevel { get; set; }
```

## ملاحظات

تتيح خريطة التنقل لوكلاء المستخدم سهولة التنقل عبر بنية المستند. عادةً ما تتوافق نقاط التنقل مع العناوين في المستند. لتعبئة العناوين حتى المستوى**ن** قم بتعيين هذه القيمة إلى`NavigationMapLevel`.

بشكل افتراضي، يتم ملء ثلاثة مستويات من العناوين: فقرات الأنماط**العنوان 1** ،**العنوان 2** و**العنوان 3**. يمكنك تعيين هذه الخاصية إلى قيمة تتراوح بين 1 إلى 9 من أجل طلب المستوى الأقصى المقابل. سيؤدي تعيينها إلى الصفر إلى تقليص خريطة التنقل إلى جذر المستند أو جذور أجزاء المستند فقط.

## أمثلة

يوضح كيفية إنشاء جدول المحتويات لمستندات Azw3.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Azw3);
options.NavigationMapLevel = 2;

doc.Save(ArtifactsDir + "HtmlSaveOptions.CreateAZW3Toc.azw3", options);
```

يوضح كيفية إنشاء جدول محتويات لمستندات Mobi.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Mobi);
options.NavigationMapLevel = 5;

doc.Save(ArtifactsDir + "HtmlSaveOptions.CreateMobiToc.mobi", options);
```

يوضح كيفية تصفية العناوين التي تظهر في لوحة التنقل الخاصة بمستند Epub المحفوظ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// كل فقرة نقوم بتنسيقها باستخدام نمط "العنوان" يمكن أن تكون بمثابة عنوان.
// يمكن أن يكون لكل عنوان أيضًا مستوى عنوان، يتم تحديده من خلال رقم نمط العنوان الخاص به.
// العناوين أدناه هي للمستويات 1-3.
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.Writeln("Heading #1");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 2"];
builder.Writeln("Heading #2");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 3"];
builder.Writeln("Heading #3");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.Writeln("Heading #4");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 2"];
builder.Writeln("Heading #5");
builder.ParagraphFormat.Style = builder.Document.Styles["Heading 3"];
builder.Writeln("Heading #6");

// عادةً ما يقوم قراء الكتب الإلكترونية بإنشاء جدول محتويات لمستنداتهم.
// كل فقرة تحتوي على نمط "عنوان" في المستند سوف تنشئ إدخالاً في جدول المحتويات هذا.
 // يمكننا استخدام خاصية "NavigationMapLevel" لتعيين الحد الأقصى لمستوى العنوان.
// لن يقوم قارئ Epub بإضافة عناوين ذات مستوى أعلى من المستوى الذي حددناه إلى جدول المحتويات.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Epub);
options.NavigationMapLevel = 2;

// تحتوي مستندنا على ستة عناوين، اثنان منها أعلى من المستوى 2.
//سيحتوي جدول محتويات هذه الوثيقة على أربعة إدخالات.
doc.Save(ArtifactsDir + "HtmlSaveOptions.EpubHeadings.epub", options);
```

### أنظر أيضا

* class [HtmlSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
