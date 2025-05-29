---
title: ImageSavingArgs.ImageStream
linktitle: ImageStream
articleTitle: ImageStream
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ImageStream في ImageSavingArgs لتحديد مكان حفظ صورك بسهولة، مما يعزز سير عملك وكفاءتك.
type: docs
weight: 40
url: /ar/net/aspose.words.saving/imagesavingargs/imagestream/
---
## ImageSavingArgs.ImageStream property

يسمح بتحديد الدفق الذي سيتم حفظ الصورة فيه.

```csharp
public Stream ImageStream { get; set; }
```

## ملاحظات

تتيح لك هذه الخاصية حفظ الصور في التدفقات بدلاً من الملفات أثناء HTML.

القيمة الافتراضية هي`باطل` . عندما تكون هذه الخاصية`باطل` سيتم حفظ الصورة في الملف المحدد في[`ImageFileName`](../imagefilename/) ملكية.

استخدام[`IImageSavingCallback`](../../iimagesavingcallback/) لا يمكنك استبدال صورة بـ أخرى. الغرض من ذلك هو فقط التحكم في مكان حفظ الصور.

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
