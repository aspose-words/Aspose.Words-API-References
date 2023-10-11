---
title: FolderFontSource.FolderPath
second_title: Référence de l'API Aspose.Words pour .NET
description: FolderFontSource propriété. Chemin daccès au dossier.
type: docs
weight: 20
url: /fr/net/aspose.words.fonts/folderfontsource/folderpath/
---
## FolderFontSource.FolderPath property

Chemin d'accès au dossier.

```csharp
public string FolderPath { get; }
```

### Exemples

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

* class [FolderFontSource](../)
* espace de noms [Aspose.Words.Fonts](../../folderfontsource/)
* Assemblée [Aspose.Words](../../../)


