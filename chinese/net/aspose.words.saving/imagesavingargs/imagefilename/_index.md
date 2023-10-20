---
title: ImageSavingArgs.ImageFileName
linktitle: ImageFileName
articleTitle: ImageFileName
second_title: 用于 .NET 的 Aspose.Words
description: ImageSavingArgs ImageFileName 财产. 获取或设置图像将保存到的文件名不带路径 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words.saving/imagesavingargs/imagefilename/
---
## ImageSavingArgs.ImageFileName property

获取或设置图像将保存到的文件名（不带路径）。

```csharp
public string ImageFileName { get; set; }
```

## 评论

此属性允许您重新定义在导出到 HTML 期间如何生成图像文件名 。

当事件被触发时，该属性包含由 Aspose.Words 生成的文件名 。您可以更改此属性的值以将图像保存到 不同的文件中。请注意，文件名必须是唯一的。

当 导出为 HTML 格式时，Aspose.Words 会自动为每个嵌入图像生成唯一的文件名。图像文件名的生成方式 取决于您将文档保存到文件还是流。

将文档保存到文件时，生成的图像文件名类似于 &lt;文档基本文件名&gt;.&lt;图像编号&gt;.&lt;扩展名&gt;。

将文档保存到流时，生成的图像文件名类似于 Aspose.Words.&lt;文档指南&gt;.&lt;图像编号&gt;.&lt;扩展名&gt;。

`ImageFileName`必须仅包含文件名而不包含路径。 Aspose.Words 确定保存的路径和值`源代码`用于使用文档文件名将 写入 HTML 的属性，[`ImagesFolder`](../../htmlsaveoptions/imagesfolder/)和 [`ImagesFolderAlias`](../../htmlsaveoptions/imagesfolderalias/)特性。

## 例子

演示如何将文档拆分为多个部分并保存它们。

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // 创建一个“HtmlFixedSaveOptions”对象，我们可以将其传递给文档的“Save”方法
    // 修改我们将文档转换为 HTML 的方式。
    HtmlSaveOptions options = new HtmlSaveOptions();

    // 如果我们正常保存文档，将会有一个输出 HTML
    // 包含所有源文档内容的文档。
    // 将“DocumentSplitCriteria”属性设置为“DocumentSplitCriteria.SectionBreak”
    // 将我们的文档保存到多个 HTML 文件：每个部分一个。
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // 将自定义回调分配给“DocumentPartSavingCallback”属性以更改文档部分保存逻辑。
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // 如果我们将包含图像的文档转换为 html，我们最终会得到一个链接到多个图像的 html 文件。
    // 每个图像将以文件的形式存在于本地文件系统中。
    // 还有一个回调可以自定义每个图像的名称和文件系统位置。
    options.ImageSavingCallback = new SavedImageRename(outFileName);

    doc.Save(ArtifactsDir + outFileName, options);
}

/// <summary>
/// 设置保存操作将文档分割成的输出文档的自定义文件名。
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

        // 以下是指定 Aspose.Words 保存文档各部分的位置的两种方法。
        // 1 - 设置输出零件文件的文件名：
        args.DocumentPartFileName = partFileName;

        // 2 - 为输出零件文件创建自定义流：
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

        // 以下是指定 Aspose.Words 保存文档各部分的位置的两种方法。
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

* class [ImageSavingArgs](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
