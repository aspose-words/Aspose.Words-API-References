---
title: TableSubstitutionRule.SetSubstitutes
linktitle: SetSubstitutes
articleTitle: SetSubstitutes
second_title: Aspose.Words pour .NET
description: Découvrez comment personnaliser les noms de polices avec la méthode TableSubstitutionRule SetSubstitutes. Améliorez votre design avec des solutions typographiques sur mesure !
type: docs
weight: 80
url: /fr/net/aspose.words.fonts/tablesubstitutionrule/setsubstitutes/
---
## TableSubstitutionRule.SetSubstitutes method

Remplacer les noms de police de substitution par le nom de police d'origine donné.

```csharp
public void SetSubstitutes(string originalFontName, params string[] substituteFontNames)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| originalFontName | String | Nom de la police d'origine. |
| substituteFontNames | String[] | Liste de noms de polices alternatifs. |

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

// Nous pouvons configurer une table de substitution de polices qui détermine
// quelles polices Aspose.Words utilisera comme substituts aux polices indisponibles.
// Définissez deux polices de substitution pour « Amethysta » : « Arvo » et « Courier New ».
// Si le premier substitut n'est pas disponible, Aspose.Words tente d'utiliser le deuxième substitut, et ainsi de suite.
doc.FontSettings = new FontSettings();
doc.FontSettings.SubstitutionSettings.TableSubstitution.SetSubstitutes(
    "Amethysta", new[] {"Arvo", "Courier New"});

 // "Amethysta" n'est pas disponible et la règle de substitution stipule que la première police à utiliser comme substitut est "Arvo".
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

 // "Arvo" n'est pas non plus disponible, mais "Courier New" l'est.
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Courier New"));

// Le document de sortie affichera le texte qui utilise la police « Amethysta » formatée avec « Courier New ».
doc.Save(ArtifactsDir + "FontSettings.TableSubstitution.pdf");
```

Montre comment travailler avec des tables de substitution de polices personnalisées.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Créez une nouvelle règle de substitution de table et chargez la table de substitution de polices Windows par défaut.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;

// Si nous sélectionnons des polices exclusivement à partir de notre dossier, nous aurons besoin d'une table de substitution personnalisée.
// Nous n'aurons plus accès aux polices Microsoft Windows,
// comme « Arial » ou « Times New Roman » car ils n'existent pas dans notre nouveau dossier de polices.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// Vous trouverez ci-dessous deux manières de charger une table de substitution à partir d'un fichier du système de fichiers local.
// 1 - À partir d'un flux :
using (FileStream fileStream = new FileStream(MyDir + "Font substitution rules.xml", FileMode.Open))
{
    tableSubstitutionRule.Load(fileStream);
}

// 2 - Directement depuis un fichier :
tableSubstitutionRule.Load(MyDir + "Font substitution rules.xml");

// Puisque nous n'avons plus accès à « Arial », notre table de polices va d'abord essayer de la remplacer par « Police inexistante ».
// Nous n'avons pas cette police, elle sera donc déplacée vers le prochain substitut, "Kreon", trouvé dans le dossier "MyFonts".
Assert.AreEqual(new[] {"Missing Font", "Kreon"}, tableSubstitutionRule.GetSubstitutes("Arial").ToArray());

// Nous pouvons étendre cette table par programmation. Nous allons ajouter une entrée remplaçant « Times New Roman » par « Arvo ».
Assert.Null(tableSubstitutionRule.GetSubstitutes("Times New Roman"));
tableSubstitutionRule.AddSubstitutes("Times New Roman", "Arvo");
Assert.AreEqual(new[] {"Arvo"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// Nous pouvons ajouter un substitut de secours secondaire pour une entrée de police existante avec AddSubstitutes().
// Si « Arvo » n'est pas disponible, notre table recherchera « M+ 2m » comme deuxième option de substitution.
tableSubstitutionRule.AddSubstitutes("Times New Roman", "M+ 2m");
Assert.AreEqual(new[] {"Arvo", "M+ 2m"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// SetSubstitutes() peut définir une nouvelle liste de polices de substitution pour une police.
tableSubstitutionRule.SetSubstitutes("Times New Roman", "Squarish Sans CT", "M+ 2m");
Assert.AreEqual(new[] {"Squarish Sans CT", "M+ 2m"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// L'écriture de texte dans des polices auxquelles nous n'avons pas accès invoquera nos règles de substitution.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Arial";
builder.Writeln("Text written in Arial, to be substituted by Kreon.");

builder.Font.Name = "Times New Roman";
builder.Writeln("Text written in Times New Roman, to be substituted by Squarish Sans CT.");

doc.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Custom.pdf");
```

### Voir également

* class [TableSubstitutionRule](../)
* espace de noms [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../../)
