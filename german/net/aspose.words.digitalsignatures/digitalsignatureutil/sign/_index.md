---
title: DigitalSignatureUtil.Sign
second_title: Aspose.Words für .NET-API-Referenz
description: DigitalSignatureUtil methode. Signiert das Quelldokument mit der angegebenenCertificateHolder UndSignOptions mit digitaler Signatur und schreibt signiertes Dokument in den Zielstream.
type: docs
weight: 30
url: /de/net/aspose.words.digitalsignatures/digitalsignatureutil/sign/
---
## Sign(Stream, Stream, CertificateHolder, SignOptions) {#sign_1}

Signiert das Quelldokument mit der angegebenen[`CertificateHolder`](../../certificateholder/) Und[`SignOptions`](../../signoptions/) mit digitaler Signatur und schreibt signiertes Dokument in den Zielstream.

Das Dokument sollte entweder seinDoc oderDocx.

**Die Ausgabe wird an den Anfang des Streams geschrieben und die Streamgröße wird mit der Inhaltslänge aktualisiert.**

```csharp
public static void Sign(Stream srcStream, Stream dstStream, CertificateHolder certHolder, 
    SignOptions signOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcStream | Stream | Der Stream, der das zu signierende Dokument enthält. |
| dstStream | Stream | Der Stream, in den das signierte Dokument geschrieben wird. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) Objekt mit Zertifikat, das zum Signieren von file. verwendet wurde. Das Zertifikat im Inhaber MUSS private Schlüssel enthalten und das Flag X509KeyStorageFlags.Exportable gesetzt haben. |
| signOptions | SignOptions | [`SignOptions`](../../signoptions/) Objekt mit verschiedenen Signiermöglichkeiten. |

### Beispiele

Zeigt, wie man Dokumente digital signiert.

```csharp
// Erstellen Sie ein X.509-Zertifikat aus einem PKCS#12-Speicher, das einen privaten Schlüssel enthalten sollte.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Erstellen Sie einen Kommentar und ein Datum, das mit unserer neuen digitalen Signatur angewendet wird.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Über einen Dateistream ein unsigniertes Dokument aus dem lokalen Dateisystem übernehmen,
// dann eine signierte Kopie davon erstellen, die durch den Dateinamen des Ausgabedateistreams bestimmt wird.
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
* namensraum [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* Montage [Aspose.Words](../../../)

---

## Sign(string, string, CertificateHolder, SignOptions) {#sign_3}

Signiert das Quelldokument mit der angegebenen[`CertificateHolder`](../../certificateholder/) Und[`SignOptions`](../../signoptions/) mit digitaler Signatur und schreibt signiertes Dokument in die Zieldatei.

Das Dokument sollte entweder seinDoc oderDocx.

```csharp
public static void Sign(string srcFileName, string dstFileName, CertificateHolder certHolder, 
    SignOptions signOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcFileName | String | Der Dateiname des zu signierenden Dokuments. |
| dstFileName | String | Der Dateiname der signierten Dokumentausgabe. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) Objekt mit Zertifikat, das zum Signieren von file. verwendet wurde. Das Zertifikat im Inhaber MUSS private Schlüssel enthalten und das Flag X509KeyStorageFlags.Exportable gesetzt haben. |
| signOptions | SignOptions | [`SignOptions`](../../signoptions/) Objekt mit verschiedenen Signiermöglichkeiten. |

### Beispiele

Zeigt, wie man einem Dokument eine Signaturzeile hinzufügt und es dann mit einem digitalen Zertifikat signiert.

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

            // Konfigurieren und fügen Sie eine Signaturzeile ein, ein Objekt im Dokument, das eine Signatur anzeigt, mit der wir es signieren.
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

            // Überschreiben Sie das oben gespeicherte unsignierte Dokument mit einer mit dem Zertifikat signierten Version.
            DigitalSignatureUtil.Sign(dstDocumentPath, dstDocumentPath, certificateHolder, signOptions);
        }

#if NET48 || JAVA
        /// <summary>
        /// Konvertiert ein Bild in ein Byte-Array.
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

### Siehe auch

* class [CertificateHolder](../../certificateholder/)
* class [SignOptions](../../signoptions/)
* class [DigitalSignatureUtil](../)
* namensraum [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* Montage [Aspose.Words](../../../)

---

## Sign(Stream, Stream, CertificateHolder) {#sign}

Signiert das Quelldokument mit der angegebenen[`CertificateHolder`](../../certificateholder/)mit digitaler Signatur und schreibt signiertes Dokument in den Zielstream.

Das Dokument sollte entweder seinDoc oderDocx.

**Die Ausgabe wird an den Anfang des Streams geschrieben und die Streamgröße wird mit der Inhaltslänge aktualisiert.**

```csharp
public static void Sign(Stream srcStream, Stream dstStream, CertificateHolder certHolder)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcStream | Stream | Der Stream, der das zu signierende Dokument enthält. |
| dstStream | Stream | Der Stream, in den das signierte Dokument geschrieben wird. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) Objekt mit Zertifikat, das zum Signieren von file. verwendet wurde. Das Zertifikat im Inhaber MUSS private Schlüssel enthalten und das Flag X509KeyStorageFlags.Exportable gesetzt haben. |

