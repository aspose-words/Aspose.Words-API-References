---
title: "Aspose::Words::ConvertUtil::PixelToPoint yöntemi"
linktitle: "PixelToPoint"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ConvertUtil::PixelToPoint yöntemi. C++'ta 96 dpi'de pikselleri puanlara dönüştürür."
type: docs
weight: 4000
url: /tr/cpp/aspose.words/convertutil/pixeltopoint/
---
## ConvertUtil::PixelToPoint(double) method


Pikselleri 96 dpi'de puana dönüştürür.

```cpp
static double Aspose::Words::ConvertUtil::PixelToPoint(double pixels)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pikseller | double | Dönüştürülecek değer. |

## Örnekler



Sayfa özelliklerini piksel cinsinden nasıl belirteceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir bölümün "Sayfa Ayarı", sayfa kenar boşluklarının boyutunu puan cinsinden tanımlar.
// Farklı bir ölçü birimi kullanmak için "ConvertUtil" sınıfını da kullanabiliriz,
// sınırları tanımlarken piksel gibi.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::PixelToPoint(100));
pageSetup->set_BottomMargin(Aspose::Words::ConvertUtil::PixelToPoint(200));
pageSetup->set_LeftMargin(Aspose::Words::ConvertUtil::PixelToPoint(225));
pageSetup->set_RightMargin(Aspose::Words::ConvertUtil::PixelToPoint(125));

// Bir piksel 0,75 puandır.
ASPOSE_ASSERT_EQ(0.75, Aspose::Words::ConvertUtil::PixelToPoint(1));
ASPOSE_ASSERT_EQ(1.0, Aspose::Words::ConvertUtil::PointToPixel(0.75));

// Kullanılan varsayılan DPI değeri 96'dır.
ASPOSE_ASSERT_EQ(0.75, Aspose::Words::ConvertUtil::PixelToPoint(1, 96));

// Yeni kenar boşluklarını göstermek için içerik ekleyin.
builder->Writeln(System::String::Format(u"This Text is {0} points/{1} pixels from the left, ", pageSetup->get_LeftMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_LeftMargin())) + System::String::Format(u"{0} points/{1} pixels from the right, ", pageSetup->get_RightMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_RightMargin())) + System::String::Format(u"{0} points/{1} pixels from the top, ", pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_TopMargin())) + System::String::Format(u"and {0} points/{1} pixels from the bottom of the page.", pageSetup->get_BottomMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_BottomMargin())));

doc->Save(get_ArtifactsDir() + u"UtilityClasses.PointsAndPixels.docx");
```

## Ayrıca Bakınız

* Class [ConvertUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## ConvertUtil::PixelToPoint(double, double) method


Pikselleri belirtilen piksel çözünürlüğünde puana dönüştürür.

```cpp
static double Aspose::Words::ConvertUtil::PixelToPoint(double pixels, double resolution)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pikseller | double | Dönüştürülecek değer. |
| çözünürlük | double | dpi (inç başına nokta) çözünürlüğü. |

## Örnekler



Varsayılan ve özel çözünürlükte puanları piksele dönüştürmenin nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bu bölümün üst kenar boşluğunun boyutunu özel bir DPI'ye göre piksel cinsinden tanımlayın.
const double myDpi = 192;

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::PixelToPoint(100, myDpi));

ASSERT_NEAR(37.5, pageSetup->get_TopMargin(), 0.01);

// Varsayılan 96 DPI'de bir piksel 0,75 puandır.
ASPOSE_ASSERT_EQ(0.75, Aspose::Words::ConvertUtil::PixelToPoint(1));

builder->Writeln(System::String::Format(u"This Text is {0} points/{1} ", pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_TopMargin(), myDpi)) + System::String::Format(u"pixels (at a DPI of {0}) from the top of the page.", myDpi));

// Yeni bir DPI ayarlayın ve üst kenar boşluğu değerini buna göre ayarlayın.
const double newDpi = 300;
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::PixelToNewDpi(pageSetup->get_TopMargin(), myDpi, newDpi));
ASSERT_NEAR(59.0, pageSetup->get_TopMargin(), 0.01);

builder->Writeln(System::String::Format(u"At a DPI of {0}, the text is now {1} points/{2} ", newDpi, pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_TopMargin(), myDpi)) + u"pixels from the top of the page.");

doc->Save(get_ArtifactsDir() + u"UtilityClasses.PointsAndPixelsDpi.docx");
```

## Ayrıca Bakınız

* Class [ConvertUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
