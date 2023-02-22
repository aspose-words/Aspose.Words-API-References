---
title: DocumentPartSavingArgs.DocumentPartFileName
second_title: Aspose.Words for .NET API 参考
description: DocumentPartSavingArgs 财产. 获取或设置文档部分将保存到的文件名不带路径
type: docs
weight: 20
url: /zh/net/aspose.words.saving/documentpartsavingargs/documentpartfilename/
---
## DocumentPartSavingArgs.DocumentPartFileName property

获取或设置文档部分将保存到的文件名（不带路径）。

```csharp
public string DocumentPartFileName { get; set; }
```

### 评论

此属性允许您重新定义在导出到 HTML 或 EPUB 期间如何生成文档部件文件名 。

调用回调时，此属性包含由 Aspose.Words 生成的 文件名。您可以更改此属性的值以将文档部分保存到 不同的文件中。请注意，每个部分的文件名必须是唯一的。

`DocumentPartFileName`必须只包含文件名而不包含路径。 Aspose.Words 使用文档文件名确定保存路径。如果未指定输出文档 文件名，例如保存到流时，此文件名仅用于引用文档部分的 。保存为 EPUB 格式时也是如此。

### 例子

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

* class [DocumentPartSavingArgs](../)
* 命名空间 [Aspose.Words.Saving](../../documentpartsavingargs/)
* 部件 [Aspose.Words](../../../)


