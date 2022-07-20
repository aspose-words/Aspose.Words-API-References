---
title: ImageFileName
second_title: Aspose.Words لمراجع .NET API
description: الحصول على أو تحديد اسم الملف بدون مسار حيث سيتم حفظ الصورة فيه.
type: docs
weight: 30
url: /ar/net/aspose.words.saving/imagesavingargs/imagefilename/
---
## ImageSavingArgs.ImageFileName property

الحصول على أو تحديد اسم الملف (بدون مسار) حيث سيتم حفظ الصورة فيه.

```csharp
public string ImageFileName { get; set; }
```

### ملاحظات

تتيح لك هذه الخاصية إعادة تعريف كيفية إنشاء أسماء ملفات الصور_ x000d_ أثناء التصدير إلى HTML.

عند إطلاق الحدث ، تحتوي هذه الخاصية على اسم الملف الذي تم إنشاؤه بواسطة Aspose.Words . يمكنك تغيير قيمة هذه الخاصية لحفظ الصورة في ملف مختلف . لاحظ أن أسماء الملفات يجب أن تكون فريدة.

تقوم Aspose.Words تلقائيًا بإنشاء اسم ملف فريد لكل صورة مضمنة عند تصدير إلى تنسيق HTML. تعتمد كيفية إنشاء اسم ملف الصورة على ما إذا كنت ستحفظ المستند إلى ملف أو إلى دفق.

عند حفظ مستند إلى ملف ، يبدو اسم ملف الصورة الذي تم إنشاؤه مثل &lt;اسم الملف الأساسي للمستند&gt;. &lt;رقم الصورة&gt;. &lt;امتداد&gt;.

عند حفظ مستند إلى دفق ، يبدو اسم ملف الصورة الذي تم إنشاؤه مثل Aspose.Words. &lt;document GU&gt;. &lt;image number&gt;. &lt;extension&gt;.

`ImageFileName` يجب أن يحتوي على اسم الملف فقط بدون المسار. Aspose. تحدد الكلمات مسار الحفظ وقيمة`src`السمة لكتابة إلى HTML باستخدام اسم ملف المستند ، و[`ImagesFolder`](../../htmlsaveoptions/imagesfolder) و_ x000d_[`ImagesFolderAlias`](../../htmlsaveoptions/imagesfolderalias) الخصائص.

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

* class [ImageSavingArgs](../../imagesavingargs)
* مساحة الاسم [Aspose.Words.Saving](../../imagesavingargs)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
