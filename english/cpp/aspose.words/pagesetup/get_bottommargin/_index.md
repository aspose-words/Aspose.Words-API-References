---
title: get_BottomMargin
second_title: Aspose.Words for C++ API Reference
description: Returns or sets the distance (in points) between the bottom edge of the page and the bottom boundary of the body text.
type: docs
weight: 105
url: /cpp/aspose.words/pagesetup/get_bottommargin/
---
## PageSetup.get_BottomMargin method


Returns or sets the distance (in points) between the bottom edge of the page and the bottom boundary of the body text.

```cpp
double Aspose::Words::PageSetup::get_BottomMargin()
```


## Examples




Shows how to adjust paper size, orientation, margins, along with other settings for a section. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->get_PageSetup()->set_PaperSize(PaperSize::Legal);
builder->get_PageSetup()->set_Orientation(Orientation::Landscape);
builder->get_PageSetup()->set_TopMargin(ConvertUtil::InchToPoint(1.0));
builder->get_PageSetup()->set_BottomMargin(ConvertUtil::InchToPoint(1.0));
builder->get_PageSetup()->set_LeftMargin(ConvertUtil::InchToPoint(1.5));
builder->get_PageSetup()->set_RightMargin(ConvertUtil::InchToPoint(1.5));
builder->get_PageSetup()->set_HeaderDistance(ConvertUtil::InchToPoint(0.2));
builder->get_PageSetup()->set_FooterDistance(ConvertUtil::InchToPoint(0.2));

builder->Writeln(u"Hello world!");

doc->Save(ArtifactsDir + u"PageSetup.PageMargins.docx");
```

