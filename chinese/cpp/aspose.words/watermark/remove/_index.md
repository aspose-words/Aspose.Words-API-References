---
title: "Aspose::Words::Watermark::Remove 方法"
linktitle: "Remove"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Watermark::Remove 方法。在 C++ 中移除水印。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words/watermark/remove/
---
## Watermark::Remove method


移除水印。

```cpp
void Aspose::Words::Watermark::Remove()
```


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

* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
