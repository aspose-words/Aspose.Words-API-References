---
title: "Metodo Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts"
linktitle: "get_SaveSubsetFonts"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts. Specifica se salvare o meno un sottoinsieme dei font TrueType incorporati nel documento. Il valore predefinito per questa proprietà è false. Questa opzione funziona solo quando la proprietà EmbedTrueTypeFonts è impostata su true in C++."
type: docs
weight: 10000
url: /it/cpp/aspose.words.fonts/fontinfocollection/get_savesubsetfonts/
---
## FontInfoCollection::get_SaveSubsetFonts method


Specifica se salvare o meno un sottoinsieme dei font TrueType incorporati nel documento. Il valore predefinito per questa proprietà è **false**. Questa opzione funziona solo quando la proprietà [EmbedTrueTypeFonts](../get_embedtruetypefonts/) è impostata su **true**.

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::get_SaveSubsetFonts() const
```


## Esempi



Mostra come salvare un documento con caratteri TrueType incorporati.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> fontInfos = doc->get_FontInfos();
fontInfos->set_EmbedTrueTypeFonts(embedAllFonts);
fontInfos->set_EmbedSystemFonts(embedAllFonts);
fontInfos->set_SaveSubsetFonts(embedAllFonts);

doc->Save(get_ArtifactsDir() + u"Font.FontInfoCollection.docx");
```

## Vedi anche

* Class [FontInfoCollection](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
