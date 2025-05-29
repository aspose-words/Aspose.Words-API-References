---
title: OfficeMath.GetMathRenderer
linktitle: GetMathRenderer
articleTitle: GetMathRenderer
second_title: Aspose.Words for .NET
description: 探索 OfficeMath 的 GetMathRenderer 方法，轻松地将方程式转换为图像，以清晰、专业的视觉效果增强您的文档。
type: docs
weight: 90
url: /zh/net/aspose.words.math/officemath/getmathrenderer/
---
## OfficeMath.GetMathRenderer method

创建并返回一个可用于将此方程式渲染为图像的对象。

```csharp
public OfficeMathRenderer GetMathRenderer()
```

### 返回值

此方程的渲染器对象。

## 评论

此方法仅调用[`OfficeMathRenderer`](../../../aspose.words.rendering/officemathrenderer/)构造函数并将 此对象作为参数传递。

## 例子

展示如何将 Office Math 对象呈现到本地文件系统中的图像文件中。

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// 创建一个“ImageSaveOptions”对象传递给节点渲染器的“Save”方法来修改
// 如何将 OfficeMath 节点渲染为图像。
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Png);

// 将“Scale”属性设置为 5，以将对象渲染为其原始大小的五倍。
saveOptions.Scale = 5;

math.GetMathRenderer().Save(ArtifactsDir + "Shape.RenderOfficeMath.png", saveOptions);
```

### 也可以看看

* class [OfficeMathRenderer](../../../aspose.words.rendering/officemathrenderer/)
* class [OfficeMath](../)
* 命名空间 [Aspose.Words.Math](../../../aspose.words.math/)
* 部件 [Aspose.Words](../../../)
