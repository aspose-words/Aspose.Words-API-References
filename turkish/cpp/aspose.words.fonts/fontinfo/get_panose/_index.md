---
title: "Aspose::Words::Fonts::FontInfo::get_Panose yöntemi"
linktitle: "get_Panose"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontInfo::get_Panose yöntemi. C++'ta PANOSE yazı tipi sınıflandırma numarasını alır veya ayarlar."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.fonts/fontinfo/get_panose/
---
## FontInfo::get_Panose method


PANOSE yazı tipi sınıflandırma numarasını alır veya ayarlar.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Fonts::FontInfo::get_Panose() const
```

## Açıklamalar


PANOSE, kontrast, ağırlık ve serif stili gibi bir yazı tipinin kritik görsel özelliklerini tanımlayan kompakt 10 baytlık bir açıklamadır. Rakamlar Aile Türü, Serif [Style](../../../aspose.words/style/), Ağırlık, Oran, Kontrast, Çizgi Varyasyonu, Kol [Style](../../../aspose.words/style/), Harf Formu, Orta Çizgi ve X-Height değerlerini temsil eder.

**null** olabilir.

## Örnekler



Bir belgedeki her bir yazı tipinin ayrıntılarına nasıl erişileceğini ve bunların nasıl yazdırılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Fonts::FontInfo>>> fontCollectionEnumerator = doc->get_FontInfos()->GetEnumerator();
while (fontCollectionEnumerator->MoveNext())
{
    System::SharedPtr<Aspose::Words::Fonts::FontInfo> fontInfo = fontCollectionEnumerator->get_Current();
    if (fontInfo != nullptr)
    {
        std::cout << (System::String(u"Font name: ") + fontInfo->get_Name()) << std::endl;

        // Alternatif adlar genellikle boştur.
        std::cout << (System::String(u"Alt name: ") + fontInfo->get_AltName()) << std::endl;
        std::cout << (System::String(u"\t- Family: ") + System::ObjectExt::ToString(fontInfo->get_Family())) << std::endl;
        std::cout << (System::String(u"\t- ") + (fontInfo->get_IsTrueType() ? System::String(u"Is TrueType") : System::String(u"Is not TrueType"))) << std::endl;
        std::cout << (System::String(u"\t- Pitch: ") + System::ObjectExt::ToString(fontInfo->get_Pitch())) << std::endl;
        std::cout << (System::String(u"\t- Charset: ") + fontInfo->get_Charset()) << std::endl;
        std::cout << "\t- Panose:" << std::endl;
        std::cout << (System::String(u"\t\tFamily Kind: ") + fontInfo->get_Panose()[0]) << std::endl;
        std::cout << (System::String(u"\t\tSerif Style: ") + fontInfo->get_Panose()[1]) << std::endl;
        std::cout << (System::String(u"\t\tWeight: ") + fontInfo->get_Panose()[2]) << std::endl;
        std::cout << (System::String(u"\t\tProportion: ") + fontInfo->get_Panose()[3]) << std::endl;
        std::cout << (System::String(u"\t\tContrast: ") + fontInfo->get_Panose()[4]) << std::endl;
        std::cout << (System::String(u"\t\tStroke Variation: ") + fontInfo->get_Panose()[5]) << std::endl;
        std::cout << (System::String(u"\t\tArm Style: ") + fontInfo->get_Panose()[6]) << std::endl;
        std::cout << (System::String(u"\t\tLetterform: ") + fontInfo->get_Panose()[7]) << std::endl;
        std::cout << (System::String(u"\t\tMidline: ") + fontInfo->get_Panose()[8]) << std::endl;
        std::cout << (System::String(u"\t\tX-Height: ") + fontInfo->get_Panose()[9]) << std::endl;
    }
}
```

## Ayrıca Bakınız

* Class [FontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
