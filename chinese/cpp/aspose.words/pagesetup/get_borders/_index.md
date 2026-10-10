---
title: "Aspose::Words::PageSetup::get_Borders 方法"
linktitle: "get_Borders"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::PageSetup::get_Borders 方法。获取 C++ 中页面边框的集合。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words/pagesetup/get_borders/
---
## PageSetup::get_Borders method


获取页面边框的集合。

```cpp
System::SharedPtr<Aspose::Words::BorderCollection> Aspose::Words::PageSetup::get_Borders()
```


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

* Class [BorderCollection](../../bordercollection/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
