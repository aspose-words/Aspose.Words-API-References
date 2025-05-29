---
title: FolderFontSource.ScanSubfolders
linktitle: ScanSubfolders
articleTitle: ScanSubfolders
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FolderFontSource ScanSubfolders för att enkelt hantera teckensnittsorganisation genom att välja att skanna undermappar för ökad effektivitet.
type: docs
weight: 30
url: /sv/net/aspose.words.fonts/folderfontsource/scansubfolders/
---
## FolderFontSource.ScanSubfolders property

Avgör om undermapparna ska genomsökas eller inte.

```csharp
public bool ScanSubfolders { get; }
```

## Exempel

Visar hur man använder en lokal systemmapp som innehåller teckensnitt som teckensnittskälla.

```csharp
// Skapa en teckensnittskälla från en mapp som innehåller teckensnittsfiler.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false, 1);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

Assert.AreEqual(FontsDir, folderFontSource.FolderPath);
Assert.AreEqual(false, folderFontSource.ScanSubfolders);
Assert.AreEqual(FontSourceType.FontsFolder, folderFontSource.Type);
Assert.AreEqual(1, folderFontSource.Priority);
```

### Se även

* class [FolderFontSource](../)
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)
