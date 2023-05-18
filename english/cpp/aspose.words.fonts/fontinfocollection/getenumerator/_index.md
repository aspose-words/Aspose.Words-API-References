---
title: Aspose::Words::Fonts::FontInfoCollection::GetEnumerator method
linktitle: GetEnumerator
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::FontInfoCollection::GetEnumerator method. Returns an enumerator object that can be used to iterate over all items in the collection in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words.fonts/fontinfocollection/getenumerator/
---
## FontInfoCollection::GetEnumerator method


Returns an enumerator object that can be used to iterate over all items in the collection.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Fonts::FontInfo>>> Aspose::Words::Fonts::FontInfoCollection::GetEnumerator() override
```


## Examples



Shows how to access and print details of each font in a document. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Document.docx");

SharedPtr<System::Collections::Generic::IEnumerator<SharedPtr<FontInfo>>> fontCollectionEnumerator = doc->get_FontInfos()->GetEnumerator();
while (fontCollectionEnumerator->MoveNext())
{
    SharedPtr<FontInfo> fontInfo = fontCollectionEnumerator->get_Current();
    if (fontInfo != nullptr)
    {
        std::cout << (String(u"Font name: ") + fontInfo->get_Name()) << std::endl;

        // Alt names are usually blank.
        std::cout << (String(u"Alt name: ") + fontInfo->get_AltName()) << std::endl;
        std::cout << (String(u"\t- Family: ") + System::ObjectExt::ToString(fontInfo->get_Family())) << std::endl;
        std::cout << (String(u"\t- ") + (fontInfo->get_IsTrueType() ? String(u"Is TrueType") : String(u"Is not TrueType"))) << std::endl;
        std::cout << (String(u"\t- Pitch: ") + System::ObjectExt::ToString(fontInfo->get_Pitch())) << std::endl;
        std::cout << (String(u"\t- Charset: ") + fontInfo->get_Charset()) << std::endl;
        std::cout << "\t- Panose:" << std::endl;
        std::cout << (String(u"\t\tFamily Kind: ") + fontInfo->get_Panose()[0]) << std::endl;
        std::cout << (String(u"\t\tSerif Style: ") + fontInfo->get_Panose()[1]) << std::endl;
        std::cout << (String(u"\t\tWeight: ") + fontInfo->get_Panose()[2]) << std::endl;
        std::cout << (String(u"\t\tProportion: ") + fontInfo->get_Panose()[3]) << std::endl;
        std::cout << (String(u"\t\tContrast: ") + fontInfo->get_Panose()[4]) << std::endl;
        std::cout << (String(u"\t\tStroke Variation: ") + fontInfo->get_Panose()[5]) << std::endl;
        std::cout << (String(u"\t\tArm Style: ") + fontInfo->get_Panose()[6]) << std::endl;
        std::cout << (String(u"\t\tLetterform: ") + fontInfo->get_Panose()[7]) << std::endl;
        std::cout << (String(u"\t\tMidline: ") + fontInfo->get_Panose()[8]) << std::endl;
        std::cout << (String(u"\t\tX-Height: ") + fontInfo->get_Panose()[9]) << std::endl;
    }
}
```

## See Also

* Class [FontInfo](../../fontinfo/)
* Class [FontInfoCollection](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
