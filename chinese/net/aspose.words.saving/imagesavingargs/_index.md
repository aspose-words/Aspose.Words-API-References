---
title: ImageSavingArgs Class
linktitle: ImageSavingArgs
articleTitle: ImageSavingArgs
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.ImageSavingArgs 类，通过可自定义的图像保存选项增强文档处理，以获得最佳性能。
type: docs
weight: 5990
url: /zh/net/aspose.words.saving/imagesavingargs/
---
## ImageSavingArgs class

为[`ImageSaving`](../iimagesavingcallback/imagesaving/)事件.

要了解更多信息，请访问[保存文档](https://docs.aspose.com/words/net/save-a-document/)文档文章。

```csharp
public class ImageSavingArgs
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [CurrentShape](../../aspose.words.saving/imagesavingargs/currentshape/) { get; } | 获取[`ShapeBase`](../../aspose.words.drawing/shapebase/)与即将保存的形状或组形状 对应的对象。 |
| [Document](../../aspose.words.saving/imagesavingargs/document/) { get; } | 获取当前正在保存的文档对象。 |
| [ImageFileName](../../aspose.words.saving/imagesavingargs/imagefilename/) { get; set; } | 获取或设置将保存图像的文件名（不带路径）。 |
| [ImageStream](../../aspose.words.saving/imagesavingargs/imagestream/) { get; set; } | 允许指定将图像保存到的流。 |
| [IsImageAvailable](../../aspose.words.saving/imagesavingargs/isimageavailable/) { get; } | 返回`真的`如果当前图像可供导出。 |
| [KeepImageStreamOpen](../../aspose.words.saving/imagesavingargs/keepimagestreamopen/) { get; set; } | 指定 Aspose.Words 是否应保持流打开或保存图像后关闭它。 |

## 评论

默认情况下，当 Aspose.Words 将文档保存为 HTML 格式时，它会将每张图片保存到名为 的单独文件中。Aspose.Words 使用文档文件名和一个唯一的编号，为文档中找到的每张图片生成唯一的文件名 。

`ImageSavingArgs`允许重新定义如何生成图像文件名，或者通过提供您自己的流对象来完全绕过将图像保存到文件中。

要应用您自己的逻辑来生成图像文件名，请使用 [`ImageFileName`](./imagefilename/)，[`CurrentShape`](./currentshape/)和[`IsImageAvailable`](./isimageavailable/) 属性。

要将图像保存到流而不是文件中，请使用[`ImageStream`](./imagestream/)财产。

## 例子

展示如何将文档拆分成多个部分并保存它们。

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // 创建一个“HtmlFixedSaveOptions”对象，我们可以将其传递给文档的“Save”方法
    // 修改我们将文档转换为 HTML 的方式。
    HtmlSaveOptions options = new HtmlSaveOptions();

    // 如果我们正常保存文档，将会有一个输出 HTML
    // 包含源文档的所有内容的文档。
    // 将“DocumentSplitCriteria”属性设置为“DocumentSplitCriteria.SectionBreak”
    // 将我们的文档保存到多个 HTML 文件中：每个部分一个。
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // 将自定义回调分配给“DocumentPartSavingCallback”属性以改变文档部分保存逻辑。
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // 如果我们将包含图像的文档转换为 html，我们最终会得到一个链接到多个图像的 html 文件。
    // 每个图像都将以文件的形式存储在本地文件系统中。
    // 还有一个回调可以自定义每个图像的名称和文件系统位置。
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

        // 以下是两种指定 Aspose.Words 保存文档各个部分的位置的方法。
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

        // 以下是两种指定 Aspose.Words 保存文档各个部分的位置的方法。
        // 1 - 为输出图像文件设置文件名：
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

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
