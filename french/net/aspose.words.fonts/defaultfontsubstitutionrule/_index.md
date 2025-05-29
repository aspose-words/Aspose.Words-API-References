---
title: DefaultFontSubstitutionRule Class
linktitle: DefaultFontSubstitutionRule
articleTitle: DefaultFontSubstitutionRule
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Fonts.DefaultFontSubstitutionRule pour une gestion fluide des polices et une mise en forme optimisée des documents. Optimisez votre flux de travail dès aujourd'hui !
type: docs
weight: 3250
url: /fr/net/aspose.words.fonts/defaultfontsubstitutionrule/
---
## DefaultFontSubstitutionRule class

Règle de substitution de police par défaut.

Pour en savoir plus, visitez le[Travailler avec les polices](https://docs.aspose.com/words/net/working-with-fonts/) article de documentation.

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

### Voir également

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* espace de noms [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../)
