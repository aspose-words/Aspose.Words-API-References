---
title: PageSet
second_title: Aspose.Words لمراجع .NET API
description: لإنشاء مجموعة من صفحة واحدة بناءً على فهرس الصفحة الدقيق.
type: docs
weight: 10
url: /ar/net/aspose.words.saving/pageset/pageset/
---
## PageSet(int) {#constructor_1}

لإنشاء مجموعة من صفحة واحدة بناءً على فهرس الصفحة الدقيق.

```csharp
public PageSet(int page)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| page | Int32 | فهرس للصفحة على أساس الصفر. |

### ملاحظات

إذا تمت مصادفة صفحة غير موجودة في المستند ، فسيتم طرح استثناء أثناء العرض.MaxValue تعني الصفحة الأخيرة في المستند.

### أنظر أيضا

* class [PageSet](../../pageset)
* مساحة الاسم [Aspose.Words.Saving](../../pageset)
* المجسم [Aspose.Words](../../../)

---

## PageSet(params int[]) {#constructor_2}

إنشاء مجموعة صفحات بناءً على فهارس الصفحات الدقيقة.

```csharp
public PageSet(params int[] pages)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| pages | Int32[] | فهارس الصفحات الصفرية. |

### ملاحظات

إذا تمت مصادفة صفحة غير موجودة في المستند ، فسيتم طرح استثناء أثناء العرض.MaxValue تعني الصفحة الأخيرة في المستند.

### أمثلة

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

// قم بإنشاء كائن "XpsSaveOptions" ، والذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .XPS.
XpsSaveOptions xpsOptions = new XpsSaveOptions();

// استخدم خاصية "PageSet" لتحديد مجموعة من صفحات المستند لحفظها في إخراج XPS.
// في هذه الحالة ، سنختار ، عبر فهرس صفري ، ثلاث صفحات فقط: الصفحة 1 والصفحة 2 والصفحة 4.
xpsOptions.PageSet = new PageSet(0, 1, 3);

doc.Save(ArtifactsDir + "XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

### أنظر أيضا

* class [PageSet](../../pageset)
* مساحة الاسم [Aspose.Words.Saving](../../pageset)
* المجسم [Aspose.Words](../../../)

---

## PageSet(params PageRange[]) {#constructor}

إنشاء مجموعة صفحات بناءً على النطاقات.

```csharp
public PageSet(params PageRange[] ranges)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| ranges | PageRange[] | صفيف من نطاقات الصفحات. |

### ملاحظات

إذا تمت مصادفة نطاق يبدأ بعد الصفحة الأخيرة في المستند ، سيتم طرح استثناء أثناء العرض. يتم اقتطاع جميع النطاقات التي تنتهي بعد الصفحة الأخيرة لتلائم المستند.

### أمثلة

يوضح كيفية استخراج الصفحات بناءً على نطاقات الصفحات الدقيقة.

```csharp
Document doc = new Document(MyDir + "Images.docx");

ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Tiff);
PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3),
    new PageRange(2, 4), new PageRange(1, 1));

imageOptions.PageSet = pageSet;
doc.Save(ArtifactsDir + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

### أنظر أيضا

* class [PageRange](../../pagerange)
* class [PageSet](../../pageset)
* مساحة الاسم [Aspose.Words.Saving](../../pageset)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
