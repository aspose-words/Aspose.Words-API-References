---
title: "Aspose::Words::Document::get_ViewOptions 方法"
linktitle: "get_ViewOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::get_ViewOptions 方法。提供选项以控制文档在 Microsoft Word 中的显示方式（C++）。"
type: docs
weight: 58000
url: /zh/cpp/aspose.words/document/get_viewoptions/
---
## Document::get_ViewOptions method


提供选项以控制文档在 Microsoft Word 中的显示方式。

```cpp
System::SharedPtr<Aspose::Words::Settings::ViewOptions> Aspose::Words::Document::get_ViewOptions()
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

* Class [ViewOptions](../../../aspose.words.settings/viewoptions/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
