---
title: Aspose::Words::DocumentBase::get_FontInfos method
linktitle: get_FontInfos
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBase::get_FontInfos method. Provides access to properties of fonts used in this document in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words/documentbase/get_fontinfos/
---
## DocumentBase::get_FontInfos method


Provides access to properties of fonts used in this document.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> Aspose::Words::DocumentBase::get_FontInfos() const
```

## Remarks


This collection of font definitions is loaded as is from the document. [Font](../../font/) definitions might be optional, missing or incomplete in some documents.

Do not rely on this collection to ascertain that a particular font is used in the document. You should only use this collection to get information about fonts that might be used in the document.

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


Shows how to save a document with embedded TrueType fonts. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> fontInfos = doc->get_FontInfos();
fontInfos->set_EmbedTrueTypeFonts(embedAllFonts);
fontInfos->set_EmbedSystemFonts(embedAllFonts);
fontInfos->set_SaveSubsetFonts(embedAllFonts);

doc->Save(get_ArtifactsDir() + u"Font.FontInfoCollection.docx");
```

## See Also

* Class [FontInfoCollection](../../../aspose.words.fonts/fontinfocollection/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
