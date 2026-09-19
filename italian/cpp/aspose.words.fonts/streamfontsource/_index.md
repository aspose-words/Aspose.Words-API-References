---
title: "Aspose::Words::Fonts::StreamFontSource class"
linktitle: "StreamFontSource"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fonts::StreamFontSource class. Classe base per l'origine del font stream definita dall'utente. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 16000
url: /it/cpp/aspose.words.fonts/streamfontsource/
---
## StreamFontSource class


Classe base per la sorgente di caratteri stream definita dall'utente. Per saperne di più, visita l'articolo di documentazione [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class StreamFontSource : public Aspose::Words::Fonts::FontSourceBase,
                         public Aspose::Fonts::IFontData
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_CacheKey](./get_cachekey/)() const | La chiave di questa origine nella cache. |
| [get_IsEmbedded](./get_isembedded/)() override |  |
| [get_Priority](../fontsourcebase/get_priority/)() const | Restituisce la priorità della sorgente del font. |
| [get_Type](./get_type/)() override | Restituisce il tipo della sorgente del font. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | Chiamato durante l'elaborazione della sorgente del font quando viene rilevato un problema che potrebbe causare una perdita di fedeltà della formattazione. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | Restituisce l'elenco dei font disponibili tramite questa sorgente. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [OpenFontDataStream](./openfontdatastream/)() | Questo metodo dovrebbe aprire lo stream con i dati del font su richiesta. |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Chiamato durante l'elaborazione della sorgente del font quando viene rilevato un problema che potrebbe causare una perdita di fedeltà della formattazione. |
| static [Type](./type/)() |  |
## Note


Per utilizzare la sorgente del font stream dovresti creare una classe derivata da [StreamFontSource](./) e fornire l'implementazione del metodo [OpenFontDataStream](./openfontdatastream/).

[OpenFontDataStream](./openfontdatastream/) method could be called several times. For the first time it will be called when Aspose.Words scans the provided font sources to get the list of available fonts. Later it may be called if the font is used in the document to parse the font data and to embed the font data to some output formats.

[StreamFontSource](./) may be useful because it allows to load the font data only when it is required and not to store it in the memory for the [FontSettings](../fontsettings/) lifetime. 
## Vedi anche

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
