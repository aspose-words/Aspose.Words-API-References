---
title: ImageSavingArgs Class
linktitle: ImageSavingArgs
articleTitle: ImageSavingArgs
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Saving.ImageSavingArgs فصل. يوفر بيانات لـImageSaving حدث في C#.
type: docs
weight: 5240
url: /ar/net/aspose.words.saving/imagesavingargs/
---
## ImageSavingArgs class

يوفر بيانات لـ[`ImageSaving`](../iimagesavingcallback/imagesaving/) حدث.

لمعرفة المزيد، قم بزيارة[حفظ مستند](https://docs.aspose.com/words/net/save-a-document/) مقالة توثيقية.

```csharp
public class ImageSavingArgs
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [CurrentShape](../../aspose.words.saving/imagesavingargs/currentshape/) { get; } | يحصل على[`ShapeBase`](../../aspose.words.drawing/shapebase/) الكائن المطابق للشكل أو شكل المجموعة الذي على وشك أن يتم حفظه. |
| [Document](../../aspose.words.saving/imagesavingargs/document/) { get; } | الحصول على كائن المستند الذي يتم حفظه حاليًا. |
| [ImageFileName](../../aspose.words.saving/imagesavingargs/imagefilename/) { get; set; } | الحصول على أو تعيين اسم الملف (بدون مسار) حيث سيتم حفظ الصورة. |
| [ImageStream](../../aspose.words.saving/imagesavingargs/imagestream/) { get; set; } | يسمح بتحديد الدفق الذي سيتم حفظ الصورة فيه. |
| [IsImageAvailable](../../aspose.words.saving/imagesavingargs/isimageavailable/) { get; } | إرجاع`حقيقي` إذا كانت الصورة الحالية متاحة للتصدير. |
| [KeepImageStreamOpen](../../aspose.words.saving/imagesavingargs/keepimagestreamopen/) { get; set; } | يحدد ما إذا كان يجب على Aspose.Words إبقاء الدفق مفتوحًا أو إغلاقه بعد حفظ الصورة. |

## ملاحظات

افتراضيًا، عندما يقوم Aspose.Words بحفظ مستند بتنسيق HTML، فإنه يحفظ كل صورة في ملف منفصل. يستخدم Aspose.Words اسم ملف المستند ورقمًا فريدًا لإنشاء ملف name فريد لكل صورة موجودة في المستند.

`ImageSavingArgs`يسمح بإعادة تعريف كيفية إنشاء أسماء ملفات الصور أو للتحايل تمامًا على حفظ الصور في الملفات عن طريق توفير كائنات الدفق الخاصة بك.

لتطبيق المنطق الخاص بك لإنشاء أسماء ملفات الصور، استخدم [`ImageFileName`](./imagefilename/) ,[`CurrentShape`](./currentshape/) و[`IsImageAvailable`](./isimageavailable/) خصائص .

لحفظ الصور في التدفقات بدلاً من الملفات، استخدم الملف[`ImageStream`](./imagestream/) ملكية.

## أمثلة

يوضح كيفية تقسيم مستند إلى أجزاء وحفظها.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // قم بإنشاء كائن "HtmlFixedSaveOptions"، والذي يمكننا تمريره إلى طريقة "حفظ" المستند
    // لتعديل كيفية تحويل المستند إلى HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // إذا قمنا بحفظ المستند بشكل طبيعي، فسيكون هناك مخرج HTML واحد
    // مستند يحتوي على جميع محتويات المستند المصدر.
    // قم بتعيين خاصية "DocumentSplitCriteria" على "DocumentSplitCriteria.SectionBreak" إلى
    // احفظ وثيقتنا في ملفات HTML متعددة: ملف واحد لكل قسم.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // قم بتعيين رد اتصال مخصص للخاصية "DocumentPartSavingCallback" لتغيير منطق حفظ جزء المستند.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // إذا قمنا بتحويل مستند يحتوي على صور إلى html، فسوف نحصل في النهاية على ملف html واحد يرتبط بعدة صور.
    // ستكون كل صورة على شكل ملف في نظام الملفات المحلي.
    // يوجد أيضًا رد اتصال يمكنه تخصيص الاسم وموقع نظام الملفات لكل صورة.
    options.ImageSavingCallback = new SavedImageRename(outFileName);

    doc.Save(ArtifactsDir + outFileName, options);
}

/// <summary>
/// يعين أسماء ملفات مخصصة لمستندات الإخراج التي تقوم عملية الحفظ بتقسيم المستند إليها.
/// </summary>
private class SavedDocumentPartRename : IDocumentPartSavingCallback
{
    public SavedDocumentPartRename(string outFileName, DocumentSplitCriteria documentSplitCriteria)
    {
        mOutFileName = outFileName;
        mDocumentSplitCriteria = documentSplitCriteria;
    }

    void IDocumentPartSavingCallback.DocumentPartSaving(DocumentPartSavingArgs args)
    {
        // يمكننا الوصول إلى المستند المصدر بأكمله عبر خاصية "المستند".
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        string partType = string.Empty;

        switch (mDocumentSplitCriteria)
        {
            case DocumentSplitCriteria.PageBreak:
                partType = "Page";
                break;
            case DocumentSplitCriteria.ColumnBreak:
                partType = "Column";
                break;
            case DocumentSplitCriteria.SectionBreak:
                partType = "Section";
                break;
            case DocumentSplitCriteria.HeadingParagraph:
                partType = "Paragraph from heading";
                break;
        }

        string partFileName = $"{mOutFileName} part {++mCount}, of type {partType}{Path.GetExtension(args.DocumentPartFileName)}";

        // فيما يلي طريقتان لتحديد المكان الذي سيحفظ فيه Aspose.Words كل جزء من المستند.
        // 1 - قم بتعيين اسم ملف لملف جزء الإخراج:
        args.DocumentPartFileName = partFileName;

        // 2 - إنشاء دفق مخصص لملف جزء الإخراج:
        args.DocumentPartStream = new FileStream(ArtifactsDir + partFileName, FileMode.Create);

        Assert.True(args.DocumentPartStream.CanWrite);
        Assert.False(args.KeepDocumentPartStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
    private readonly DocumentSplitCriteria mDocumentSplitCriteria;
}

/// <summary>
/// يعين أسماء ملفات مخصصة لملفات الصور التي ينشئها تحويل HTML.
/// </summary>
public class SavedImageRename : IImageSavingCallback
{
    public SavedImageRename(string outFileName)
    {
        mOutFileName = outFileName;
    }

    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        string imageFileName = $"{mOutFileName} shape {++mCount}, of type {args.CurrentShape.ShapeType}{Path.GetExtension(args.ImageFileName)}";

        // فيما يلي طريقتان لتحديد المكان الذي سيحفظ فيه Aspose.Words كل جزء من المستند.
        // 1 - قم بتعيين اسم ملف لملف الصورة الناتج:
        args.ImageFileName = imageFileName;

        // 2 - إنشاء دفق مخصص لملف الصورة الناتج:
        args.ImageStream = new FileStream(ArtifactsDir + imageFileName, FileMode.Create);

        Assert.True(args.ImageStream.CanWrite);
        Assert.True(args.IsImageAvailable);
        Assert.False(args.KeepImageStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
