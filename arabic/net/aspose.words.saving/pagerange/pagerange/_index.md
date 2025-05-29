---
title: PageRange
linktitle: PageRange
articleTitle: PageRange
second_title: Aspose.Words لـ .NET
description: أنشئ نطاقات صفحات مخصصة بسهولة باستخدام مُنشئ نطاقات الصفحات. حسّن إدارة مستنداتك بدقة ومرونة.
type: docs
weight: 10
url: /ar/net/aspose.words.saving/pagerange/pagerange/
---
## PageRange constructor

ينشئ كائن نطاق صفحة جديد.

```csharp
public PageRange(int from, int to)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| from | Int32 | فهرس الصفحة الأولية المستند إلى الصفر. |
| to | Int32 | فهرس الصفحة النهائية المبني على الصفر. إذا تجاوز فهرس الصفحة الأخيرة في المستند، يتم اقتطاعه ليتناسب مع المستند عند العرض. |

## ملاحظات

MaxValue تعني الصفحة الأخيرة في المستند.

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

* class [PageRange](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
