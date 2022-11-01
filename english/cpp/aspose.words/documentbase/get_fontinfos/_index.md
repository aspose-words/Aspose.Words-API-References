---
title: get_FontInfos
second_title: Aspose.Words for C++ API Reference
description: Provides access to properties of fonts used in this document.
type: docs
weight: 27
url: /cpp/aspose.words/documentbase/get_fontinfos/
---
## DocumentBase.get_FontInfos method


Provides access to properties of fonts used in this document.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> Aspose::Words::DocumentBase::get_FontInfos() const
```


This collection of font definitions is loaded as is from the document. [Font](../../font/) definitions might be optional, missing or incomplete in some documents.

Do not rely on this collection to ascertain that a particular font is used in the document. You should only use this collection to get information about fonts that might be used in the document.

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


Shows how to save a document with embedded TrueType fonts. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Document.docx");

SharedPtr<Aspose::Words::Fonts::FontInfoCollection> fontInfos = doc->get_FontInfos();
fontInfos->set_EmbedTrueTypeFonts(embedAllFonts);
fontInfos->set_EmbedSystemFonts(embedAllFonts);
fontInfos->set_SaveSubsetFonts(embedAllFonts);

doc->Save(ArtifactsDir + u"Font.FontInfoCollection.docx");

if (embedAllFonts)
{
    ASSERT_LT(25000, MakeObject<System::IO::FileInfo>(ArtifactsDir + u"Font.FontInfoCollection.docx")->get_Length());
}
else
{
    ASSERT_GE(15000, MakeObject<System::IO::FileInfo>(ArtifactsDir + u"Font.FontInfoCollection.docx")->get_Length());
}
```

