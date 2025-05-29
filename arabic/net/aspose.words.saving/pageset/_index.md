---
title: PageSet Class
linktitle: PageSet
articleTitle: PageSet
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Saving.PageSet لإدارة مستندات فعّالة. حدّد مجموعات صفحات عشوائية بسهولة، وحسّن سير عملك اليوم!
type: docs
weight: 6170
url: /ar/net/aspose.words.saving/pageset/
---
## PageSet class

يصف مجموعة عشوائية من الصفحات.

لمعرفة المزيد، قم بزيارة[البرمجة باستخدام المستندات](https://docs.aspose.com/words/net/programming-with-documents/) مقالة توثيقية.

```csharp
public sealed class PageSet : IEnumerable<int>
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [PageSet](pageset/#constructor_1)(*int*) | ينشئ مجموعة من صفحة واحدة استنادًا إلى فهرس الصفحة الدقيق. |
| [PageSet](pageset/#constructor_2)(*params int[]*) | ينشئ مجموعة صفحات استنادًا إلى مؤشرات الصفحات الدقيقة. |
| [PageSet](pageset/#constructor)(*params PageRange[]*) | ينشئ مجموعة صفحات استنادًا إلى النطاقات. |

## الخصائص

| اسم | وصف |
| --- | --- |
| static [All](../../aspose.words.saving/pageset/all/) { get; } | يحصل على مجموعة تحتوي على جميع صفحات المستند بالترتيب الأصلي. |
| static [Even](../../aspose.words.saving/pageset/even/) { get; } | يحصل على مجموعة تحتوي على جميع الصفحات الزوجية للمستند بالترتيب الأصلي. |
| static [Odd](../../aspose.words.saving/pageset/odd/) { get; } | يحصل على مجموعة من جميع الصفحات الفردية للمستند بالترتيب الأصلي. |

## طُرق

| اسم | وصف |
| --- | --- |
| [GetEnumerator](../../aspose.words.saving/pageset/getenumerator/)() |  |

## أمثلة

يوضح كيفية عرض صفحة واحدة من مستند إلى صورة JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// قم بإنشاء كائن "ImageSaveOptions" الذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل الطريقة التي تقوم بها هذه الطريقة بتحويل المستند إلى صورة.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
// اضبط "PageSet" على "1" لتحديد الصفحة الثانية عبر
// الفهرس المبني على الصفر لبدء عرض المستند منه.
options.PageSet = new PageSet(1);

// عندما نحفظ المستند بتنسيق JPEG، يقوم Aspose.Words بعرض صفحة واحدة فقط.
// ستحتوي هذه الصورة على صفحة واحدة بدءًا من الصفحة الثانية،
// والتي ستكون فقط الصفحة الثانية من المستند الأصلي.
doc.Save(ArtifactsDir + "ImageSaveOptions.OnePage.jpg", options);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
