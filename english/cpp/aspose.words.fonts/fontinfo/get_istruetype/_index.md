---
title: Aspose::Words::Fonts::FontInfo::get_IsTrueType method
linktitle: get_IsTrueType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::FontInfo::get_IsTrueType method. Indicates that this font is a TrueType or OpenType font as opposed to a raster or vector font. Default is true in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.fonts/fontinfo/get_istruetype/
---
## FontInfo::get_IsTrueType method


Indicates that this font is a TrueType or OpenType font as opposed to a raster or vector font. Default is **true**.

```cpp
bool Aspose::Words::Fonts::FontInfo::get_IsTrueType() const
```


## Examples



Shows how to print the details of what fonts are present in a document. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> allFonts = doc->get_FontInfos();

// Print all the used and unused fonts in the document.
for (int32_t i = 0; i < allFonts->get_Count(); i++)
{
    std::cout << System::String::Format(u"Font index #{0}", i) << std::endl;
    std::cout << System::String::Format(u"\tName: {0}", allFonts->idx_get(i)->get_Name()) << std::endl;
    std::cout << System::String::Format(u"\tIs {0}a trueType font", (allFonts->idx_get(i)->get_IsTrueType() ? System::String(u"") : System::String(u"not "))) << std::endl;
}
```

## See Also

* Class [FontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
