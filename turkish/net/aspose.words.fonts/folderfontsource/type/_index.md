---
title: FolderFontSource.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words for .NET
description: FolderFontSource Type mülk. Yazı tipi kaynağının türünü döndürür C#'da.
type: docs
weight: 40
url: /tr/net/aspose.words.fonts/folderfontsource/type/
---
## FolderFontSource.Type property

Yazı tipi kaynağının türünü döndürür.

```csharp
public override FontSourceType Type { get; }
```

## Örnekler

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

* enum [FontSourceType](../../fontsourcetype/)
* class [FolderFontSource](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
