---
title: DigitalSignatureUtil.Sign
linktitle: Sign
articleTitle: Sign
second_title: .NET için Aspose.Words
description: Belgelerinizi DigitalSignatureUtil'in Sign metoduyla zahmetsizce imzalayın. CertificateHolder ve SignOptions kullanarak dijital imzaları güvenli bir şekilde uygulayın.
type: docs
weight: 30
url: /tr/net/aspose.words.digitalsignatures/digitalsignatureutil/sign/
---
## Sign(*Stream, Stream, [CertificateHolder](../../certificateholder/), [SignOptions](../../signoptions/)*) {#sign_1}

Verileni kullanarak kaynak belgeyi işaretler[`CertificateHolder`](../../certificateholder/) Ve[`SignOptions`](../../signoptions/) dijital imza ile imzalanmış belgeyi hedef akışa yazar.

Desteklenen biçimler şunlardır: Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott.

**Çıktı, akışın başlangıcına yazılacak ve akış boyutu içerik uzunluğuna göre güncellenecektir.**

```csharp
public static void Sign(Stream srcStream, Stream dstStream, CertificateHolder certHolder, 
    SignOptions signOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| srcStream | Stream | İmzalanacak belgenin bulunduğu akış. |
| dstStream | Stream | İmzalanan belgenin yazılacağı akış. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) Dosyayı imzalamak için kullanılan sertifikaya sahip nesne. Sahibindeki sertifika özel anahtarlar içermeli ve X509KeyStorageFlags.Exportable bayrağı ayarlanmalıdır. |
| signOptions | SignOptions | [`SignOptions`](../../signoptions/) Çeşitli imzalama seçeneklerine sahip nesne. |

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

* class [CertificateHolder](../../certificateholder/)
* class [SignOptions](../../signoptions/)
* class [DigitalSignatureUtil](../)
* ad alanı [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../../)

---

## Sign(*string, string, [CertificateHolder](../../certificateholder/), [SignOptions](../../signoptions/)*) {#sign_3}

Verileni kullanarak kaynak belgeyi işaretler[`CertificateHolder`](../../certificateholder/) Ve[`SignOptions`](../../signoptions/) dijital imza ile imzalanmış belgeyi hedef dosyaya yazar.

Desteklenen biçimler şunlardır: Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott.

```csharp
public static void Sign(string srcFileName, string dstFileName, CertificateHolder certHolder, 
    SignOptions signOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| srcFileName | String | İmzalanacak belgenin dosya adı. |
| dstFileName | String | İmzalanmış belge çıktısının dosya adı. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) Dosyayı imzalamak için kullanılan sertifikaya sahip nesne. Sahibindeki sertifika özel anahtarlar içermeli ve X509KeyStorageFlags.Exportable bayrağı ayarlanmalıdır. |
| signOptions | SignOptions | [`SignOptions`](../../signoptions/) Çeşitli imzalama seçeneklerine sahip nesne. |

## Örnekler

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

* class [CertificateHolder](../../certificateholder/)
* class [SignOptions](../../signoptions/)
* class [DigitalSignatureUtil](../)
* ad alanı [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../../)

---

## Sign(*Stream, Stream, [CertificateHolder](../../certificateholder/)*) {#sign}

Verileni kullanarak kaynak belgeyi işaretler[`CertificateHolder`](../../certificateholder/) dijital imza ile imzalanmış belgeyi hedef akışa yazar.

Desteklenen biçimler şunlardır: Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott.

**Çıktı, akışın başlangıcına yazılacak ve akış boyutu içerik uzunluğuna göre güncellenecektir.**

