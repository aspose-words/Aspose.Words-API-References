---
title: FileFormatUtil.DetectFileFormat
linktitle: DetectFileFormat
articleTitle: DetectFileFormat
second_title: Aspose.Words for .NET
description: FileFormatUtil DetectFileFormat yöntem. Disk dosyasında saklanan bir belgenin biçimi hakkındaki bilgileri algılar ve döndürür C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words/fileformatutil/detectfileformat/
---
## DetectFileFormat(*string*) {#detectfileformat_1}

Disk dosyasında saklanan bir belgenin biçimi hakkındaki bilgileri algılar ve döndürür.

```csharp
public static FileFormatInfo DetectFileFormat(string fileName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Dosya adı. |

### Geri dönüş değeri

A[`FileFormatInfo`](../../fileformatinfo/) algılanan bilgileri içeren nesne.

## Notlar

Bu yöntem belge biçimini algılasa bile, 'nin belirtilen belgenin geçerli olduğunu garanti etmez. Bu yöntem yalnızca belge biçimini, algılama için yeterli olan okuma verileriyle algılar. Bir belgenin geçerli olduğunu tam olarak doğrulamak için belgeyi bir[`Document`](../../document/) nesne.

Bu yöntem atar[`FileCorruptedException`](../../filecorruptedexception/) biçim tanındığında ancak bozulma nedeniyle algılama tamamlanamadığında.

## Örnekler

Belge biçimini ve şifrelemeyi algılamak için FileFormatUtil sınıfının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();

// Belgeyi şifrelemek için SaveOptions nesnesini yapılandırın
// bir şifre ile kaydettiğimizde ve ardından belgeyi kaydettiğimizde.
OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.Odt);
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "File.DetectDocumentEncryption.odt", saveOptions);

// Belgemizin dosya türünü ve şifreleme durumunu doğrulayın.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDocumentEncryption.odt");

Assert.AreEqual(".odt", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.True(info.IsEncrypted);
```

Belge biçimini ve dijital imzaların varlığını algılamak için FileFormatUtil sınıfının nasıl kullanılacağını gösterir.

```csharp
// Bir belgenin dijital olarak imzalanmadığını doğrulamak için FileFormatInfo örneğini kullanın.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.docx");

Assert.AreEqual(".docx", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.False(info.HasDigitalSignature);

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "File.DetectDigitalSignatures.docx",
    certificateHolder, new SignOptions() { SignTime = DateTime.Now });

// İmzalandığını onaylamak için yeni bir FileFormatInstance kullanın.
info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDigitalSignatures.docx");

Assert.True(info.HasDigitalSignature);

// Bunun gibi bir koleksiyonda imzalı bir belgenin imzalarına yükleyebilir ve erişebiliriz.
Assert.AreEqual(1, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "File.DetectDigitalSignatures.docx").Count);
```

### Ayrıca bakınız

* class [FileFormatInfo](../../fileformatinfo/)
* class [FileFormatUtil](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## DetectFileFormat(*Stream*) {#detectfileformat}

Bir akışta saklanan bir belgenin biçimi hakkındaki bilgileri algılar ve döndürür.

```csharp
public static FileFormatInfo DetectFileFormat(Stream stream)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Akış. |

### Geri dönüş değeri

A[`FileFormatInfo`](../../fileformatinfo/) algılanan bilgileri içeren nesne.

## Notlar

Akış belgenin başına yerleştirilmelidir.

Bu yöntem geri döndüğünde akıştaki konum orijinal konumuna geri yüklenir.

Bu yöntem belge biçimini algılasa bile, 'nin belirtilen belgenin geçerli olduğunu garanti etmez. Bu yöntem yalnızca belge biçimini, algılama için yeterli olan okuma verileriyle algılar. Bir belgenin geçerli olduğunu tam olarak doğrulamak için belgeyi bir[`Document`](../../document/) nesne.

Bu yöntem atar[`FileCorruptedException`](../../filecorruptedexception/) biçim tanındığında ancak bozulma nedeniyle algılama tamamlanamadığında.

## Örnekler

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

* class [FileFormatInfo](../../fileformatinfo/)
* class [FileFormatUtil](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
