---
title: FolderFontSource Class
linktitle: FolderFontSource
articleTitle: FolderFontSource
second_title: Aspose.Words pour .NET
description: Découvrez la classe Aspose.Words.Fonts.FolderFontSource, votre solution pour gérer efficacement les polices TrueType. Améliorez la typographie de vos documents dès aujourd'hui !
type: docs
weight: 3290
url: /fr/net/aspose.words.fonts/folderfontsource/
---
## FolderFontSource class

Représente le dossier contenant les fichiers de polices TrueType.

Pour en savoir plus, visitez le[Travailler avec les polices](https://docs.aspose.com/words/net/working-with-fonts/) article de documentation.

```csharp
public class FolderFontSource : FontSourceBase
```

## Constructeurs

| Nom | La description |
| --- | --- |
| [FolderFontSource](folderfontsource/#constructor)(*string, bool*) | Cteur. |
| [FolderFontSource](folderfontsource/#constructor_1)(*string, bool, int*) | Cteur. |

## Propriétés

| Nom | La description |
| --- | --- |
| [FolderPath](../../aspose.words.fonts/folderfontsource/folderpath/) { get; } | Chemin vers le dossier. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Renvoie la priorité de la source de la police. |
| [ScanSubfolders](../../aspose.words.fonts/folderfontsource/scansubfolders/) { get; } | Détermine s'il faut ou non analyser les sous-dossiers. |
| override [Type](../../aspose.words.fonts/folderfontsource/type/) { get; } | Renvoie le type de la source de la police. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Appelé pendant le traitement de la source de police lorsqu'un problème est détecté qui pourrait entraîner une perte de fidélité du formatage. |

## Méthodes

| Nom | La description |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Renvoie la liste des polices disponibles via cette source. |

## Exemples

Montre comment utiliser un dossier système local contenant des polices comme source de polices.

```csharp
// Créez une source de police à partir d'un dossier contenant des fichiers de police.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false, 1);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

Assert.AreEqual(FontsDir, folderFontSource.FolderPath);
Assert.AreEqual(false, folderFontSource.ScanSubfolders);
Assert.AreEqual(FontSourceType.FontsFolder, folderFontSource.Type);
Assert.AreEqual(1, folderFontSource.Priority);
```

### Voir également

* class [FontSourceBase](../fontsourcebase/)
* espace de noms [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../)
