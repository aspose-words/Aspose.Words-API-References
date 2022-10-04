---
title: Sign
second_title: Aspose.Words för .NET API Referens
description: Signerar källdokument med givenCertificateHolderaspose.words.digitalsignatures/certificateholder/ ochSignOptionsaspose.words.digitalsignatures/signoptions/ med digital signatur och skriver signerat dokument till destinationsströmmen.
type: docs
weight: 30
url: /sv/net/aspose.words.digitalsignatures/digitalsignatureutil/sign/
---
## Sign(Stream, Stream, CertificateHolder, SignOptions) {#sign_1}

Signerar källdokument med given[`CertificateHolder`](../../certificateholder/) och[`SignOptions`](../../signoptions/) med digital signatur och skriver signerat dokument till destinationsströmmen.

Dokument bör vara antingenDoc ellerDocx.

**Utdata kommer att skrivas till starten av strömmen och strömstorleken kommer att uppdateras med innehållets längd.**

```csharp
public static void Sign(Stream srcStream, Stream dstStream, CertificateHolder certHolder, 
    SignOptions signOptions)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| srcStream | Stream | Strömmen som innehåller dokumentet som ska signeras. |
| dstStream | Stream | Streamen som det signerade dokumentet kommer att skrivas till. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) objekt med certifikat som användes för att signera filen. Certifikatet i innehavaren MÅSTE innehålla privata nycklar och ha flaggan X509KeyStorageFlags.Exportable inställd. |
| signOptions | SignOptions | [`SignOptions`](../../signoptions/) objekt med olika signeringsalternativ. |

### Exempel

Visar hur man digitalt signerar dokument.

```csharp
// Skapa ett X.509-certifikat från en PKCS#12-butik, som bör innehålla en privat nyckel.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Skapa en kommentar och ett datum som kommer att tillämpas med vår nya digitala signatur.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Ta ett osignerat dokument från det lokala filsystemet via en filström,
// skapa sedan en signerad kopia av den som bestäms av filnamnet på utdatafilströmmen.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

### Se även

* class [CertificateHolder](../../certificateholder/)
* class [SignOptions](../../signoptions/)
* class [DigitalSignatureUtil](../)
* namnutrymme [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* hopsättning [Aspose.Words](../../../)

---

## Sign(string, string, CertificateHolder, SignOptions) {#sign_3}

Signerar källdokument med given[`CertificateHolder`](../../certificateholder/) och[`SignOptions`](../../signoptions/) med digital signatur och skriver signerat dokument till destinationsfilen.

Dokument bör vara antingenDoc ellerDocx.

```csharp
public static void Sign(string srcFileName, string dstFileName, CertificateHolder certHolder, 
    SignOptions signOptions)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| srcFileName | String | Filnamnet på dokumentet som ska undertecknas. |
| dstFileName | String | Filnamnet på det signerade dokumentutmatningen. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) objekt med certifikat som användes för att signera filen. Certifikatet i innehavaren MÅSTE innehålla privata nycklar och ha flaggan X509KeyStorageFlags.Exportable inställd. |
| signOptions | SignOptions | [`SignOptions`](../../signoptions/) objekt med olika signeringsalternativ. |

### Exempel

Visar hur man lägger till en signaturrad i ett dokument och sedan signerar den med ett digitalt certifikat.

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
        /// Skapar en kopia av ett källdokument som är signerat med den angivna signatärinformationen och X509-certifikatet.
        /// </summary>
        private static void SignDocument(string srcDocumentPath, string dstDocumentPath,
            Signee signeeInfo, string certificatePath, string certificatePassword)
        {
            Document document = new Document(srcDocumentPath);
            DocumentBuilder builder = new DocumentBuilder(document);

            // Konfigurera och infoga en signaturrad, ett objekt i dokumentet som kommer att visa en signatur som vi signerar det med.
            SignatureLineOptions signatureLineOptions = new SignatureLineOptions
            {
                Signer = signeeInfo.Name, 
                SignerTitle = signeeInfo.Position
            };

            SignatureLine signatureLine = builder.InsertSignatureLine(signatureLineOptions).SignatureLine;
            signatureLine.Id = signeeInfo.PersonId;

            // Först kommer vi att spara en osignerad version av vårt dokument.
            builder.Document.Save(dstDocumentPath);

            CertificateHolder certificateHolder = CertificateHolder.Create(certificatePath, certificatePassword);

            SignOptions signOptions = new SignOptions
            {
                SignatureLineId = signeeInfo.PersonId,
                SignatureLineImage = signeeInfo.Image
            };

            // Skriv över det osignerade dokumentet vi sparade ovan med en version signerad med certifikatet.
            DigitalSignatureUtil.Sign(dstDocumentPath, dstDocumentPath, certificateHolder, signOptions);
        }

#if NET48 || JAVA
        /// <summary>
        /// Konverterar en bild till en byte-array.
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

### Se även

* class [CertificateHolder](../../certificateholder/)
* class [SignOptions](../../signoptions/)
* class [DigitalSignatureUtil](../)
* namnutrymme [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* hopsättning [Aspose.Words](../../../)

---

## Sign(Stream, Stream, CertificateHolder) {#sign}

Signerar källdokument med given[`CertificateHolder`](../../certificateholder/)med digital signatur och skriver signerat dokument till destinationsströmmen.

Dokument bör vara antingenDoc ellerDocx.

**Utdata kommer att skrivas till starten av strömmen och strömstorleken kommer att uppdateras med innehållets längd.**

```csharp
public static void Sign(Stream srcStream, Stream dstStream, CertificateHolder certHolder)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| srcStream | Stream | Strömmen som innehåller dokumentet som ska signeras. |
| dstStream | Stream | Streamen som det signerade dokumentet kommer att skrivas till. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) objekt med certifikat som användes för att signera filen. Certifikatet i innehavaren MÅSTE innehålla privata nycklar och ha flaggan X509KeyStorageFlags.Exportable inställd. |

