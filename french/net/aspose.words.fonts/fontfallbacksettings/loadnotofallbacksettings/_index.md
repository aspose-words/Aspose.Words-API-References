---
title: FontFallbackSettings.LoadNotoFallbackSettings
second_title: Référence de l'API Aspose.Words pour .NET
description: FontFallbackSettings méthode. Charge les paramètres de secours prédéfinis qui utilisent les polices Google Noto.
type: docs
weight: 40
url: /fr/net/aspose.words.fonts/fontfallbacksettings/loadnotofallbacksettings/
---
## FontFallbackSettings.LoadNotoFallbackSettings method

Charge les paramètres de secours prédéfinis qui utilisent les polices Google Noto.

```csharp
public void LoadNotoFallbackSettings()
```

### Exemples

Montre comment ajouter des paramètres de secours de police prédéfinis pour les polices Google Noto.

```csharp
FontSettings fontSettings = new FontSettings();

// Ce sont des polices gratuites sous licence SIL Open Font License.
// Nous pouvons télécharger les polices ici :
// https://www.google.com/get/noto/#sans-lgc
fontSettings.SetFontsFolder(FontsDir + "Noto", false);

 // Notez que les paramètres prédéfinis utilisent uniquement des polices Noto de style Sans avec une épaisseur normale.
// Certaines polices Noto utilisent des fonctionnalités typographiques avancées.
// Les polices présentant une typographie avancée peuvent ne pas être rendues correctement car Aspose.Words ne les prend actuellement pas en charge.
fontSettings.FallbackSettings.LoadNotoFallbackSettings();
fontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = false;
fontSettings.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Noto Sans";

Document doc = new Document();
doc.FontSettings = fontSettings;
```

Montre comment charger les paramètres de police de secours prédéfinis.

```csharp
Document doc = new Document();

FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;
FontFallbackSettings fontFallbackSettings = fontSettings.FallbackSettings;

// Enregistrez le jeu de polices de secours par défaut dans un document XML.
// Par exemple, l'un des éléments a une valeur de « 0C00-0C7F » pour Range et une valeur « Vani » correspondante pour FallbackFonts.
// Cela signifie que si la police utilisée par un texte ne comporte pas de symboles pour le bloc Unicode 0x0C00-0x0C7F,
// le schéma de secours utilisera les symboles du substitut de police "Vani".
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.Default.xml");

// Vous trouverez ci-dessous deux modèles de polices de secours prédéfinis parmi lesquels nous pouvons choisir.
// 1 - Utiliser le schéma Microsoft Office par défaut, qui est le même que celui par défaut :
fontFallbackSettings.LoadMsOfficeFallbackSettings();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.LoadMsOfficeFallbackSettings.xml");

// 2 - Utiliser le schéma construit à partir des polices Google Noto :
fontFallbackSettings.LoadNotoFallbackSettings();
fontFallbackSettings.Save(ArtifactsDir + "FontSettings.FallbackSettings.LoadNotoFallbackSettings.xml");
```

### Voir également

* class [FontFallbackSettings](../)
* espace de noms [Aspose.Words.Fonts](../../fontfallbacksettings/)
* Assemblée [Aspose.Words](../../../)


