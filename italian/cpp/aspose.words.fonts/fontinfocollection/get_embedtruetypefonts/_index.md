---
title: "Metodo Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts"
linktitle: "get_EmbedTrueTypeFonts"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts. Specifica se incorporare o meno i font TrueType in un documento al momento del salvataggio. Il valore predefinito per questa proprietà è false in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words.fonts/fontinfocollection/get_embedtruetypefonts/
---
## FontInfoCollection::get_EmbedTrueTypeFonts method


Specifica se incorporare o meno i caratteri TrueType in un documento al momento del salvataggio. Il valore predefinito per questa proprietà è **false**.

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::get_EmbedTrueTypeFonts() const
```

## Note


L'incorporamento dei font TrueType consente ad altri di visualizzare il documento con gli stessi font utilizzati per crearlo, ma può aumentare notevolmente le dimensioni del documento.

Questa opzione funziona solo per i formati DOC, DOCX e RTF.

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
