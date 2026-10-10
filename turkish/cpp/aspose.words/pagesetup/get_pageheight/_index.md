---
title: "Aspose::Words::PageSetup::get_PageHeight yöntemi"
linktitle: "get_PageHeight"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::PageSetup::get_PageHeight yöntemi. C++'da sayfanın yüksekliğini puan cinsinden döndürür veya ayarlar."
type: docs
weight: 33000
url: /tr/cpp/aspose.words/pagesetup/get_pageheight/
---
## PageSetup::get_PageHeight method


Sayfanın yüksekliğini puan cinsinden alır veya ayarlar.

```cpp
double Aspose::Words::PageSetup::get_PageHeight()
```


## Örnekler



Bir görüntünün nasıl ekleneceğini ve filigran olarak nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Görüntüyü başlığa ekleyin, böylece her sayfada görünür.
builder->MoveToHeaderFooter(Aspose::Words::HeaderFooterType::HeaderPrimary);
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertImage(get_ImageDir() + u"Transparent background logo.png");
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);
shape->set_BehindText(true);

// Görüntüyü sayfanın ortasına yerleştirin.
shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::Page);
shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
shape->set_Left((builder->get_PageSetup()->get_PageWidth() - shape->get_Width()) / 2);
shape->set_Top((builder->get_PageSetup()->get_PageHeight() - shape->get_Height()) / 2);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertWatermark.docx");
```

## Ayrıca Bakınız

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
