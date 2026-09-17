---
title: "Aspose::Words::Fonts::FontFallbackSettings::LoadNotoFallbackSettings méthode"
linktitle: "LoadNotoFallbackSettings"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::FontFallbackSettings::LoadNotoFallbackSettings méthode. Charge les paramètres de secours prédéfinis qui utilisent les polices Google Noto en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.fonts/fontfallbacksettings/loadnotofallbacksettings/
---
## FontFallbackSettings::LoadNotoFallbackSettings method


Charge les paramètres de secours prédéfinis qui utilisent les polices Google Noto.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::LoadNotoFallbackSettings()
```


## Exemples



Montre comment ajouter des paramètres de secours de police prédéfinis pour les polices Google Noto.
```cpp
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();

// Ce sont des polices gratuites sous licence SIL Open Font License.
// Nous pouvons télécharger les polices ici:
// https://www.google.com/get/noto/#sans-lgc
fontSettings->SetFontsFolder(get_FontsDir() + u"Noto", false);

// Notez que les paramètres prédéfinis n'utilisent que des polices Noto de style Sans avec un poids régulier.
// Certaines des polices Noto utilisent des fonctionnalités typographiques avancées.
// Les polices comportant une typographie avancée peuvent ne pas être rendues correctement car Aspose.Words ne les prend actuellement pas en charge.
fontSettings->get_FallbackSettings()->LoadNotoFallbackSettings();
fontSettings->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(false);
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Noto Sans");

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(fontSettings);
```


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
