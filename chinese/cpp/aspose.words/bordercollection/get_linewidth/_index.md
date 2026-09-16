---
title: "Aspose::Words::BorderCollection::get_LineWidth 方法"
linktitle: "get_LineWidth"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::BorderCollection::get_LineWidth 方法。获取或设置 C++ 中以点为单位的边框宽度。"
type: docs
weight: 11000
url: /zh/cpp/aspose.words/bordercollection/get_linewidth/
---
## BorderCollection::get_LineWidth method


获取或设置以点为单位的边框宽度。

```cpp
double Aspose::Words::BorderCollection::get_LineWidth()
```

## 备注


返回集合中第一个边框的宽度。

设置集合中所有边框的宽度（不包括对角线边框）。

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
