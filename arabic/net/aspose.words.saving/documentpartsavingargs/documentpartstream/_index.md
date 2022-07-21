---
title: DocumentPartStream
second_title: Aspose.Words لمراجع .NET API
description: يسمح بتحديد التدفق حيث سيتم حفظ جزء المستند فيه.
type: docs
weight: 30
url: /ar/net/aspose.words.saving/documentpartsavingargs/documentpartstream/
---
## DocumentPartSavingArgs.DocumentPartStream property

يسمح بتحديد التدفق حيث سيتم حفظ جزء المستند فيه.

```csharp
public Stream DocumentPartStream { get; set; }
```

### ملاحظات

تتيح لك هذه الخاصية حفظ أجزاء المستند في التدفقات بدلاً من الملفات أثناء تصدير HTML.

النظام الأساسي`لا شيء` . عندما تكون هذه الخاصية`لا شيء` ، سيتم حفظ جزء المستند في ملف محدد في[`DocumentPartFileName`](../documentpartfilename) منشأه.

عند الحفظ إلى دفق بتنسيق HTML يطلبه[`Save`](../../../aspose.words/document/save) أو[`Save`](../../../aspose.words/document/save) وجزء المستند الأول على وشك الحفظ ، Aspose.Words يقترح هنا تيار الإخراج الرئيسي الذي مر به المتصل في البداية.

عند الحفظ بتنسيق EPUB وهو تنسيق حاوية يستند إلى HTML ،`DocumentPartStream` لا يمكن تحديد لأنه سيتم تغليف جميع الأجزاء الفرعية في حزمة إخراج واحدة.

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

* class [DocumentPartSavingArgs](../../documentpartsavingargs)
* مساحة الاسم [Aspose.Words.Saving](../../documentpartsavingargs)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
