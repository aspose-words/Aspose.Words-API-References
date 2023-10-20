---
title: FontSubstitutionSettings Class
linktitle: FontSubstitutionSettings
articleTitle: FontSubstitutionSettings
second_title: Aspose.Words pour .NET
description: Aspose.Words.Fonts.FontSubstitutionSettings classe. Spécifie les paramètres du mécanisme de substitution de police en C#.
type: docs
weight: 3010
url: /fr/net/aspose.words.fonts/fontsubstitutionsettings/
---
## FontSubstitutionSettings class

Spécifie les paramètres du mécanisme de substitution de police.

Pour en savoir plus, visitez le[Travailler avec des polices](https://docs.aspose.com/words/net/working-with-fonts/) article documentaire.

```csharp
public class FontSubstitutionSettings
```

## Propriétés

| Nom | La description |
| --- | --- |
| [DefaultFontSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/defaultfontsubstitution/) { get; } | Paramètres liés à la règle de substitution de police par défaut. |
| [FontConfigSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/fontconfigsubstitution/) { get; } | Paramètres liés à la règle de substitution de configuration de police. |
| [FontInfoSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/fontinfosubstitution/) { get; } | Paramètres liés à la règle de substitution des informations de police. |
| [FontNameSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/fontnamesubstitution/) { get; } | Paramètres liés à la règle de substitution du nom de police. |
| [TableSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/tablesubstitution/) { get; } | Paramètres liés à la règle de substitution de table. |

## Remarques

Le processus de substitution de police se compose de plusieurs règles qui sont vérifiées une par une dans un ordre spécifique. Si la première règle ne peut pas résoudre la police, la deuxième règle est vérifiée et ainsi de suite.

L'ordre des règles est le suivant : 1. Règle de substitution du nom de police (activée par défaut) 2. Règle de substitution de la configuration de la police (désactivée par défaut) 3. Règle de substitution de table (activée par défaut) 4. Règle de substitution des informations de police (activé par défaut) 5. Règle de police par défaut (activée par défaut)

Notez que la règle de substitution des informations sur la police résoudra toujours la police si[`FontInfo`](../fontinfo/) est disponible et remplacera la règle de police par défaut. Si vous souhaitez utiliser la règle de police par défaut, vous devez désactiver la règle de substitution des informations de police .

Notez que la règle de substitution de configuration de police résoudra la police dans la plupart des cas et remplacera ainsi toutes les autres règles.

## Exemples

Montre comment accéder à la source de police système d’un document et définir des substituts de police.

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

// Définit une police qui existe dans le répertoire des polices Windows en remplacement d'une autre qui n'existe pas.
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

// La réinitialisation des sources de polices nous laisse toujours la source de police système ainsi que nos substituts.
doc.FontSettings.ResetFontSources();

Assert.AreEqual(1, doc.FontSettings.GetFontsSources().Length);
Assert.AreEqual(FontSourceType.SystemFonts, doc.FontSettings.GetFontsSources()[0].Type);
Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
```

### Voir également

* espace de noms [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../)
