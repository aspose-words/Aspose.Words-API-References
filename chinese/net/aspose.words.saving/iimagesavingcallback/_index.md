---
title: IImageSavingCallback
second_title: Aspose.Words for .NET API 参考
description: 如果您想控制 Aspose.Words 在 将文档保存为 HTML 时如何保存图像请实现此接口可能被其他格式使用
type: docs
weight: 4910
url: /zh/net/aspose.words.saving/iimagesavingcallback/
---
## IImageSavingCallback interface

如果您想控制 Aspose.Words 在 将文档保存为 HTML 时如何保存图像，请实现此接口。可能被其他格式使用。

```csharp
public interface IImageSavingCallback
```

## 方法

| 姓名 | 描述 |
| --- | --- |
| [ImageSaving](../../aspose.words.saving/iimagesavingcallback/imagesaving)(ImageSavingArgs) | 当 Aspose.Words 将图像保存到 HTML 时调用。 |

### 例子

显示如何在保存到 Markdown 文档期间重命名图像名称。

```csharp
{
    Document doc = new Document(MyDir + "Rendering.docx");

    MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();

    // 如果我们将包含图像的文档转换为 Markdown，我们最终会得到一个链接到多个图像的 Markdown 文件。
    // 每个图像都会在本地文件系统中以文件的形式存在。
    // 还有一个回调可以自定义每张图片的名称和文件系统位置。
    saveOptions.ImageSavingCallback = new SavedImageRename("MarkdownSaveOptions.HandleDocument.md");

    // 我们回调的 ImageSaving() 方法会在这个时候运行。
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

显示如何将文档拆分为多个部分并保存它们。

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // 创建一个“HtmlFixedSaveOptions”对象，我们可以将它传递给文档的“Save”方法
    // 修改我们如何将文档转换为 HTML。
    HtmlSaveOptions options = new HtmlSaveOptions();

    // 如果我们正常保存文档，就会有一个输出HTML
    // 包含所有源文档内容的文档。
    // 将“DocumentSplitCriteria”属性设置为“DocumentSplitCriteria.SectionBreak”以
    // 将我们的文档保存到多个 HTML 文件中：每个部分一个。
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // 将自定义回调分配给“DocumentPartSavingCallback”属性以更改文档部分保存逻辑。
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // 如果我们将包含图像的文档转换为 html，我们最终会得到一个链接到多个图像的 html 文件。
    // 每个图像都会在本地文件系统中以文件的形式存在。
    // 还有一个回调可以自定义每张图片的名称和文件系统位置。
    options.ImageSavingCallback = new SavedImageRename(outFileName);

    doc.Save(ArtifactsDir + outFileName, options);
}

/// <summary>
/// 为保存操作将文档拆分成的输出文档设置自定义文件名。
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
        // 我们可以通过“Document”属性访问整个源文档。
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

        // 下面是指定 Aspose.Words 将文档的每个部分保存在哪里的两种方法。
        // 1 - 为输出部分文件设置文件名：
        args.DocumentPartFileName = partFileName;

        // 2 - 为输出部分文件创建自定义流：
        args.DocumentPartStream = new FileStream(ArtifactsDir + partFileName, FileMode.Create);

        Assert.True(args.DocumentPartStream.CanWrite);
        Assert.False(args.KeepDocumentPartStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
    private readonly DocumentSplitCriteria mDocumentSplitCriteria;
}

/// <summary>
/// 为 HTML 转换创建的图像文件设置自定义文件名。
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

        // 下面是指定 Aspose.Words 将文档的每个部分保存在哪里的两种方法。
        // 1 - 设置输出图像文件的文件名：
        args.ImageFileName = imageFileName;

        // 2 - 为输出图像文件创建自定义流：
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

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving)
* 部件 [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
