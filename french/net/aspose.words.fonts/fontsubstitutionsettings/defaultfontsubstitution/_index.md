---
title: FontSubstitutionSettings.DefaultFontSubstitution
linktitle: DefaultFontSubstitution
articleTitle: DefaultFontSubstitution
second_title: Aspose.Words pour .NET
description: FontSubstitutionSettings DefaultFontSubstitution propriété. Paramètres liés à la règle de substitution de police par défaut en C#.
type: docs
weight: 10
url: /fr/net/aspose.words.fonts/fontsubstitutionsettings/defaultfontsubstitution/
---
## FontSubstitutionSettings.DefaultFontSubstitution property

Paramètres liés à la règle de substitution de police par défaut.

```csharp
public DefaultFontSubstitutionRule DefaultFontSubstitution { get; }
```

## Exemples

Montre comment définir la règle de substitution de police par défaut.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Récupère la règle de substitution par défaut dans FontSettings.
// Cette règle remplacera toutes les polices manquantes par "Times New Roman".
DefaultFontSubstitutionRule defaultFontSubstitutionRule =
    fontSettings.SubstitutionSettings.DefaultFontSubstitution;
Assert.True(defaultFontSubstitutionRule.Enabled);
Assert.AreEqual("Times New Roman", defaultFontSubstitutionRule.DefaultFontName);

// Définissez le substitut de police par défaut sur "Courier New".
defaultFontSubstitutionRule.DefaultFontName = "Courier New";

// A l'aide d'un générateur de documents, on ajoute du texte dans une police dont on n'est pas obligé pour voir la substitution s'effectuer,
// puis affiche le résultat dans un PDF.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Missing Font";
builder.Writeln("Line written in a missing font, which will be substituted with Courier New.");

doc.Save(ArtifactsDir + "FontSettings.DefaultFontSubstitutionRule.pdf");
```

### Voir également

* class [DefaultFontSubstitutionRule](../../defaultfontsubstitutionrule/)
* class [FontSubstitutionSettings](../)
* espace de noms [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../../)
