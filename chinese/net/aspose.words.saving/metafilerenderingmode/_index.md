---
title: MetafileRenderingMode Enum
linktitle: MetafileRenderingMode
articleTitle: MetafileRenderingMode
second_title: Aspose.Words for .NET
description: 了解 Aspose.Words.Saving.MetafileRenderingMode 如何增强 WMF 和 EMF 元文件渲染以实现最佳文档质量和性能。
type: docs
weight: 6070
url: /zh/net/aspose.words.saving/metafilerenderingmode/
---
## MetafileRenderingMode enumeration

指定 Aspose.Words 如何呈现 WMF 和 EMF 元文件。

```csharp
public enum MetafileRenderingMode
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| VectorWithFallback | `0` | Aspose.Words 尝试将图元文件渲染为矢量图形。如果 Aspose.Words 无法将图元文件中的部分记录正确渲染为矢量图形，则 Aspose.Words 会将该图元文件渲染为位图。 |
| Vector | `1` | Aspose.Words 将图元文件渲染为矢量图形。 |
| Bitmap | `2` | Aspose.Words 调用 GDI+ 将元文件渲染为位图，然后将位图保存到输出文档。 |

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
