---
title: "Aspose::Words::Saving::SvgSaveOptions::get_TextOutputMode 方法"
linktitle: "get_TextOutputMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::SvgSaveOptions::get_TextOutputMode 方法。获取或设置一个值，用于确定在 C++ 中文本在 SVG 中的渲染方式。"
type: docs
weight: 10000
url: /zh/cpp/aspose.words.saving/svgsaveoptions/get_textoutputmode/
---
## SvgSaveOptions::get_TextOutputMode method


获取或设置决定文本在 SVG 中如何呈现的值。

```cpp
Aspose::Words::Saving::SvgTextOutputMode Aspose::Words::Saving::SvgSaveOptions::get_TextOutputMode() const
```

## 备注


使用此属性获取或设置文档内部文本在保存为 SVG 格式时的渲染模式。

默认值是 [UseTargetMachineFonts](../../svgtextoutputmode/)。

## 示例



展示在将 .docx 文档转换为 .svg 时如何模拟图像的属性。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// 配置 SvgSaveOptions 对象，以在保存时不包含页面边框或可选择的文本。
auto options = System::MakeObject<Aspose::Words::Saving::SvgSaveOptions>();
options->set_FitToViewPort(true);
options->set_ShowPageBorder(false);
options->set_TextOutputMode(Aspose::Words::Saving::SvgTextOutputMode::UsePlacedGlyphs);

doc->Save(get_ArtifactsDir() + u"SvgSaveOptions.SaveLikeImage.svg", options);
```

## 另见

* Enum [SvgTextOutputMode](../../svgtextoutputmode/)
* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
