---
title: Aspose::Words::Fonts::FontInfoCollection::set_SaveSubsetFonts method
linktitle: set_SaveSubsetFonts
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::FontInfoCollection::set_SaveSubsetFonts method. Specifies whether or not to save a subset of the embedded TrueType fonts with the document. Default value for this property is false.This option works only when EmbedTrueTypeFonts property is set to true in C++.'
type: docs
weight: 17000
url: /cpp/aspose.words.fonts/fontinfocollection/set_savesubsetfonts/
---
## FontInfoCollection::set_SaveSubsetFonts method


Specifies whether or not to save a subset of the embedded TrueType fonts with the document. Default value for this property is **false**.

This option works only when [EmbedTrueTypeFonts](../get_embedtruetypefonts/) property is set to **true**.

```cpp
void Aspose::Words::Fonts::FontInfoCollection::set_SaveSubsetFonts(bool value)
```

## Remarks

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
