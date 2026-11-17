---
title: Aspose::Words::PageSetup::set_HeaderDistance method
linktitle: set_HeaderDistance
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::PageSetup::set_HeaderDistance method. Sets the distance (in points) between the header and the top of the page in C++.'
type: docs
weight: 63000
url: /cpp/aspose.words/pagesetup/set_headerdistance/
---
## PageSetup::set_HeaderDistance method


Sets the distance (in points) between the header and the top of the page.

```cpp
void Aspose::Words::PageSetup::set_HeaderDistance(double value)
```

## Examples


Shows how to adjust paper size, orientation, margins, along with other settings for a section.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_PageSetup()->set_PaperSize(PaperSize::Legal);
builder->get_PageSetup()->set_Orientation(Orientation::Landscape);
builder->get_PageSetup()->set_TopMargin(ConvertUtil::InchToPoint(1.0));
builder->get_PageSetup()->set_BottomMargin(ConvertUtil::InchToPoint(1.0));
builder->get_PageSetup()->set_LeftMargin(ConvertUtil::InchToPoint(1.5));
builder->get_PageSetup()->set_RightMargin(ConvertUtil::InchToPoint(1.5));
builder->get_PageSetup()->set_HeaderDistance(ConvertUtil::InchToPoint(0.2));
builder->get_PageSetup()->set_FooterDistance(ConvertUtil::InchToPoint(0.2));

builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"PageSetup.PageMargins.docx");
```
## See Also

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
