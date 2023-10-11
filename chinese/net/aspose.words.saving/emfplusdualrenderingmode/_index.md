---
title: Enum EmfPlusDualRenderingMode
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Saving.EmfPlusDualRenderingMode 枚举. 指定 Aspose.Words 应如何渲染 EMF 双图元文件
type: docs
weight: 4980
url: /zh/net/aspose.words.saving/emfplusdualrenderingmode/
---
## EmfPlusDualRenderingMode enumeration

指定 Aspose.Words 应如何渲染 EMF+ 双图元文件。

```csharp
public enum EmfPlusDualRenderingMode
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| EmfPlusWithFallback | `0` | Aspose.Words 尝试渲染 EMF+ Dual 图元文件的 EMF+ 部分。如果某些 EMF+ 记录不受支持 ，则 Aspose.Words 会渲染 EMF+ Dual 图元文件的 EMF 部分。 |
| EmfPlus | `1` | Aspose.Words 渲染 EMF+ 双图元文件的 EMF+ 部分。 |
| Emf | `2` | Aspose.Words 渲染 EMF+ Dual 图元文件的 EMF 部分。 |

### 例子

演示如何在保存为 PDF 时配置增强型 Windows 图元文件相关的渲染选项。

```csharp
Document doc = new Document(MyDir + "EMF.docx");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions saveOptions = new PdfSaveOptions();

// 将“EmfPlusDualRenderingMode”属性设置为“EmfPlusDualRenderingMode.Emf”
// 仅渲染 EMF+ 双图元文件的 EMF 部分。
// 将“EmfPlusDualRenderingMode”属性设置为“EmfPlusDualRenderingMode.EmfPlus”
// 渲染 EMF+ 双图元文件的 EMF+ 部分。
// 将“EmfPlusDualRenderingMode”属性设置为“EmfPlusDualRenderingMode.EmfPlusWithFallback”
// 如果支持所有 EMF+ 记录，则渲染 EMF+ 双图元文件的 EMF+ 部分。
// 否则，Aspose.Words 将渲染 EMF 部分。
saveOptions.MetafileRenderingOptions.EmfPlusDualRenderingMode = renderingMode;

// 将“UseEmfEmbeddedToWmf”属性设置为“true”以渲染嵌入的 EMF 数据
// 用于我们可以渲染为矢量图形的图元文件。
saveOptions.MetafileRenderingOptions.UseEmfEmbeddedToWmf = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderMetafile.pdf", saveOptions);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)


