---
title: "Aspose::Words::Settings::ViewOptions::get_ZoomPercent 方法"
linktitle: "get_ZoomPercent"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Settings::ViewOptions::get_ZoomPercent 方法。获取或设置您希望在 C++ 中查看文档的百分比。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.settings/viewoptions/get_zoompercent/
---
## ViewOptions::get_ZoomPercent method


获取或设置查看文档的百分比。

```cpp
int32_t Aspose::Words::Settings::ViewOptions::get_ZoomPercent() const
```

## 备注


虽然 Aspose.Words 能够读取和写入此选项，但其使用取决于具体应用。例如，MS Word 2013 并不遵守此选项的值。

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

## 另见

* Class [ViewOptions](../)
* Namespace [Aspose::Words::Settings](../../)
* Library [Aspose.Words for C++](../../../)
