---
title: "Aspose::Words::Settings::ZoomType enum"
linktitle: "ZoomType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Settings::ZoomType enum. 表示文档在 Microsoft Word 中以何种大小显示在屏幕上的可能取值（C++）。"
type: docs
weight: 22000
url: /zh/cpp/aspose.words.settings/zoomtype/
---
## ZoomType enum


Microsoft Word 中文档在屏幕上显示大小的可能取值。

```cpp
enum class ZoomType
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 自定义 | 0 | 缩放比例是显式设置的。当控件大小变化时，它不会自动重新计算。 |
| None | n/a | 指示使用显式的缩放比例。与 [Custom](./) 相同。 |
| FullPage | 1 | 缩放比例会自动重新计算以适应整页。 |
| PageWidth | 2 | 缩放比例会自动重新计算以适应页面宽度。 |
| TextFit | 3 | 缩放比例会自动重新计算以适应文本。 |


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

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
