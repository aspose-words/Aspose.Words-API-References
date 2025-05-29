---
title: FolderFontSource.FolderPath
linktitle: FolderPath
articleTitle: FolderPath
second_title: .NET için Aspose.Words
description: Font klasörünüze kolay erişim için FolderFontSource FolderPath özelliğini keşfedin. Tasarım iş akışınızı bugün kolaylaştırın!
type: docs
weight: 20
url: /tr/net/aspose.words.fonts/folderfontsource/folderpath/
---
## FolderFontSource.FolderPath property

Klasöre giden yol.

```csharp
public string FolderPath { get; }
```

## Örnekler

Font kaynağı olarak fontları içeren yerel bir sistem klasörünün nasıl kullanılacağını gösterir.

```csharp
// Font dosyalarını içeren bir klasörden bir font kaynağı oluştur.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false, 1);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

Assert.AreEqual(FontsDir, folderFontSource.FolderPath);
Assert.AreEqual(false, folderFontSource.ScanSubfolders);
Assert.AreEqual(FontSourceType.FontsFolder, folderFontSource.Type);
Assert.AreEqual(1, folderFontSource.Priority);
```

### Ayrıca bakınız

* class [FolderFontSource](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
