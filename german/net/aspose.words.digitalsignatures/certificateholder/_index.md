---
title: CertificateHolder Class
linktitle: CertificateHolder
articleTitle: CertificateHolder
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.DigitalSignatures.CertificateHolder, Ihren Schlüssel zur Verwaltung von X509Certificate2-Instanzen für sichere digitale Signaturen.
type: docs
weight: 570
url: /de/net/aspose.words.digitalsignatures/certificateholder/
---
## CertificateHolder class

Stellt einen Inhaber von**X509Zertifikat2** Instanz.

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit digitalen Signaturen](https://docs.aspose.com/words/net/working-with-digital-signatures/) Dokumentationsartikel.

```csharp
public class CertificateHolder
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Certificate](../../aspose.words.digitalsignatures/certificateholder/certificate/) { get; } | Gibt die Instanz von**X509Zertifikat2** die private und öffentliche Schlüssel sowie die Zertifikatskette enthält. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create)(*byte[], SecureString*) | Erstellt`CertificateHolder` Objekt, das ein Byte-Array des PKCS12-Speichers und sein Passwort verwendet. |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create_1)(*byte[], string*) | Erstellt`CertificateHolder` Objekt, das ein Byte-Array des PKCS12-Speichers und sein Passwort verwendet. |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create_2)(*string, string*) | Erstellt`CertificateHolder`Objekt mit Pfad zum PKCS12-Speicher und dessen Kennwort. |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create_3)(*string, string, string*) | Erstellt`CertificateHolder` Objekt mit Pfad zum PKCS12-Speicher, seinem Passwort und dem Alias, mit dem der private Schlüssel und das Zertifikat gefunden werden. |

## Bemerkungen

`CertificateHolder` kann nur durch statische Factory-Methoden erstellt werden. Es enthält eine Instanz von**X509Zertifikat2** die verwendet wird, um private, öffentliche Schlüssel und Zertifikatsketten in das System einzuführen. Diese Klasse wird angewendet in[`DigitalSignatureUtil`](../digitalsignatureutil/) Und[`PdfDigitalSignatureDetails`](../../aspose.words.saving/pdfdigitalsignaturedetails/) anstelle veralteter Methoden mit X509Certificate2 als Parameter.

## Beispiele

Zeigt, wie eine verschlüsselte Dokumentdatei signiert wird.

```csharp
// Erstellen Sie ein X.509-Zertifikat aus einem PKCS#12-Speicher, das einen privaten Schlüssel enthalten sollte.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Erstellen Sie einen Kommentar, ein Datum und ein Entschlüsselungskennwort, das mit unserer neuen digitalen Signatur angewendet wird.
SignOptions signOptions = new SignOptions
{
    Comments = "Comment",
    SignTime = DateTime.Now,
    DecryptionPassword = "docPassword"
};

// Legen Sie einen lokalen Systemdateinamen für das unsignierte Eingabedokument und einen Ausgabedateinamen für die neue digital signierte Kopie fest.
string inputFileName = MyDir + "Encrypted.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.DecryptionPassword.docx";

DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

Zeigt, wie Dokumente digital signiert werden.

```csharp
// Erstellen Sie ein X.509-Zertifikat aus einem PKCS#12-Speicher, das einen privaten Schlüssel enthalten sollte.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Erstellen Sie einen Kommentar und ein Datum, die mit unserer neuen digitalen Signatur angewendet werden.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Über einen Dateistream ein unsigniertes Dokument aus dem lokalen Dateisystem holen,
// Erstellen Sie dann eine signierte Kopie davon, die durch den Dateinamen des Ausgabedateistreams bestimmt wird.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

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

* namensraum [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* Montage [Aspose.Words](../../)
