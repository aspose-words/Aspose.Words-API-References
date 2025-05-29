---
title: SignOptions Class
linktitle: SignOptions
articleTitle: SignOptions
second_title: .NET için Aspose.Words
description: Gelişmiş iş akışı için esnek ve güvenli seçeneklerle belge imzalama sürecinizi özelleştirmek üzere Aspose.Words.DigitalSignatures.SignOptions sınıfını keşfedin.
type: docs
weight: 620
url: /tr/net/aspose.words.digitalsignatures/signoptions/
---
## SignOptions class

Belge imzalama seçeneklerini belirtmenize olanak tanır.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Dijital İmzalarla Çalışın](https://docs.aspose.com/words/net/working-with-digital-signatures/) belgeleme makalesi.

```csharp
public class SignOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [SignOptions](signoptions/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Comments](../../aspose.words.digitalsignatures/signoptions/comments/) { get; set; } | Dijital imzadaki yorumları belirtir. Varsayılan değer**boş dize**(Empty ). |
| [DecryptionPassword](../../aspose.words.digitalsignatures/signoptions/decryptionpassword/) { get; set; } | Kaynak belgeyi şifresini çözmek için kullanılan parola. Varsayılan değer**boş dize** (Empty ). |
| [ProviderId](../../aspose.words.digitalsignatures/signoptions/providerid/) { get; set; } | İmza sağlayıcısının sınıf kimliğini belirtir. Varsayılan değer**Boş (tamamı sıfır) Kılavuz** . |
| [SignatureLineId](../../aspose.words.digitalsignatures/signoptions/signaturelineid/) { get; set; } | İmza satırı tanımlayıcısı. Varsayılan değer**Boş (tamamı sıfır) Kılavuz** . |
| [SignatureLineImage](../../aspose.words.digitalsignatures/signoptions/signaturelineimage/) { get; set; } | İlişkili olarak gösterilecek görüntü[`SignatureLine`](../../aspose.words.drawing/signatureline/) . Varsayılan değer`hükümsüz` . |
| [SignTime](../../aspose.words.digitalsignatures/signoptions/signtime/) { get; set; } | İmzalama tarihi. Varsayılan değer**şimdiki zaman** (Now) |
| [XmlDsigLevel](../../aspose.words.digitalsignatures/signoptions/xmldsiglevel/) { get; set; } | XML-DSig standardına dayalı bir dijital imzanın düzeyini belirtir. Varsayılan değerXmlDSig . |

## Örnekler

Belgelerin dijital olarak nasıl imzalanacağını gösterir.

```csharp
// Özel bir anahtar içermesi gereken bir PKCS#12 deposundan bir X.509 sertifikası oluşturun.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Yeni dijital imzamızla uygulanacak bir yorum ve tarih oluşturun.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Yerel dosya sisteminden bir dosya akışı aracılığıyla imzalanmamış bir belge alın,
// daha sonra çıktı dosya akışının dosya adına göre belirlenen imzalı bir kopyasını oluşturur.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../)
