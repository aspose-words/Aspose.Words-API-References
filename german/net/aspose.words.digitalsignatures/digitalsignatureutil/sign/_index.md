---
title: DigitalSignatureUtil.Sign
second_title: Aspose.Words für .NET-API-Referenz
description: DigitalSignatureUtil methode. Signiert Quelldokument mit gegebenCertificateHolder undSignOptions mit digitaler Signatur und schreibt signiertes Dokument in Zielstream.
type: docs
weight: 30
url: /de/net/aspose.words.digitalsignatures/digitalsignatureutil/sign/
---
## Sign(Stream, Stream, CertificateHolder, SignOptions) {#sign_1}

Signiert Quelldokument mit gegeben[`CertificateHolder`](../../certificateholder/) und[`SignOptions`](../../signoptions/) mit digitaler Signatur und schreibt signiertes Dokument in Zielstream.

Dokument sollte entweder seinDoc oderDocx.

**Die Ausgabe wird an den Anfang des Streams geschrieben und die Streamgröße wird mit der Inhaltslänge aktualisiert.**

```csharp
public static void Sign(Stream srcStream, Stream dstStream, CertificateHolder certHolder, 
    SignOptions signOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcStream | Stream | Der Stream, der das zu signierende Dokument enthält. |
| dstStream | Stream | Der Stream, in den das signierte Dokument geschrieben wird. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) Objekt mit Zertifikat, das zum Signieren von file. verwendet wurde. Das Zertifikat im Halter MUSS private Schlüssel enthalten und das X509KeyStorageFlags.Exportable-Flag gesetzt haben. |
| signOptions | SignOptions | [`SignOptions`](../../signoptions/) Objekt mit verschiedenen Signiermöglichkeiten. |

### Beispiele

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

// Nimm ein unsigniertes Dokument aus dem lokalen Dateisystem über einen Dateistream,
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
* namensraum [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* Montage [Aspose.Words](../../../)

---

## Sign(string, string, CertificateHolder, SignOptions) {#sign_3}

Signiert Quelldokument mit gegeben[`CertificateHolder`](../../certificateholder/) und[`SignOptions`](../../signoptions/) mit digitaler Signatur und schreibt signiertes Dokument in Zieldatei.

Dokument sollte entweder seinDoc oderDocx.

```csharp
public static void Sign(string srcFileName, string dstFileName, CertificateHolder certHolder, 
    SignOptions signOptions)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcFileName | String | Der Dateiname des zu signierenden Dokuments. |
| dstFileName | String | Der Dateiname der signierten Dokumentausgabe. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) Objekt mit Zertifikat, das zum Signieren von file. verwendet wurde. Das Zertifikat im Halter MUSS private Schlüssel enthalten und das X509KeyStorageFlags.Exportable-Flag gesetzt haben. |
| signOptions | SignOptions | [`SignOptions`](../../signoptions/) Objekt mit verschiedenen Signiermöglichkeiten. |

### Beispiele

Zeigt, wie Sie einem Dokument eine Signaturzeile hinzufügen und es dann mit einem digitalen Zertifikat signieren.

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
        /// Erstellt eine Kopie eines Quelldokuments, das mit den bereitgestellten Informationen zum Unterzeichner und dem X509-Zertifikat signiert wurde.
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

            // Überschreiben Sie das unsignierte Dokument, das wir oben gespeichert haben, mit einer Version, die mit dem Zertifikat signiert wurde.
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

Signiert Quelldokument mit gegeben[`CertificateHolder`](../../certificateholder/)mit digitaler Signatur und schreibt signiertes Dokument in Zielstream.

Dokument sollte entweder seinDoc oderDocx.

**Die Ausgabe wird an den Anfang des Streams geschrieben und die Streamgröße wird mit der Inhaltslänge aktualisiert.**

```csharp
public static void Sign(Stream srcStream, Stream dstStream, CertificateHolder certHolder)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcStream | Stream | Der Stream, der das zu signierende Dokument enthält. |
| dstStream | Stream | Der Stream, in den das signierte Dokument geschrieben wird. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) Objekt mit Zertifikat, das zum Signieren von file. verwendet wurde. Das Zertifikat im Halter MUSS private Schlüssel enthalten und das X509KeyStorageFlags.Exportable-Flag gesetzt haben. |

### Beispiele

Zeigt, wie Dokumente mit X.509-Zertifikaten signiert werden.

```csharp
// Sicherstellen, dass ein Dokument nicht signiert ist.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Erstellen Sie ein CertificateHolder-Objekt aus einer PKCS12-Datei, mit der wir das Dokument signieren.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Es gibt zwei Möglichkeiten, eine signierte Kopie eines Dokuments im lokalen Dateisystem zu speichern:
// 1 - Kennzeichnen eines Dokuments durch einen lokalen Systemdateinamen und Speichern einer signierten Kopie an einem Ort, der durch einen anderen Dateinamen angegeben ist.
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx", 
    certificateHolder, new SignOptions() { SignTime = DateTime.Now } );

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - Nehmen Sie ein Dokument aus einem Stream und speichern Sie eine signierte Kopie in einem anderen Stream.
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

Signiert Quelldokument mit gegeben[`CertificateHolder`](../../certificateholder/) mit digitaler Signatur und schreibt signiertes Dokument in Zieldatei.

Dokument sollte entweder seinDoc oderDocx.

```csharp
public static void Sign(string srcFileName, string dstFileName, CertificateHolder certHolder)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| srcFileName | String | Der Dateiname des zu signierenden Dokuments. |
| dstFileName | String | Der Dateiname der signierten Dokumentausgabe. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) Objekt mit Zertifikat, das zum Signieren von file. verwendet wurde. Das Zertifikat im Halter MUSS private Schlüssel enthalten und das X509KeyStorageFlags.Exportable-Flag gesetzt haben. |

### Beispiele

Zeigt, wie Dokumente mit X.509-Zertifikaten signiert werden.

```csharp
// Sicherstellen, dass ein Dokument nicht signiert ist.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Erstellen Sie ein CertificateHolder-Objekt aus einer PKCS12-Datei, mit der wir das Dokument signieren.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Es gibt zwei Möglichkeiten, eine signierte Kopie eines Dokuments im lokalen Dateisystem zu speichern:
// 1 - Kennzeichnen eines Dokuments durch einen lokalen Systemdateinamen und Speichern einer signierten Kopie an einem Ort, der durch einen anderen Dateinamen angegeben ist.
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx", 
    certificateHolder, new SignOptions() { SignTime = DateTime.Now } );

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - Nehmen Sie ein Dokument aus einem Stream und speichern Sie eine signierte Kopie in einem anderen Stream.
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


