---
title: FontFamily
second_title: Aspose.Words for C++ API Reference
description: Represents the font family.
type: docs
weight: 261
url: /cpp/aspose.words.fonts/fontfamily/
---
## FontFamily enum


Represents the font family.

### Values

| Name | Value | Description |
| --- | --- | --- |
| Auto | 0 | Specifies a generic family name. This name is used when information about a font does not exist or does not matter. The default font is used. |
| Roman | 1 | Specifies a proportional font with serifs. An example is Times New Roman. |
| Swiss | 2 | Specifies a proportional font without serifs. An example is Arial. |
| Modern | 3 | Specifies a monospace font with or without serifs. Monospace fonts are usually modern; examples include Pica, Elite, and Courier New. |
| Script | 4 | Specifies a font that is designed to look like handwriting; examples include Script and Cursive. |
| Decorative | 5 | Specifies a novelty font. An example is Old English. |


A font family is a set of fonts having common stroke width and serif characteristics.

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

