---
title: "Aspose::Words::Saving::SvgSaveOptions::get_FitToViewPort 方法"
linktitle: "get_FitToViewPort"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::SvgSaveOptions::get_FitToViewPort 方法。指定输出 SVG 是否应填满可用的视口区域（浏览器窗口或容器）。当设置为 true 时，输出 SVG 的宽度和高度将设为 100%。默认值在 C++ 中为 false。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.saving/svgsaveoptions/get_fittoviewport/
---
## SvgSaveOptions::get_FitToViewPort method


指定输出 SVG 是否应填满可用的视口区域（浏览器窗口或容器）。设置为 **true** 时，输出 SVG 的宽度和高度将设为 100%。默认值为 **false**。

```cpp
bool Aspose::Words::Saving::SvgSaveOptions::get_FitToViewPort() const
```


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

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
