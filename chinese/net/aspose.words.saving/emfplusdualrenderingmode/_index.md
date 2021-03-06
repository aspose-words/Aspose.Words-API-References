---
title: EmfPlusDualRenderingMode
second_title: Aspose.Words for .NET API 参考
description: 指定 Aspose.Words 应如何呈现 EMF 双元文件
type: docs
weight: 4720
url: /zh/net/aspose.words.saving/emfplusdualrenderingmode/
---
## EmfPlusDualRenderingMode enumeration

指定 Aspose.Words 应如何呈现 EMF+ 双元文件。

```csharp
public enum EmfPlusDualRenderingMode
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| EmfPlusWithFallback | `0` | Aspose.Words 尝试渲染 EMF+ 双元文件的 EMF+ 部分。如果不支持某些 EMF+ 记录 ，则 Aspose.Words 呈现 EMF+ 双元文件的 EMF 部分。 |
| EmfPlus | `1` | Aspose.Words 呈现 EMF+ 部分 EMF+ 双元文件。 |
| Emf | `2` | Aspose.Words 呈现 EMF+ 双元文件的 EMF 部分。 |

### 例子

显示保存为 PDF 时如何配置增强的 Windows 图元文件相关的呈现选项。

```csharp
Document doc = new Document(MyDir + "EMF.docx");

// 创建一个“PdfSaveOptions”对象，我们可以将它传递给文档的“Save”方法
// 修改该方法如何将文档转换为 .PDF。
PdfSaveOptions saveOptions = new PdfSaveOptions();

// 将“EmfPlusDualRenderingMode”属性设置为“EmfPlusDualRenderingMode.Emf”
// 仅渲染 EMF+ 双元文件的 EMF 部分。
// 将“EmfPlusDualRenderingMode”属性设置为“EmfPlusDualRenderingMode.EmfPlus”以
// 渲染 EMF+ 双元文件的 EMF+ 部分。
// 将“EmfPlusDualRenderingMode”属性设置为“EmfPlusDualRenderingMode.EmfPlusWithFallback”
// 如果支持所有 EMF+ 记录，则呈现 EMF+ 双元文件的 EMF+ 部分。
// 否则，Aspose.Words 将渲染 EMF 部分。
saveOptions.MetafileRenderingOptions.EmfPlusDualRenderingMode = renderingMode;

// 将“UseEmfEmbeddedToWmf”属性设置为“true”以呈现嵌入的 EMF 数据
// 对于我们可以渲染为矢量图形的元文件。
saveOptions.MetafileRenderingOptions.UseEmfEmbeddedToWmf = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderMetafile.pdf", saveOptions);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving)
* 部件 [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
