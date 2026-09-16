---
title: "Aspose::Words::BorderCollection::get_Shadow 方法"
linktitle: "get_Shadow"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::BorderCollection::get_Shadow 方法。获取或设置一个值，指示边框是否具有阴影（在 C++ 中）。"
type: docs
weight: 13000
url: /zh/cpp/aspose.words/bordercollection/get_shadow/
---
## BorderCollection::get_Shadow method


获取或设置指示边框是否有阴影的值。

```cpp
bool Aspose::Words::BorderCollection::get_Shadow()
```

## 备注


获取集合中第一个边框的值。

设置集合中所有边框的值（不包括对角线边框）。

## 示例



展示如何创建带阴影的绿色波浪形页面边框。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();

pageSetup->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::DoubleWave);
pageSetup->get_Borders()->set_LineWidth(2);
pageSetup->get_Borders()->set_Color(System::Drawing::Color::get_Green());
pageSetup->get_Borders()->set_DistanceFromText(24);
pageSetup->get_Borders()->set_Shadow(true);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageBorders.docx");
```

## 另见

* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
