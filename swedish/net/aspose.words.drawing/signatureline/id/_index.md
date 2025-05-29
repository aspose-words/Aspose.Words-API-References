---
title: SignatureLine.Id
linktitle: Id
articleTitle: Id
second_title: Aspose.Words för .NET
description: Upptäck egenskapen SignatureLine Id för att enkelt hantera och anpassa signaturradsidentifierare för sömlös dokumentintegration och förbättrad användarupplevelse.
type: docs
weight: 40
url: /sv/net/aspose.words.drawing/signatureline/id/
---
## SignatureLine.Id property

Hämtar eller ställer in identifierare för denna signaturrad.

Denna identifierare kan associeras med en digital signatur vid signering av dokument med[`DigitalSignatureUtil`](../../../aspose.words.digitalsignatures/digitalsignatureutil/). Detta värde måste vara unikt och som standard genereras det slumpmässigt av en ny Guid (NewGuid).

```csharp
public Guid Id { get; set; }
```

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

* class [SignatureLine](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
