---
title: "Aspose::Words::Border::get_Shadow 方法"
linktitle: "get_Shadow"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Border::get_Shadow 方法。获取或设置指示边框是否具有阴影的值，适用于 C++。"
type: docs
weight: 9000
url: /zh/cpp/aspose.words/border/get_shadow/
---
## Border::get_Shadow method


获取或设置指示边框是否有阴影的值。

```cpp
bool Aspose::Words::Border::get_Shadow()
```

## 备注


在 Microsoft Word 中，要使边框具有阴影，四个边（左、上、右、下）的边框必须具有相同的类型、宽度、颜色，并且所有边框的 Shadow 属性都应设置为 **true**。

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

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
