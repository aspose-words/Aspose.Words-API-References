---
title: "Aspose::Words::ConvertUtil::PixelToNewDpi yöntemi"
linktitle: "PixelToNewDpi"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ConvertUtil::PixelToNewDpi yöntemi. C++'ta pikselleri bir çözünürlükten diğerine dönüştürür."
type: docs
weight: 3000
url: /tr/cpp/aspose.words/convertutil/pixeltonewdpi/
---
## ConvertUtil::PixelToNewDpi method


Piksel değerlerini bir çözünürlükten diğerine dönüştürür.

```cpp
static int32_t Aspose::Words::ConvertUtil::PixelToNewDpi(double pixels, double oldDpi, double newDpi)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pikseller | double | Dönüştürülecek değer. |
| oldDpi | double | Mevcut dpi (inç başına nokta) çözünürlüğü. |
| newDpi | double | Yeni dpi (inç başına nokta) çözünürlüğü. |

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
