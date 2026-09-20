---
title: "Aspose::Words::WatermarkType 枚举"
linktitle: "WatermarkType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::WatermarkType 枚举。指定 C++ 中的水印类型。"
type: docs
weight: 131000
url: /zh/cpp/aspose.words/watermarktype/
---
## WatermarkType enum


指定水印类型。

```cpp
enum class WatermarkType
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 文本 | 0 | 指示文本将用作水印。此类水印对应于 WordArt 对象。 |
| 图像 | 1 | 指示图像将用作水印。此类水印对应于带有图像的形状。 |
| None | 2 | 指示水印未设置。 |


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
