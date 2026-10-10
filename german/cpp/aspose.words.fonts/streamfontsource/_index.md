---
title: "Aspose::Words::Fonts::StreamFontSource class"
linktitle: "StreamFontSource"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::StreamFontSource class. Basisklasse für benutzerdefinierte Stream‑Schriftquellen. Weitere Informationen finden Sie im Dokumentationsartikel zu C++."
type: docs
weight: 16000
url: /de/cpp/aspose.words.fonts/streamfontsource/
---
## StreamFontSource class


Basisklasse für benutzerdefinierte Stream-Schriftquellen. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class StreamFontSource : public Aspose::Words::Fonts::FontSourceBase,
                         public Aspose::Fonts::IFontData
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_CacheKey](./get_cachekey/)() const | Der Schlüssel dieser Quelle im Cache. |
| [get_IsEmbedded](./get_isembedded/)() override |  |
| [get_Priority](../fontsourcebase/get_priority/)() const | Gibt die Priorität der Schriftquellen zurück. |
| [get_Type](./get_type/)() override | Gibt den Typ der Schriftquelle zurück. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | Wird während der Verarbeitung der Schriftquelle aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Formatierungsgenauigkeit führen könnte. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | Gibt eine Liste der über diese Quelle verfügbaren Schriften zurück. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [OpenFontDataStream](./openfontdatastream/)() | Diese Methode sollte den Stream mit Schriftartdaten bei Bedarf öffnen. |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Wird während der Verarbeitung der Schriftquelle aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Formatierungsgenauigkeit führen könnte. |
| static [Type](./type/)() |  |
## Hinweise


Um die Stream‑Schriftquelle zu verwenden, sollten Sie eine abgeleitete Klasse von [StreamFontSource](./) erstellen und eine Implementierung der Methode [OpenFontDataStream](./openfontdatastream/) bereitstellen.

[OpenFontDataStream](./openfontdatastream/) method could be called several times. For the first time it will be called when Aspose.Words scans the provided font sources to get the list of available fonts. Later it may be called if the font is used in the document to parse the font data and to embed the font data to some output formats.

[StreamFontSource](./) may be useful because it allows to load the font data only when it is required and not to store it in the memory for the [FontSettings](../fontsettings/) lifetime. 
## Siehe auch

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
