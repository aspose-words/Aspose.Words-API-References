---
title: "Aspose::Words::Fonts::FontFallbackSettings::Save méthode"
linktitle: "Save"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::FontFallbackSettings::Save méthode. Enregistre les paramètres de secours actuels dans un flux en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words.fonts/fontfallbacksettings/save/
---
## FontFallbackSettings::Save(const System::SharedPtr\<System::IO::Stream\>\&) method


Enregistre les paramètres de secours actuels dans un flux.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::Save(const System::SharedPtr<System::IO::Stream> &outputStream)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Flux de sortie. |

## Exemples



Montre comment charger et enregistrer les paramètres de secours de police depuis/vers un flux.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Chargez un document XML qui définit un ensemble de paramètres de secours de police.
{
    auto fontFallbackStream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Font fallback rules.xml", System::IO::FileMode::Open);
    auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
    fontSettings->get_FallbackSettings()->Load(fontFallbackStream);

    doc->set_FontSettings(fontSettings);
}

doc->Save(get_ArtifactsDir() + u"FontSettings.LoadFontFallbackSettingsFromStream.pdf");

// Utilisez un flux pour enregistrer les paramètres de secours de police actuels de notre document sous forme de document XML.
{
    auto fontFallbackStream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"FallbackSettings.xml", System::IO::FileMode::Create);
    doc->get_FontSettings()->get_FallbackSettings()->Save(fontFallbackStream);
}
```

## Voir aussi

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FontFallbackSettings::Save(const System::String\&) method


Enregistre les paramètres de secours actuels dans un fichier.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::Save(const System::String &fileName)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Nom du fichier de sortie. |

## Exemples



Montre comment charger et enregistrer les paramètres de secours de police depuis/vers un document XML dans le système de fichiers local.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Chargez un document XML qui définit un ensemble de paramètres de secours de police.
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_FallbackSettings()->Load(get_MyDir() + u"Font fallback rules.xml");

doc->set_FontSettings(fontSettings);
doc->Save(get_ArtifactsDir() + u"FontSettings.LoadFontFallbackSettingsFromFile.pdf");

// Enregistrez les paramètres de secours de police actuels de notre document sous forme de document XML.
doc->get_FontSettings()->get_FallbackSettings()->Save(get_ArtifactsDir() + u"FallbackSettings.xml");
```

## Voir aussi

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FontFallbackSettings::Save(std::basic_ostream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::Fonts::FontFallbackSettings::Save(std::basic_ostream<CharType, Traits> &outputStream)
```

## Voir aussi

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
