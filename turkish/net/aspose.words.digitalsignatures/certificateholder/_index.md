---
title: CertificateHolder Class
linktitle: CertificateHolder
articleTitle: CertificateHolder
second_title: .NET için Aspose.Words
description: Güvenli dijital imzalar için X509Certificate2 örneklerini yönetmenin anahtarı olan Aspose.Words.DigitalSignatures.CertificateHolder sınıfını keşfedin.
type: docs
weight: 570
url: /tr/net/aspose.words.digitalsignatures/certificateholder/
---
## CertificateHolder class

Bir hisse senedinin sahibini temsil eder**X509Sertifika2** örnek.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Dijital İmzalarla Çalışın](https://docs.aspose.com/words/net/working-with-digital-signatures/) belgeleme makalesi.

```csharp
public class CertificateHolder
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Certificate](../../aspose.words.digitalsignatures/certificateholder/certificate/) { get; } | örneğini döndürür**X509Sertifika2** özel, genel anahtarları ve sertifika zincirini tutan. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create)(*byte[], SecureString*) | Oluşturur`CertificateHolder` PKCS12 deposunun bayt dizisini ve şifresini kullanan nesne. |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create_1)(*byte[], string*) | Oluşturur`CertificateHolder` PKCS12 deposunun bayt dizisini ve şifresini kullanan nesne. |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create_2)(*string, string*) | Oluşturur`CertificateHolder`PKCS12 deposuna giden yolu ve parolasını kullanan nesne. |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create_3)(*string, string, string*) | Oluşturur`CertificateHolder` PKCS12 deposuna giden yolu, parolasını ve özel anahtar ve sertifikanın bulunacağı takma adı kullanan nesne. |

## Notlar

`CertificateHolder` yalnızca statik fabrika yöntemleri tarafından oluşturulabilir. Bir örneğini içerir**X509Sertifika2** Sisteme özel, genel anahtarlar ve sertifika zincirlerini tanıtmak için kullanılan sınıf. Bu sınıf,[`DigitalSignatureUtil`](../digitalsignatureutil/) Ve[`PdfDigitalSignatureDetails`](../../aspose.words.saving/pdfdigitalsignaturedetails/) ile eski yöntemler yerineX509Certificate2 parametre olarak.

## Örnekler

Şifrelenmiş belge dosyasının nasıl imzalanacağını gösterir.

```csharp
// Özel bir anahtar içermesi gereken bir PKCS#12 deposundan bir X.509 sertifikası oluşturun.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Yeni dijital imzamızla uygulanacak bir yorum, tarih ve şifre çözme şifresi oluşturun.
SignOptions signOptions = new SignOptions
{
    Comments = "Comment",
    SignTime = DateTime.Now,
    DecryptionPassword = "docPassword"
};

// İmzalanmamış girdi belgesi için yerel bir sistem dosya adı ve yeni dijital olarak imzalanmış kopyası için bir çıktı dosya adı ayarlayın.
string inputFileName = MyDir + "Encrypted.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.DecryptionPassword.docx";

DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

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

Bir belgeye imza satırının nasıl ekleneceğini ve ardından dijital sertifika kullanılarak nasıl imzalanacağını gösterir.

```csharp
[Description("WORDSNET-16868")]
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
/// Sağlanan imzalayan bilgileri ve X509 sertifikası kullanılarak imzalanmış bir kaynak belgenin kopyasını oluşturur.
/// </summary>
private static void SignDocument(string srcDocumentPath, string dstDocumentPath,
    Signee signeeInfo, string certificatePath, string certificatePassword)
{
    Document document = new Document(srcDocumentPath);
    DocumentBuilder builder = new DocumentBuilder(document);

    // Belgeye imzamızı koyacağımız bir nesne olan imza satırını yapılandırın ve ekleyin.
    SignatureLineOptions signatureLineOptions = new SignatureLineOptions
    {
        Signer = signeeInfo.Name, 
        SignerTitle = signeeInfo.Position
    };

    SignatureLine signatureLine = builder.InsertSignatureLine(signatureLineOptions).SignatureLine;
    signatureLine.Id = signeeInfo.PersonId;

    // İlk olarak belgemizin imzasız halini kaydedeceğiz.
    builder.Document.Save(dstDocumentPath);

    CertificateHolder certificateHolder = CertificateHolder.Create(certificatePath, certificatePassword);

    SignOptions signOptions = new SignOptions
    {
        SignatureLineId = signeeInfo.PersonId,
        SignatureLineImage = signeeInfo.Image
    };

    // Yukarıda kaydettiğimiz imzasız belgenin üzerine sertifika kullanılarak imzalanmış bir sürüm yaz.
    DigitalSignatureUtil.Sign(dstDocumentPath, dstDocumentPath, certificateHolder, signOptions);
}

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
    var signImagePath = ImageDir + "Logo.jpg";

    mSignees = new List<Signee>
    {
        new Signee(Guid.NewGuid(), "Ron Williams", "Chief Executive Officer", TestUtil.ImageToByteArray(signImagePath)),
        new Signee(Guid.NewGuid(), "Stephen Morse", "Head of Compliance", TestUtil.ImageToByteArray(signImagePath))
    };
}

private static List<Signee> mSignees;
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../)
