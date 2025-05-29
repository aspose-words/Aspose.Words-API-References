---
title: MetafileRenderingOptions Class
linktitle: MetafileRenderingOptions
articleTitle: MetafileRenderingOptions
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Saving.MetafileRenderingOptions，增强文档中的图元文件渲染控制和自定义功能。立即优化您的工作流程！
type: docs
weight: 6080
url: /zh/net/aspose.words.saving/metafilerenderingoptions/
---
## MetafileRenderingOptions class

允许指定额外的图元文件渲染选项。

要了解更多信息，请访问[处理 Windows 图元文件](https://docs.aspose.com/words/net/handling-windows-metafiles/)文档文章。

```csharp
public class MetafileRenderingOptions
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [MetafileRenderingOptions](metafilerenderingoptions/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [EmfPlusDualRenderingMode](../../aspose.words.saving/metafilerenderingoptions/emfplusdualrenderingmode/) { get; set; } | 获取或设置一个值，确定如何呈现 EMF+ Dual 图元文件。 |
| [EmulateRasterOperations](../../aspose.words.saving/metafilerenderingoptions/emulaterasteroperations/) { get; set; } | 获取或设置一个值，确定是否应该模拟光栅操作。 |
| [EmulateRenderingToSizeOnPage](../../aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpage/) { get; set; } | 获取或设置一个值，该值确定图元文件渲染是否根据页面 上的大小模拟图元文件的显示，还是模拟图元文件的默认大小显示。 |
| [EmulateRenderingToSizeOnPageResolution](../../aspose.words.saving/metafilerenderingoptions/emulaterenderingtosizeonpageresolution/) { get; set; } | 获取或设置用于模拟图元文件渲染到页面大小的分辨率（以像素/英寸为单位）。 |
| [RenderingMode](../../aspose.words.saving/metafilerenderingoptions/renderingmode/) { get; set; } | 获取或设置一个值，确定如何呈现图元文件图像。 |
| [UseEmfEmbeddedToWmf](../../aspose.words.saving/metafilerenderingoptions/useemfembeddedtowmf/) { get; set; } | 获取或设置一个值，该值确定如何呈现嵌入 EMF 元文件的 WMF 元文件。 |
| [UseGdiRasterOperationsEmulation](../../aspose.words.saving/metafilerenderingoptions/usegdirasteroperationsemulation/) { get; set; } | 获取或设置一个值，确定是否使用 GDI+ 进行光栅操作模拟。 |

## 例子

显示添加了位图渲染的回退并更改了有关不受支持的元文件记录的警告类型。

```csharp
public void HandleBinaryRasterWarnings()
{
    Document doc = new Document(MyDir + "WMF with image.docx");

    MetafileRenderingOptions metafileRenderingOptions = new MetafileRenderingOptions();

    // 将“EmulateRasterOperations”属性设置为“false”，以便在
    // 它遇到一个元文件，这将需要光栅操作才能在输出 PDF 中呈现。
    metafileRenderingOptions.EmulateRasterOperations = false;

    // 将“RenderingMode”属性设置为“VectorWithFallback”以尝试使用矢量图形渲染每个元文件。
    metafileRenderingOptions.RenderingMode = MetafileRenderingMode.VectorWithFallback;

    // 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
    // 修改该方法将文档转换为 .PDF 并应用配置的方式
    // 在我们的 MetafileRenderingOptions 对象中进行保存操作。
    PdfSaveOptions saveOptions = new PdfSaveOptions();
    saveOptions.MetafileRenderingOptions = metafileRenderingOptions;

    HandleDocumentWarnings callback = new HandleDocumentWarnings();
    doc.WarningCallback = callback;

    doc.Save(ArtifactsDir + "PdfSaveOptions.HandleBinaryRasterWarnings.pdf", saveOptions);

    Assert.AreEqual(1, callback.Warnings.Count);
    Assert.AreEqual("'R2_XORPEN' binary raster operation is not supported.",
        callback.Warnings[0].Description);
}

/// <summary>
/// 打印并收集保存文档时发生的与格式丢失相关的警告。
/// </summary>
public class HandleDocumentWarnings : IWarningCallback
{
    public void Warning(WarningInfo info)
    {
        if (info.WarningType == WarningType.MinorFormattingLoss)
        {
            Console.WriteLine("Unsupported operation: " + info.Description);
            Warnings.Warning(info);
        }
    }

    public WarningInfoCollection Warnings = new WarningInfoCollection();
}
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
