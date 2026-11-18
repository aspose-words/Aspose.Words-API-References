---
title: Aspose::Words::PageSetup::set_LeftMargin method
linktitle: set_LeftMargin
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::PageSetup::set_LeftMargin method. Sets the distance (in points) between the left edge of the page and the left boundary of the body text in C++.'
type: docs
weight: 66000
url: /cpp/aspose.words/pagesetup/set_leftmargin/
---
## PageSetup::set_LeftMargin method


Sets the distance (in points) between the left edge of the page and the left boundary of the body text.

```cpp
void Aspose::Words::PageSetup::set_LeftMargin(double value)
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
