---
title: TableSubstitutionRule.AddSubstitutes
linktitle: AddSubstitutes
articleTitle: AddSubstitutes
second_title: Aspose.Words pour .NET
description: Améliorez votre typographie avec la méthode TableSubstitutionRule AddSubstitutes, permettant une intégration transparente de polices de substitution pour n'importe quelle police d'origine.
type: docs
weight: 10
url: /fr/net/aspose.words.fonts/tablesubstitutionrule/addsubstitutes/
---
## TableSubstitutionRule.AddSubstitutes method

Ajoute des noms de police de substitution pour le nom de police d'origine donné.

```csharp
public void AddSubstitutes(string originalFontName, params string[] substituteFontNames)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| originalFontName | String | Nom de la police d'origine. |
| substituteFontNames | String[] | Liste de noms de polices alternatifs. |

## Exemples

Montre comment accéder à la source de police système d'un document et définir des substituts de police.

```csharp
Document doc = new Document();
doc.FontSettings = new FontSettings();

// Par défaut, un document vierge contient toujours une source de police système.
Assert.AreEqual(1, doc.FontSettings.GetFontsSources().Length);

SystemFontSource systemFontSource = (SystemFontSource) doc.FontSettings.GetFontsSources()[0];
Assert.AreEqual(FontSourceType.SystemFonts, systemFontSource.Type);
Assert.AreEqual(0, systemFontSource.Priority);

PlatformID pid = Environment.OSVersion.Platform;
bool isWindows = (pid == PlatformID.Win32NT) || (pid == PlatformID.Win32S) ||
                 (pid == PlatformID.Win32Windows) || (pid == PlatformID.WinCE);
if (isWindows)
{
    const string fontsPath = @"C:\WINDOWS\Fonts";
    Assert.AreEqual(fontsPath.ToLower(),
        SystemFontSource.GetSystemFontFolders().FirstOrDefault()?.ToLower());
}

foreach (string systemFontFolder in SystemFontSource.GetSystemFontFolders())
{
    Console.WriteLine(systemFontFolder);
}

// Définissez une police qui existe dans le répertoire des polices Windows en remplacement d'une police qui n'existe pas.
doc.FontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;
doc.FontSettings.SubstitutionSettings.TableSubstitution.AddSubstitutes("Kreon-Regular", new[] {"Calibri"});

Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
Assert.Contains("Calibri",
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").ToArray());

// Alternativement, nous pourrions ajouter un dossier source de police dans lequel le dossier correspondant contient la police.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
doc.FontSettings.SetFontsSources(new FontSourceBase[] {systemFontSource, folderFontSource});
Assert.AreEqual(2, doc.FontSettings.GetFontsSources().Length);

// La réinitialisation des sources de polices nous laisse toujours avec la source de polices système ainsi que nos substituts.
doc.FontSettings.ResetFontSources();

Assert.AreEqual(1, doc.FontSettings.GetFontsSources().Length);
Assert.AreEqual(FontSourceType.SystemFonts, doc.FontSettings.GetFontsSources()[0].Type);
Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
Assert.True(doc.FontSettings.SubstitutionSettings.FontNameSubstitution.Enabled);
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
