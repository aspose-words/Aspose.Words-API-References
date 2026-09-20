---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg 方法"
linktitle: "get_ExportShapesAsSvg"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg 方法。控制在保存为 HTML、MHTML、EPUB 或 AZW3 时是否将 Shape 节点转换为 SVG 图像。默认值在 C++ 中为 false。"
type: docs
weight: 27000
url: /zh/cpp/aspose.words.saving/htmlsaveoptions/get_exportshapesassvg/
---
## HtmlSaveOptions::get_ExportShapesAsSvg method


控制在保存为 HTML、MHTML、EPUB 或 AZW3 时是否将 [Shape](../../../aspose.words.drawing/shape/) 节点转换为 SVG 图像。默认值为 **false**。

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg() const
```

## 备注


如果此选项设置为 **true**，则 [Shape](../../../aspose.words.drawing/shape/) 节点将导出为 <svg> 元素。否则，它们将渲染为位图并导出为 <img> 元素。

## 示例



展示如何将形状导出为可缩放矢量图形。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBox = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100.0, 60.0);
builder->MoveTo(textBox->get_FirstParagraph());
builder->Write(u"My text box");

// 当我们将文档保存为 HTML 时，可以传入一个 SaveOptions 对象
// 用于确定保存操作将如何导出文本框形状。
// 如果我们将 \"ExportTextBoxAsSvg\" 标志设置为 \"true\"，
// 保存操作将把带文本的形状转换为 SVG 对象。
// 如果我们将 \"ExportTextBoxAsSvg\" 标志设置为 \"false\"，
// 保存操作将把带文本的形状转换为图像。
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportShapesAsSvg(exportShapesAsSvg);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportTextBox.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportTextBox.html");

if (exportShapesAsSvg)
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<span style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\">") + u"<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" version=\"1.1\" width=\"133\" height=\"80\">"));
}
else
{
    ASSERT_TRUE(outDocContents.Contains(System::String(u"<p style=\"margin-top:0pt; margin-bottom:0pt\">") + u"<img src=\"HtmlSaveOptions.ExportTextBox.001.png\" width=\"136\" height=\"83\" alt=\"\" " + u"style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" + u"</p>"));
}
```

## 另见

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