### Beispiele

Zeigt, wie Dokumente mit X.509-Zertifikaten signiert werden.

```csharp
// Stellen Sie sicher, dass ein Dokument nicht signiert ist.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Erstellen Sie ein CertificateHolder-Objekt aus einer PKCS12-Datei, das wir zum Signieren des Dokuments verwenden.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Es gibt zwei Möglichkeiten, eine signierte Kopie eines Dokuments im lokalen Dateisystem zu speichern:
// 1 – Bestimmen Sie ein Dokument durch einen lokalen Systemdateinamen und speichern Sie eine signierte Kopie an einem durch einen anderen Dateinamen angegebenen Speicherort.
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx", 
    certificateHolder, new SignOptions() { SignTime = DateTime.Now } );

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

// Bitte überprüfen Sie, ob alle digitalen Signaturen des Dokuments gültig sind, und überprüfen Sie deren Details.
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
* namensraum [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* Montage [Aspose.Words](../../../)

---

## Sign(string, string, CertificateHolder) {#sign_2}

Signiert das Quelldokument mit der angegebenen[`CertificateHolder`](../../certificateholder/) mit digitaler Signatur und schreibt signiertes Dokument in die Zieldatei.

Das Dokument sollte entweder seinDoc oderDocx.

```csharp
public static void Sign(string srcFileName, string dstFileName, CertificateHolder certHolder)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcFileName | String | Der Dateiname des zu signierenden Dokuments. |
| dstFileName | String | Der Dateiname der signierten Dokumentausgabe. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) Objekt mit Zertifikat, das zum Signieren von file. verwendet wurde. Das Zertifikat im Inhaber MUSS private Schlüssel enthalten und das Flag X509KeyStorageFlags.Exportable gesetzt haben. |

### Beispiele

Zeigt, wie Dokumente mit X.509-Zertifikaten signiert werden.

```csharp
// Stellen Sie sicher, dass ein Dokument nicht signiert ist.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Erstellen Sie ein CertificateHolder-Objekt aus einer PKCS12-Datei, das wir zum Signieren des Dokuments verwenden.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Es gibt zwei Möglichkeiten, eine signierte Kopie eines Dokuments im lokalen Dateisystem zu speichern:
// 1 – Bestimmen Sie ein Dokument durch einen lokalen Systemdateinamen und speichern Sie eine signierte Kopie an einem durch einen anderen Dateinamen angegebenen Speicherort.
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx", 
    certificateHolder, new SignOptions() { SignTime = DateTime.Now } );

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

// Bitte überprüfen Sie, ob alle digitalen Signaturen des Dokuments gültig sind, und überprüfen Sie deren Details.
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
* namensraum [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* Montage [Aspose.Words](../../../)


