---
title: FolderFontSource.Type
linktitle: Type
articleTitle: Type
second_title: .NET için Aspose.Words
description: FolderFontSource Type özelliğini keşfedin. Tasarım projelerinizi geliştirmek ve iş akışınızı kolaylaştırmak için font kaynak türlerini kolayca tanımlayın.
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

* enum [FontSourceType](../../fontsourcetype/)
* class [FolderFontSource](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
