---
title: Class CertificateHolder
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.DigitalSignatures.CertificateHolder klas. Stellt einen Inhaber dar X509Zertifikat2 Instanz.
type: docs
weight: 370
url: /de/net/aspose.words.digitalsignatures/certificateholder/
---
## CertificateHolder class

Stellt einen Inhaber dar **X509Zertifikat2** Instanz.

Um mehr zu erfahren, besuchen Sie die[Arbeiten Sie mit digitalen Signaturen](https://docs.aspose.com/words/net/working-with-digital-signatures/) Dokumentationsartikel.

```csharp
public class CertificateHolder
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Certificate](../../aspose.words.digitalsignatures/certificateholder/certificate/) { get; } | Gibt die Instanz von zurück **X509Zertifikat2** das private, öffentliche Schlüssel und die Zertifikatskette enthält. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create)(byte[], SecureString) | Erstellt`CertificateHolder` Objekt unter Verwendung des Byte-Arrays des PKCS12-Speichers und seines Passworts. |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create_1)(byte[], string) | Erstellt`CertificateHolder` Objekt unter Verwendung des Byte-Arrays des PKCS12-Speichers und seines Passworts. |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create_2)(string, string) | Erstellt`CertificateHolder` Objekt unter Verwendung des Pfads zum PKCS12-Speicher und seines Passworts. |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create_3)(string, string, string) | Erstellt`CertificateHolder` Objekt unter Verwendung des Pfads zum PKCS12-Speicher, seines Passworts und des Alias, mit dem der private Schlüssel und das Zertifikat gefunden werden. |

### Bemerkungen

`CertificateHolder` kann nur mit statischen Factory-Methoden erstellt werden. Es enthält eine Instanz von **X509Zertifikat2** die verwendet wird, um private, öffentliche Schlüssel und Zertifikatsketten in das System einzuführen. Diese Klasse wird in angewendet[`DigitalSignatureUtil`](../digitalsignatureutil/) Und[`PdfDigitalSignatureDetails`](../../aspose.words.saving/pdfdigitalsignaturedetails/) statt veralteter Methoden mit X509Certificate2 als Parameter.

### Beispiele

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

// Legen Sie einen lokalen Systemdateinamen für das unsignierte Eingabedokument und einen Ausgabedateinamen für seine neue digital signierte Kopie fest.
string inputFileName = MyDir + "Encrypted.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.DecryptionPassword.docx";

DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

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

* namensraum [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* Montage [Aspose.Words](../../)


