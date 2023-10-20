---
title: Document.FontSettings
linktitle: FontSettings
articleTitle: FontSettings
second_title: Aspose.Words pour .NET
description: Document FontSettings propriété. Obtient ou définit les paramètres de police du document en C#.
type: docs
weight: 140
url: /fr/net/aspose.words/document/fontsettings/
---
## Document.FontSettings property

Obtient ou définit les paramètres de police du document.

```csharp
public FontSettings FontSettings { get; set; }
```

## Remarques

Cette propriété permet de spécifier les paramètres de police par document. Si réglé sur`nul` , paramètres de police statique par défaut [`DefaultInstance`](../../../aspose.words.fonts/fontsettings/defaultinstance/) sera utilisé.

La valeur par défaut est`nul`.

## Exemples

Montre comment définir les règles de substitution de police.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();

// Les sources de polices par défaut contiennent la première police utilisée par le document.
Assert.AreEqual(1, fontSources.Length);
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// La deuxième police, "Amethysta", n'est pas disponible.
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// On peut configurer une table de substitution de polices qui détermine
// quelles polices Aspose.Words utilisera comme substituts aux polices indisponibles.
// Définissez deux polices de substitution pour "Amethysta" : "Arvo" et "Courier New".
// Si le premier substitut n'est pas disponible, Aspose.Words tente d'utiliser le deuxième substitut, et ainsi de suite.
doc.FontSettings = new FontSettings();
doc.FontSettings.SubstitutionSettings.TableSubstitution.SetSubstitutes(
    "Amethysta", new[] {"Arvo", "Courier New"});

 // "Amethysta" n'est pas disponible et la règle de substitution stipule que la première police à utiliser comme substitut est "Arvo".
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

 // "Arvo" n'est pas non plus disponible, mais "Courier New" l'est.
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Courier New"));

// Le document de sortie affichera le texte qui utilise la police "Amethysta" formatée avec "Courier New".
doc.Save(ArtifactsDir + "FontSettings.TableSubstitution.pdf");
```

### Voir également

* class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* class [Document](../)
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