### Exempel

Visar hur man signerar dokument med X.509-certifikat.

```csharp
// Kontrollera att ett dokument inte är signerat.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Skapa ett CertificateHolder-objekt från en PKCS12-fil, som vi kommer att använda för att signera dokumentet.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Det finns två sätt att spara en signerad kopia av ett dokument till det lokala filsystemet:
// 1 - Ange ett dokument med ett lokalt systemfilnamn och spara en signerad kopia på en plats som anges med ett annat filnamn.
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx", 
    certificateHolder, new SignOptions() { SignTime = DateTime.Now } );

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - Ta ett dokument från en stream och spara en signerad kopia till en annan stream.
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// Kontrollera att alla dokumentets digitala signaturer är giltiga och kontrollera deras uppgifter.
Document signedDoc = new Document(ArtifactsDir + "Document.DigitalSignature.docx");
DigitalSignatureCollection digitalSignatureCollection = signedDoc.DigitalSignatures;

Assert.True(digitalSignatureCollection.IsValid);
Assert.AreEqual(1, digitalSignatureCollection.Count);
Assert.AreEqual(DigitalSignatureType.XmlDsig, digitalSignatureCollection[0].SignatureType);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].IssuerName);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].SubjectName);
```

### Se även

* class [CertificateHolder](../../certificateholder/)
* class [DigitalSignatureUtil](../)
* namnutrymme [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* hopsättning [Aspose.Words](../../../)

---

## Sign(string, string, CertificateHolder) {#sign_2}

Signerar källdokument med given[`CertificateHolder`](../../certificateholder/) med digital signatur och skriver signerat dokument till destinationsfilen.

Dokument bör vara antingenDoc ellerDocx.

```csharp
public static void Sign(string srcFileName, string dstFileName, CertificateHolder certHolder)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| srcFileName | String | Filnamnet på dokumentet som ska undertecknas. |
| dstFileName | String | Filnamnet på det signerade dokumentutmatningen. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) objekt med certifikat som användes för att signera filen. Certifikatet i innehavaren MÅSTE innehålla privata nycklar och ha flaggan X509KeyStorageFlags.Exportable inställd. |

### Exempel

Visar hur man signerar dokument med X.509-certifikat.

```csharp
// Kontrollera att ett dokument inte är signerat.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Skapa ett CertificateHolder-objekt från en PKCS12-fil, som vi kommer att använda för att signera dokumentet.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Det finns två sätt att spara en signerad kopia av ett dokument till det lokala filsystemet:
// 1 - Ange ett dokument med ett lokalt systemfilnamn och spara en signerad kopia på en plats som anges med ett annat filnamn.
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx", 
    certificateHolder, new SignOptions() { SignTime = DateTime.Now } );

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - Ta ett dokument från en stream och spara en signerad kopia till en annan stream.
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// Kontrollera att alla dokumentets digitala signaturer är giltiga och kontrollera deras uppgifter.
Document signedDoc = new Document(ArtifactsDir + "Document.DigitalSignature.docx");
DigitalSignatureCollection digitalSignatureCollection = signedDoc.DigitalSignatures;

Assert.True(digitalSignatureCollection.IsValid);
Assert.AreEqual(1, digitalSignatureCollection.Count);
Assert.AreEqual(DigitalSignatureType.XmlDsig, digitalSignatureCollection[0].SignatureType);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].IssuerName);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].SubjectName);
```

### Se även

* class [CertificateHolder](../../certificateholder/)
* class [DigitalSignatureUtil](../)
* namnutrymme [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* hopsättning [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
