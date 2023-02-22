---
title: Class CertificateHolder
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.DigitalSignatures.CertificateHolder sınıf. Şunun sahibini temsil eder X509Sertifika2 misal.
type: docs
weight: 360
url: /tr/net/aspose.words.digitalsignatures/certificateholder/
---
## CertificateHolder class

Şunun sahibini temsil eder: **X509Sertifika2** misal.

```csharp
public class CertificateHolder
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Certificate](../../aspose.words.digitalsignatures/certificateholder/certificate/) { get; } | Örneğini döndürür **X509Sertifika2** özel, genel anahtarları ve sertifika zincirini tutan. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create)(byte[], SecureString) | PKCS12 deposunun bayt dizisini ve parolasını kullanarak CertificateHolder nesnesi oluşturur. |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create_1)(byte[], string) | PKCS12 deposunun bayt dizisini ve parolasını kullanarak CertificateHolder nesnesi oluşturur. |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create_2)(string, string) | PKCS12 deposunun yolunu ve parolasını kullanarak CertificateHolder nesnesi oluşturur. |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create_3)(string, string, string) | PKCS12 deposunun yolunu, parolasını ve diğer adı kullanarak, hangi özel anahtar ve sertifikanın bulunacağını kullanarak CertificateHolder nesnesi oluşturur. |

### Notlar

**Sertifika sahibi** yalnızca statik fabrika yöntemleriyle oluşturulabilir. Bir örneğini içerir **X509Sertifika2** özel, genel anahtarları ve sertifika zincirlerini sisteme tanıtmak için kullanılır. Bu sınıf,[`DigitalSignatureUtil`](../digitalsignatureutil/) ve[`PdfDigitalSignatureDetails`](../../aspose.words.saving/pdfdigitalsignaturedetails/) ile eski yöntemler yerineX509Certificate2 parametreler olarak.

### Örnekler

Şifreli belge dosyasının nasıl imzalanacağını gösterir.

```csharp
// PKCS#12 deposundan özel anahtar içermesi gereken bir X.509 sertifikası oluşturun.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Yeni dijital imzamızla uygulanacak bir yorum, tarih ve şifre çözme şifresi oluşturun.
SignOptions signOptions = new SignOptions
{
    Comments = "Comment",
    SignTime = DateTime.Now,
    DecryptionPassword = "docPassword"
};

// İmzasız giriş belgesi için yerel bir sistem dosya adı ve dijital olarak imzalanmış yeni kopyası için bir çıkış dosya adı ayarlayın.
string inputFileName = MyDir + "Encrypted.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.DecryptionPassword.docx";

DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

Belgelerin dijital olarak nasıl imzalanacağını gösterir.

```csharp
// PKCS#12 deposundan özel anahtar içermesi gereken bir X.509 sertifikası oluşturun.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Yeni dijital imzamızla uygulanacak bir yorum ve tarih oluşturun.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Dosya akışı yoluyla yerel dosya sisteminden imzasız bir belge alın,
// ardından çıktı dosyası akışının dosya adıyla belirlenen imzalı bir kopyasını oluşturun.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

Belgeye imza satırının nasıl ekleneceğini ve ardından dijital sertifika kullanarak nasıl imzalanacağını gösterir.

```csharp
public static void Sign()
        {
            string signeeName = "Ron Williams";
            string srcDocumentPath = MyDir + "Document.docx";
            string dstDocumentPath = ArtifactsDir + "SignDocumentCustom.Sign.docx";
            string certificatePath = MyDir + "morzal.pfx";
            string certificatePassword = "aw";

            CreateSignees();

            Signee signeeInfo = mSignees.Find(c => c.Name == signeeName);

            if (signeeInfo != null)
                SignDocument(srcDocumentPath, dstDocumentPath, signeeInfo, certificatePath, certificatePassword);
            else
                Assert.Fail("Signee does not exist.");
        }

        /// <summary>
        /// Sağlanan imza sahibi bilgileri ve X509 sertifikası kullanılarak imzalanmış bir kaynak belgenin bir kopyasını oluşturur.
        /// </summary>
        private static void SignDocument(string srcDocumentPath, string dstDocumentPath,
            Signee signeeInfo, string certificatePath, string certificatePassword)
        {
            Document document = new Document(srcDocumentPath);
            DocumentBuilder builder = new DocumentBuilder(document);

            // Bir imza satırı, belgede imzaladığımız bir imzayı gösterecek bir nesne yapılandırın ve ekleyin.
            SignatureLineOptions signatureLineOptions = new SignatureLineOptions
            {
                Signer = signeeInfo.Name, 
                SignerTitle = signeeInfo.Position
            };

            SignatureLine signatureLine = builder.InsertSignatureLine(signatureLineOptions).SignatureLine;
            signatureLine.Id = signeeInfo.PersonId;

            // İlk olarak belgemizin imzasız bir versiyonunu kaydedeceğiz.
            builder.Document.Save(dstDocumentPath);

            CertificateHolder certificateHolder = CertificateHolder.Create(certificatePath, certificatePassword);

            SignOptions signOptions = new SignOptions
            {
                SignatureLineId = signeeInfo.PersonId,
                SignatureLineImage = signeeInfo.Image
            };

            // Yukarıda kaydettiğimiz imzasız belgenin üzerine sertifika kullanılarak imzalanmış bir sürüm yazın.
            DigitalSignatureUtil.Sign(dstDocumentPath, dstDocumentPath, certificateHolder, signOptions);
        }

#if NET48 || JAVA
        /// <summary>
        /// Bir görüntüyü bir bayt dizisine dönüştürür.
        /// </summary>
        private static byte[] ImageToByteArray(Image imageIn)
        {
            using (MemoryStream ms = new MemoryStream())
            {
                imageIn.Save(ms, ImageFormat.Png);
                return ms.ToArray();
            }
        }
#endif

        public class Signee
        {
            public Guid PersonId { get; set; }
            public string Name { get; set; }
            public string Position { get; set; }
            public byte[] Image { get; set; }

            public Signee(Guid guid, string name, string position, byte[] image)
            {
                PersonId = guid;
                Name = name;
                Position = position;
                Image = image;
            }
        }

        private static void CreateSignees()
        {
            mSignees = new List<Signee>
            {
                #if NET48 || JAVA
                new Signee(Guid.NewGuid(), "Ron Williams", "Chief Executive Officer",
                    ImageToByteArray(Image.FromFile(ImageDir + "Logo.jpg"))),
                #elif NET5_0_OR_GREATER || __MOBILE__
                new Signee(Guid.NewGuid(), "Ron Williams", "Chief Executive Officer", 
                    SkiaSharp.SKBitmap.Decode(ImageDir + "Logo.jpg").Bytes),
                #endif

                #if NET48 || JAVA
                new Signee(Guid.NewGuid(), "Stephen Morse", "Head of Compliance",
                    ImageToByteArray(Image.FromFile(ImageDir + "Logo.jpg")))
                #elif NET5_0_OR_GREATER || __MOBILE__
                new Signee(Guid.NewGuid(), "Stephen Morse", "Head of Compliance", 
                    SkiaSharp.SKBitmap.Decode(ImageDir + "Logo.jpg").Bytes)
                #endif
            };
        }

        private static List<Signee> mSignees;
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../)


