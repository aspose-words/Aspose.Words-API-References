---
title: FontSettings.FallbackSettings
second_title: Référence de l'API Aspose.Words pour .NET
description: FontSettings propriété. Paramètres liés au mécanisme de secours des polices.
type: docs
weight: 30
url: /fr/net/aspose.words.fonts/fontsettings/fallbacksettings/
---
## FontSettings.FallbackSettings property

Paramètres liés au mécanisme de secours des polices.

```csharp
public FontFallbackSettings FallbackSettings { get; }
```

### Exemples

Montre comment distribuer les polices de secours sur les plages de codes de caractères Unicode.

```csharp
Document doc = new Document();

FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;
FontFallbackSettings fontFallbackSettings = fontSettings.FallbackSettings;

// Configurez nos paramètres de police pour sourcer les polices uniquement à partir du dossier "MyFonts".
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// L'appel de la méthode "BuildAutomatic" générera un schéma de secours qui
// distribue les polices accessibles sur autant de codes de caractères Unicode que possible.
// Dans notre cas, il n'a accès qu'à la poignée de polices contenues dans le dossier "MyFonts".
fontFallbackSettings.BuildAutomatic();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettingsCustom.BuildAutomatic.xml");

// Nous pouvons également charger un schéma de substitution personnalisé à partir d'un fichier comme celui-ci.
// Ce schéma applique la police "AllegroOpen" sur les blocs Unicode "0000-00ff", la police "AllegroOpen" sur "0100-024f",
// et la police "M+ 2m" dans toutes les autres plages que les autres polices du schéma ne couvrent pas.
fontFallbackSettings.Load(MyDir + "Custom font fallback settings.xml");

// Créez un générateur de documents et définissez sa police sur une police qui n'existe dans aucune de nos sources.
// Nos paramètres de police appelleront le schéma de secours pour les caractères que nous tapons en utilisant la police indisponible.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Missing Font";

// Utilisez le constructeur pour imprimer chaque caractère Unicode de 0x0021 à 0x052F,
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

* class [FontFallbackSettings](../../fontfallbacksettings/)
* class [FontSettings](../)
* espace de noms [Aspose.Words.Fonts](../../fontsettings/)
* Assemblée [Aspose.Words](../../../)


