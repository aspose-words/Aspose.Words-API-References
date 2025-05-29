---
title: Document.OriginalFileName
linktitle: OriginalFileName
articleTitle: OriginalFileName
second_title: .NET için Aspose.Words
description: Belgenizin orijinal dosya adını Document OriginalFileName özelliğiyle zahmetsizce alın. İş akışınızı ve organizasyonunuzu bugün geliştirin!
type: docs
weight: 300
url: /tr/net/aspose.words/document/originalfilename/
---
## Document.OriginalFileName property

Belgenin orijinal dosya adını alır.

```csharp
public string OriginalFileName { get; }
```

## Notlar

İade`hükümsüz` Belge bir akıştan yüklendiyse veya boş oluşturulduysa.

## Örnekler

Bir belgenin yükleme işleminin ayrıntılarının nasıl alınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(MyDir + "Document.docx", doc.OriginalFileName);
Assert.AreEqual(LoadFormat.Docx, doc.OriginalLoadFormat);
```

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

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
