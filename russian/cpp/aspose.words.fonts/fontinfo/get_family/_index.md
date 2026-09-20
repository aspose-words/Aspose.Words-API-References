---
title: "Aspose::Words::Fonts::FontInfo::get_Family метод"
linktitle: "get_Family"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fonts::FontInfo::get_Name метод"
type: docs
weight: 4000
url: /ru/cpp/aspose.words.fonts/fontinfo/get_family/
---
## FontInfo::get_Family method


Получает или задает семейство шрифтов, к которому принадлежит данный шрифт.

```cpp
Aspose::Words::Fonts::FontFamily Aspose::Words::Fonts::FontInfo::get_Family() const
```


## Примеры



Показывает, как получить доступ и вывести детали каждого шрифта в документе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Fonts::FontInfo>>> fontCollectionEnumerator = doc->get_FontInfos()->GetEnumerator();
while (fontCollectionEnumerator->MoveNext())
{
    System::SharedPtr<Aspose::Words::Fonts::FontInfo> fontInfo = fontCollectionEnumerator->get_Current();
    if (fontInfo != nullptr)
    {
        std::cout << (System::String(u"Font name: ") + fontInfo->get_Name()) << std::endl;

        // Альтернативные имена обычно пусты.
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

## См. также

* Enum [FontFamily](../../fontfamily/)
* Class [FontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
