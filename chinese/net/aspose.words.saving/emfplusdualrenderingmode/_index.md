---
title: EmfPlusDualRenderingMode Enum
linktitle: EmfPlusDualRenderingMode
articleTitle: EmfPlusDualRenderingMode
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words 的 EMF Plus Dual 渲染模式枚举，实现最佳的 EMF Dual 图元文件渲染。精准提升您的文档处理能力！
type: docs
weight: 5730
url: /zh/net/aspose.words.saving/emfplusdualrenderingmode/
---
## EmfPlusDualRenderingMode enumeration

指定 Aspose.Words 如何呈现 EMF+ Dual 元文件。

```csharp
public enum EmfPlusDualRenderingMode
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| EmfPlusWithFallback | `0` | Aspose.Words 尝试渲染 EMF+ Dual 图元文件中的 EMF+ 部分。如果某些 EMF+ 记录不受支持 ，则 Aspose.Words 会渲染 EMF+ Dual 图元文件中的 EMF 部分。 |
| EmfPlus | `1` | Aspose.Words 呈现 EMF+ Dual 图元文件的 EMF+ 部分。 |
| Emf | `2` | Aspose.Words 将 EMF 部分渲染为 EMF+ Dual 图元文件。 |

## 例子

展示如何在保存为 PDF 时配置增强型 Windows 图元文件相关的渲染选项。

```csharp
Document doc = new Document(MyDir + "EMF.docx");

// 创建一个“PdfSaveOptions”对象，我们可以将其传递给文档的“Save”方法
// 修改该方法将文档转换为 .PDF 的方式。
PdfSaveOptions saveOptions = new PdfSaveOptions();

// 将“EmfPlusDualRenderingMode”属性设置为“EmfPlusDualRenderingMode.Emf”
// 仅呈现 EMF+ 双元文件的 EMF 部分。
// 将“EmfPlusDualRenderingMode”属性设置为“EmfPlusDualRenderingMode.EmfPlus”
// 呈现 EMF+ 双元文件的 EMF+ 部分。
// 将“EmfPlusDualRenderingMode”属性设置为“EmfPlusDualRenderingMode.EmfPlusWithFallback”
// 如果所有 EMF+ 记录都受支持，则呈现 EMF+ 双元文件的 EMF+ 部分。
// 否则，Aspose.Words 将呈现 EMF 部分。
saveOptions.MetafileRenderingOptions.EmfPlusDualRenderingMode = renderingMode;

// 将“UseEmfEmbeddedToWmf”属性设置为“true”以呈现嵌入的 EMF 数据
// 对于我们可以渲染为矢量图形的元文件。
saveOptions.MetafileRenderingOptions.UseEmfEmbeddedToWmf = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.RenderMetafile.pdf", saveOptions);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
