---
title: ImlRenderingMode Enum
linktitle: ImlRenderingMode
articleTitle: ImlRenderingMode
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words ImlRenderingMode 枚举，实现最佳 InkML 渲染。通过精确的墨迹对象可视化增强您的文档输出！
type: docs
weight: 6000
url: /zh/net/aspose.words.saving/imlrenderingmode/
---
## ImlRenderingMode enumeration

指定如何将墨迹（InkML）对象呈现为固定页面格式。

```csharp
public enum ImlRenderingMode
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Fallback | `0` | 如果墨水（InkML）对象有后备形状，Aspose.Words 将渲染后备形状而不是 InkML。 |
| InkML | `1` | Aspose.Words 忽略墨水（InkML）对象的后备形状并呈现 InkML 本身。 这是默认模式。 |

## 例子

展示如何渲染 Ink 对象。

```csharp
Document doc = new Document(MyDir + "Ink object.docx");

// 设置“ImlRenderingMode.InkML”忽略墨水（InkML）对象的后备形状并呈现 InkML 本身。
// 如果渲染结果不令人满意，
// 请使用“ImlRenderingMode.Fallback”来获得与以前版本类似的结果。
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Jpeg)
{
    ImlRenderingMode = ImlRenderingMode.InkML
};

doc.Save(ArtifactsDir + "ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
