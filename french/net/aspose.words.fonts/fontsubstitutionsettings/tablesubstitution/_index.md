---
title: FontSubstitutionSettings.TableSubstitution
second_title: Référence de l'API Aspose.Words pour .NET
description: FontSubstitutionSettings propriété. Paramètres liés à la règle de substitution de table.
type: docs
weight: 50
url: /fr/net/aspose.words.fonts/fontsubstitutionsettings/tablesubstitution/
---
## FontSubstitutionSettings.TableSubstitution property

Paramètres liés à la règle de substitution de table.

```csharp
public TableSubstitutionRule TableSubstitution { get; }
```

### Exemples

Montre comment travailler avec des tables de substitution de polices personnalisées.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Crée une nouvelle règle de substitution de table et charge la table de substitution de police Windows par défaut.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;

// Si nous sélectionnons des polices exclusivement à partir de notre dossier, nous aurons besoin d'une table de substitution personnalisée.
// Nous n'aurons plus accès aux polices Microsoft Windows,
// tels que "Arial" ou "Times New Roman" car ils n'existent pas dans notre nouveau dossier de polices.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// Vous trouverez ci-dessous deux manières de charger une table de substitution à partir d'un fichier du système de fichiers local.
// 1 - Depuis un flux :
using (FileStream fileStream = new FileStream(MyDir + "Font substitution rules.xml", FileMode.Open))
{
    tableSubstitutionRule.Load(fileStream);
}

// 2 - Directement depuis un fichier :
tableSubstitutionRule.Load(MyDir + "Font substitution rules.xml");

// Puisque nous n'avons plus accès à "Arial", notre table de polices essaiera d'abord de la remplacer par "Police inexistante".
// Nous n'avons pas cette police donc elle passera au substitut suivant, "Kreon", trouvé dans le dossier "MyFonts".
Assert.AreEqual(new[] {"Missing Font", "Kreon"}, tableSubstitutionRule.GetSubstitutes("Arial").ToArray());

// Nous pouvons développer cette table par programmation. Nous allons ajouter une entrée qui remplace "Times New Roman" par "Arvo"
Assert.Null(tableSubstitutionRule.GetSubstitutes("Times New Roman"));
tableSubstitutionRule.AddSubstitutes("Times New Roman", "Arvo");
Assert.AreEqual(new[] {"Arvo"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// Nous pouvons ajouter un substitut de secours secondaire pour une entrée de police existante avec AddSubstitutes().
// Si "Arvo" n'est pas disponible, notre table recherchera "M+ 2m" comme seconde option de substitution.
tableSubstitutionRule.AddSubstitutes("Times New Roman", "M+ 2m");
Assert.AreEqual(new[] {"Arvo", "M+ 2m"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// SetSubstitutes() peut définir une nouvelle liste de polices de substitution pour une police.
tableSubstitutionRule.SetSubstitutes("Times New Roman", new[] {"Squarish Sans CT", "M+ 2m"});
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

* class [TableSubstitutionRule](../../tablesubstitutionrule/)
* class [FontSubstitutionSettings](../)
* espace de noms [Aspose.Words.Fonts](../../fontsubstitutionsettings/)
* Assemblée [Aspose.Words](../../../)


