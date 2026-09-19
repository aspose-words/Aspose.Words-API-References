---
title: "Metodo Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts"
linktitle: "get_EmbedSystemFonts"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts. Specifica se incorporare o meno i font di sistema nel documento. Il valore predefinito per questa proprietà è false. Questa opzione funziona solo quando l'opzione EmbedTrueTypeFonts è impostata su true in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words.fonts/fontinfocollection/get_embedsystemfonts/
---
## FontInfoCollection::get_EmbedSystemFonts method


Specifica se incorporare o meno i font di sistema nel documento. Il valore predefinito per questa proprietà è **false**. Questa opzione funziona solo quando l'opzione [EmbedTrueTypeFonts](../get_embedtruetypefonts/) è impostata su **true**.

```cpp
bool Aspose::Words::Fonts::FontInfoCollection::get_EmbedSystemFonts() const
```

## Note


Impostare questa proprietà su **true** è utile se l'utente utilizza un sistema dell'Asia orientale e desidera creare un documento leggibile da altri che non hanno i font per quella lingua sul proprio sistema. Ad esempio, un utente su un sistema giapponese potrebbe scegliere di incorporare i font in un documento affinché il documento giapponese sia leggibile su tutti i sistemi.

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
