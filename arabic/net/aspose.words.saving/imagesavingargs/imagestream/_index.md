---
title: ImageSavingArgs.ImageStream
linktitle: ImageStream
articleTitle: ImageStream
second_title: Aspose.Words لـ .NET
description: ImageSavingArgs ImageStream ملكية. يسمح بتحديد الدفق الذي سيتم حفظ الصورة فيه في C#.
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

القيمة الافتراضية هي`باطل` . عندما تكون هذه الخاصية`باطل` ، سيتم حفظ الصورة في ملف محدد في ملف[`ImageFileName`](../imagefilename/) ملكية.

استخدام[`IImageSavingCallback`](../../iimagesavingcallback/) لا يمكنك استبدال صورة بـ أخرى. الغرض منه هو فقط التحكم في الموقع حيث يتم حفظ الصور.

## أمثلة

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

* class [ImageSavingArgs](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
