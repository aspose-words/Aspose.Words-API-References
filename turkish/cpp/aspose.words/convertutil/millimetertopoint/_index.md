---
title: "Aspose::Words::ConvertUtil::MillimeterToPoint yöntemi"
linktitle: "MillimeterToPoint"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ConvertUtil::MillimeterToPoint yöntemi. C++'ta milimetreleri puana dönüştürür."
type: docs
weight: 2000
url: /tr/cpp/aspose.words/convertutil/millimetertopoint/
---
## ConvertUtil::MillimeterToPoint method


Milimetreleri puana dönüştürür.

```cpp
static double Aspose::Words::ConvertUtil::MillimeterToPoint(double millimeters)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| milimetre | double | Dönüştürülecek değer. |

## Örnekler



Sayfa özelliklerini milimetre cinsinden nasıl belirteceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bir bölümün "Sayfa Ayarı", sayfa kenar boşluklarının boyutunu puan cinsinden tanımlar.
// Daha tanıdık bir ölçü birimi kullanmak için "ConvertUtil" sınıfını da kullanabiliriz,
// sınırları tanımlarken milimetre gibi.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::MillimeterToPoint(30));
pageSetup->set_BottomMargin(Aspose::Words::ConvertUtil::MillimeterToPoint(50));
pageSetup->set_LeftMargin(Aspose::Words::ConvertUtil::MillimeterToPoint(80));
pageSetup->set_RightMargin(Aspose::Words::ConvertUtil::MillimeterToPoint(40));

// Bir santimetre yaklaşık olarak 28,3 puandır.
ASSERT_NEAR(28.34, Aspose::Words::ConvertUtil::MillimeterToPoint(10), 0.01);

// Yeni kenar boşluklarını göstermek için içerik ekleyin.
builder->Writeln(System::String::Format(u"This Text is {0} points from the left, ", pageSetup->get_LeftMargin()) + System::String::Format(u"{0} points from the right, ", pageSetup->get_RightMargin()) + System::String::Format(u"{0} points from the top, ", pageSetup->get_TopMargin()) + System::String::Format(u"and {0} points from the bottom of the page.", pageSetup->get_BottomMargin()));

doc->Save(get_ArtifactsDir() + u"UtilityClasses.PointsAndMillimeters.docx");
```

## Ayrıca Bakınız

* Class [ConvertUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
