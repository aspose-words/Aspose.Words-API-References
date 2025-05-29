---
title: FileFormatInfo Class
linktitle: FileFormatInfo
articleTitle: FileFormatInfo
second_title: .NET için Aspose.Words
description: Verimli belge biçimi algılaması için Aspose.Words.FileFormatInfo sınıfını keşfedin. Dosya yönetimi çözümlerinizi geliştirmek için ayrıntılı verilere erişin.
type: docs
weight: 3220
url: /tr/net/aspose.words/fileformatinfo/
---
## FileFormatInfo class

tarafından döndürülen verileri içerir[`FileFormatUtil`](../fileformatutil/) belge biçimi algılama yöntemleri.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Dosya Biçimini Algıla ve Biçim Uyumluluğunu Kontrol Et](https://docs.aspose.com/words/net/detect-file-format-and-check-format-compatibility/) belgeleme makalesi.

```csharp
public class FileFormatInfo
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Encoding](../../aspose.words/fileformatinfo/encoding/) { get; } | Geçerli belge biçimine uygulanabilirse algılanan kodlamayı alır. Şu anda yalnızca HTML belgeleri için kodlamayı algılar. |
| [HasDigitalSignature](../../aspose.words/fileformatinfo/hasdigitalsignature/) { get; } | Geri Döndürür`doğru`eğer bu belge bir dijital imza içeriyorsa. Bu özellik yalnızca bir belgede dijital imzanın mevcut olduğunu bildirir, ancak imzanın geçerli olup olmadığını belirtmez. |
| [HasMacros](../../aspose.words/fileformatinfo/hasmacros/) { get; } | Geri Döndürür`doğru` eğer bu belge bir VBA makrosu içeriyorsa. |
| [IsEncrypted](../../aspose.words/fileformatinfo/isencrypted/) { get; } | Geri Döndürür`doğru` belge şifrelenmişse ve açmak için parola gerekiyorsa. |
| [LoadFormat](../../aspose.words/fileformatinfo/loadformat/) { get; } | Algılanan belge biçimini alır. |

## Notlar

Bu sınıfın örneklerini doğrudan oluşturmazsınız. Bu sınıfın nesneleri by döndürülür[`DetectFileFormat`](../fileformatutil/detectfileformat/) Yöntemler.

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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
