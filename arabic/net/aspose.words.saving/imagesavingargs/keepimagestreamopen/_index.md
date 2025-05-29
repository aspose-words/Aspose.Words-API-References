---
title: ImageSavingArgs.KeepImageStreamOpen
linktitle: KeepImageStreamOpen
articleTitle: KeepImageStreamOpen
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية KeepImageStreamOpen في ImageSavingArgs لـ Aspose.Words. تحكم في سلوك التدفق لحفظ الصور بكفاءة وتحسين الأداء.
type: docs
weight: 60
url: /ar/net/aspose.words.saving/imagesavingargs/keepimagestreamopen/
---
## ImageSavingArgs.KeepImageStreamOpen property

يحدد ما إذا كان يجب على Aspose.Words إبقاء الدفق مفتوحًا أو إغلاقه بعد حفظ الصورة.

```csharp
public bool KeepImageStreamOpen { get; set; }
```

## ملاحظات

الافتراضي هو`خطأ شنيع` وسوف يقوم Aspose.Words بإغلاق الدفق الذي قدمته في[`ImageStream`](../imagestream/) الخاصية بعد كتابة صورة فيها. حدد`حقيقي` للحفاظ على مجرى النهر مفتوحا.

## أمثلة

يوضح كيفية إشراك استدعاء حفظ الصورة في عملية تحويل HTML.

```csharp
public void ImageSavingCallback()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // عندما نحفظ المستند في HTML، يمكننا تمرير كائن SaveOptions لتعيين معاودة الاتصال
    // لتخصيص عملية حفظ الصورة.
    HtmlSaveOptions options = new HtmlSaveOptions();
    options.ImageSavingCallback = new ImageShapePrinter();

    doc.Save(ArtifactsDir + "HtmlSaveOptions.ImageSavingCallback.html", options);
}

/// <summary>
/// طباعة خصائص كل صورة أثناء عملية الحفظ التي تحفظها في ملف صورة في نظام الملفات المحلي
/// أثناء تصدير المستند إلى HTML.
/// </summary>
private class ImageShapePrinter : IImageSavingCallback
{
    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        args.KeepImageStreamOpen = false;
        Assert.True(args.IsImageAvailable);

        Console.WriteLine($"{args.Document.OriginalFileName.Split('\\').Last()} Image #{++mImageCount}");

        LayoutCollector layoutCollector = new LayoutCollector(args.Document);

        Console.WriteLine($"\tOn page:\t{layoutCollector.GetStartPageIndex(args.CurrentShape)}");
        Console.WriteLine($"\tDimensions:\t{args.CurrentShape.Bounds}");
        Console.WriteLine($"\tAlignment:\t{args.CurrentShape.VerticalAlignment}");
        Console.WriteLine($"\tWrap type:\t{args.CurrentShape.WrapType}");
        Console.WriteLine($"Output filename:\t{args.ImageFileName}\n");
    }

    private int mImageCount;
}
```

### أنظر أيضا

* class [ImageSavingArgs](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
