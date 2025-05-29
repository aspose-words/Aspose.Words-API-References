---
title: DigitalSignatureUtil.Sign
linktitle: Sign
articleTitle: Sign
second_title: Aspose.Words per .NET
description: Firma i tuoi documenti senza sforzo con il metodo Sign di DigitalSignatureUtil. Applica firme digitali in modo sicuro utilizzando CertificateHolder e SignOptions.
type: docs
weight: 30
url: /it/net/aspose.words.digitalsignatures/digitalsignatureutil/sign/
---
## Sign(*Stream, Stream, [CertificateHolder](../../certificateholder/), [SignOptions](../../signoptions/)*) {#sign_1}

Firma il documento sorgente utilizzando i dati forniti[`CertificateHolder`](../../certificateholder/) E[`SignOptions`](../../signoptions/) con firma digitale e scrive il documento firmato nel flusso di destinazione.

I formati supportati sono: Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott.

**L'output verrà scritto all'inizio del flusso e la dimensione del flusso verrà aggiornata in base alla lunghezza del contenuto.**

```csharp
public static void Sign(Stream srcStream, Stream dstStream, CertificateHolder certHolder, 
    SignOptions signOptions)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| srcStream | Stream | Il flusso che contiene il documento da firmare. |
| dstStream | Stream | Il flusso in cui verrà scritto il documento firmato. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) oggetto con certificato utilizzato per firmare il file. Il certificato nel titolare DEVE contenere chiavi private e avere impostato il flag X509KeyStorageFlags.Exportable. |
| signOptions | SignOptions | [`SignOptions`](../../signoptions/) oggetto con varie opzioni di firma. |

## Esempi

Mostra come firmare digitalmente i documenti.

```csharp
// Creare un certificato X.509 da un archivio PKCS#12, che dovrebbe contenere una chiave privata.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Crea un commento e una data che verranno applicati con la nostra nuova firma digitale.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Prendi un documento non firmato dal file system locale tramite un flusso di file,
// quindi crea una copia firmata determinata dal nome file del flusso di file di output.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

### Guarda anche

* class [CertificateHolder](../../certificateholder/)
* class [SignOptions](../../signoptions/)
* class [DigitalSignatureUtil](../)
* spazio dei nomi [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* assemblea [Aspose.Words](../../../)

---

## Sign(*string, string, [CertificateHolder](../../certificateholder/), [SignOptions](../../signoptions/)*) {#sign_3}

Firma il documento sorgente utilizzando i dati forniti[`CertificateHolder`](../../certificateholder/) E[`SignOptions`](../../signoptions/) con firma digitale e scrive il documento firmato nel file di destinazione.

I formati supportati sono: Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott.

```csharp
public static void Sign(string srcFileName, string dstFileName, CertificateHolder certHolder, 
    SignOptions signOptions)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| srcFileName | String | Nome del file del documento da firmare. |
| dstFileName | String | Nome del file di output del documento firmato. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) oggetto con certificato utilizzato per firmare il file. Il certificato nel titolare DEVE contenere chiavi private e avere impostato il flag X509KeyStorageFlags.Exportable. |
| signOptions | SignOptions | [`SignOptions`](../../signoptions/) oggetto con varie opzioni di firma. |

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

* class [CertificateHolder](../../certificateholder/)
* class [SignOptions](../../signoptions/)
* class [DigitalSignatureUtil](../)
* spazio dei nomi [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* assemblea [Aspose.Words](../../../)

---

## Sign(*Stream, Stream, [CertificateHolder](../../certificateholder/)*) {#sign}

Firma il documento sorgente utilizzando i dati forniti[`CertificateHolder`](../../certificateholder/) con firma digitale e scrive il documento firmato nel flusso di destinazione.

I formati supportati sono: Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott.

**L'output verrà scritto all'inizio del flusso e la dimensione del flusso verrà aggiornata in base alla lunghezza del contenuto.**

```csharp
public static void Sign(Stream srcStream, Stream dstStream, CertificateHolder certHolder)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| srcStream | Stream | Il flusso che contiene il documento da firmare. |
| dstStream | Stream | Il flusso in cui verrà scritto il documento firmato. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) oggetto con certificato utilizzato per firmare il file. Il certificato nel titolare DEVE contenere chiavi private e avere impostato il flag X509KeyStorageFlags.Exportable. |

