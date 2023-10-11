---
title: FolderFontSource.FolderPath
second_title: Aspose.Words for .NET API Referansı
description: FolderFontSource mülk. Klasörün yolu.
type: docs
weight: 20
url: /tr/net/aspose.words.fonts/folderfontsource/folderpath/
---
## FolderFontSource.FolderPath property

Klasörün yolu.

```csharp
public string FolderPath { get; }
```

### Örnekler

Yazı tipi kaynağı olarak yazı tiplerini içeren yerel sistem klasörünün nasıl kullanılacağını gösterir.

```csharp
// Yazı tipi dosyalarını içeren bir klasörden yazı tipi kaynağı oluşturun.
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
* ad alanı [Aspose.Words.Fonts](../../folderfontsource/)
* toplantı [Aspose.Words](../../../)


