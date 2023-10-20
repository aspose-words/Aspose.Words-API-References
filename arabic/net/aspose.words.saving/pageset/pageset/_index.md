---
title: PageSet
linktitle: PageSet
articleTitle: PageSet
second_title: Aspose.Words لـ .NET
description: PageSet البناء. إنشاء مجموعة من صفحة واحدة بناءً على فهرس الصفحات المحدد في C#.
type: docs
weight: 10
url: /ar/net/aspose.words.saving/pageset/pageset/
---
## PageSet(*int*) {#constructor_1}

إنشاء مجموعة من صفحة واحدة بناءً على فهرس الصفحات المحدد.

```csharp
public PageSet(int page)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| page | Int32 | الفهرس الصفري للصفحة. |

## ملاحظات

إذا تمت مصادفة صفحة غير موجودة في المستند، فسيتم طرح استثناء أثناء العرض. MaxValue تعني الصفحة الأخيرة في المستند.

### أنظر أيضا

* class [PageSet](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)

---

## PageSet(*params int[]*) {#constructor_2}

إنشاء مجموعة صفحات بناءً على فهارس الصفحات المحددة.

```csharp
public PageSet(params int[] pages)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| pages | Int32[] | الفهارس الصفرية للصفحات. |

## ملاحظات

إذا تمت مصادفة صفحة غير موجودة في المستند، فسيتم طرح استثناء أثناء العرض. MaxValue تعني الصفحة الأخيرة في المستند.

## أمثلة

يوضح كيفية استخراج الصفحات بناءً على فهارس الصفحات الدقيقة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أضف خمس صفحات إلى المستند.
for (int i = 1; i < 6; i++)
{
    builder.Write("Page " + i);
    builder.InsertBreak(BreakType.PageBreak);
}

// قم بإنشاء كائن "XpsSaveOptions"، والذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذا الأسلوب للمستند إلى .XPS.
XpsSaveOptions xpsOptions = new XpsSaveOptions();

// استخدم خاصية "PageSet" لتحديد مجموعة من صفحات المستند لحفظها لإخراج XPS.
// في هذه الحالة سنختار عبر فهرس صفري ثلاث صفحات فقط: الصفحة 1، الصفحة 2، والصفحة 4.
xpsOptions.PageSet = new PageSet(0, 1, 3);

doc.Save(ArtifactsDir + "XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

### أنظر أيضا

* class [PageSet](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)

---

## PageSet(*params PageRange[]*) {#constructor}

إنشاء مجموعة صفحات بناءً على النطاقات.

```csharp
public PageSet(params PageRange[] ranges)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| ranges | PageRange[] | مجموعة من نطاقات الصفحات. |

## ملاحظات

إذا تمت مواجهة نطاق يبدأ بعد الصفحة الأخيرة في المستند، فسيتم طرح استثناء أثناء العرض. يتم اقتطاع جميع النطاقات التي تنتهي بعد الصفحة الأخيرة لتناسب المستند.

## أمثلة

يوضح كيفية استخراج الصفحات بناءً على نطاقات الصفحات المحددة.

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
