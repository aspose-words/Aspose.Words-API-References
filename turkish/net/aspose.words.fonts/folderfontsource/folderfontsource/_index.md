---
title: FolderFontSource
linktitle: FolderFontSource
articleTitle: FolderFontSource
second_title: .NET için Aspose.Words
description: Kusursuz font yönetimi için FolderFontSource oluşturucusunu keşfedin. Web projelerinizi bugün verimli font kaynaklarıyla geliştirin!
type: docs
weight: 10
url: /tr/net/aspose.words.fonts/folderfontsource/folderfontsource/
---
## FolderFontSource(*string, bool*) {#constructor}

İşlemci.

```csharp
public FolderFontSource(string folderPath, bool scanSubfolders)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| folderPath | String | Klasöre giden yol. |
| scanSubfolders | Boolean | Alt klasörlerin taranıp taranmayacağını belirler. |

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

---

## FolderFontSource(*string, bool, int*) {#constructor_1}

İşlemci.

```csharp
public FolderFontSource(string folderPath, bool scanSubfolders, int priority)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| folderPath | String | Klasöre giden yol. |
| scanSubfolders | Boolean | Alt klasörlerin taranıp taranmayacağını belirler. |
| priority | Int32 | Yazı tipi kaynağı önceliği. Bkz.[`Priority`](../../fontsourcebase/priority/) Daha fazla bilgi için mülk açıklamasına bakın. |

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
