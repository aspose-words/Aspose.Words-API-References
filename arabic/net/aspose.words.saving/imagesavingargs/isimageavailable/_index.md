---
title: ImageSavingArgs.IsImageAvailable
linktitle: IsImageAvailable
articleTitle: IsImageAvailable
second_title: Aspose.Words لـ .NET
description: تحقق من جاهزية الصورة للتصدير باستخدام خاصية IsImageAvailable في ImageSavingArgs. تمتع بإدارة سلسة وفعّالة للصور!
type: docs
weight: 50
url: /ar/net/aspose.words.saving/imagesavingargs/isimageavailable/
---
## ImageSavingArgs.IsImageAvailable property

إرجاع`حقيقي` إذا كانت الصورة الحالية متاحة للتصدير.

```csharp
public bool IsImageAvailable { get; }
```

## ملاحظات

قد لا تتوفر بعض الصور في المستند، على سبيل المثال، لأن image مرتبط، والرابط غير قابل للوصول أو لا يشير إلى صورة صالحة. في هذه الحالة، تُصدّر Aspose.Words رمزًا عليه علامة صليب حمراء. تُرجع هذه الخاصية `حقيقي` إذا كانت الصورة الأصلية متاحة؛ يتم إرجاعها`خطأ شنيع`إذا لم تكن الصورة الأصلية متاحة، فسيتم تقديم أيقونة "لا توجد صورة" للحفظ.

عند حفظ شكل مجموعة أو شكل لا يتطلب أي صورة، تكون هذه الخاصية دائمًا`حقيقي`.

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

* property [CurrentShape](../currentshape/)
* class [ImageSavingArgs](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
