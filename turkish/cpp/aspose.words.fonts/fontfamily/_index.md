---
title: "Aspose::Words::Fonts::FontFamily enum"
linktitle: "FontFamily"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontFamily enum. C++'da yazı tipi ailesini temsil eder."
type: docs
weight: 21000
url: /tr/cpp/aspose.words.fonts/fontfamily/
---
## FontFamily enum


Yazı tipi ailesini temsil eder.

```cpp
enum class FontFamily
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Otomatik | 0 | Genel bir aile adı belirtir. Bu ad, bir yazı tipi hakkında bilgi mevcut olmadığında veya önemli olmadığında kullanılır. Varsayılan yazı tipi kullanılır. |
| Roman | 1 | Serifli orantılı bir yazı tipini belirtir. Bir örnek Times New Roman'dır. |
| Swiss | 2 | Serifsiz orantılı bir yazı tipini belirtir. Bir örnek Arial'dır. |
| Modern | 3 | Serifli ya da serifsiz bir monospaced (tek genişlikli) yazı tipini belirtir. Monospaced yazı tipleri genellikle modern olur; örnekler arasında Pica, Elite ve Courier New bulunur. |
| Script | 4 | El yazısı gibi görünmesi için tasarlanmış bir yazı tipini belirtir; örnekler arasında Script ve Cursive bulunur. |
| Decorative | 5 | Yeni bir yazı tipini belirtir. Bir örnek Old English'tir. |

## Açıklamalar


Bir yazı tipi ailesi, ortak çizgi kalınlığı ve serif özelliklerine sahip yazı tiplerinin bir kümesidir.

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

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
