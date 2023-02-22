---
title: ImageSavingArgs.Document
second_title: Aspose.Words لمراجع .NET API
description: ImageSavingArgs ملكية. الحصول على كائن المستند الذي يتم حفظه حاليًا.
type: docs
weight: 20
url: /ar/net/aspose.words.saving/imagesavingargs/document/
---
## ImageSavingArgs.Document property

الحصول على كائن المستند الذي يتم حفظه حاليًا.

```csharp
public Document Document { get; }
```

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

* class [Document](../../../aspose.words/document/)
* class [ImageSavingArgs](../)
* مساحة الاسم [Aspose.Words.Saving](../../imagesavingargs/)
* المجسم [Aspose.Words](../../../)


