---
title: SystemFontSource Class
linktitle: SystemFontSource
articleTitle: SystemFontSource
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Fonts.SystemFontSource, votre passerelle pour accéder à toutes les polices TrueType de votre système pour une création de documents transparente.
type: docs
weight: 3480
url: /fr/net/aspose.words.fonts/systemfontsource/
---
## SystemFontSource class

Représente toutes les polices TrueType installées sur le système.

Pour en savoir plus, visitez le[Travailler avec les polices](https://docs.aspose.com/words/net/working-with-fonts/) article de documentation.

```csharp
public class SystemFontSource : FontSourceBase
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [SystemFontSource](systemfontsource/#constructor)() | Cteur. |
| [SystemFontSource](systemfontsource/#constructor_1)(*int*) | Cteur. |

## Propriétés

| Nom | La description |
| --- | --- |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Renvoie la priorité de la source de la police. |
| override [Type](../../aspose.words.fonts/systemfontsource/type/) { get; } | Renvoie le type de la source de la police. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Appelé pendant le traitement de la source de police lorsqu'un problème est détecté qui pourrait entraîner une perte de fidélité du formatage. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Renvoie la liste des polices disponibles via cette source. |
| static [GetSystemFontFolders](../../aspose.words.fonts/systemfontsource/getsystemfontfolders/)() | Renvoie les dossiers de polices système ou un tableau vide si les dossiers ne sont pas accessibles. |

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

### Voir également

* class [FontSourceBase](../fontsourcebase/)
* espace de noms [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../)
