---
title: FileFormatInfo Class
linktitle: FileFormatInfo
articleTitle: FileFormatInfo
second_title: Aspose.Words for .NET
description: Aspose.Words.FileFormatInfo sınıf. Tarafından döndürülen verileri içerirFileFormatUtil belge biçimi algılama yöntemleri C#'da.
type: docs
weight: 2810
url: /tr/net/aspose.words/fileformatinfo/
---
## FileFormatInfo class

Tarafından döndürülen verileri içerir[`FileFormatUtil`](../fileformatutil/) belge biçimi algılama yöntemleri.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Dosya Formatını Algıla ve Format Uyumluluğunu Kontrol Et](https://docs.aspose.com/words/net/detect-file-format-and-check-format-compatibility/) dokümantasyon makalesi.

```csharp
public class FileFormatInfo
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Encoding](../../aspose.words/fileformatinfo/encoding/) { get; } | Geçerli belge biçimine uygunsa, algılanan kodlamayı alır. Şu anda yalnızca HTML belgeleri için kodlamayı algılar. |
| [HasDigitalSignature](../../aspose.words/fileformatinfo/hasdigitalsignature/) { get; } | İadeler`doğru`Bu belge dijital imza içeriyorsa. Bu özellik yalnızca bir belgede dijital imzanın bulunduğunu bildirir, ancak imzanın geçerli olup olmadığını belirtmez. |
| [IsEncrypted](../../aspose.words/fileformatinfo/isencrypted/) { get; } | İadeler`doğru` belge şifrelenmişse ve açmak için şifre gerektiriyorsa. |
| [LoadFormat](../../aspose.words/fileformatinfo/loadformat/) { get; } | Algılanan belge biçimini alır. |

## Notlar

Bu sınıfın örneklerini doğrudan oluşturmazsınız. Bu sınıfın nesneleri tarafından döndürülür[`DetectFileFormat`](../fileformatutil/detectfileformat/) yöntemler.

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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
