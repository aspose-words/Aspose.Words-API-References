---
title: DigitalSignatureUtil.Sign
linktitle: Sign
articleTitle: Sign
second_title: Aspose.Words für .NET
description: Signieren Sie Ihre Dokumente mühelos mit der Sign-Methode von DigitalSignatureUtil. Wenden Sie digitale Signaturen sicher mit CertificateHolder und SignOptions an.
type: docs
weight: 30
url: /de/net/aspose.words.digitalsignatures/digitalsignatureutil/sign/
---
## Sign(*Stream, Stream, [CertificateHolder](../../certificateholder/), [SignOptions](../../signoptions/)*) {#sign_1}

Signiert das Quelldokument mit der angegebenen[`CertificateHolder`](../../certificateholder/) Und[`SignOptions`](../../signoptions/) mit digitaler Signatur und schreibt das signierte Dokument in den Zielstream.

Unterstützte Formate sind: Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott.

**Die Ausgabe wird an den Anfang des Streams geschrieben und die Streamgröße wird mit der Inhaltslänge aktualisiert.**

```csharp
public static void Sign(Stream srcStream, Stream dstStream, CertificateHolder certHolder, 
    SignOptions signOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcStream | Stream | Der Stream, der das zu signierende Dokument enthält. |
| dstStream | Stream | Der Stream, in den das signierte Dokument geschrieben wird. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) Objekt mit Zertifikat, das zum Signieren der Datei verwendet wurde. Das Zertifikat im Inhaber MUSS private Schlüssel enthalten und das Flag X509KeyStorageFlags.Exportable gesetzt haben. |
| signOptions | SignOptions | [`SignOptions`](../../signoptions/) Objekt mit verschiedenen Signaturoptionen. |

## Beispiele

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

### Siehe auch

* class [CertificateHolder](../../certificateholder/)
* class [SignOptions](../../signoptions/)
* class [DigitalSignatureUtil](../)
* namensraum [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* Montage [Aspose.Words](../../../)

---

## Sign(*string, string, [CertificateHolder](../../certificateholder/), [SignOptions](../../signoptions/)*) {#sign_3}

Signiert das Quelldokument mit der angegebenen[`CertificateHolder`](../../certificateholder/) Und[`SignOptions`](../../signoptions/) mit digitaler Signatur und schreibt das signierte Dokument in die Zieldatei.

Unterstützte Formate sind: Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott.

```csharp
public static void Sign(string srcFileName, string dstFileName, CertificateHolder certHolder, 
    SignOptions signOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcFileName | String | Der Dateiname des zu signierenden Dokuments. |
| dstFileName | String | Der Dateiname der signierten Dokumentausgabe. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) Objekt mit Zertifikat, das zum Signieren der Datei verwendet wurde. Das Zertifikat im Inhaber MUSS private Schlüssel enthalten und das Flag X509KeyStorageFlags.Exportable gesetzt haben. |
| signOptions | SignOptions | [`SignOptions`](../../signoptions/) Objekt mit verschiedenen Signaturoptionen. |

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

