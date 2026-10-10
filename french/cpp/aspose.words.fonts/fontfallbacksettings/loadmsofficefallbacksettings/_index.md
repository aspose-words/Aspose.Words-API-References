---
title: "Aspose::Words::Fonts::FontFallbackSettings::LoadMsOfficeFallbackSettings méthode"
linktitle: "LoadMsOfficeFallbackSettings"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::FontFallbackSettings::LoadMsOfficeFallbackSettings méthode. Charge les paramètres de secours prédéfinis qui imitent le secours de Microsoft Word et utilisent les polices Microsoft Office en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.fonts/fontfallbacksettings/loadmsofficefallbacksettings/
---
## FontFallbackSettings::LoadMsOfficeFallbackSettings method


Charge les paramètres de secours prédéfinis qui imitent le secours de Microsoft Word et utilisent les polices Microsoft Office.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::LoadMsOfficeFallbackSettings()
```


## Exemples



Montre comment charger des paramètres de secours de police pré‑définis.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);
System::SharedPtr<Aspose::Words::Fonts::FontFallbackSettings> fontFallbackSettings = fontSettings->get_FallbackSettings();

// Enregistrez le schéma de police de secours par défaut dans un document XML.
// Par exemple, l'un des éléments a une valeur "0C00-0C7F" pour Range et une valeur correspondante "Vani" pour FallbackFonts.
// Cela signifie que si la police utilisée par un texte ne possède pas de symboles pour le bloc Unicode 0x0C00-0x0C7F,
// le schéma de secours utilisera les symboles de la police de substitution "Vani".
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettings.Default.xml");

// Voici deux schémas de secours de police pré‑définis parmi lesquels nous pouvons choisir.
// 1 - Utilisez le schéma Microsoft Office par défaut, qui est le même que le schéma par défaut :
fontFallbackSettings->LoadMsOfficeFallbackSettings();
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettings.LoadMsOfficeFallbackSettings.xml");

// 2 - Utilisez le schéma construit à partir des polices Google Noto :
fontFallbackSettings->LoadNotoFallbackSettings();
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettings.LoadNotoFallbackSettings.xml");
```

## Voir aussi

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
