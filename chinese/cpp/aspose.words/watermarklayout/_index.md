---
title: "Aspose::Words::WatermarkLayout enum"
linktitle: "WatermarkLayout"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::WatermarkLayout 枚举。定义水印相对于水印中心的布局（C++）。"
type: docs
weight: 130000
url: /zh/cpp/aspose.words/watermarklayout/
---
## WatermarkLayout enum


定义水印相对于水印中心的布局。

```cpp
enum class WatermarkLayout
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| Horizontal | 0 | 水平水印布局。对应 0 度旋转。 |
| Diagonal | 315 | 对角线水印布局。对应 315 度旋转。 |


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
