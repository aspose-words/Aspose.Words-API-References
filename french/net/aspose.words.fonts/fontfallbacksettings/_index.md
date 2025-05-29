---
title: FontFallbackSettings Class
linktitle: FontFallbackSettings
articleTitle: FontFallbackSettings
second_title: Aspose.Words pour .NET
description: Découvrez Aspose.Words.Fonts.FontFallbackSettings pour des options de secours de police personnalisables, garantissant un rendu de document transparent et un affichage de texte amélioré.
type: docs
weight: 3330
url: /fr/net/aspose.words.fonts/fontfallbacksettings/
---
## FontFallbackSettings class

Spécifie les paramètres du mécanisme de secours des polices.

Pour en savoir plus, visitez le[Travailler avec les polices](https://docs.aspose.com/words/net/working-with-fonts/) article de documentation.

```csharp
public class FontFallbackSettings
```

## Méthodes

| Nom | La description |
| --- | --- |
| [BuildAutomatic](../../aspose.words.fonts/fontfallbacksettings/buildautomatic/)() | Crée automatiquement les paramètres de secours en analysant les polices disponibles. |
| [Load](../../aspose.words.fonts/fontfallbacksettings/load/#load)(*Stream*) | Charge les paramètres de secours à partir du flux XML. |
| [Load](../../aspose.words.fonts/fontfallbacksettings/load/#load_1)(*string*) | Charge les paramètres de secours des polices à partir du fichier XML. |
| [LoadMsOfficeFallbackSettings](../../aspose.words.fonts/fontfallbacksettings/loadmsofficefallbacksettings/)() | Charge les paramètres de secours prédéfinis qui imitent le secours de Microsoft Word et utilisent les polices Microsoft Office. |
| [LoadNotoFallbackSettings](../../aspose.words.fonts/fontfallbacksettings/loadnotofallbacksettings/)() | Charge les paramètres de secours prédéfinis qui utilisent les polices Google Noto. |
| [Save](../../aspose.words.fonts/fontfallbacksettings/save/#save)(*Stream*) | Enregistre les paramètres de secours actuels dans le flux. |
| [Save](../../aspose.words.fonts/fontfallbacksettings/save/#save_1)(*string*) | Enregistre les paramètres de secours actuels dans un fichier. |

## Remarques

Par défaut, les paramètres de secours sont initialisés avec des paramètres prédéfinis qui imitent le secours de Microsoft Word.

## Exemples

Montre comment distribuer les polices de secours sur les plages de codes de caractères Unicode.

```csharp
Document doc = new Document();

FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;
FontFallbackSettings fontFallbackSettings = fontSettings.FallbackSettings;

// Configurez nos paramètres de police pour obtenir des polices uniquement à partir du dossier « MyFonts ».
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// L'appel de la méthode « BuildAutomatic » générera un schéma de secours qui
// distribue les polices accessibles sur autant de codes de caractères Unicode que possible.
// Dans notre cas, il n'a accès qu'à la poignée de polices présentes dans le dossier « MyFonts ».
fontFallbackSettings.BuildAutomatic();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettingsCustom.BuildAutomatic.xml");

// Nous pouvons également charger un schéma de substitution personnalisé à partir d'un fichier comme celui-ci.
// Ce schéma applique la police « AllegroOpen » sur les blocs Unicode « 0000-00ff », la police « AllegroOpen » sur « 0100-024f »,
// et la police « M+ 2m » dans toutes les autres plages que les autres polices du schéma ne couvrent pas.
fontFallbackSettings.Load(MyDir + "Custom font fallback settings.xml");

// Créez un générateur de documents et définissez sa police sur une police qui n'existe dans aucune de nos sources.
// Nos paramètres de police invoqueront le schéma de secours pour les caractères que nous tapons à l'aide de la police non disponible.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Missing Font";

// Utilisez le générateur pour imprimer chaque caractère Unicode de 0x0021 à 0x052F,
// avec des lignes descriptives divisant les blocs Unicode que nous avons définis dans notre schéma de secours de police personnalisé.
for (int i = 0x0021; i < 0x0530; i++)
{
    switch (i)
    {
        case 0x0021:
            builder.Writeln(
                "\n\n0x0021 - 0x00FF: \nBasic Latin/Latin-1 Supplement Unicode blocks in \"AllegroOpen\" font:");
            break;
        case 0x0100:
            builder.Writeln(
                "\n\n0x0100 - 0x024F: \nLatin Extended A/B blocks, mostly in \"AllegroOpen\" font:");
            break;
        case 0x0250:
            builder.Writeln("\n\n0x0250 - 0x052F: \nIPA/Greek/Cyrillic blocks in \"M+ 2m\" font:");
            break;
    }

    builder.Write($"{Convert.ToChar(i)}");
}

doc.Save(ArtifactsDir + "FontSettings.FallbackSettingsCustom.pdf");
```

### Voir également

* espace de noms [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../)
