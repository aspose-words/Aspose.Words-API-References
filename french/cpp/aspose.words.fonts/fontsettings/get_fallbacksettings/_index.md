---
title: "Aspose::Words::Fonts::FontSettings::get_FallbackSettings méthode"
linktitle: "get_FallbackSettings"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fonts::FontSettings::get_FallbackSettings méthode. Paramètres liés au mécanisme de secours de police en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.fonts/fontsettings/get_fallbacksettings/
---
## FontSettings::get_FallbackSettings method


[Settings](../../../aspose.words.settings/) related to font fallback mechanism.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontFallbackSettings> Aspose::Words::Fonts::FontSettings::get_FallbackSettings() const
```


## Exemples



Montre comment répartir les polices de secours sur les plages de codes de caractères Unicode.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);
System::SharedPtr<Aspose::Words::Fonts::FontFallbackSettings> fontFallbackSettings = fontSettings->get_FallbackSettings();

// Configurez nos paramètres de police pour obtenir les polices uniquement depuis le dossier "MyFonts".
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false);
fontSettings->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

// Appeler la méthode "BuildAutomatic" générera un schéma de secours qui
// répartit les polices accessibles sur le plus grand nombre possible de codes de caractères Unicode.
// Dans notre cas, il n'a accès qu'à une poignée de polices dans le dossier "MyFonts".
fontFallbackSettings->BuildAutomatic();
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettingsCustom.BuildAutomatic.xml");

// Nous pouvons également charger un schéma de substitution personnalisé à partir d'un fichier comme celui-ci.
// Ce schéma applique la police "AllegroOpen" sur les blocs Unicode "0000-00ff", la police "AllegroOpen" sur "0100-024f",
// et la police "M+ 2m" dans toutes les autres plages que les autres polices du schéma ne couvrent pas.
fontFallbackSettings->Load(get_MyDir() + u"Custom font fallback settings.xml");

// Créez un constructeur de document et définissez sa police sur une qui n'existe dans aucune de nos sources.
// Nos paramètres de police invoqueront le schéma de secours pour les caractères que nous tapons avec la police indisponible.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Name(u"Missing Font");

// Utilisez le constructeur pour imprimer chaque caractère Unicode de 0x0021 à 0x052F,
// avec des lignes descriptives divisant les blocs Unicode que nous avons définis dans notre schéma de secours de police personnalisé.
for (int32_t i = 0x0021; i < 0x0530; i++)
{
    switch (i)
    {
        case 0x0021:
            builder->Writeln(u"\n\n0x0021 - 0x00FF: \nBasic Latin/Latin-1 Supplement Unicode blocks in \"AllegroOpen\" font:");
            break;

        case 0x0100:
            builder->Writeln(u"\n\n0x0100 - 0x024F: \nLatin Extended A/B blocks, mostly in \"AllegroOpen\" font:");
            break;

        case 0x0250:
            builder->Writeln(u"\n\n0x0250 - 0x052F: \nIPA/Greek/Cyrillic blocks in \"M+ 2m\" font:");
            break;

    }

    builder->Write(System::String::Format(u"{0}", System::Convert::ToChar(i)));
}

doc->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettingsCustom.pdf");
```

## Voir aussi

* Class [FontFallbackSettings](../../fontfallbacksettings/)
* Class [FontSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
