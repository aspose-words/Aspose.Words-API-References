---
title: FileFormatUtil.LoadFormatToExtension
linktitle: LoadFormatToExtension
articleTitle: LoadFormatToExtension
second_title: .NET için Aspose.Words
description: Yükleme biçimi değerlerini FileFormatUtil'in LoadFormatToExtension metoduyla zahmetsizce dosya uzantılarına dönüştürün. Doğru, küçük harfli uzantıları kolayca elde edin!
type: docs
weight: 60
url: /tr/net/aspose.words/fileformatutil/loadformattoextension/
---
## FileFormatUtil.LoadFormatToExtension method

Yükleme biçiminde numaralandırılmış bir değeri dosya uzantısına dönüştürür. Döndürülen uzantı, başında nokta bulunan küçük harfli bir dizedir.

```csharp
public static string LoadFormatToExtension(LoadFormat loadFormat)
```

### istisnalar

| istisna | şart |
| --- | --- |
| ArgumentException | Dönüştürülemediğinde atar. |

## Notlar

TheWordML değer ".wml"ye dönüştürülür.

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

* enum [LoadFormat](../../loadformat/)
* class [FileFormatUtil](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
