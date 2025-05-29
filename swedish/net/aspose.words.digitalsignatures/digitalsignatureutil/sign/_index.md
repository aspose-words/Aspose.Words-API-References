---
title: DigitalSignatureUtil.Sign
linktitle: Sign
articleTitle: Sign
second_title: Aspose.Words för .NET
description: Signera dina dokument enkelt med DigitalSignatureUtils signeringsmetod. Använd digitala signaturer säkert med CertificateHolder och SignOptions.
type: docs
weight: 30
url: /sv/net/aspose.words.digitalsignatures/digitalsignatureutil/sign/
---
## Sign(*Stream, Stream, [CertificateHolder](../../certificateholder/), [SignOptions](../../signoptions/)*) {#sign_1}

Signerar källdokument med hjälp av angivet[`CertificateHolder`](../../certificateholder/) och[`SignOptions`](../../signoptions/) med digital signatur och skriver signerat dokument till destinationsströmmen.

Format som stöds är: Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott.

**Utdata kommer att skrivas till början av strömmen och strömstorleken kommer att uppdateras med innehållets längd.**

```csharp
public static void Sign(Stream srcStream, Stream dstStream, CertificateHolder certHolder, 
    SignOptions signOptions)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| srcStream | Stream | Den ström som innehåller dokumentet som ska signeras. |
| dstStream | Stream | Den ström som signerade dokumentet kommer att skrivas till. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) objekt med certifikat som användes för att signera filen. Certifikatinnehavaren MÅSTE innehålla privata nycklar och ha flaggan X509KeyStorageFlags.Exportable satt. |
| signOptions | SignOptions | [`SignOptions`](../../signoptions/) objekt med olika signeringsalternativ. |

## Exempel

Visar hur man signerar dokument digitalt.

```csharp
// Skapa ett X.509-certifikat från ett PKCS#12-arkiv, vilket ska innehålla en privat nyckel.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Skapa en kommentar och ett datum som kommer att tillämpas med vår nya digitala signatur.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Hämta ett osignerat dokument från det lokala filsystemet via en filström,
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
* namnutrymme [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* hopsättning [Aspose.Words](../../../)

---

## Sign(*string, string, [CertificateHolder](../../certificateholder/), [SignOptions](../../signoptions/)*) {#sign_3}

Signerar källdokument med hjälp av angivet[`CertificateHolder`](../../certificateholder/) och[`SignOptions`](../../signoptions/) med digital signatur och skriver signerat dokument till destinationsfilen.

Format som stöds är: Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott.

```csharp
public static void Sign(string srcFileName, string dstFileName, CertificateHolder certHolder, 
    SignOptions signOptions)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| srcFileName | String | Filnamnet på dokumentet som ska signeras. |
| dstFileName | String | Filnamnet på det signerade dokumentet som utdata. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) objekt med certifikat som användes för att signera filen. Certifikatinnehavaren MÅSTE innehålla privata nycklar och ha flaggan X509KeyStorageFlags.Exportable satt. |
| signOptions | SignOptions | [`SignOptions`](../../signoptions/) objekt med olika signeringsalternativ. |

## Exempel

Visar hur man lägger till en signaturrad i ett dokument och sedan signerar det med ett digitalt certifikat.

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
/// Skapar en kopia av ett källdokument som signerats med den angivna informationen om signeraren och ett X509-certifikat.
/// </summary>
private static void SignDocument(string srcDocumentPath, string dstDocumentPath,
    Signee signeeInfo, string certificatePath, string certificatePassword)
{
    Document document = new Document(srcDocumentPath);
    DocumentBuilder builder = new DocumentBuilder(document);

    // Konfigurera och infoga en signaturrad, ett objekt i dokumentet som visar en signatur som vi signerar det med.
    SignatureLineOptions signatureLineOptions = new SignatureLineOptions
    {
        Signer = signeeInfo.Name, 
        SignerTitle = signeeInfo.Position
    };

    SignatureLine signatureLine = builder.InsertSignatureLine(signatureLineOptions).SignatureLine;
    signatureLine.Id = signeeInfo.PersonId;

    // Först sparar vi en osignerad version av vårt dokument.
    builder.Document.Save(dstDocumentPath);

    CertificateHolder certificateHolder = CertificateHolder.Create(certificatePath, certificatePassword);

    SignOptions signOptions = new SignOptions
    {
        SignatureLineId = signeeInfo.PersonId,
        SignatureLineImage = signeeInfo.Image
    };

    // Skriv över det osignerade dokumentet som vi sparade ovan med en version som signerats med certifikatet.
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

### Se även

* class [CertificateHolder](../../certificateholder/)
* class [SignOptions](../../signoptions/)
* class [DigitalSignatureUtil](../)
* namnutrymme [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* hopsättning [Aspose.Words](../../../)

---

## Sign(*Stream, Stream, [CertificateHolder](../../certificateholder/)*) {#sign}

Signerar källdokument med hjälp av angivet[`CertificateHolder`](../../certificateholder/) med digital signatur och skriver signerat dokument till destinationsströmmen.

Format som stöds är: Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott.

**Utdata kommer att skrivas till början av strömmen och strömstorleken kommer att uppdateras med innehållets längd.**

```csharp
public static void Sign(Stream srcStream, Stream dstStream, CertificateHolder certHolder)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| srcStream | Stream | Den ström som innehåller dokumentet som ska signeras. |
| dstStream | Stream | Den ström som signerade dokumentet kommer att skrivas till. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) objekt med certifikat som användes för att signera filen. Certifikatinnehavaren MÅSTE innehålla privata nycklar och ha flaggan X509KeyStorageFlags.Exportable satt. |

