---
title: Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts method
linktitle: get_SaveSubsetFonts
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts method. Specifies whether or not to save a subset of the embedded TrueType fonts with the document. Default value for this property is false. This option works only when EmbedTrueTypeFonts property is set to true in C++.'
type: docs
weight: 10000
url: /cpp/aspose.words.fonts/fontinfocollection/get_savesubsetfonts/
---
## FontInfoCollection::get_SaveSubsetFonts method


Specifies whether or not to save a subset of the embedded TrueType fonts with the document. Default value for this property is **false**. This option works only when [EmbedTrueTypeFonts](../get_embedtruetypefonts/) property is set to **true**.

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts() const
```


## Examples



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

* Class [FontInfoCollection](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
