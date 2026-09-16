---
title: "Aspose::Words::PageSetup::get_BorderAlwaysInFront 方法"
linktitle: "get_BorderAlwaysInFront"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::PageSetup::get_BorderAlwaysInFront 方法。指定页面边框相对于交叉文本和对象的位置，在 C++ 中。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words/pagesetup/get_borderalwaysinfront/
---
## PageSetup::get_BorderAlwaysInFront method


指定页面边框相对于交叉文本和对象的位置。

```cpp
bool Aspose::Words::PageSetup::get_BorderAlwaysInFront()
```


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

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
