---
title: PageRange
linktitle: PageRange
articleTitle: PageRange
second_title: Aspose.Words لـ .NET
description: PageRange البناء. إنشاء كائن نطاق صفحات جديد في C#.
type: docs
weight: 10
url: /ar/net/aspose.words.saving/pagerange/pagerange/
---
## PageRange constructor

إنشاء كائن نطاق صفحات جديد.

```csharp
public PageRange(int from, int to)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| from | Int32 | الفهرس الصفري لصفحة البداية. |
| to | Int32 | فهرس الصفحة النهائية ذو الأساس الصفري. إذا تجاوز فهرس الصفحة الأخيرة في المستند، فسيتم اقتطاعه ليناسب المستند عند العرض. |

## ملاحظات

MaxValue تعني الصفحة الأخيرة في المستند.

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

* class [PageRange](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
