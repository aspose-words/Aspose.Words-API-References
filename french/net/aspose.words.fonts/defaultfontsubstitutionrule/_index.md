---
title: DefaultFontSubstitutionRule Class
linktitle: DefaultFontSubstitutionRule
articleTitle: DefaultFontSubstitutionRule
second_title: Aspose.Words pour .NET
description: Aspose.Words.Fonts.DefaultFontSubstitutionRule classe. Règle de substitution de police par défaut en C#.
type: docs
weight: 2840
url: /fr/net/aspose.words.fonts/defaultfontsubstitutionrule/
---
## DefaultFontSubstitutionRule class

Règle de substitution de police par défaut.

Pour en savoir plus, visitez le[Travailler avec des polices](https://docs.aspose.com/words/net/working-with-fonts/) article documentaire.

```csharp
public class DefaultFontSubstitutionRule : FontSubstitutionRule
```

## Propriétés

| Nom | La description |
| --- | --- |
| [DefaultFontName](../../aspose.words.fonts/defaultfontsubstitutionrule/defaultfontname/) { get; set; } | Obtient ou définit le nom de la police par défaut. |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | Spécifie si la règle est activée ou non. |

## Remarques

Cette règle définit un nom de police par défaut unique à utiliser pour la substitution si la police d'origine n'est pas disponible.

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

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* espace de noms [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../)
