---
title: ImageSavingArgs
second_title: Aspose.Words لمراجع .NET API
description: توفير بيانات لملفImageSaving./iimagesavingcallback/imagesaving الحدث ._ x000d_
type: docs
weight: 4980
url: /ar/net/aspose.words.saving/imagesavingargs/
---
## ImageSavingArgs class

توفير بيانات لملف[`ImageSaving`](../iimagesavingcallback/imagesaving) الحدث ._ x000d_

```csharp
public class ImageSavingArgs
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [CurrentShape](../../aspose.words.saving/imagesavingargs/currentshape) { get; } | يحصل على ملف[`ShapeBase`](../../aspose.words.drawing/shapebase) كائن مطابق للشكل أو شكل المجموعة الذي على وشك حفظه . |
| [Document](../../aspose.words.saving/imagesavingargs/document) { get; } | الحصول على كائن المستند الذي يتم حفظه حاليًا. |
| [ImageFileName](../../aspose.words.saving/imagesavingargs/imagefilename) { get; set; } | الحصول على أو تحديد اسم الملف (بدون مسار) حيث سيتم حفظ الصورة فيه. |
| [ImageStream](../../aspose.words.saving/imagesavingargs/imagestream) { get; set; } | يسمح بتحديد التدفق حيث سيتم حفظ الصورة فيه. |
| [IsImageAvailable](../../aspose.words.saving/imagesavingargs/isimageavailable) { get; } | عوائد`حقيقي` إذا كانت الصورة الحالية متاحة للتصدير. |
| [KeepImageStreamOpen](../../aspose.words.saving/imagesavingargs/keepimagestreamopen) { get; set; } | يحدد ما إذا كان يجب على Aspose.Words إبقاء الدفق مفتوحًا أو إغلاقه بعد حفظ الصورة. |

### ملاحظات

بشكل افتراضي ، عندما يحفظ Aspose.Words مستند إلى HTML ، فإنه يحفظ كل صورة في ملف منفصل. يستخدم Aspose.Words اسم ملف المستند ورقمًا فريدًا لإنشاء اسم ملف فريد_ x000d_ لكل صورة موجودة في المستند.

[`ImageSavingArgs`](../imagesavingargs) يسمح بإعادة تعريف كيفية إنشاء أسماء ملفات الصور أو التحايل تمامًا على حفظ الصور في ملفات من خلال توفير كائنات البث الخاصة بك.

لتطبيق منطقك الخاص لتوليد أسماء ملفات الصور ، استخدم [`ImageFileName`](./imagefilename) و[`CurrentShape`](./currentshape) و[`IsImageAvailable`](./isimageavailable) الخصائص.

لحفظ الصور في التدفقات بدلاً من الملفات ، استخدم ملحق[`ImageStream`](./imagestream) منشأه.

### أمثلة

يوضح كيفية تقسيم مستند إلى أجزاء وحفظها.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // قم بإنشاء كائن "HtmlFixedSaveOptions" ، والذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
    // لتعديل كيفية تحويل المستند إلى HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // إذا حفظنا المستند بشكل طبيعي ، فسيكون هناك ناتج HTML واحد
    // مستند بجميع محتويات المستند المصدر.
    // تعيين خاصية "DocumentSplitCriteria" إلى "DocumentSplitCriteria.SectionBreak" إلى
    // احفظ وثيقتنا في عدة ملفات HTML: واحد لكل قسم.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // تعيين رد اتصال مخصص لخاصية "DocumentPartSavingCallback" لتغيير منطق حفظ جزء المستند.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // إذا قمنا بتحويل مستند يحتوي على صور إلى html ، فسننتهي بملف html واحد يرتبط بعدة صور.
    // ستكون كل صورة في شكل ملف في نظام الملفات المحلي.
    // يوجد أيضًا رد اتصال يمكنه تخصيص اسم وموقع نظام الملفات لكل صورة.
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
        // يمكننا الوصول إلى المستند المصدر بالكامل عبر خاصية "المستند".
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

        // فيما يلي طريقتان لتحديد مكان حفظ Aspose.Words كل جزء من المستند.
        // 1 - حدد اسم ملف لملف جزء الإخراج:
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

        // فيما يلي طريقتان لتحديد مكان حفظ Aspose.Words كل جزء من المستند.
        // 1 - حدد اسم ملف لملف الصورة الناتج:
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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
