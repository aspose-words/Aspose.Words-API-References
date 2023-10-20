---
title: ImlRenderingMode Enum
linktitle: ImlRenderingMode
articleTitle: ImlRenderingMode
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Saving.ImlRenderingMode 枚举. 指定如何将墨迹 InkML 对象呈现为固定页面格式 在 C#.
type: docs
weight: 5250
url: /zh/net/aspose.words.saving/imlrenderingmode/
---
## ImlRenderingMode enumeration

指定如何将墨迹 (InkML) 对象呈现为固定页面格式。

```csharp
public enum ImlRenderingMode
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Fallback | `0` | 如果后备形状可用于墨水 (InkML) 对象，Aspose.Words 会呈现后备形状而不是 InkML。 |
| InkML | `1` | Aspose.Words 忽略墨迹 (InkML) 对象的后备形状并呈现 InkML 本身。 这是默认模式。 |

## 例子

展示如何渲染 Ink 对象。

```csharp
Document doc = new Document(MyDir + "Ink object.docx");

// 设置 'ImlRenderingMode.InkML' 忽略墨迹 (InkML) 对象的后备形状并呈现 InkML 本身。
// 如果渲染结果不理想，
// 请使用 'ImlRenderingMode.Fallback' 获得与以前版本类似的结果。
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Jpeg)
{
    ImlRenderingMode = ImlRenderingMode.InkML
};

doc.Save(ArtifactsDir + "ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
