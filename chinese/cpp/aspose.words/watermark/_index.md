---
title: "Aspose::Words::Watermark 类"
linktitle: "水印"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Watermark 类。表示用于处理文档水印的类。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 76000
url: /zh/cpp/aspose.words/watermark/
---
## Watermark class


表示用于处理文档水印的类。要了解更多，请访问 [Working with Watermark](https://docs.aspose.com/words/cpp/working-with-watermark/) 文档文章。

```cpp
class Watermark : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Type](./get_type/)() | 获取水印类型。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | 移除水印。 |
| [SetImage](./setimage/)(const System::SharedPtr\<System::Drawing::Image\>\&) | 向文档中添加图像水印。 |
| [SetImage](./setimage/)(const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | 向文档中添加图像水印。 |
| [SetImage](./setimage/)(const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | 向文档中添加图像水印。 |
| [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | 向文档中添加图像水印。 |
| [SetText](./settext/)(const System::String\&) | 向文档中添加文字水印。 |
| [SetText](./settext/)(const System::String\&, const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | 向文档中添加文字水印。 |
| static [Type](./type/)() |  |

## 示例



展示如何创建文本水印。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 添加纯文本水印。
doc->get_Watermark()->SetText(u"Aspose Watermark");

// 如果我们希望使用它作为水印来编辑文本格式，
// 我们可以在创建水印时传入 TextWatermarkOptions 对象来实现。
auto textWatermarkOptions = System::MakeObject<Aspose::Words::TextWatermarkOptions>();
textWatermarkOptions->set_FontFamily(u"Arial");
textWatermarkOptions->set_FontSize(36.0f);
textWatermarkOptions->set_Color(System::Drawing::Color::get_Black());
textWatermarkOptions->set_Layout(Aspose::Words::WatermarkLayout::Diagonal);
textWatermarkOptions->set_IsSemitrasparent(false);

doc->get_Watermark()->SetText(u"Aspose Watermark", textWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.TextWatermark.docx");

// 我们可以这样从文档中移除水印。
if (doc->get_Watermark()->get_Type() == Aspose::Words::WatermarkType::Text)
{
    doc->get_Watermark()->Remove();
}
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
