---
title: "Aspose::Words::ConvertUtil class"
linktitle: "ConvertUtil"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ConvertUtil class. Çeşitli ölçü birimleri arasında dönüşüm yapmak için yardımcı işlevler sağlar. Daha fazla bilgi edinmek için C++'daki dokümantasyon makalesini ziyaret edin."
type: docs
weight: 19000
url: /tr/cpp/aspose.words/convertutil/
---
## ConvertUtil class


Çeşitli ölçü birimleri arasında dönüştürme yapmak için yardımcı işlevler sağlar. Daha fazla bilgi edinmek için [Convert Between Measurement Units](https://docs.aspose.com/words/cpp/convert-between-measurement-units/) dokümantasyon makalesini ziyaret edin.

```cpp
class ConvertUtil
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [ConvertUtil](./convertutil/)() |  |
| static [InchToPoint](./inchtopoint/)(double) | İnçleri puana dönüştürür. |
| static [MillimeterToPoint](./millimetertopoint/)(double) | Milimetreleri puana dönüştürür. |
| static [PixelToNewDpi](./pixeltonewdpi/)(double, double, double) | Piksel değerlerini bir çözünürlükten diğerine dönüştürür. |
| static [PixelToPoint](./pixeltopoint/)(double) | Pikselleri 96 dpi'de puana dönüştürür. |
| static [PixelToPoint](./pixeltopoint/)(double, double) | Pikselleri belirtilen piksel çözünürlüğünde puana dönüştürür. |
| static [PointToInch](./pointtoinch/)(double) | Puanları inçe dönüştürür. |
| static [PointToPixel](./pointtopixel/)(double) | Puanları 96 dpi'de piksellere dönüştürür. |
| static [PointToPixel](./pointtopixel/)(double, double) | Puanları belirtilen piksel çözünürlüğünde piksellere dönüştürür. |

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


Sayfa özelliklerini inç cinsinden nasıl belirteceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir bölümün "Sayfa Ayarı", sayfa kenar boşluklarının boyutunu puan cinsinden tanımlar.
// Daha tanıdık bir ölçü birimi kullanmak için "ConvertUtil" sınıfını da kullanabiliriz,
// örneğin sınırları tanımlarken inç olarak.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::InchToPoint(1.0));
pageSetup->set_BottomMargin(Aspose::Words::ConvertUtil::InchToPoint(2.0));
pageSetup->set_LeftMargin(Aspose::Words::ConvertUtil::InchToPoint(2.5));
pageSetup->set_RightMargin(Aspose::Words::ConvertUtil::InchToPoint(1.5));

// Bir inç 72 puandır.
ASPOSE_ASSERT_EQ(72.0, Aspose::Words::ConvertUtil::InchToPoint(1));
ASPOSE_ASSERT_EQ(1.0, Aspose::Words::ConvertUtil::PointToInch(72));

// Yeni kenar boşluklarını göstermek için içerik ekleyin.
builder->Writeln(System::String::Format(u"This Text is {0} points/{1} inches from the left, ", pageSetup->get_LeftMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_LeftMargin())) + System::String::Format(u"{0} points/{1} inches from the right, ", pageSetup->get_RightMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_RightMargin())) + System::String::Format(u"{0} points/{1} inches from the top, ", pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_TopMargin())) + System::String::Format(u"and {0} points/{1} inches from the bottom of the page.", pageSetup->get_BottomMargin(), Aspose::Words::ConvertUtil::PointToInch(pageSetup->get_BottomMargin())));

doc->Save(get_ArtifactsDir() + u"UtilityClasses.PointsAndInches.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
