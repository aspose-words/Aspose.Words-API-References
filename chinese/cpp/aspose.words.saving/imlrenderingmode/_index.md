---
title: "Aspose::Words::Saving::ImlRenderingMode 枚举"
linktitle: "ImlRenderingMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::ImlRenderingMode 枚举。指定在 C++ 中如何将墨水（InkML）对象渲染为固定页面格式。"
type: docs
weight: 66000
url: /zh/cpp/aspose.words.saving/imlrenderingmode/
---
## ImlRenderingMode enum


指定墨水（InkML）对象如何呈现为固定页面格式。

```cpp
enum class ImlRenderingMode
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| Fallback | 0 | 如果墨水（InkML）对象有可用的回退形状，Aspose.Words 将渲染回退形状而不是 InkML。 |
| InkML | 1 | Aspose.Words 忽略墨水（InkML）对象的回退形状，直接渲染 InkML 本身。这是默认模式。 |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
