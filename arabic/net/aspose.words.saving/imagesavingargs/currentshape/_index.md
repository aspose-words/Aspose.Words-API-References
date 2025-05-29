---
title: ImageSavingArgs.CurrentShape
linktitle: CurrentShape
articleTitle: CurrentShape
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية CurrentShape الخاصة بـ ImageSavingArgs للوصول إلى كائن ShapeBase لحفظ الشكل وتجميع الأشكال بكفاءة في مشاريعك.
type: docs
weight: 10
url: /ar/net/aspose.words.saving/imagesavingargs/currentshape/
---
## ImageSavingArgs.CurrentShape property

يحصل على[`ShapeBase`](../../../aspose.words.drawing/shapebase/) الكائن المقابل للشكل أو شكل المجموعة الذي سيتم حفظه.

```csharp
public ShapeBase CurrentShape { get; }
```

## ملاحظات

[`IImageSavingCallback`](../../iimagesavingcallback/) يمكن تشغيله أثناء حفظ شكل أو شكل مجموعة. لهذا السبب تحتوي الخاصية على[`ShapeBase`](../../../aspose.words.drawing/shapebase/) النوع. يمكنك التحقق مما إذا كان شكل المجموعة بمقارنة [`ShapeType`](../../../aspose.words.drawing/shapebase/shapetype/) معGroup أو عن طريق إرساله إلى إحدى الفئات المشتقة: [`Shape`](../../../aspose.words.drawing/shape/) أو[`GroupShape`](../../../aspose.words.drawing/groupshape/).

يستخدم Aspose.Words اسم ملف المستند ورقمًا فريدًا لإنشاء اسم ملف فريد لكل صورة موجودة في المستند. يمكنك استخدام`CurrentShape`خاصية لإنشاء اسم ملف "أفضل" لـ من خلال فحص خصائص الشكل مثل[`Title`](../../../aspose.words.drawing/imagedata/title/) (الشكل فقط)،[`SourceFullName`](../../../aspose.words.drawing/imagedata/sourcefullname/) (الشكل فقط) و[`Name`](../../../aspose.words.drawing/shapebase/name/)بالطبع يمكنك إنشاء أسماء الملفات باستخدام أي خصائص أو معايير أخرى ولكن لاحظ أن أسماء الملفات الفرعية يجب أن تكون فريدة ضمن عملية التصدير.

قد لا تتوفر بعض الصور في المستند. للتحقق من توفر الصور، استخدم [`IsImageAvailable`](../isimageavailable/) ملكية.

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

* class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* class [ImageSavingArgs](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
