---
title: FontSourceType Enum
linktitle: FontSourceType
articleTitle: FontSourceType
second_title: .NET için Aspose.Words
description: Verimli font kaynak yönetimi için Aspose.Words.Fonts.FontSourceType enum'unu keşfedin. Esnek font seçenekleriyle belge işlemenizi optimize edin.
type: docs
weight: 3420
url: /tr/net/aspose.words.fonts/fontsourcetype/
---
## FontSourceType enumeration

Yazı tipi kaynağının türünü belirtir.

```csharp
public enum FontSourceType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| FontFile | `0` | Bir[`FileFontSource`](../filefontsource/) tek bir yazı tipi dosyasını temsil eden nesne. |
| FontsFolder | `1` | Bir[`FolderFontSource`](../folderfontsource/) font dosyalarının bulunduğu klasörü temsil eden nesne. |
| MemoryFont | `2` | Bir[`MemoryFontSource`](../memoryfontsource/) bellekteki tek bir yazı tipini temsil eden nesne. |
| SystemFonts | `3` | Bir[`SystemFontSource`](../systemfontsource/) sisteme yüklenen tüm yazı tiplerini temsil eden nesne. |
| FontStream | `4` | Bir[`StreamFontSource`](../streamfontsource/) yazı tipi verilerine sahip bir akışı temsil eden nesne. |

## Örnekler

Yerel dosya sistemindeki bir yazı tipi dosyasının yazı tipi kaynağı olarak nasıl kullanılacağını gösterir.

```csharp
FileFontSource fileFontSource = new FileFontSource(MyDir + "Alte DIN 1451 Mittelschrift.ttf", 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {fileFontSource});

Assert.AreEqual(MyDir + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.FilePath);
Assert.AreEqual(FontSourceType.FontFile, fileFontSource.Type);
Assert.AreEqual(0, fileFontSource.Priority);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Fonts](../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../)
