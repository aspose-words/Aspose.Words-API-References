---
title: CertificateHolder Class
linktitle: CertificateHolder
articleTitle: CertificateHolder
second_title: Aspose.Words för .NET
description: Upptäck klassen Aspose.Words.DigitalSignatures.CertificateHolder, din nyckel till att hantera X509Certificate2-instanser för säkra digitala signaturer.
type: docs
weight: 570
url: /sv/net/aspose.words.digitalsignatures/certificateholder/
---
## CertificateHolder class

Representerar en innehavare av**X509Certifikat2** instans.

För att lära dig mer, besök[Arbeta med digitala signaturer](https://docs.aspose.com/words/net/working-with-digital-signatures/) dokumentationsartikel.

```csharp
public class CertificateHolder
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Certificate](../../aspose.words.digitalsignatures/certificateholder/certificate/) { get; } | Returnerar instansen av**X509Certifikat2** som innehåller privata, publika nycklar och certifikatkedja. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create)(*byte[], SecureString*) | Skapar`CertificateHolder` objekt som använder byte-arrayen för PKCS12-arkivet och dess lösenord. |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create_1)(*byte[], string*) | Skapar`CertificateHolder` objekt som använder byte-arrayen för PKCS12-arkivet och dess lösenord. |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create_2)(*string, string*) | Skapar`CertificateHolder`objekt med sökvägen till PKCS12-arkivet och dess lösenord. |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create_3)(*string, string, string*) | Skapar`CertificateHolder` objekt med sökvägen till PKCS12-arkivet, dess lösenord och alias med vilket privat nyckel och certifikat som ska hittas. |

## Anmärkningar

`CertificateHolder` kan endast skapas med statiska fabriksmetoder. Den innehåller en instans av**X509Certifikat2** som används för att introducera privata, publika nycklar och certifikatkedjor i systemet. Denna klass tillämpas i[`DigitalSignatureUtil`](../digitalsignatureutil/) och[`PdfDigitalSignatureDetails`](../../aspose.words.saving/pdfdigitalsignaturedetails/) istället för föråldrade metoder med X509Certificate2 som parametrar.

## Exempel

Visar hur man signerar en krypterad dokumentfil.

```csharp
// Skapa ett X.509-certifikat från ett PKCS#12-arkiv, vilket ska innehålla en privat nyckel.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Skapa ett lösenord för kommentar, datum och dekryptering som kommer att tillämpas med vår nya digitala signatur.
SignOptions signOptions = new SignOptions
{
    Comments = "Comment",
    SignTime = DateTime.Now,
    DecryptionPassword = "docPassword"
};

// Ange ett lokalt systemfilnamn för det osignerade indatadokumentet och ett utdatafilnamn för dess nya digitalt signerade kopia.
string inputFileName = MyDir + "Encrypted.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.DecryptionPassword.docx";

DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

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

* namnutrymme [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* hopsättning [Aspose.Words](../../)
