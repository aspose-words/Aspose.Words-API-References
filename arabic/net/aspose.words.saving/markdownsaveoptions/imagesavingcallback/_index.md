---
title: MarkdownSaveOptions.ImageSavingCallback
linktitle: ImageSavingCallback
articleTitle: ImageSavingCallback
second_title: Aspose.Words لـ .NET
description: تحكّم في حفظ الصور بتنسيق Markdown باستخدام ImageSavingCallback من MarkdownSaveOptions. حسّن تنسيق مستنداتك وسهّل سير عملك!
type: docs
weight: 70
url: /ar/net/aspose.words.saving/markdownsaveoptions/imagesavingcallback/
---
## MarkdownSaveOptions.ImageSavingCallback property

يسمح بالتحكم في كيفية حفظ الصور عند حفظ مستند في Markdown تنسيق.

```csharp
public IImageSavingCallback ImageSavingCallback { get; set; }
```

## أمثلة

يوضح كيفية إعادة تسمية الصورة أثناء الحفظ في مستند Markdown.

```csharp
public void RenameImages()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
    // إذا قمنا بتحويل مستند يحتوي على صور إلى Markdown، فسنحصل في النهاية على ملف Markdown واحد يرتبط بالعديد من الصور.
    //ستكون كل صورة في شكل ملف في نظام الملفات المحلي.
    // هناك أيضًا معاودة اتصال يمكنها تخصيص اسم وموقع نظام الملفات لكل صورة.
    saveOptions.ImageSavingCallback = new SavedImageRename("MarkdownSaveOptions.HandleDocument.md");
    saveOptions.SaveFormat = SaveFormat.Markdown;

    // سيتم تشغيل طريقة ImageSaving() الخاصة بإرجاع الاتصال لدينا في هذا الوقت.
    doc.Save(ArtifactsDir + "MarkdownSaveOptions.HandleDocument.md", saveOptions);

    Assert.AreEqual(1,
        Directory.GetFiles(ArtifactsDir)
            .Where(s => s.StartsWith(ArtifactsDir + "MarkdownSaveOptions.HandleDocument.md shape"))
            .Count(f => f.EndsWith(".jpeg")));
    Assert.AreEqual(8,
        Directory.GetFiles(ArtifactsDir)
            .Where(s => s.StartsWith(ArtifactsDir + "MarkdownSaveOptions.HandleDocument.md shape"))
            .Count(f => f.EndsWith(".png")));
}

/// <summary>
/// إعادة تسمية الصور المحفوظة التي تم إنتاجها عند حفظ مستند Markdown.
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

        args.ImageFileName = imageFileName;
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

* interface [IImageSavingCallback](../../iimagesavingcallback/)
* class [MarkdownSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
