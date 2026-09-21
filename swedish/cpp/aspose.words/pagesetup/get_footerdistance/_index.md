---
title: "Aspose::Words::PageSetup::get_FooterDistance metod"
linktitle: "get_FooterDistance"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::PageSetup::get_FooterDistance metod. Returnerar eller anger avståndet (i punkter) mellan sidfoten och sidans botten i C++."
type: docs
weight: 16000
url: /sv/cpp/aspose.words/pagesetup/get_footerdistance/
---
## PageSetup::get_FooterDistance method


Returnerar eller anger avståndet (i punkter) mellan sidfoten och sidans nederkant.

```cpp
double Aspose::Words::PageSetup::get_FooterDistance()
```


## Exempel



Visar hur man justerar papperstorlek, orientering, marginaler samt andra inställningar för ett avsnitt.
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

## Se även

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
