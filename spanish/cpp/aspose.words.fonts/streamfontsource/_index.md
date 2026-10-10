---
title: "Aspose::Words::Fonts::StreamFontSource class"
linktitle: "StreamFontSource"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fonts::StreamFontSource class. Clase base para la fuente de fuente de flujo definida por el usuario. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 16000
url: /es/cpp/aspose.words.fonts/streamfontsource/
---
## StreamFontSource class


Clase base para la fuente de fuentes de flujo definida por el usuario. Para obtener más información, visite el artículo de documentación [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class StreamFontSource : public Aspose::Words::Fonts::FontSourceBase,
                         public Aspose::Fonts::IFontData
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_CacheKey](./get_cachekey/)() const | La clave de esta fuente en la caché. |
| [get_IsEmbedded](./get_isembedded/)() override |  |
| [get_Priority](../fontsourcebase/get_priority/)() const | Devuelve la prioridad de la fuente de fuentes. |
| [get_Type](./get_type/)() override | Devuelve el tipo de la fuente de fuentes. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | Se llama durante el procesamiento de la fuente de fuentes cuando se detecta un problema que podría resultar en una pérdida de fidelidad del formato. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | Devuelve la lista de fuentes disponibles a través de esta fuente. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [OpenFontDataStream](./openfontdatastream/)() | Este método debería abrir el flujo con los datos de la fuente bajo demanda. |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Se llama durante el procesamiento de la fuente de fuentes cuando se detecta un problema que podría resultar en una pérdida de fidelidad del formato. |
| static [Type](./type/)() |  |
## Observaciones


Para usar la fuente de fuente de flujo, debe crear una clase derivada de [StreamFontSource](./) y proporcionar la implementación del método [OpenFontDataStream](./openfontdatastream/).

[OpenFontDataStream](./openfontdatastream/) method could be called several times. For the first time it will be called when Aspose.Words scans the provided font sources to get the list of available fonts. Later it may be called if the font is used in the document to parse the font data and to embed the font data to some output formats.

[StreamFontSource](./) may be useful because it allows to load the font data only when it is required and not to store it in the memory for the [FontSettings](../fontsettings/) lifetime. 
## Ver también

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
