---
title: DefaultFontSubstitutionRule.DefaultFontName
linktitle: DefaultFontName
articleTitle: DefaultFontName
second_title: Aspose.Words pour .NET
description: Découvrez comment gérer facilement la règle DefaultFontSubstitutionRule et personnaliser le nom de votre police par défaut pour une flexibilité de conception améliorée.
type: docs
weight: 10
url: /fr/net/aspose.words.fonts/defaultfontsubstitutionrule/defaultfontname/
---
## DefaultFontSubstitutionRule.DefaultFontName property

Obtient ou définit le nom de la police par défaut.

```csharp
public string DefaultFontName { get; set; }
```

## Remarques

La valeur par défaut est « Times New Roman ».

## Exemples

Montre comment définir la règle de substitution de police par défaut.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Obtenez la règle de substitution par défaut dans FontSettings.
// Cette règle remplacera toutes les polices manquantes par « Times New Roman ».
DefaultFontSubstitutionRule defaultFontSubstitutionRule =
    fontSettings.SubstitutionSettings.DefaultFontSubstitution;
Assert.True(defaultFontSubstitutionRule.Enabled);
Assert.AreEqual("Times New Roman", defaultFontSubstitutionRule.DefaultFontName);

// Définissez le substitut de police par défaut sur « Courier New ».
defaultFontSubstitutionRule.DefaultFontName = "Courier New";

// À l'aide d'un générateur de documents, ajoutez du texte dans une police dont nous n'avons pas besoin pour voir la substitution avoir lieu,
// puis restituer le résultat dans un PDF.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Missing Font";
builder.Writeln("Line written in a missing font, which will be substituted with Courier New.");

doc.Save(ArtifactsDir + "FontSettings.DefaultFontSubstitutionRule.pdf");
```

Montre comment spécifier une police par défaut.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Arvo";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();

// Les sources de polices utilisées par le document contiennent la police « Arial », mais pas « Arvo ».
Assert.AreEqual(1, fontSources.Length);
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// Définissez la propriété « DefaultFontName » sur « Courier New » pour,
// lors du rendu du document, appliquez cette police dans tous les cas où une autre police n'est pas disponible.
FontSettings.DefaultInstance.SubstitutionSettings.DefaultFontSubstitution.DefaultFontName = "Courier New";

Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Courier New"));

// Aspose.Words utilisera désormais la police par défaut à la place de toutes les polices manquantes lors de tous les appels de rendu.
doc.Save(ArtifactsDir + "FontSettings.DefaultFontName.pdf");
```

### Voir également

* class [DefaultFontSubstitutionRule](../)
* espace de noms [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../../)
