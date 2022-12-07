---
title: get_IsTrueType
second_title: Aspose.Words for C++ API Reference
description: Indicates that this font is a TrueType or OpenType font as opposed to a raster or vector font. Default is true.
type: docs
weight: 53
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
auto doc = MakeObject<Document>(MyDir + u"Embedded font.docx");

SharedPtr<Aspose::Words::Fonts::FontInfoCollection> allFonts = doc->get_FontInfos();

// Print all the used and unused fonts in the document.
for (int i = 0; i < allFonts->get_Count(); i++)
{
    std::cout << "Font index #" << i << std::endl;
    std::cout << "\tName: " << allFonts->idx_get(i)->get_Name() << std::endl;
    std::cout << "\tIs " << (allFonts->idx_get(i)->get_IsTrueType() ? String(u"") : String(u"not ")) << "a trueType font" << std::endl;
}
```

## See Also

* Class [FontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words](../../../)
