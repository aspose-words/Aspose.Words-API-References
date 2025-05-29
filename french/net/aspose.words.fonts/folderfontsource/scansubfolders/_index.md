---
title: FolderFontSource.ScanSubfolders
linktitle: ScanSubfolders
articleTitle: ScanSubfolders
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FolderFontSource ScanSubfolders pour gérer facilement l'organisation des polices en choisissant d'analyser les sous-dossiers pour une efficacité accrue.
type: docs
weight: 30
url: /fr/net/aspose.words.fonts/folderfontsource/scansubfolders/
---
## FolderFontSource.ScanSubfolders property

Détermine s'il faut ou non analyser les sous-dossiers.

```csharp
public bool ScanSubfolders { get; }
```

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

* class [FolderFontSource](../)
* espace de noms [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Assemblée [Aspose.Words](../../../)
