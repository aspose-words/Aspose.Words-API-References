---
title: FolderFontSource.ScanSubfolders
linktitle: ScanSubfolders
articleTitle: ScanSubfolders
second_title: .NET için Aspose.Words
description: Gelişmiş verimlilik için alt klasörleri taramayı seçerek yazı tipi organizasyonunu kolayca yönetmek için FolderFontSource ScanSubfolders özelliğini keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words.fonts/folderfontsource/scansubfolders/
---
## FolderFontSource.ScanSubfolders property

Alt klasörlerin taranıp taranmayacağını belirler.

```csharp
public bool ScanSubfolders { get; }
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
