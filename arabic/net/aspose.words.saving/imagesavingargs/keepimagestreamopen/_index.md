---
title: ImageSavingArgs.KeepImageStreamOpen
second_title: Aspose.Words لمراجع .NET API
description: ImageSavingArgs ملكية. يحدد ما إذا كان يجب على Aspose.Words إبقاء الدفق مفتوحًا أو إغلاقه بعد حفظ الصورة.
type: docs
weight: 60
url: /ar/net/aspose.words.saving/imagesavingargs/keepimagestreamopen/
---
## ImageSavingArgs.KeepImageStreamOpen property

يحدد ما إذا كان يجب على Aspose.Words إبقاء الدفق مفتوحًا أو إغلاقه بعد حفظ الصورة.

```csharp
public bool KeepImageStreamOpen { get; set; }
```

### ملاحظات

الافتراضي هو`خاطئة` و Aspose.Words ستغلق الدفق الذي قدمته في[`ImageStream`](../imagestream/) الخاصية بعد كتابة صورة فيها . حدد`حقيقي` لإبقاء الدفق مفتوحًا.

### أمثلة

يوضح كيفية إشراك رد اتصال حفظ الصورة في عملية تحويل HTML.

```csharp
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // عندما نحفظ المستند إلى HTML ، يمكننا تمرير كائن SaveOptions لتعيين رد اتصال
    // لتخصيص عملية حفظ الصورة.
    HtmlSaveOptions options = new HtmlSaveOptions();
    options.ImageSavingCallback = new ImageShapePrinter();

    doc.Save(ArtifactsDir + "HtmlSaveOptions.ImageSavingCallback.html", options);
}

/// <summary>
/// يطبع خصائص كل صورة حيث أن عملية الحفظ تحفظها في ملف صورة في نظام الملفات المحلي
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

* class [ImageSavingArgs](../)
* مساحة الاسم [Aspose.Words.Saving](../../imagesavingargs/)
* المجسم [Aspose.Words](../../../)