## Esempi

Mostra come firmare documenti con certificati X.509.

```csharp
// Verifica che un documento non sia firmato.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Crea un oggetto CertificateHolder da un file PKCS12, che utilizzeremo per firmare il documento.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Esistono due modi per salvare una copia firmata di un documento nel file system locale:
// 1 - Designa un documento tramite un nome file di sistema locale e salva una copia firmata in una posizione specificata da un altro nome file.
SignOptions signOptions = new SignOptions { SignTime = DateTime.Now };
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx",
    certificateHolder, signOptions);

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - Prendi un documento da un flusso e salva una copia firmata in un altro flusso.
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// Si prega di verificare che tutte le firme digitali del documento siano valide e di controllarne i dettagli.
Document signedDoc = new Document(ArtifactsDir + "Document.DigitalSignature.docx");
DigitalSignatureCollection digitalSignatureCollection = signedDoc.DigitalSignatures;

Assert.True(digitalSignatureCollection.IsValid);
Assert.AreEqual(1, digitalSignatureCollection.Count);
Assert.AreEqual(DigitalSignatureType.XmlDsig, digitalSignatureCollection[0].SignatureType);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].IssuerName);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].SubjectName);
```

### Guarda anche

* class [CertificateHolder](../../certificateholder/)
* class [DigitalSignatureUtil](../)
* spazio dei nomi [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* assemblea [Aspose.Words](../../../)

---

## Sign(*string, string, [CertificateHolder](../../certificateholder/)*) {#sign_2}

Firma il documento sorgente utilizzando i dati forniti[`CertificateHolder`](../../certificateholder/) con firma digitale e scrive il documento firmato nel file di destinazione.

I formati supportati sono: Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott.

```csharp
public static void Sign(string srcFileName, string dstFileName, CertificateHolder certHolder)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| srcFileName | String | Nome del file del documento da firmare. |
| dstFileName | String | Nome del file di output del documento firmato. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) oggetto con certificato utilizzato per firmare il file. Il certificato nel titolare DEVE contenere chiavi private e avere impostato il flag X509KeyStorageFlags.Exportable. |

## Esempi

Mostra come firmare documenti con certificati X.509.

```csharp
// Verifica che un documento non sia firmato.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Crea un oggetto CertificateHolder da un file PKCS12, che utilizzeremo per firmare il documento.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Esistono due modi per salvare una copia firmata di un documento nel file system locale:
// 1 - Designa un documento tramite un nome file di sistema locale e salva una copia firmata in una posizione specificata da un altro nome file.
SignOptions signOptions = new SignOptions { SignTime = DateTime.Now };
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx",
    certificateHolder, signOptions);

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - Prendi un documento da un flusso e salva una copia firmata in un altro flusso.
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// Si prega di verificare che tutte le firme digitali del documento siano valide e di controllarne i dettagli.
Document signedDoc = new Document(ArtifactsDir + "Document.DigitalSignature.docx");
DigitalSignatureCollection digitalSignatureCollection = signedDoc.DigitalSignatures;

Assert.True(digitalSignatureCollection.IsValid);
Assert.AreEqual(1, digitalSignatureCollection.Count);
Assert.AreEqual(DigitalSignatureType.XmlDsig, digitalSignatureCollection[0].SignatureType);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].IssuerName);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].SubjectName);
```

### Guarda anche

* class [CertificateHolder](../../certificateholder/)
* class [DigitalSignatureUtil](../)
* spazio dei nomi [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* assemblea [Aspose.Words](../../../)