```csharp
public static void Sign(Stream srcStream, Stream dstStream, CertificateHolder certHolder)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| srcStream | Stream | İmzalanacak belgenin bulunduğu akış. |
| dstStream | Stream | İmzalanan belgenin yazılacağı akış. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) Dosyayı imzalamak için kullanılan sertifikaya sahip nesne. Sahibindeki sertifika özel anahtarlar içermeli ve X509KeyStorageFlags.Exportable bayrağı ayarlanmalıdır. |

## Örnekler

X.509 sertifikalarıyla belgelerin nasıl imzalanacağını gösterir.

```csharp
// Bir belgenin imzalanmadığını doğrulayın.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Belgeyi imzalamak için kullanacağımız PKCS12 dosyasından bir CertificateHolder nesnesi oluşturalım.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Bir belgenin imzalı bir kopyasını yerel dosya sistemine kaydetmenin iki yolu vardır:
// 1 - Bir belgeyi yerel sistem dosya adıyla tanımlayın ve imzalı bir kopyasını başka bir dosya adıyla belirtilen bir konuma kaydedin.
SignOptions signOptions = new SignOptions { SignTime = DateTime.Now };
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx",
    certificateHolder, signOptions);

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - Bir akıştan bir belge alın ve imzalı bir kopyasını başka bir akışa kaydedin.
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// Lütfen belgenin tüm dijital imzalarının geçerli olduğunu doğrulayın ve ayrıntılarını kontrol edin.
Document signedDoc = new Document(ArtifactsDir + "Document.DigitalSignature.docx");
DigitalSignatureCollection digitalSignatureCollection = signedDoc.DigitalSignatures;

Assert.True(digitalSignatureCollection.IsValid);
Assert.AreEqual(1, digitalSignatureCollection.Count);
Assert.AreEqual(DigitalSignatureType.XmlDsig, digitalSignatureCollection[0].SignatureType);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].IssuerName);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].SubjectName);
```

### Ayrıca bakınız

* class [CertificateHolder](../../certificateholder/)
* class [DigitalSignatureUtil](../)
* ad alanı [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../../)

---

## Sign(*string, string, [CertificateHolder](../../certificateholder/)*) {#sign_2}

Verileni kullanarak kaynak belgeyi işaretler[`CertificateHolder`](../../certificateholder/) dijital imza ile imzalanmış belgeyi hedef dosyaya yazar.

Desteklenen biçimler şunlardır: Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott.

```csharp
public static void Sign(string srcFileName, string dstFileName, CertificateHolder certHolder)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| srcFileName | String | İmzalanacak belgenin dosya adı. |
| dstFileName | String | İmzalanmış belge çıktısının dosya adı. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) Dosyayı imzalamak için kullanılan sertifikaya sahip nesne. Sahibindeki sertifika özel anahtarlar içermeli ve X509KeyStorageFlags.Exportable bayrağı ayarlanmalıdır. |

## Örnekler

X.509 sertifikalarıyla belgelerin nasıl imzalanacağını gösterir.

```csharp
// Bir belgenin imzalanmadığını doğrulayın.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Belgeyi imzalamak için kullanacağımız PKCS12 dosyasından bir CertificateHolder nesnesi oluşturalım.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Bir belgenin imzalı bir kopyasını yerel dosya sistemine kaydetmenin iki yolu vardır:
// 1 - Bir belgeyi yerel sistem dosya adıyla tanımlayın ve imzalı bir kopyasını başka bir dosya adıyla belirtilen bir konuma kaydedin.
SignOptions signOptions = new SignOptions { SignTime = DateTime.Now };
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx",
    certificateHolder, signOptions);

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - Bir akıştan bir belge alın ve imzalı bir kopyasını başka bir akışa kaydedin.
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// Lütfen belgenin tüm dijital imzalarının geçerli olduğunu doğrulayın ve ayrıntılarını kontrol edin.
Document signedDoc = new Document(ArtifactsDir + "Document.DigitalSignature.docx");
DigitalSignatureCollection digitalSignatureCollection = signedDoc.DigitalSignatures;

Assert.True(digitalSignatureCollection.IsValid);
Assert.AreEqual(1, digitalSignatureCollection.Count);
Assert.AreEqual(DigitalSignatureType.XmlDsig, digitalSignatureCollection[0].SignatureType);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].IssuerName);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].SubjectName);
```

### Ayrıca bakınız

* class [CertificateHolder](../../certificateholder/)
* class [DigitalSignatureUtil](../)
* ad alanı [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* toplantı [Aspose.Words](../../../)
