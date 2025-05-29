---
title: FileFormatUtil.ExtensionToSaveFormat
linktitle: ExtensionToSaveFormat
articleTitle: ExtensionToSaveFormat
second_title: .NET için Aspose.Words
description: FileFormatUtil ExtensionToSaveFormat metoduyla dosya adı uzantılarını SaveFormat değerlerine zahmetsizce dönüştürün. Dosya yönetiminizi bugün basitleştirin!
type: docs
weight: 40
url: /tr/net/aspose.words/fileformatutil/extensiontosaveformat/
---
## FileFormatUtil.ExtensionToSaveFormat method

Bir dosya adı uzantısını bir[`SaveFormat`](../../saveformat/) değer.

```csharp
public static SaveFormat ExtensionToSaveFormat(string extension)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| extension | String | Dosya uzantısı. Önünde nokta olabilir veya olmayabilir. Büyük/küçük harfe duyarlı değildir. |

### istisnalar

| istisna | şart |
| --- | --- |
| ArgumentNullException | Parametre şuysa fırlatır:`hükümsüz`. |

## Notlar

Uzantı tanınamıyorsa, şunu döndürür:Unknown.

## Örnekler

Bir belgenin biçimini algılamak için FileFormatUtil yöntemlerinin nasıl kullanılacağını gösterir.

```csharp
// Dosya uzantısı eksik olan bir dosyadan bir belge yükleyin ve ardından dosya biçimini algılayın.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // Aşağıda bir LoadFormat'ı karşılık gelen SaveFormat'a dönüştürmenin iki yöntemi bulunmaktadır.
    // 1 - LoadFormat için dosya uzantısı dizesini al, ardından bu dizeden karşılık gelen SaveFormat'ı al:
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - LoadFormat'ı doğrudan SaveFormat'ına dönüştür:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // Akıştan bir belge yükleyin ve ardından otomatik olarak algılanan dosya uzantısıyla kaydedin.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### Ayrıca bakınız

* enum [SaveFormat](../../saveformat/)
* class [FileFormatUtil](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