* class [CertificateHolder](../../certificateholder/)
* class [SignOptions](../../signoptions/)
* class [DigitalSignatureUtil](../)
* namensraum [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* Montage [Aspose.Words](../../../)

---

## Sign(*Stream, Stream, [CertificateHolder](../../certificateholder/)*) {#sign}

Signiert das Quelldokument mit der angegebenen[`CertificateHolder`](../../certificateholder/) mit digitaler Signatur und schreibt das signierte Dokument in den Zielstream.

Unterstützte Formate sind: Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott.

**Die Ausgabe wird an den Anfang des Streams geschrieben und die Streamgröße wird mit der Inhaltslänge aktualisiert.**

```csharp
public static void Sign(Stream srcStream, Stream dstStream, CertificateHolder certHolder)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcStream | Stream | Der Stream, der das zu signierende Dokument enthält. |
| dstStream | Stream | Der Stream, in den das signierte Dokument geschrieben wird. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) Objekt mit Zertifikat, das zum Signieren der Datei verwendet wurde. Das Zertifikat im Inhaber MUSS private Schlüssel enthalten und das Flag X509KeyStorageFlags.Exportable gesetzt haben. |

## Beispiele

Zeigt, wie Dokumente mit X.509-Zertifikaten signiert werden.

```csharp
// Überprüfen Sie, ob ein Dokument signiert ist.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Erstellen Sie ein CertificateHolder-Objekt aus einer PKCS12-Datei, das wir zum Signieren des Dokuments verwenden.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Es gibt zwei Möglichkeiten, eine signierte Kopie eines Dokuments im lokalen Dateisystem zu speichern:
// 1 – Kennzeichnen Sie ein Dokument durch einen lokalen Systemdateinamen und speichern Sie eine signierte Kopie an einem durch einen anderen Dateinamen angegebenen Speicherort.
SignOptions signOptions = new SignOptions { SignTime = DateTime.Now };
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx",
    certificateHolder, signOptions);

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 – Nehmen Sie ein Dokument aus einem Stream und speichern Sie eine signierte Kopie in einem anderen Stream.
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// Bitte überprüfen Sie, ob alle digitalen Signaturen des Dokuments gültig sind und kontrollieren Sie deren Details.
Document signedDoc = new Document(ArtifactsDir + "Document.DigitalSignature.docx");
DigitalSignatureCollection digitalSignatureCollection = signedDoc.DigitalSignatures;

Assert.True(digitalSignatureCollection.IsValid);
Assert.AreEqual(1, digitalSignatureCollection.Count);
Assert.AreEqual(DigitalSignatureType.XmlDsig, digitalSignatureCollection[0].SignatureType);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].IssuerName);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].SubjectName);
```

### Siehe auch

* class [CertificateHolder](../../certificateholder/)
* class [DigitalSignatureUtil](../)
* namensraum [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* Montage [Aspose.Words](../../../)

---

## Sign(*string, string, [CertificateHolder](../../certificateholder/)*) {#sign_2}

Signiert das Quelldokument mit der angegebenen[`CertificateHolder`](../../certificateholder/) mit digitaler Signatur und schreibt das signierte Dokument in die Zieldatei.

Unterstützte Formate sind: Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott.

```csharp
public static void Sign(string srcFileName, string dstFileName, CertificateHolder certHolder)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcFileName | String | Der Dateiname des zu signierenden Dokuments. |
| dstFileName | String | Der Dateiname der signierten Dokumentausgabe. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) Objekt mit Zertifikat, das zum Signieren der Datei verwendet wurde. Das Zertifikat im Inhaber MUSS private Schlüssel enthalten und das Flag X509KeyStorageFlags.Exportable gesetzt haben. |

## Beispiele

Zeigt, wie Dokumente mit X.509-Zertifikaten signiert werden.

```csharp
// Überprüfen Sie, ob ein Dokument signiert ist.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Erstellen Sie ein CertificateHolder-Objekt aus einer PKCS12-Datei, das wir zum Signieren des Dokuments verwenden.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Es gibt zwei Möglichkeiten, eine signierte Kopie eines Dokuments im lokalen Dateisystem zu speichern:
// 1 – Kennzeichnen Sie ein Dokument durch einen lokalen Systemdateinamen und speichern Sie eine signierte Kopie an einem durch einen anderen Dateinamen angegebenen Speicherort.
SignOptions signOptions = new SignOptions { SignTime = DateTime.Now };
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx",
    certificateHolder, signOptions);

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 – Nehmen Sie ein Dokument aus einem Stream und speichern Sie eine signierte Kopie in einem anderen Stream.
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// Bitte überprüfen Sie, ob alle digitalen Signaturen des Dokuments gültig sind und kontrollieren Sie deren Details.
Document signedDoc = new Document(ArtifactsDir + "Document.DigitalSignature.docx");
DigitalSignatureCollection digitalSignatureCollection = signedDoc.DigitalSignatures;

Assert.True(digitalSignatureCollection.IsValid);
Assert.AreEqual(1, digitalSignatureCollection.Count);
Assert.AreEqual(DigitalSignatureType.XmlDsig, digitalSignatureCollection[0].SignatureType);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].IssuerName);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].SubjectName);
```

### Siehe auch

* class [CertificateHolder](../../certificateholder/)
* class [DigitalSignatureUtil](../)
* namensraum [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* Montage [Aspose.Words](../../../)
