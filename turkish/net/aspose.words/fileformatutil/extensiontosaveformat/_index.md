---
title: FileFormatUtil.ExtensionToSaveFormat
second_title: Aspose.Words for .NET API Referansı
description: FileFormatUtil yöntem. Dosya adı uzantısını bir dosya adı uzantısına dönüştürürSaveFormat değer.
type: docs
weight: 40
url: /tr/net/aspose.words/fileformatutil/extensiontosaveformat/
---
## FileFormatUtil.ExtensionToSaveFormat method

Dosya adı uzantısını bir dosya adı uzantısına dönüştürür[`SaveFormat`](../../saveformat/) değer.

```csharp
public static SaveFormat ExtensionToSaveFormat(string extension)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| extension | String | Dosya uzantısı. Başında nokta olsun ya da olmasın olabilir. Büyük/küçük harfe duyarlı değildir. |

### istisnalar

| istisna | şart |
| --- | --- |
| ArgumentNullException | Parametre şu şekildeyse atar`hükümsüz`. |

### Notlar

Uzantı tanınamıyorsa şunu döndürür:Unknown.

### Örnekler

Bir belgenin biçimini algılamak için FileFormatUtil yöntemlerinin nasıl kullanılacağını gösterir.

```csharp
// Dosya uzantısı eksik olan bir dosyadan belge yükleyin ve ardından dosya biçimini tespit edin.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // Aşağıda bir LoadFormat'ı karşılık gelen SaveFormat'a dönüştürmenin iki yöntemi verilmiştir.
    // 1 - LoadFormat için dosya uzantısı dizesini alın, ardından bu dizeden karşılık gelen SaveFormat'ı alın:
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - LoadFormat'ı doğrudan SaveFormat'ına dönüştürün:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // Akıştan bir belge yükleyin ve ardından onu otomatik olarak algılanan dosya uzantısına kaydedin.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### Ayrıca bakınız

* enum [SaveFormat](../../saveformat/)
* class [FileFormatUtil](../)
* ad alanı [Aspose.Words](../../fileformatutil/)
* toplantı [Aspose.Words](../../../)


