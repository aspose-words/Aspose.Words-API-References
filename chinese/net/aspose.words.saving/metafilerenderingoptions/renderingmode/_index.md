---
title: MetafileRenderingOptions.RenderingMode
second_title: Aspose.Words for .NET API 参考
description: MetafileRenderingOptions 财产. 获取或设置一个值确定图元文件图像应如何呈现
type: docs
weight: 60
url: /zh/net/aspose.words.saving/metafilerenderingoptions/renderingmode/
---
## MetafileRenderingOptions.RenderingMode property

获取或设置一个值，确定图元文件图像应如何呈现。

```csharp
public MetafileRenderingMode RenderingMode { get; set; }
```

### 评论

默认值取决于保存格式。对于图像来说是Bitmap. 对于其他格式是VectorWithFallback。

### 例子

显示添加了位图渲染的回退和更改有关不支持的图元文件记录的警告类型。

```csharp
public void HandleBinaryRasterWarnings()
{
    Document doc = new Document(MyDir + "WMF with image.docx");

    MetafileRenderingOptions metafileRenderingOptions = new MetafileRenderingOptions();

    // 将“EmulateRasterOperations”属性设置为“false”以在以下情况下回退到位图：
    // 它遇到一个图元文件，这将需要光栅操作才能在输出 PDF 中呈现。
    metafileRenderingOptions.EmulateRasterOperations = false;

    // 将“RenderingMode”属性设置为“VectorWithFallback”以尝试使用矢量图形渲染每个图元文件。
    metafileRenderingOptions.RenderingMode = MetafileRenderingMode.VectorWithFallback;

    // 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
    // 修改该方法将文档转换为 .PDF 并应用配置的方式
    // 在我们的MetafileRenderingOptions对象中进行保存操作。
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

* enum [MetafileRenderingMode](../../metafilerenderingmode/)
* class [MetafileRenderingOptions](../)
* 命名空间 [Aspose.Words.Saving](../../metafilerenderingoptions/)
* 部件 [Aspose.Words](../../../)


