---
title: "Metodo Aspose::Words::DocumentBase::get_FontInfos"
linktitle: "get_FontInfos"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::DocumentBase::get_FontInfos. Fornisce l'accesso alle proprietà dei caratteri utilizzati in questo documento in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words/documentbase/get_fontinfos/
---
## DocumentBase::get_FontInfos method


Fornisce l'accesso alle proprietà dei caratteri utilizzati in questo documento.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> Aspose::Words::DocumentBase::get_FontInfos() const
```

## Note


Questa raccolta di definizioni di caratteri è caricata così com'è dal documento. Le definizioni di [Font](../../font/) potrebbero essere opzionali, mancanti o incomplete in alcuni documenti.

Non fare affidamento su questa raccolta per accertare che un determinato carattere sia utilizzato nel documento. Dovresti usarla solo per ottenere informazioni sui caratteri che potrebbero essere utilizzati nel documento.

## Esempi



Mostra come stampare i dettagli dei caratteri presenti in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font.docx");

System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> allFonts = doc->get_FontInfos();

// Stampa tutti i caratteri utilizzati e non utilizzati nel documento.
for (int32_t i = 0; i < allFonts->get_Count(); i++)
{
    std::cout << System::String::Format(u"Font index #{0}", i) << std::endl;
    std::cout << System::String::Format(u"\tName: {0}", allFonts->idx_get(i)->get_Name()) << std::endl;
    std::cout << System::String::Format(u"\tIs {0}a trueType font", (allFonts->idx_get(i)->get_IsTrueType() ? System::String(u"") : System::String(u"not "))) << std::endl;
}
```


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

* Class [FontInfoCollection](../../../aspose.words.fonts/fontinfocollection/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
