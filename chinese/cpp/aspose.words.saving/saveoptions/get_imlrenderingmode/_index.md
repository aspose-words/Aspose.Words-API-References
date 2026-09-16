---
title: "Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode 方法"
linktitle: "get_ImlRenderingMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode 方法。获取或设置一个值，用于确定在 C++ 中如何渲染墨水（InkML）对象。"
type: docs
weight: 10000
url: /zh/cpp/aspose.words.saving/saveoptions/get_imlrenderingmode/
---
## SaveOptions::get_ImlRenderingMode method


获取或设置决定墨水 (InkML) 对象渲染方式的值。

```cpp
Aspose::Words::Saving::ImlRenderingMode Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode() const
```

## 备注


默认值是 [InkML](../../imlrenderingmode/)。

当文档导出为固定页面格式时使用此属性。

## 示例



展示如何渲染 Ink 对象。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Ink object.docx");

// 设置 'ImlRenderingMode.InkML' 会忽略墨水（InkML）对象的回退形状，直接渲染 InkML 本身。
// 如果渲染结果不令人满意，
// 请使用 'ImlRenderingMode.Fallback' 以获得类似于以前版本的结果。
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
saveOptions->set_ImlRenderingMode(Aspose::Words::Saving::ImlRenderingMode::InkML);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
```

## 另见

* Enum [ImlRenderingMode](../../imlrenderingmode/)
* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
