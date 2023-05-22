---
title: Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts method
linktitle: get_EmbedTrueTypeFonts
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts method. Specifies whether or not to embed TrueType fonts in a document when it is saved. Default value for this property is false in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words.fonts/fontinfocollection/get_embedtruetypefonts/
---
## FontInfoCollection::get_EmbedTrueTypeFonts method


Specifies whether or not to embed TrueType fonts in a document when it is saved. Default value for this property is **false**.

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts() const
```

## Remarks


Embedding TrueType fonts allows others to view the document with the same fonts that were used to create it, but may substantially increase the document size.

This option works for DOC, DOCX and RTF formats only.

## Examples



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

## See Also

* Class [FontInfoCollection](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
