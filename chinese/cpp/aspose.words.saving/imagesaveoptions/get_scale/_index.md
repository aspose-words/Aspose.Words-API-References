---
title: "Aspose::Words::Saving::ImageSaveOptions::get_Scale 方法"
linktitle: "get_Scale"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::ImageSaveOptions::get_Scale 方法。获取或设置在 C++ 中生成的图像的缩放因子。"
type: docs
weight: 14000
url: /zh/cpp/aspose.words.saving/imagesaveoptions/get_scale/
---
## ImageSaveOptions::get_Scale method


获取或设置 Floyd‑Steinberg 方法中二值化误差阈值。当 [ImageBinarizationMethod](../imagebinarizationmethod/) 为 [FloydSteinbergDithering](../imagebinarizationmethod/) 时。

```cpp
float Aspose::Words::Saving::ImageSaveOptions::get_Scale() const
```


## 示例



展示在 Aspose.Words 将文档转换为图像的同时如何编辑该图像。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// 当我们将文档保存为图像时，可以传递一个 SaveOptions 对象给
// 在保存操作渲染图像的同时编辑该图像。
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
// 我们可以调整这些属性以改变图像的亮度和对比度。
// 两者均采用 0-1 的比例，默认值为 0.5。
options->set_ImageBrightness(0.3f);
options->set_ImageContrast(0.7f);
// 我们可以使用这些属性调整水平和垂直分辨率。
// 这将影响图像的尺寸。
// 这些属性的默认值为 96.0，对应分辨率为 96dpi。
options->set_HorizontalResolution(72.f);
options->set_VerticalResolution(72.f);
// 我们可以使用此属性对图像进行缩放。默认值为 1.0，表示 100% 的缩放比例。
// 我们可以使用此属性抵消因更改分辨率而导致的图像尺寸变化。
options->set_Scale(96.f / 72.f);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.EditImage.png", options);
```


展示如何将 Office [Math](../../../aspose.words.math/) 对象渲染为本地文件系统中的图像文件。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto math = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

// 创建一个 "ImageSaveOptions" 对象，以传递给节点渲染器的 "Save" 方法进行修改。
// 它如何将 OfficeMath 节点渲染为图像。
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);

// 将 "Scale" 属性设置为 5，以将对象渲染为原始大小的五倍。
saveOptions->set_Scale(5.0f);

math->GetMathRenderer()->Save(get_ArtifactsDir() + u"Shape.RenderOfficeMath.png", saveOptions);
```

## 另见

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
