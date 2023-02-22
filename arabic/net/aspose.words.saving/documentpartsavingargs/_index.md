---
title: Class DocumentPartSavingArgs
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Saving.DocumentPartSavingArgs فصل. توفير بيانات لملفDocumentPartSaving رد الاتصال .
type: docs
weight: 4680
url: /ar/net/aspose.words.saving/documentpartsavingargs/
---
## DocumentPartSavingArgs class

توفير بيانات لملف[`DocumentPartSaving`](../idocumentpartsavingcallback/documentpartsaving/) رد الاتصال .

```csharp
public class DocumentPartSavingArgs
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Document](../../aspose.words.saving/documentpartsavingargs/document/) { get; } | يحصل على كائن المستند الذي يتم حفظه . |
| [DocumentPartFileName](../../aspose.words.saving/documentpartsavingargs/documentpartfilename/) { get; set; } | الحصول على أو تحديد اسم الملف (بدون مسار) حيث سيتم حفظ جزء المستند فيه. |
| [DocumentPartStream](../../aspose.words.saving/documentpartsavingargs/documentpartstream/) { get; set; } | يسمح بتحديد التدفق حيث سيتم حفظ جزء المستند فيه. |
| [KeepDocumentPartStreamOpen](../../aspose.words.saving/documentpartsavingargs/keepdocumentpartstreamopen/) { get; set; } | يحدد ما إذا كان يجب على Aspose.Words إبقاء الدفق مفتوحًا أو إغلاقه بعد حفظ جزء من المستند. |

### ملاحظات

عندما يحفظ Aspose.Words مستندًا بتنسيق HTML أو تنسيقات ذات صلة وملفات[`DocumentSplitCriteria`](../htmlsaveoptions/documentsplitcriteria/)تم تحديد ، ويتم تقسيم المستند إلى أجزاء وبشكل افتراضي ، يتم حفظ كل جزء من أجزاء المستند في ملف منفصل.

فصل`DocumentPartSavingArgs` يسمح لك بالتحكم في كيفية حفظ كل جزء من المستند. يسمح بإعادة تعريف كيفية إنشاء أسماء الملفات أو التحايل تمامًا على حفظ أجزاء المستند في ملفات من خلال توفير كائنات البث الخاصة بك.

لحفظ أجزاء المستند في تدفقات بدلاً من الملفات ، استخدم ملحق[`DocumentPartStream`](./documentpartstream/) منشأه.

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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)


