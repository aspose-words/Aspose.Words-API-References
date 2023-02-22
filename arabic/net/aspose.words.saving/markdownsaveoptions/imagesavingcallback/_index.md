---
title: MarkdownSaveOptions.ImageSavingCallback
second_title: Aspose.Words لمراجع .NET API
description: MarkdownSaveOptions ملكية. يسمح بالتحكم في كيفية حفظ الصور عند حفظ المستند في Markdown التنسيق .
type: docs
weight: 30
url: /ar/net/aspose.words.saving/markdownsaveoptions/imagesavingcallback/
---
## MarkdownSaveOptions.ImageSavingCallback property

يسمح بالتحكم في كيفية حفظ الصور عند حفظ المستند في Markdown التنسيق .

```csharp
public IImageSavingCallback ImageSavingCallback { get; set; }
```

### أمثلة

يوضح كيفية إعادة تسمية اسم الصورة أثناء الحفظ في مستند Markdown.

```csharp
{
    Document doc = new Document(MyDir + "Rendering.docx");

    MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();

    // إذا قمنا بتحويل مستند يحتوي على صور إلى Markdown ، فسننتهي بملف Markdown واحد يرتبط بعدة صور.
    // ستكون كل صورة في شكل ملف في نظام الملفات المحلي.
    // يوجد أيضًا رد اتصال يمكنه تخصيص اسم وموقع نظام الملفات لكل صورة.
    saveOptions.ImageSavingCallback = new SavedImageRename("MarkdownSaveOptions.HandleDocument.md");

    // سيتم تشغيل طريقة ImageSaving () لرد الاتصال لدينا في هذا الوقت.
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
/// يعيد تسمية الصور المحفوظة التي تم إنتاجها عند حفظ مستند Markdown.
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
* مساحة الاسم [Aspose.Words.Saving](../../markdownsaveoptions/)
* المجسم [Aspose.Words](../../../)


