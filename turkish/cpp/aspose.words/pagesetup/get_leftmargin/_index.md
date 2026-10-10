---
title: "Aspose::Words::PageSetup::get_LeftMargin yöntemi"
linktitle: "get_LeftMargin"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::PageSetup::get_LeftMargin metodu. Sayfa sol kenarı ile gövde metninin sol sınırı arasındaki mesafeyi (nokta cinsinden) C++'ta döndürür veya ayarlar."
type: docs
weight: 22000
url: /tr/cpp/aspose.words/pagesetup/get_leftmargin/
---
## PageSetup::get_LeftMargin method


Sayfanın sol kenarı ile gövde metninin sol sınırı arasındaki mesafeyi (puan cinsinden) alır veya ayarlar.

```cpp
double Aspose::Words::PageSetup::get_LeftMargin()
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
