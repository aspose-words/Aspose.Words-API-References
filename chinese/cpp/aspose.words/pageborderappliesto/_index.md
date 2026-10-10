---
title: "Aspose::Words::PageBorderAppliesTo enum"
linktitle: "PageBorderAppliesTo"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::PageBorderAppliesTo enum. 指定在 C++ 中页面边框打印到哪些页面。"
type: docs
weight: 106000
url: /zh/cpp/aspose.words/pageborderappliesto/
---
## PageBorderAppliesTo enum


指定页面边框打印的页面。

```cpp
enum class PageBorderAppliesTo
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| AllPages | 0 | 页面边框显示在章节的所有页面上。 |
| FirstPage | 1 | 页面边框仅显示在章节的首页。 |
| OtherPages | 2 | 页面边框显示在章节的所有页面，除首页之外。 |


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
