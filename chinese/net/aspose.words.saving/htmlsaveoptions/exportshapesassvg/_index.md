---
title: HtmlSaveOptions.ExportShapesAsSvg
linktitle: ExportShapesAsSvg
articleTitle: ExportShapesAsSvg
second_title: Aspose.Words for .NET
description: 了解如何在保存为 HTML、MHTML、EPUB 或 AZW3 格式时使用 HtmlSaveOptions ExportShapesAsSvg 将 Shape 节点转换为 SVG 图像。
type: docs
weight: 250
url: /zh/net/aspose.words.saving/htmlsaveoptions/exportshapesassvg/
---
## HtmlSaveOptions.ExportShapesAsSvg property

控制是否[`Shape`](../../../aspose.words.drawing/shape/)将 保存为HTML、MHTML、EPUB或AZW3时，节点将转换为SVG图像。 默认值为`错误的`.

```csharp
public bool ExportShapesAsSvg { get; set; }
```

## 评论

如果此选项设置为`真的`，[`Shape`](../../../aspose.words.drawing/shape/)节点导出为 &lt;svg&gt; 元素。 否则，它们将呈现为位图并导出为 &lt;img&gt; 元素。

## 例子

展示如何将形状导出为可缩放矢量图形。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBox = builder.InsertShape(ShapeType.TextBox, 100.0, 60.0);
builder.MoveTo(textBox.FirstParagraph);
builder.Write("My text box");

// 当我们将文档保存为 HTML 时，我们可以传递一个 SaveOptions 对象
// 确定保存操作将如何导出文本框形状。
// 如果我们将“ExportTextBoxAsSvg”标志设置为“true”，
// 保存操作将把带有文本的形状转换为 SVG 对象。
// 如果我们将“ExportTextBoxAsSvg”标志设置为“false”，
// 保存操作将把带有文本的形状转换为图像。
HtmlSaveOptions options = new HtmlSaveOptions { ExportShapesAsSvg = exportShapesAsSvg };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportTextBox.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportTextBox.html");

if (exportShapesAsSvg)
{
    Assert.True(outDocContents.Contains(
        "<span style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\">" +
        "<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" 版本=\"1.1\" 宽度=\"133\" 高度=\"80\">"));
}
else
{
    Assert.True(outDocContents.Contains(
        "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
            "<img src=\"HtmlSaveOptions.ExportTextBox.001.png\" width=\"136\" height=\"83\" alt=\"\" " +
            "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" +
        "</p>"));
}
```

### 也可以看看

* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
