---
title: FolderFontSource.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FolderFontSource Type. Identifiera enkelt teckensnittskälltyper för att förbättra dina designprojekt och effektivisera ditt arbetsflöde.
type: docs
weight: 40
url: /sv/net/aspose.words.fonts/folderfontsource/type/
---
## FolderFontSource.Type property

Returnerar typen av teckensnittskällan.

```csharp
public override FontSourceType Type { get; }
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

* enum [FontSourceType](../../fontsourcetype/)
* class [FolderFontSource](../)
* namnutrymme [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* hopsättning [Aspose.Words](../../../)
