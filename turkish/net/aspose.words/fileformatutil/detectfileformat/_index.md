---
title: FileFormatUtil.DetectFileFormat
linktitle: DetectFileFormat
articleTitle: DetectFileFormat
second_title: .NET için Aspose.Words
description: FileFormatUtil'in DetectFileFormat yöntemi ile belge biçimlerini hızla tanımlayın. Verimli dosya yönetimi için doğru biçim içgörüleri edinin.
type: docs
weight: 30
url: /tr/net/aspose.words/fileformatutil/detectfileformat/
---
## DetectFileFormat(*string*) {#detectfileformat_1}

Bir disk dosyasında saklanan bir belgenin biçimi hakkında bilgi algılar ve döndürür.

```csharp
public static FileFormatInfo DetectFileFormat(string fileName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Dosya adı. |

### Geri dönüş değeri

A[`FileFormatInfo`](../../fileformatinfo/) Algılanan bilgiyi içeren nesne.

## Notlar

Bu yöntem belge biçimini algılasa bile, belirtilen belgenin geçerli olduğunu garanti etmez. Bu yöntem yalnızca algılama için yeterli olan verileri okuyarak belge biçimini algılar. Bir belgenin geçerli olduğunu tam olarak doğrulamak için belgeyi bir[`Document`](../../document/) nesne.

Bu yöntem atar[`FileCorruptedException`](../../filecorruptedexception/) is biçimi tanındığında, ancak bozulma nedeniyle algılama tamamlanamıyor.

## Örnekler

Belge biçimini ve şifrelemeyi algılamak için FileFormatUtil sınıfının nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document();

// Belgeyi şifrelemek için bir SaveOptions nesnesi yapılandırın
// kaydederken bir şifre ile kaydediyoruz ve ardından belgeyi kaydediyoruz.
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
SignOptions signOptions = new SignOptions() { SignTime = DateTime.Now };
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "File.DetectDigitalSignatures.docx",
    certificateHolder, signOptions);

// İmzalandığını doğrulamak için yeni bir FileFormatInstance kullanın.
info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDigitalSignatures.docx");

Assert.True(info.HasDigitalSignature);

// İmzalanmış bir belgenin imzalarını bu şekilde bir koleksiyona yükleyebilir ve erişebiliriz.
Assert.AreEqual(1, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "File.DetectDigitalSignatures.docx").Count);
```

### Ayrıca bakınız

* class [FileFormatInfo](../../fileformatinfo/)
* class [FileFormatUtil](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## DetectFileFormat(*Stream*) {#detectfileformat}

Bir akışta depolanan bir belgenin biçimi hakkında bilgi algılar ve döndürür.

```csharp
public static FileFormatInfo DetectFileFormat(Stream stream)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Dere. |

### Geri dönüş değeri

A[`FileFormatInfo`](../../fileformatinfo/) Algılanan bilgiyi içeren nesne.

## Notlar

Akış, belgenin başında konumlandırılmalıdır.

Bu yöntem geri döndüğünde akıştaki konum orijinal konumuna geri yüklenir.

Bu yöntem belge biçimini algılasa bile, belirtilen belgenin geçerli olduğunu garanti etmez. Bu yöntem yalnızca algılama için yeterli olan verileri okuyarak belge biçimini algılar. Bir belgenin geçerli olduğunu tam olarak doğrulamak için belgeyi bir[`Document`](../../document/) nesne.

Bu yöntem atar[`FileCorruptedException`](../../filecorruptedexception/) is biçimi tanındığında, ancak bozulma nedeniyle algılama tamamlanamıyor.

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

* class [FileFormatInfo](../../fileformatinfo/)
* class [FileFormatUtil](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
