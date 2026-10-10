---
title: "Aspose::Words::Font::get_Shading 方法"
linktitle: "get_Shading"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Font::get_Shading 方法。返回一个 Shading 对象，引用该字体的阴影格式（C++）。"
type: docs
weight: 34000
url: /zh/cpp/aspose.words/font/get_shading/
---
## Font::get_Shading method


返回一个 [Shading](../../shading/) 对象，引用该字体的阴影格式。

```cpp
System::SharedPtr<Aspose::Words::Shading> Aspose::Words::Font::get_Shading()
```


## 示例



展示如何对文档生成器创建的文本应用阴影。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Color(System::Drawing::Color::get_White());

// 使使用我们白色字体颜色创建的文本可见的一种方法
// 是应用背景阴影效果。
System::SharedPtr<Aspose::Words::Shading> shading = builder->get_Font()->get_Shading();
shading->set_Texture(Aspose::Words::TextureIndex::TextureDiagonalUp);
shading->set_BackgroundPatternColor(System::Drawing::Color::get_OrangeRed());
shading->set_ForegroundPatternColor(System::Drawing::Color::get_DarkBlue());

builder->Writeln(u"White text on an orange background with a two-tone texture.");

doc->Save(get_ArtifactsDir() + u"Font.Shading.docx");
```

## 另见

* Class [Shading](../../shading/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
