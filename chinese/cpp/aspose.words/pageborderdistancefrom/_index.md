---
title: "Aspose::Words::PageBorderDistanceFrom 枚举"
linktitle: "PageBorderDistanceFrom"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::PageBorderDistanceFrom 枚举。指定页面边框相对于页面边距的定位（C++）。"
type: docs
weight: 107000
url: /zh/cpp/aspose.words/pageborderdistancefrom/
---
## PageBorderDistanceFrom enum


指定页面边框相对于页面边距的位置。

```cpp
enum class PageBorderDistanceFrom
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| Text | 0 | [Border](../border/) 位置是相对于页面边距测量的。 |
| PageEdge | 1 | [Border](../border/) 位置是相对于页面边缘测量的。 |


## 示例



展示如何在首页顶部创建宽蓝色条带边框。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_BorderAlwaysInFront(false);
pageSetup->set_BorderDistanceFrom(Aspose::Words::PageBorderDistanceFrom::PageEdge);
pageSetup->set_BorderAppliesTo(Aspose::Words::PageBorderAppliesTo::FirstPage);

System::SharedPtr<Aspose::Words::Border> border = pageSetup->get_Borders()->idx_get(Aspose::Words::BorderType::Top);
border->set_LineStyle(Aspose::Words::LineStyle::Single);
border->set_LineWidth(30);
border->set_Color(System::Drawing::Color::get_Blue());
border->set_DistanceFromText(0);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageBorderProperties.docx");
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
