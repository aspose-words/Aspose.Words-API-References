---
title: PageSet
linktitle: PageSet
articleTitle: PageSet
second_title: Aspose.Words لـ .NET
description: قم بإنشاء مجموعة مخصصة من صفحة واحدة بسهولة باستخدام منشئ PageSet، المصمم لفهرسة الصفحات بدقة وتجربة مستخدم سلسة.
type: docs
weight: 10
url: /ar/net/aspose.words.saving/pageset/pageset/
---
## PageSet(*int*) {#constructor_1}

ينشئ مجموعة من صفحة واحدة استنادًا إلى فهرس الصفحة الدقيق.

```csharp
public PageSet(int page)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| page | Int32 | فهرس الصفحة يبدأ من الصفر. |

## ملاحظات

إذا تم العثور على صفحة غير موجودة في المستند، فسيتم طرح استثناء أثناء العرض. MaxValue تعني الصفحة الأخيرة في المستند.

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

* class [PageSet](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)

---

## PageSet(*params int[]*) {#constructor_2}

ينشئ مجموعة صفحات استنادًا إلى مؤشرات الصفحات الدقيقة.

```csharp
public PageSet(params int[] pages)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| pages | Int32[] | فهرس الصفحات يبدأ من الصفر. |

## ملاحظات

إذا تم العثور على صفحة غير موجودة في المستند، فسيتم طرح استثناء أثناء العرض. MaxValue تعني الصفحة الأخيرة في المستند.

## أمثلة

يوضح كيفية استخراج الصفحات استنادًا إلى مؤشرات الصفحات الدقيقة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//أضف خمس صفحات إلى المستند.
for (int i = 1; i < 6; i++)
{
    builder.Write("Page " + i);
    builder.InsertBreak(BreakType.PageBreak);
}

// قم بإنشاء كائن "XpsSaveOptions"، والذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .XPS.
XpsSaveOptions xpsOptions = new XpsSaveOptions();

// استخدم خاصية "PageSet" لتحديد مجموعة من صفحات المستند لحفظها في تنسيق XPS الناتج.
// في هذه الحالة سوف نختار، من خلال فهرس يعتمد على الصفر، ثلاث صفحات فقط: الصفحة 1، والصفحة 2، والصفحة 4.
xpsOptions.PageSet = new PageSet(0, 1, 3);

doc.Save(ArtifactsDir + "XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

### أنظر أيضا

* class [PageSet](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)

---

## PageSet(*params PageRange[]*) {#constructor}

ينشئ مجموعة صفحات استنادًا إلى النطاقات.

```csharp
public PageSet(params PageRange[] ranges)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| ranges | PageRange[] | مجموعة من نطاقات الصفحات. |

## ملاحظات

إذا تم العثور على نطاق يبدأ بعد الصفحة الأخيرة في المستند، فسيتم طرح استثناء أثناء العرض. سيتم اقتطاع جميع النطاقات التي تنتهي بعد الصفحة الأخيرة لتتناسب مع المستند.

## أمثلة

يوضح كيفية استخراج الصفحات استنادًا إلى نطاقات الصفحات الدقيقة.

```csharp
Document doc = new Document(MyDir + "Images.docx");

ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Tiff);
PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3),
    new PageRange(2, 4), new PageRange(1, 1));

imageOptions.PageSet = pageSet;
doc.Save(ArtifactsDir + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

### أنظر أيضا

* class [PageRange](../../pagerange/)
* class [PageSet](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
