---
title: MarkdownSaveOptions.ImageSavingCallback
second_title: Aspose.Words for .NET API 参考
description: MarkdownSaveOptions 财产. 允许控制将文档保存到 时图像的保存方式Markdown格式.
type: docs
weight: 30
url: /zh/net/aspose.words.saving/markdownsaveoptions/imagesavingcallback/
---
## MarkdownSaveOptions.ImageSavingCallback property

允许控制将文档保存到 时图像的保存方式Markdown格式.

```csharp
public IImageSavingCallback ImageSavingCallback { get; set; }
```

### 例子

演示如何在保存到 Markdown 文档期间重命名图像名称。

```csharp
public void RenameImages()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();

    // 如果我们将包含图像的文档转换为 Markdown，我们最终会得到一个链接到多个图像的 Markdown 文件。
    // 每个图像将以文件的形式存在于本地文件系统中。
    // 还有一个回调可以自定义每个图像的名称和文件系统位置。
    saveOptions.ImageSavingCallback = new SavedImageRename("MarkdownSaveOptions.HandleDocument.md");

    // 我们回调的 ImageSaving() 方法将在此时运行。
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
/// 重命名保存 Markdown 文档时生成的保存图像。
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

### 也可以看看

* interface [IImageSavingCallback](../../iimagesavingcallback/)
* class [MarkdownSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../markdownsaveoptions/)
* 部件 [Aspose.Words](../../../)


