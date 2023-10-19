---
title: FolderFontSource
linktitle: FolderFontSource
articleTitle: FolderFontSource
second_title: Aspose.Words for .NET
description: FolderFontSource inşaatçı. Ctor C#'da.
type: docs
weight: 10
url: /tr/net/aspose.words.fonts/folderfontsource/folderfontsource/
---
## FolderFontSource(*string, bool*) {#constructor}

Ctor.

```csharp
public FolderFontSource(string folderPath, bool scanSubfolders)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| folderPath | String | Klasör yolu. |
| scanSubfolders | Boolean | Alt klasörlerin taranıp taranmayacağını belirler. |

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

* class [FolderFontSource](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)

---

## FolderFontSource(*string, bool, int*) {#constructor_1}

Ctor.

```csharp
public FolderFontSource(string folderPath, bool scanSubfolders, int priority)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| folderPath | String | Klasör yolu. |
| scanSubfolders | Boolean | Alt klasörlerin taranıp taranmayacağını belirler. |
| priority | Int32 | Yazı tipi kaynağı önceliği. Bkz.[`Priority`](../../fontsourcebase/priority/) Daha fazla bilgi için özellik açıklaması. |

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

* class [FolderFontSource](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
