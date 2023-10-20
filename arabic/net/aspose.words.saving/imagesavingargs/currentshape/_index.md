---
title: ImageSavingArgs.CurrentShape
linktitle: CurrentShape
articleTitle: CurrentShape
second_title: Aspose.Words لـ .NET
description: ImageSavingArgs CurrentShape ملكية. يحصل علىShapeBase الكائن المطابق للشكل أو شكل المجموعة الذي على وشك أن يتم حفظه في C#.
type: docs
weight: 10
url: /ar/net/aspose.words.saving/imagesavingargs/currentshape/
---
## ImageSavingArgs.CurrentShape property

يحصل على[`ShapeBase`](../../../aspose.words.drawing/shapebase/) الكائن المطابق للشكل أو شكل المجموعة الذي على وشك أن يتم حفظه.

```csharp
public ShapeBase CurrentShape { get; }
```

## ملاحظات

[`IImageSavingCallback`](../../iimagesavingcallback/) يمكن إطلاقها مع حفظ شكل أو شكل مجموعة. لهذا السبب الملكية[`ShapeBase`](../../../aspose.words.drawing/shapebase/) يكتب. يمكنك التحقق مما إذا كان شكل مجموعة يقارن [`ShapeType`](../../../aspose.words.drawing/shapebase/shapetype/) معGroup أو عن طريق إرسالها إلى أحد الفئات المشتقة: [`Shape`](../../../aspose.words.drawing/shape/) أو[`GroupShape`](../../../aspose.words.drawing/groupshape/).

يستخدم Aspose.Words اسم ملف المستند ورقمًا فريدًا لإنشاء اسم ملف فريد لكل صورة موجودة في المستند. يمكنك استخدام ال`CurrentShape`الخاصية لإنشاء اسم ملف "أفضل" عن طريق فحص خصائص الشكل مثل[`Title`](../../../aspose.words.drawing/imagedata/title/) (الشكل فقط)،[`SourceFullName`](../../../aspose.words.drawing/imagedata/sourcefullname/) (الشكل فقط) و[`Name`](../../../aspose.words.drawing/shapebase/name/). بالطبع يمكنك إنشاء أسماء الملفات باستخدام أي خصائص أو معايير أخرى ولكن لاحظ أن أسماء الملفات الفرعية يجب أن تكون فريدة ضمن عملية التصدير.

قد تكون بعض الصور في المستند غير متوفرة. للتحقق من توفر الصورة استخدم[`IsImageAvailable`](../isimageavailable/) ملكية.

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

* class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* class [ImageSavingArgs](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
