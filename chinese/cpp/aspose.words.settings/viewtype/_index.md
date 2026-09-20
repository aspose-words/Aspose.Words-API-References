---
title: "Aspose::Words::Settings::ViewType 枚举"
linktitle: "ViewType"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Settings::ViewType 枚举。Microsoft Word 在 C++ 中的视图模式的可能取值。"
type: docs
weight: 21000
url: /zh/cpp/aspose.words.settings/viewtype/
---
## ViewType enum


Microsoft Word 中视图模式的可能取值。

```cpp
enum class ViewType
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| None | 0 | 文档应以应用程序的默认视图呈现。 |
| Reading | 0 | 文档应以应用程序的默认视图呈现。 |
| PageLayout | 1 | 文档应以显示打印效果的视图打开。 |
| Outline | 3 | 文档应以针对大纲或创建长文档进行优化的视图呈现。 |
| 普通 | 4 | 文档应以针对大纲或创建长文档进行优化的视图呈现。 |
| Web | 5 | 文档应以模拟该文档在网页中显示方式的视图呈现。 |


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
