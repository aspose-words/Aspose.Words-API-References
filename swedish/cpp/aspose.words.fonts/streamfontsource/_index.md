---
title: "Aspose::Words::Fonts::StreamFontSource-klass"
linktitle: "StreamFontSource"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::StreamFontSource-klass. Bas-klass för användardefinierad strömtypsnittskälla. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 16000
url: /sv/cpp/aspose.words.fonts/streamfontsource/
---
## StreamFontSource class


Basklass för användardefinierad strömteckensnittskälla. För att lära dig mer, besök dokumentationsartikeln [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class StreamFontSource : public Aspose::Words::Fonts::FontSourceBase,
                         public Aspose::Fonts::IFontData
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_CacheKey](./get_cachekey/)() const | Nyckeln för denna källa i cachen. |
| [get_IsEmbedded](./get_isembedded/)() override |  |
| [get_Priority](../fontsourcebase/get_priority/)() const | Returnerar prioriteten för teckensnittskällan. |
| [get_Type](./get_type/)() override | Returnerar typen av teckensnittskälla. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | Kallas under bearbetning av teckensnittskällan när ett problem upptäcks som kan leda till förlust av formateringsnoggrannhet. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | Returnerar en lista över teckensnitt som är tillgängliga via denna källa. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [OpenFontDataStream](./openfontdatastream/)() | Denna metod bör öppna strömmen med typsnittsdata på begäran. |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Kallas under bearbetning av teckensnittskällan när ett problem upptäcks som kan leda till förlust av formateringsnoggrannhet. |
| static [Type](./type/)() |  |
## Anmärkningar


För att använda strömtypsnittskällan bör du skapa en avledd klass från [StreamFontSource](./) och tillhandahålla en implementation av metoden [OpenFontDataStream](./openfontdatastream/).

[OpenFontDataStream](./openfontdatastream/) method could be called several times. For the first time it will be called when Aspose.Words scans the provided font sources to get the list of available fonts. Later it may be called if the font is used in the document to parse the font data and to embed the font data to some output formats.

[StreamFontSource](./) may be useful because it allows to load the font data only when it is required and not to store it in the memory for the [FontSettings](../fontsettings/) lifetime. 
## Se även

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
