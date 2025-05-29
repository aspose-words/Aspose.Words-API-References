---
title: SignatureLine.Id
linktitle: Id
articleTitle: Id
second_title: Aspose.Words per .NET
description: Scopri la proprietà SignatureLine Id per gestire e personalizzare facilmente gli identificatori della riga della firma, per un'integrazione fluida dei documenti e un'esperienza utente migliorata.
type: docs
weight: 40
url: /it/net/aspose.words.drawing/signatureline/id/
---
## SignatureLine.Id property

Ottiene o imposta l'identificatore per questa riga della firma.

Questo identificatore può essere associato a una firma digitale, quando si firma un documento utilizzando[`DigitalSignatureUtil`](../../../aspose.words.digitalsignatures/digitalsignatureutil/). Questo valore deve essere univoco e per impostazione predefinita viene generato casualmente il nuovo Guid (NewGuid).

```csharp
public Guid Id { get; set; }
```

## Esempi

Mostra come aggiungere una riga per la firma a un documento e poi firmarlo utilizzando un certificato digitale.

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
/// Crea una copia di un documento sorgente firmato utilizzando le informazioni fornite sul firmatario e il certificato X509.
/// </summary>
private static void SignDocument(string srcDocumentPath, string dstDocumentPath,
    Signee signeeInfo, string certificatePath, string certificatePassword)
{
    Document document = new Document(srcDocumentPath);
    DocumentBuilder builder = new DocumentBuilder(document);

    // Configura e inserisci una riga della firma, un oggetto nel documento che visualizzerà la firma con cui lo firmeremo.
    SignatureLineOptions signatureLineOptions = new SignatureLineOptions
    {
        Signer = signeeInfo.Name, 
        SignerTitle = signeeInfo.Position
    };

    SignatureLine signatureLine = builder.InsertSignatureLine(signatureLineOptions).SignatureLine;
    signatureLine.Id = signeeInfo.PersonId;

    // Per prima cosa, salveremo una versione non firmata del nostro documento.
    builder.Document.Save(dstDocumentPath);

    CertificateHolder certificateHolder = CertificateHolder.Create(certificatePath, certificatePassword);

    SignOptions signOptions = new SignOptions
    {
        SignatureLineId = signeeInfo.PersonId,
        SignatureLineImage = signeeInfo.Image
    };

    // Sovrascrivi il documento non firmato salvato sopra con una versione firmata utilizzando il certificato.
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

### Guarda anche

* class [SignatureLine](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
