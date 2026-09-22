---
title: "Aspose::Words::PageSetup::get_TopMargin yöntemi"
linktitle: "get_TopMargin"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::PageSetup::get_TopMargin yöntemi. C++'ta sayfanın üst kenarı ile gövde metninin üst sınırı arasındaki mesafeyi (puan cinsinden) alır veya ayarlar."
type: docs
weight: 46000
url: /tr/cpp/aspose.words/pagesetup/get_topmargin/
---
## PageSetup::get_TopMargin method


Sayfanın üst kenarı ile gövde metninin üst sınırı arasındaki mesafeyi (nokta cinsinden) döndürür veya ayarlar.

```cpp
double Aspose::Words::PageSetup::get_TopMargin()
```


## Örnekler



Bir bölüm için kağıt boyutunu, yönlendirmeyi, kenar boşluklarını ve diğer ayarları nasıl ayarlayacağınızı gösterir.
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

## Ayrıca Bakınız

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
