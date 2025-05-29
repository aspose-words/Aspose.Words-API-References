---
title: MetafileRenderingOptions.EmulateRasterOperations
linktitle: EmulateRasterOperations
articleTitle: EmulateRasterOperations
second_title: Aspose.Words for .NET
description: 发现 MetafileRenderingOptions EmulateRasterOperations 属性来控制光栅操作模拟，有效增强您的渲染能力。
type: docs
weight: 30
url: /zh/net/aspose.words.saving/metafilerenderingoptions/emulaterasteroperations/
---
## MetafileRenderingOptions.EmulateRasterOperations property

获取或设置一个值，确定是否应该模拟光栅操作。

```csharp
public bool EmulateRasterOperations { get; set; }
```

## 评论

特定的光栅操作可以在图元文件中使用。它们无法直接渲染为矢量图形。 模拟光栅操作需要对生成的矢量图形进行部分光栅化，这可能会影响 图元文件的渲染性能。

当此值设置为`真的`Aspose.Words 模拟了光栅操作。最终输出结果可能是部分光栅化的，性能可能会降低。

当此值设置为`错误的`Aspose.Words 不模拟光栅操作。当 Aspose.Words 在图元文件中遇到光栅操作时，它会回退到使用 操作系统将图元文件渲染为位图。

仅当图元文件呈现为矢量图形时才使用此选项。

默认值为`真的`。

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

* class [MetafileRenderingOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
