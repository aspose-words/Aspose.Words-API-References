---
title: Aspose::Words::Fonts::FontInfo::get_Charset method
linktitle: get_Charset
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::FontInfo::get_Charset method. Gets or sets the character set for the font in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words.fonts/fontinfo/get_charset/
---
## FontInfo::get_Charset method


Gets or sets the character set for the font.

```cpp
int32_t Aspose::Words::Fonts::FontInfo::get_Charset()
```


## Examples



Shows how to access and print details of each font in a document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Document.docx"));

System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Fonts::FontInfo>>> fontCollectionEnumerator = doc->get_FontInfos()->GetEnumerator();
while (fontCollectionEnumerator->MoveNext())
{
    System::SharedPtr<Aspose::Words::Fonts::FontInfo> fontInfo = fontCollectionEnumerator->get_Current();
    if (fontInfo != nullptr)
    {
        System::Console::WriteLine(System::String(u"Font name: ") + fontInfo->get_Name());

        // Alt names are usually blank.
        System::Console::WriteLine(System::String(u"Alt name: ") + fontInfo->get_AltName());
        System::Console::WriteLine(System::String(u"\t- Family: ") + System::ObjectExt::ToString(fontInfo->get_Family()));
        System::Console::WriteLine(System::String(u"\t- ") + (fontInfo->get_IsTrueType() ? System::String(u"Is TrueType") : System::String(u"Is not TrueType")));
        System::Console::WriteLine(System::String(u"\t- Pitch: ") + System::ObjectExt::ToString(fontInfo->get_Pitch()));
        System::Console::WriteLine(System::String(u"\t- Charset: ") + fontInfo->get_Charset());
        System::Console::WriteLine(u"\t- Panose:");
        System::Console::WriteLine(System::String(u"\t\tFamily Kind: ") + fontInfo->get_Panose()[0]);
        System::Console::WriteLine(System::String(u"\t\tSerif Style: ") + fontInfo->get_Panose()[1]);
        System::Console::WriteLine(System::String(u"\t\tWeight: ") + fontInfo->get_Panose()[2]);
        System::Console::WriteLine(System::String(u"\t\tProportion: ") + fontInfo->get_Panose()[3]);
        System::Console::WriteLine(System::String(u"\t\tContrast: ") + fontInfo->get_Panose()[4]);
        System::Console::WriteLine(System::String(u"\t\tStroke Variation: ") + fontInfo->get_Panose()[5]);
        System::Console::WriteLine(System::String(u"\t\tArm Style: ") + fontInfo->get_Panose()[6]);
        System::Console::WriteLine(System::String(u"\t\tLetterform: ") + fontInfo->get_Panose()[7]);
        System::Console::WriteLine(System::String(u"\t\tMidline: ") + fontInfo->get_Panose()[8]);
        System::Console::WriteLine(System::String(u"\t\tX-Height: ") + fontInfo->get_Panose()[9]);
    }
}
```

## See Also

* Class [FontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
