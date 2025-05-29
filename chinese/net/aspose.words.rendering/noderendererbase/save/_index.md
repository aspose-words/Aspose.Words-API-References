---
title: NodeRendererBase.Save
linktitle: Save
articleTitle: Save
second_title: Aspose.Words for .NET
description: 探索 NodeRendererBase 的 Save 方法。轻松将形状渲染为图像并保存到文件中，实现无缝集成并提高生产力。
type: docs
weight: 90
url: /zh/net/aspose.words.rendering/noderendererbase/save/
---
## Save(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#save_2}

将形状渲染为图像并保存到文件中。

```csharp
public void Save(string fileName, ImageSaveOptions saveOptions)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | String | 图像文件的名称。如果指定名称的文件已存在，则现有文件将被覆盖。 |
| saveOptions | ImageSaveOptions | 指定控制形状渲染和保存方式的选项。可以是`无效的`。 |

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

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [NodeRendererBase](../)
* 命名空间 [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* 部件 [Aspose.Words](../../../)

---

## Save(*string, [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)*) {#save_3}

将形状渲染为 SVG 图像并保存到文件中。

```csharp
public void Save(string fileName, SvgSaveOptions saveOptions)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | String | 图像文件的名称。如果指定名称的文件已存在，则现有文件将被覆盖。 |
| saveOptions | SvgSaveOptions | 指定控制形状渲染和保存方式的选项。可以是`无效的`。 |

## 例子

展示如何在渲染办公室数学时传递保存选项。

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

SvgSaveOptions options = new SvgSaveOptions();
options.TextOutputMode = SvgTextOutputMode.UsePlacedGlyphs;

math.GetMathRenderer().Save(ArtifactsDir + "SvgSaveOptions.Output.svg", options);

using (MemoryStream stream = new MemoryStream())
    math.GetMathRenderer().Save(stream, options);
```

### 也可以看看

* class [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)
* class [NodeRendererBase](../)
* 命名空间 [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* 部件 [Aspose.Words](../../../)

---

## Save(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#save}

将形状渲染为图像并保存到流中。

```csharp
public void Save(Stream stream, ImageSaveOptions saveOptions)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | Stream | 保存形状图像的流。 |
| saveOptions | ImageSaveOptions | 指定控制形状渲染和保存方式的选项。可以是`无效的` . 如果这是`无效的`，图像将以 PNG 格式保存。 |

## 例子

展示如何使用形状渲染器将形状导出到本地文件系统中的文件。

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(7, shapes.Length);

// 文档中有 7 个形状，包括一个组形状和 2 个子形状。
// 我们将把每个形状渲染到本地文件系统中的图像文件中
// 同时忽略组形状，因为它们没有外观。
// 这将生成 6 个图像文件。
foreach (Shape shape in doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>())
{
    ShapeRenderer renderer = shape.GetShapeRenderer();
    ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Png);
    renderer.Save(ArtifactsDir + $"Shape.RenderAllShapes.{shape.Name}.png", options);
}
```

### 也可以看看

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [NodeRendererBase](../)
* 命名空间 [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* 部件 [Aspose.Words](../../../)

---

## Save(*Stream, [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)*) {#save_1}

将形状渲染为 SVG 图像并保存到流中。

```csharp
public void Save(Stream stream, SvgSaveOptions saveOptions)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | Stream | 保存形状的 SVG 图像的流。 |
| saveOptions | SvgSaveOptions | 指定控制形状渲染和保存方式的选项。可以是`无效的` . 如果这是`无效的`，图像将使用默认选项保存。 |

## 例子

展示如何在渲染办公室数学时传递保存选项。

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath math = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

SvgSaveOptions options = new SvgSaveOptions();
options.TextOutputMode = SvgTextOutputMode.UsePlacedGlyphs;

math.GetMathRenderer().Save(ArtifactsDir + "SvgSaveOptions.Output.svg", options);

using (MemoryStream stream = new MemoryStream())
    math.GetMathRenderer().Save(stream, options);
```

### 也可以看看

* class [SvgSaveOptions](../../../aspose.words.saving/svgsaveoptions/)
* class [NodeRendererBase](../)
* 命名空间 [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* 部件 [Aspose.Words](../../../)
