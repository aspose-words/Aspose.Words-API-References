---
title: Sign
second_title: Aspose.Words for .NET API Referansı
description: Verilenleri kullanarak kaynak belgeyi imzalarCertificateHolderaspose.words.digitalsignatures/certificateholder veSignOptionsaspose.words.digitalsignatures/signoptions dijital imzalı ve imzalı belgeyi hedef akışa yazar.
type: docs
weight: 30
url: /tr/net/aspose.words.digitalsignatures/digitalsignatureutil/sign/
---
## Sign(Stream, Stream, CertificateHolder, SignOptions) {#sign_1}

Verilenleri kullanarak kaynak belgeyi imzalar[`CertificateHolder`](../../certificateholder) ve[`SignOptions`](../../signoptions) dijital imzalı ve imzalı belgeyi hedef akışa yazar.

Belge ya olmalıdırDoc veyaDocx.

**Çıktı akışın başına yazılacak ve akış boyutu içerik uzunluğu ile güncellenecektir.**

```csharp
public static void Sign(Stream srcStream, Stream dstStream, CertificateHolder certHolder, 
    SignOptions signOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| srcStream | Stream | İmzalanacak belgeyi içeren akış. |
| dstStream | Stream | Belgenin imzalandığı akışa yazılacak. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder) dosya imzalamak için kullanılan sertifikaya sahip nesne. Sahibindeki sertifikanın özel anahtarlar içermesi ve X509KeyStorageFlags.Exportable bayrağının ayarlanmış olması ZORUNLUDUR. |
| signOptions | SignOptions | [`SignOptions`](../../signoptions) çeşitli imzalama seçenekleriyle nesne. |

### Örnekler

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

### Ayrıca bakınız

* class [CertificateHolder](../../certificateholder)
* class [SignOptions](../../signoptions)
* class [DigitalSignatureUtil](../../digitalsignatureutil)
* ad alanı [Aspose.Words.DigitalSignatures](../../digitalsignatureutil)
* toplantı [Aspose.Words](../../../)

---

## Sign(string, string, CertificateHolder, SignOptions) {#sign_3}

Verilenleri kullanarak kaynak belgeyi imzalar[`CertificateHolder`](../../certificateholder) ve[`SignOptions`](../../signoptions) dijital imzalı ve imzalı belgeyi hedef dosyaya yazar.

Belge ya olmalıdırDoc veyaDocx.

```csharp
public static void Sign(string srcFileName, string dstFileName, CertificateHolder certHolder, 
    SignOptions signOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| srcFileName | String | İmzalanacak belgenin dosya adı. |
| dstFileName | String | İmzalı belge çıktısının dosya adı. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder) dosya imzalamak için kullanılan sertifikaya sahip nesne. Sahibindeki sertifikanın özel anahtarlar içermesi ve X509KeyStorageFlags.Exportable bayrağının ayarlanmış olması ZORUNLUDUR. |
| signOptions | SignOptions | [`SignOptions`](../../signoptions) çeşitli imzalama seçenekleriyle nesne. |

### Örnekler

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

* class [CertificateHolder](../../certificateholder)
* class [SignOptions](../../signoptions)
* class [DigitalSignatureUtil](../../digitalsignatureutil)
* ad alanı [Aspose.Words.DigitalSignatures](../../digitalsignatureutil)
* toplantı [Aspose.Words](../../../)

---

## Sign(Stream, Stream, CertificateHolder) {#sign}

Verilenleri kullanarak kaynak belgeyi imzalar[`CertificateHolder`](../../certificateholder)dijital imza ile ve imzalı belgeyi hedef akışa yazar.

Belge ya olmalıdırDoc veyaDocx.

**Çıktı akışın başına yazılacak ve akış boyutu içerik uzunluğu ile güncellenecektir.**

```csharp
public static void Sign(Stream srcStream, Stream dstStream, CertificateHolder certHolder)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| srcStream | Stream | İmzalanacak belgeyi içeren akış. |
| dstStream | Stream | Belgenin imzalandığı akışa yazılacak. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder) dosya imzalamak için kullanılan sertifikaya sahip nesne. Sahibindeki sertifikanın özel anahtarlar içermesi ve X509KeyStorageFlags.Exportable bayrağının ayarlanmış olması ZORUNLUDUR. |

### Örnekler

X.509 sertifikalarıyla belgelerin nasıl imzalanacağını gösterir.

```csharp
// Bir belgenin imzalanmadığını doğrulayın.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Belgeyi imzalamak için kullanacağımız bir PKCS12 dosyasından bir CertificateHolder nesnesi oluşturun.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Belgenin imzalı bir kopyasını yerel dosya sistemine kaydetmenin iki yolu vardır:
// 1 - Bir belgeyi yerel sistem dosya adıyla atayın ve imzalı bir kopyayı başka bir dosya adıyla belirtilen bir konuma kaydedin.
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx", 
    certificateHolder, new SignOptions() { SignTime = DateTime.Now } );

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

* class [CertificateHolder](../../certificateholder)
* class [DigitalSignatureUtil](../../digitalsignatureutil)
* ad alanı [Aspose.Words.DigitalSignatures](../../digitalsignatureutil)
* toplantı [Aspose.Words](../../../)

---

## Sign(string, string, CertificateHolder) {#sign_2}

Verilenleri kullanarak kaynak belgeyi imzalar[`CertificateHolder`](../../certificateholder) dijital imza ile ve imzalı belgeyi hedef dosyaya yazar.

Belge ya olmalıdırDoc veyaDocx.

```csharp
public static void Sign(string srcFileName, string dstFileName, CertificateHolder certHolder)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| srcFileName | String | İmzalanacak belgenin dosya adı. |
| dstFileName | String | İmzalı belge çıktısının dosya adı. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder) dosya imzalamak için kullanılan sertifikaya sahip nesne. Sahibindeki sertifikanın özel anahtarlar içermesi ve X509KeyStorageFlags.Exportable bayrağının ayarlanmış olması ZORUNLUDUR. |

### Örnekler

X.509 sertifikalarıyla belgelerin nasıl imzalanacağını gösterir.

```csharp
// Bir belgenin imzalanmadığını doğrulayın.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Belgeyi imzalamak için kullanacağımız bir PKCS12 dosyasından bir CertificateHolder nesnesi oluşturun.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Belgenin imzalı bir kopyasını yerel dosya sistemine kaydetmenin iki yolu vardır:
// 1 - Bir belgeyi yerel sistem dosya adıyla atayın ve imzalı bir kopyayı başka bir dosya adıyla belirtilen bir konuma kaydedin.
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx", 
    certificateHolder, new SignOptions() { SignTime = DateTime.Now } );

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

* class [CertificateHolder](../../certificateholder)
* class [DigitalSignatureUtil](../../digitalsignatureutil)
* ad alanı [Aspose.Words.DigitalSignatures](../../digitalsignatureutil)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
