---
title: "Aspose::Words::Saving::SvgSaveOptions::get_ShowPageBorder 方法"
linktitle: "get_ShowPageBorder"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::SvgSaveOptions::get_ShowPageBorder 方法。控制是否在页面轮廓上添加边框。默认在 C++ 中为 true。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words.saving/svgsaveoptions/get_showpageborder/
---
## SvgSaveOptions::get_ShowPageBorder method


控制是否在页面轮廓添加边框。默认值为 **true**。

```cpp
bool Aspose::Words::Saving::SvgSaveOptions::get_ShowPageBorder() const
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
