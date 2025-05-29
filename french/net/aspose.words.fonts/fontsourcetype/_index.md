---
title: FontSourceType Enum
linktitle: FontSourceType
articleTitle: FontSourceType
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.Fonts.FontSourceType pour une gestion efficace des sources de polices. Optimisez le traitement de vos documents grâce à des options de polices flexibles.
type: docs
weight: 3420
url: /fr/net/aspose.words.fonts/fontsourcetype/
---
## FontSourceType enumeration

Spécifie le type de source de police.

```csharp
public enum FontSourceType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| FontFile | `0` | A[`FileFontSource`](../filefontsource/) objet qui représente un fichier de police unique. |
| FontsFolder | `1` | A[`FolderFontSource`](../folderfontsource/) objet qui représente un dossier contenant des fichiers de polices. |
| MemoryFont | `2` | A[`MemoryFontSource`](../memoryfontsource/) objet qui représente une police unique en mémoire. |
| SystemFonts | `3` | A[`SystemFontSource`](../systemfontsource/) objet qui représente toutes les polices installées sur le système. |
| FontStream | `4` | A[`StreamFontSource`](../streamfontsource/) objet qui représente un flux avec des données de police. |

## Exemples

Montre comment utiliser un fichier de police dans le système de fichiers local comme source de police.

```csharp
FileFontSource fileFontSource = new FileFontSource(MyDir + "Alte DIN 1451 Mittelschrift.ttf", 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {fileFontSource});

Assert.AreEqual(MyDir + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.FilePath);
Assert.AreEqual(FontSourceType.FontFile, fileFontSource.Type);
Assert.AreEqual(0, fileFontSource.Priority);
```

### Voir également

* espace de noms [Aspose.Words.Fonts](../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../)
