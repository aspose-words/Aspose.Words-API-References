---
title: ImageSavingArgs.IsImageAvailable
second_title: Aspose.Words لمراجع .NET API
description: ImageSavingArgs ملكية. إرجاعحقيقي إذا كانت الصورة الحالية متاحة للتصدير.
type: docs
weight: 50
url: /ar/net/aspose.words.saving/imagesavingargs/isimageavailable/
---
## ImageSavingArgs.IsImageAvailable property

إرجاع`حقيقي` إذا كانت الصورة الحالية متاحة للتصدير.

```csharp
public bool IsImageAvailable { get; }
```

### ملاحظات

يمكن أن تكون بعض الصور في المستند غير متاحة، على سبيل المثال، لأن الصورة مرتبطة ولا يمكن الوصول إلى الرابط أو لا يشير إلى صورة صالحة. في هذه الحالة يقوم Aspose.Words بتصدير رمز بعلامة الصليب الأحمر. تُرجع هذه الخاصية `حقيقي` إذا كانت الصورة الأصلية متوفرة؛ عائدات`خطأ شنيع`إذا كانت الصورة الأصلية غير متوفرة وسيتم عرض أيقونة "بدون صورة" للحفظ.

عند حفظ شكل مجموعة أو شكل لا يتطلب أي صورة، تكون هذه الخاصية دائمًا`حقيقي`.

### أمثلة

يوضح كيفية تضمين رد اتصال لحفظ الصورة في عملية تحويل HTML.

```csharp
public void ImageSavingCallback()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // عندما نحفظ المستند إلى HTML، يمكننا تمرير كائن SaveOptions لتعيين رد اتصال
    // لتخصيص عملية حفظ الصورة.
    HtmlSaveOptions options = new HtmlSaveOptions();
    options.ImageSavingCallback = new ImageShapePrinter();

    doc.Save(ArtifactsDir + "HtmlSaveOptions.ImageSavingCallback.html", options);
}

/// <summary>
/// يطبع خصائص كل صورة بينما تقوم عملية الحفظ بحفظها في ملف صورة في نظام الملفات المحلي
/// أثناء تصدير مستند إلى HTML.
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
* مساحة الاسم [Aspose.Words.Saving](../../imagesavingargs/)
* المجسم [Aspose.Words](../../../)


