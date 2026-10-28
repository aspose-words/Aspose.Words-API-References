---
title: Aspose::Words::Fonts::FontInfoCollection::set_EmbedSystemFonts method
linktitle: set_EmbedSystemFonts
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::FontInfoCollection::set_EmbedSystemFonts method. Specifies whether or not to embed System fonts into the document. Default value for this property is false.This option works only when EmbedTrueTypeFonts option is set to true in C++.'
type: docs
weight: 15000
url: /cpp/aspose.words.fonts/fontinfocollection/set_embedsystemfonts/
---
## FontInfoCollection::set_EmbedSystemFonts method


Specifies whether or not to embed System fonts into the document. Default value for this property is **false**.

This option works only when [EmbedTrueTypeFonts](../get_embedtruetypefonts/) option is set to **true**.

```cpp
void Aspose::Words::Fonts::FontInfoCollection::set_EmbedSystemFonts(bool value)
```

## Remarks


 Setting this property to **true** is useful if the user is on an East Asian system and wants to create a document that is readable by others who do not have fonts for that language on their system. For example, a user on a Japanese system could choose to embed the fonts in a document so that the Japanese document would be readable on all systems. 

This option works for DOC, DOCX and RTF formats only.
## Examples


Shows how to save a document with embedded TrueType fonts.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Document.docx"));

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> fontInfos = doc->get_FontInfos();
fontInfos->set_EmbedTrueTypeFonts(embedAllFonts);
fontInfos->set_EmbedSystemFonts(embedAllFonts);
fontInfos->set_SaveSubsetFonts(embedAllFonts);

doc->Save(get_ArtifactsDir() + u"Font.FontInfoCollection.docx");
```
## See Also

* Class [FontInfoCollection](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
