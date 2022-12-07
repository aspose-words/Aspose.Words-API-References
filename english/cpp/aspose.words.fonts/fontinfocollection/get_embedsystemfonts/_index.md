---
title: get_EmbedSystemFonts
second_title: Aspose.Words for C++ API Reference
description: Specifies whether or not to embed System fonts into the document. Default value for this property is false. This option works only when EmbedTrueTypeFonts option is set to true.
type: docs
weight: 92
url: /cpp/aspose.words.fonts/fontinfocollection/get_embedsystemfonts/
---
## FontInfoCollection::get_EmbedSystemFonts method


Specifies whether or not to embed System fonts into the document. Default value for this property is **false**. This option works only when [EmbedTrueTypeFonts](../get_embedtruetypefonts/) option is set to **true**.

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts() const
```

## Remarks


Setting this property to **true** is useful if the user is on an East Asian system and wants to create a document that is readable by others who do not have fonts for that language on their system. For example, a user on a Japanese system could choose to embed the fonts in a document so that the Japanese document would be readable on all systems.

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
* Library [Aspose.Words](../../../)
