---
title: FolderFontSource.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words pour .NET
description: FolderFontSource Type propriété. Renvoie le type de la source de police en C#.
type: docs
weight: 40
url: /fr/net/aspose.words.fonts/folderfontsource/type/
---
## FolderFontSource.Type property

Renvoie le type de la source de police.

```csharp
public override FontSourceType Type { get; }
```

## Exemples

Montre comment utiliser un dossier système local contenant des polices comme source de polices.

```csharp
// Crée une source de police à partir d'un dossier contenant des fichiers de police.
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

* enum [FontSourceType](../../fontsourcetype/)
* class [FolderFontSource](../)
* espace de noms [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../../)
