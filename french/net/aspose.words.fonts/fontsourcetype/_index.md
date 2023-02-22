---
title: Enum FontSourceType
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.Fonts.FontSourceType énumération. Spécifie le type dune source de police.
type: docs
weight: 2810
url: /fr/net/aspose.words.fonts/fontsourcetype/
---
## FontSourceType enumeration

Spécifie le type d'une source de police.

```csharp
public enum FontSourceType
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| FontFile | `0` | A[`FileFontSource`](../filefontsource/) objet qui représente un seul fichier de police. |
| FontsFolder | `1` | A[`FolderFontSource`](../folderfontsource/) objet qui représente le dossier avec les fichiers de police. |
| MemoryFont | `2` | A[`MemoryFontSource`](../memoryfontsource/) objet qui représente une seule police en mémoire. |
| SystemFonts | `3` | A[`SystemFontSource`](../systemfontsource/) objet qui représente toutes les polices installées sur le système. |
| FontStream | `4` | A[`StreamFontSource`](../streamfontsource/) objet qui représente un flux avec des données de police. |

### Exemples

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


