---
title: "Aspose::Words::BorderCollection::get_Color 方法"
linktitle: "get_Color"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::BorderCollection::get_Color 方法。获取或设置边框颜色（在 C++ 中）。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words/bordercollection/get_color/
---
## BorderCollection::get_Color method


获取或设置边框颜色。

```cpp
System::Drawing::Color Aspose::Words::BorderCollection::get_Color()
```

## 备注


返回集合中第一个边框的颜色。

为集合中除对角线边框外的所有边框设置颜色。

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
