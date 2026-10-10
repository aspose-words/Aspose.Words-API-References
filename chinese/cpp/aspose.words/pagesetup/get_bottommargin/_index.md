---
title: "Aspose::Words::PageSetup::get_BottomMargin 方法"
linktitle: "get_BottomMargin"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::PageSetup::get_BottomMargin 方法。返回或设置页面底部边缘与正文底部边界之间的距离（单位为点），在 C++ 中。"
type: docs
weight: 10000
url: /zh/cpp/aspose.words/pagesetup/get_bottommargin/
---
## PageSetup::get_BottomMargin method


返回或设置页面底部边缘与正文底部边界之间的距离（以点为单位）。

```cpp
double Aspose::Words::PageSetup::get_BottomMargin()
```


## 示例



展示如何为节调整纸张大小、方向、边距以及其他设置。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Legal);
builder->get_PageSetup()->set_Orientation(Aspose::Words::Orientation::Landscape);
builder->get_PageSetup()->set_TopMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
builder->get_PageSetup()->set_BottomMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
builder->get_PageSetup()->set_LeftMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));
builder->get_PageSetup()->set_RightMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));
builder->get_PageSetup()->set_HeaderDistance(Aspose::Words::ConvertUtil::InchToPoint(0.2));
builder->get_PageSetup()->set_FooterDistance(Aspose::Words::ConvertUtil::InchToPoint(0.2));

builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"PageSetup.PageMargins.docx");
```

## 另见

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
