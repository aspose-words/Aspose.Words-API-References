---
title: "Aspose::Words::Saving::SvgTextOutputMode 枚举"
linktitle: "SvgTextOutputMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::SvgTextOutputMode 枚举。允许指定在 C++ 中将文档保存为 SVG 格式时，文档内部文本的渲染方式。"
type: docs
weight: 83000
url: /zh/cpp/aspose.words.saving/svgtextoutputmode/
---
## SvgTextOutputMode enum


允许指定文档内部文本在保存为 SVG 格式时的渲染方式。

```cpp
enum class SvgTextOutputMode
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| UseSvgFonts | 0 | 使用 SVG 字体渲染文本。注意，并非所有浏览器都支持 SVG 字体。 |
| UseTargetMachineFonts | 1 | [Fonts](../../aspose.words.fonts/) 已安装在目标机器上，用于渲染文本。注意，如果文档中使用的某些字体在目标机器上不可用，文档可能会呈现不同。 |
| UsePlacedGlyphs | 2 | 文本使用曲线渲染。注意，如果使用此选项，文本选择将无法工作。 |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
