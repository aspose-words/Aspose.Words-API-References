---
title: DocumentPartSavingArgs.DocumentPartFileName
linktitle: DocumentPartFileName
articleTitle: DocumentPartFileName
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية DocumentPartFileName لـ DocumentPartSavingArgs. أدر أسماء الملفات بسهولة لحفظ أجزاء المستند بسلاسة دون مسارات.
type: docs
weight: 20
url: /ar/net/aspose.words.saving/documentpartsavingargs/documentpartfilename/
---
## DocumentPartSavingArgs.DocumentPartFileName property

يحصل على اسم الملف (بدون مسار) الذي سيتم حفظ جزء المستند فيه أو يعينه.

```csharp
public string DocumentPartFileName { get; set; }
```

## ملاحظات

تتيح لك هذه الخاصية إعادة تعريف كيفية إنشاء أسماء ملفات أجزاء المستند أثناء التصدير إلى HTML أو EPUB.

عند استدعاء دالة الاستدعاء، تحتوي هذه الخاصية على اسم الملف الذي تم إنشاؤه بواسطة Aspose.Words . يمكنك تغيير قيمة هذه الخاصية لحفظ جزء المستند في ملف مختلف. يُرجى ملاحظة أن اسم الملف لكل جزء يجب أن يكون فريدًا.

`DocumentPartFileName` يجب أن يحتوي على اسم الملف فقط دون المسار. يحدد Aspose.Words مسار الحفظ باستخدام اسم ملف المستند. إذا لم يُحدد اسم ملف المستند الناتج ، على سبيل المثال عند الحفظ في مسار، فسيتم استخدام اسم الملف هذا فقط للإشارة إلى أجزاء المستند. وينطبق الأمر نفسه عند الحفظ بتنسيق EPUB.

## أمثلة

يوضح كيفية تقسيم المستند إلى أجزاء وحفظها.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // قم بإنشاء كائن "HtmlFixedSaveOptions"، والذي يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
    // لتعديل كيفية تحويل المستند إلى HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // إذا قمنا بحفظ المستند بشكل طبيعي، فسيكون هناك إخراج HTML واحد
    // مستند يحتوي على كافة محتويات المستند المصدر.
    // اضبط خاصية "DocumentSplitCriteria" إلى "DocumentSplitCriteria.SectionBreak" إلى
    // احفظ مستندنا في ملفات HTML متعددة: ملف واحد لكل قسم.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // قم بتعيين معاودة اتصال مخصصة لخاصية "DocumentPartSavingCallback" لتغيير منطق حفظ جزء المستند.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // إذا قمنا بتحويل مستند يحتوي على صور إلى html، فسنحصل في النهاية على ملف html واحد يرتبط بالعديد من الصور.
    //ستكون كل صورة في شكل ملف في نظام الملفات المحلي.
    // هناك أيضًا معاودة اتصال يمكنها تخصيص اسم وموقع نظام الملفات لكل صورة.
    options.ImageSavingCallback = new SavedImageRename(outFileName);

    doc.Save(ArtifactsDir + outFileName, options);
}

/// <summary>
/// تعيين أسماء ملفات مخصصة لمستندات الإخراج التي تقوم عملية الحفظ بتقسيم المستند إليها.
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
        //يمكننا الوصول إلى المستند المصدر بأكمله عبر خاصية "المستند".
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
        // 1 - تعيين اسم ملف لملف جزء الإخراج:
        args.DocumentPartFileName = partFileName;

        // 2 - إنشاء تدفق مخصص لملف جزء الإخراج:
        args.DocumentPartStream = new FileStream(ArtifactsDir + partFileName, FileMode.Create);

        Assert.True(args.DocumentPartStream.CanWrite);
        Assert.False(args.KeepDocumentPartStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
    private readonly DocumentSplitCriteria mDocumentSplitCriteria;
}

/// <summary>
/// تعيين أسماء ملفات مخصصة لملفات الصور التي ينشئها تحويل HTML.
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
        // 1 - تعيين اسم ملف لملف الصورة الناتجة:
        args.ImageFileName = imageFileName;

        // 2 - إنشاء تدفق مخصص لملف الصورة الناتج:
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

* class [DocumentPartSavingArgs](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
