---
title: "Aspose::Words::Settings::ViewOptions::get_ZoomType 方法"
linktitle: "get_ZoomType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Settings::ViewOptions::get_ZoomType 方法。获取或设置基于窗口大小的缩放值（C++）。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words.settings/viewoptions/get_zoomtype/
---
## ViewOptions::get_ZoomType method


获取或设置基于窗口大小的缩放值。

```cpp
Aspose::Words::Settings::ZoomType Aspose::Words::Settings::ViewOptions::get_ZoomType() const
```


## 示例



展示如何设置自定义缩放比例，旧版本的 Microsoft Word 在加载文档时会应用该比例。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->get_ViewOptions()->set_ViewType(Aspose::Words::Settings::ViewType::PageLayout);
doc->get_ViewOptions()->set_ZoomPercent(50);

ASSERT_EQ(Aspose::Words::Settings::ZoomType::Custom, doc->get_ViewOptions()->get_ZoomType());
ASSERT_EQ(Aspose::Words::Settings::ZoomType::None, doc->get_ViewOptions()->get_ZoomType());

doc->Save(get_ArtifactsDir() + u"ViewOptions.SetZoomPercentage.doc");
```


展示如何设置自定义缩放类型，旧版本的 Microsoft Word 在加载文档时会应用该设置。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// 将 "ZoomType" 属性设置为 "ZoomType.PageWidth" 以获取 Microsoft Word
// 以自动缩放文档以适应页面宽度。
// 将 "ZoomType" 属性设置为 "ZoomType.FullPage" 以获取 Microsoft Word
// 以自动缩放文档，使整个首页可见。
// 将 "ZoomType" 属性设置为 "ZoomType.TextFit" 以获取 Microsoft Word
// 以自动缩放文档以适应首页内部文本边距。
doc->get_ViewOptions()->set_ZoomType(zoomType);

doc->Save(get_ArtifactsDir() + u"ViewOptions.SetZoomType.doc");
```

## 另见

* Enum [ZoomType](../../zoomtype/)
* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
