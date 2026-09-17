---
title: "Aspose::Words::Fonts::StreamFontSource class"
linktitle: "StreamFontSource"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::StreamFontSource class. Classe de base pour la source de police de flux définie par l'utilisateur. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 16000
url: /fr/cpp/aspose.words.fonts/streamfontsource/
---
## StreamFontSource class


Classe de base pour la source de police en flux définie par l'utilisateur. Pour en savoir plus, consultez l'article de documentation [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class StreamFontSource : public Aspose::Words::Fonts::FontSourceBase,
                         public Aspose::Fonts::IFontData
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_CacheKey](./get_cachekey/)() const | La clé de cette source dans le cache. |
| [get_IsEmbedded](./get_isembedded/)() override |  |
| [get_Priority](../fontsourcebase/get_priority/)() const | Renvoie la priorité de la source de police. |
| [get_Type](./get_type/)() override | Renvoie le type de la source de police. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | Appelé lors du traitement de la source de police lorsqu'un problème est détecté pouvant entraîner une perte de fidélité du formatage. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | Renvoie la liste des polices disponibles via cette source. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [OpenFontDataStream](./openfontdatastream/)() | Cette méthode doit ouvrir le flux contenant les données de police à la demande. |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Appelé lors du traitement de la source de police lorsqu'un problème est détecté pouvant entraîner une perte de fidélité du formatage. |
| static [Type](./type/)() |  |
## Remarques


Pour utiliser la source de police en flux, vous devez créer une classe dérivée de [StreamFontSource](./) et fournir une implémentation de la méthode [OpenFontDataStream](./openfontdatastream/).

[OpenFontDataStream](./openfontdatastream/) method could be called several times. For the first time it will be called when Aspose.Words scans the provided font sources to get the list of available fonts. Later it may be called if the font is used in the document to parse the font data and to embed the font data to some output formats.

[StreamFontSource](./) may be useful because it allows to load the font data only when it is required and not to store it in the memory for the [FontSettings](../fontsettings/) lifetime. 
## Voir aussi

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
