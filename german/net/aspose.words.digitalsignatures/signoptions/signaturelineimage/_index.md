---
title: SignOptions.SignatureLineImage
linktitle: SignatureLineImage
articleTitle: SignatureLineImage
second_title: Aspose.Words für .NET
description: Entdecken Sie die SignOptions SignatureLineImage-Eigenschaft, um Ihre digitalen Signaturen mit benutzerdefinierten Bildern zu verbessern. Steigern Sie noch heute die Professionalität Ihrer Marke!
type: docs
weight: 60
url: /de/net/aspose.words.digitalsignatures/signoptions/signaturelineimage/
---
## SignOptions.SignatureLineImage property

Das Bild, das in den zugehörigen[`SignatureLine`](../../../aspose.words.drawing/signatureline/) . Der Standardwert ist`null` .

```csharp
public byte[] SignatureLineImage { get; set; }
```

## Beispiele

Zeigt, wie Sie einem Dokument eine Signaturzeile hinzufügen und es dann mit einem digitalen Zertifikat signieren.

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
/// Erstellt eine Kopie eines Quelldokuments, das mit den bereitgestellten Unterzeichnerinformationen und dem X509-Zertifikat signiert wurde.
/// </summary>
private static void SignDocument(string srcDocumentPath, string dstDocumentPath,
    Signee signeeInfo, string certificatePath, string certificatePassword)
{
    Document document = new Document(srcDocumentPath);
    DocumentBuilder builder = new DocumentBuilder(document);

    // Konfigurieren und fügen Sie eine Signaturzeile ein, ein Objekt im Dokument, das eine Signatur anzeigt, mit der wir es unterschreiben.
    SignatureLineOptions signatureLineOptions = new SignatureLineOptions
    {
        Signer = signeeInfo.Name, 
        SignerTitle = signeeInfo.Position
    };

    SignatureLine signatureLine = builder.InsertSignatureLine(signatureLineOptions).SignatureLine;
    signatureLine.Id = signeeInfo.PersonId;

    // Zuerst speichern wir eine unsignierte Version unseres Dokuments.
    builder.Document.Save(dstDocumentPath);

    CertificateHolder certificateHolder = CertificateHolder.Create(certificatePath, certificatePassword);

    SignOptions signOptions = new SignOptions
    {
        SignatureLineId = signeeInfo.PersonId,
        SignatureLineImage = signeeInfo.Image
    };

    // Überschreiben Sie das oben gespeicherte, nicht signierte Dokument mit einer mit dem Zertifikat signierten Version.
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

### Siehe auch

* class [SignOptions](../)
* namensraum [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* Montage [Aspose.Words](../../../)
