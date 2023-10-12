---
title: MetafileRenderingOptions.EmulateRasterOperations
second_title: Aspose.Words for .NET API 参考
description: MetafileRenderingOptions 财产. 获取或设置一个值确定是否应模拟光栅操作
type: docs
weight: 30
url: /zh/net/aspose.words.saving/metafilerenderingoptions/emulaterasteroperations/
---
## MetafileRenderingOptions.EmulateRasterOperations property

获取或设置一个值，确定是否应模拟光栅操作。

```csharp
public bool EmulateRasterOperations { get; set; }
```

### 评论

可以在图元文件中使用特定的光栅操作。它们无法直接渲染为矢量图形。 模拟光栅操作需要对生成的矢量图形进行部分光栅化，这可能会影响 图元文件渲染性能。

当该值设置为`真的`，Aspose.Words 模拟光栅操作。生成的输出 Maybe 部分光栅化，性能可能会变慢。

当该值设置为`错误的`，Aspose.Words 不模拟光栅操作。当 Aspose.Words 在图元文件中遇到光栅操作时，它会使用 the 操作系统将图元文件渲染为位图。

仅当图元文件呈现为矢量图形时才使用此选项。

默认值为`真的`。

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

* class [MetafileRenderingOptions](../)
* 命名空间 [Aspose.Words.Saving](../../metafilerenderingoptions/)
* 部件 [Aspose.Words](../../../)