## Exempel

Visar hur man signerar dokument med X.509-certifikat.

```csharp
// Verifiera att ett dokument inte är signerat.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Skapa ett CertificateHolder-objekt från en PKCS12-fil, som vi kommer att använda för att signera dokumentet.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Det finns två sätt att spara en signerad kopia av ett dokument i det lokala filsystemet:
// 1 - Ange ett dokument med ett lokalt systemfilnamn och spara en signerad kopia på en plats som anges med ett annat filnamn.
SignOptions signOptions = new SignOptions { SignTime = DateTime.Now };
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx",
    certificateHolder, signOptions);

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - Ta ett dokument från en ström och spara en signerad kopia till en annan ström.
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
* namnutrymme [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* hopsättning [Aspose.Words](../../../)

---

## Sign(*string, string, [CertificateHolder](../../certificateholder/)*) {#sign_2}

Signerar källdokument med hjälp av angivet[`CertificateHolder`](../../certificateholder/) med digital signatur och skriver signerat dokument till destinationsfilen.

Format som stöds är: Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott.

```csharp
public static void Sign(string srcFileName, string dstFileName, CertificateHolder certHolder)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| srcFileName | String | Filnamnet på dokumentet som ska signeras. |
| dstFileName | String | Filnamnet på det signerade dokumentet som utdata. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) objekt med certifikat som användes för att signera filen. Certifikatinnehavaren MÅSTE innehålla privata nycklar och ha flaggan X509KeyStorageFlags.Exportable satt. |

## Exempel

Visar hur man signerar dokument med X.509-certifikat.

```csharp
// Verifiera att ett dokument inte är signerat.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Skapa ett CertificateHolder-objekt från en PKCS12-fil, som vi kommer att använda för att signera dokumentet.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Det finns två sätt att spara en signerad kopia av ett dokument i det lokala filsystemet:
// 1 - Ange ett dokument med ett lokalt systemfilnamn och spara en signerad kopia på en plats som anges med ett annat filnamn.
SignOptions signOptions = new SignOptions { SignTime = DateTime.Now };
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx",
    certificateHolder, signOptions);

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - Ta ett dokument från en ström och spara en signerad kopia till en annan ström.
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
* namnutrymme [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* hopsättning [Aspose.Words](../../../)
