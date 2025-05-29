---
title: SvgTextOutputMode Enum
linktitle: SvgTextOutputMode
articleTitle: SvgTextOutputMode
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Saving.SvgTextOutputMode 枚举以自定义 SVG 格式的文本渲染，增强文档呈现和视觉吸引力。
type: docs
weight: 6410
url: /zh/net/aspose.words.saving/svgtextoutputmode/
---
## SvgTextOutputMode enumeration

允许指定在以 SVG 格式保存时如何呈现文档内的文本。

```csharp
public enum SvgTextOutputMode
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| UseSvgFonts | `0` | SVG 字体用于渲染文本。请注意，并非所有浏览器都支持 SVG 字体。 |
| UseTargetMachineFonts | `1` | 目标机器上安装的字体用于呈现文本。 请注意，如果文档中使用的某些字体在目标机器上不可用，则文档的外观可能会有所不同。 |
| UsePlacedGlyphs | `2` | 文本使用曲线渲染。请注意，如果使用此选项，文本选择将不起作用。 |

## 例子

展示如何在将 .docx 文档转换为 .svg 时模仿图像的属性。

```csharp
Document doc = new Document(MyDir + "Document.docx");

// 配置 SvgSaveOptions 对象以保存无页面边框或可选文本。
SvgSaveOptions options = new SvgSaveOptions
{
    FitToViewPort = true,
    ShowPageBorder = false,
    TextOutputMode = SvgTextOutputMode.UsePlacedGlyphs
};

doc.Save(ArtifactsDir + "SvgSaveOptions.SaveLikeImage.svg", options);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
