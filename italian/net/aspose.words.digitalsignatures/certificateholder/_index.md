---
title: CertificateHolder
second_title: Aspose.Words per .NET API Reference
description: Rappresenta un titolare di Certificato X5092 esempio.
type: docs
weight: 360
url: /it/net/aspose.words.digitalsignatures/certificateholder/
---
## CertificateHolder class

Rappresenta un titolare di **Certificato X5092** esempio.

```csharp
public class CertificateHolder
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Certificate](../../aspose.words.digitalsignatures/certificateholder/certificate) { get; } | Restituisce l'istanza di **Certificato X5092** che contiene chiavi private, pubbliche e catena di certificati. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create#create)(byte[], SecureString) | Crea oggetto CertificateHolder utilizzando l'array di byte dell'archivio PKCS12 e la relativa password. |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create#create_1)(byte[], string) | Crea oggetto CertificateHolder utilizzando l'array di byte dell'archivio PKCS12 e la relativa password. |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create#create_2)(string, string) | Crea oggetto CertificateHolder utilizzando il percorso dell'archivio PKCS12 e la relativa password. |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create#create_3)(string, string, string) | Crea l'oggetto CertificateHolder utilizzando il percorso dell'archivio PKCS12, la relativa password e l'alias utilizzando quale chiave privata e certificato verranno trovati. |

### Osservazioni

**Titolare del certificato** può essere creato solo con metodi di fabbrica statici. Contiene un'istanza di **Certificato X5092** che viene utilizzato per introdurre chiavi private, pubbliche e catene di certificati nel sistema. Questa classe viene applicata in[`DigitalSignatureUtil`](../digitalsignatureutil) e[`PdfDigitalSignatureDetails`](../../aspose.words.saving/pdfdigitalsignaturedetails) invece di metodi obsoleti con X509Certificate2 come parametri.

### Esempi

Mostra come firmare un file di documento crittografato.

```csharp
// Crea un certificato X.509 da un archivio PKCS#12, che dovrebbe contenere una chiave privata.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Crea un commento, una data e una password di decrittazione che verranno applicati con la nostra nuova firma digitale.
SignOptions signOptions = new SignOptions
{
    Comments = "Comment",
    SignTime = DateTime.Now,
    DecryptionPassword = "docPassword"
};

// Imposta un nome file di sistema locale per il documento di input non firmato e un nome file di output per la sua nuova copia firmata digitalmente.
string inputFileName = MyDir + "Encrypted.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.DecryptionPassword.docx";

DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

Mostra come firmare digitalmente i documenti.

```csharp
// Crea un certificato X.509 da un archivio PKCS#12, che dovrebbe contenere una chiave privata.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Crea un commento e una data che verranno applicati con la nostra nuova firma digitale.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Prendi un documento non firmato dal file system locale tramite un flusso di file,
// quindi creane una copia firmata determinata dal nome del file del flusso di file di output.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

Mostra come aggiungere una riga di firma a un documento e quindi firmarlo utilizzando un certificato digitale.

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
        /// Crea una copia di un documento di origine firmato utilizzando le informazioni sul firmatario fornite e il certificato X509.
        /// </summary>
        private static void SignDocument(string srcDocumentPath, string dstDocumentPath,
            Signee signeeInfo, string certificatePath, string certificatePassword)
        {
            Document document = new Document(srcDocumentPath);
            DocumentBuilder builder = new DocumentBuilder(document);

            // Configura e inserisci una linea di firma, un oggetto nel documento che visualizzerà una firma con cui lo firmiamo.
            SignatureLineOptions signatureLineOptions = new SignatureLineOptions
            {
                Signer = signeeInfo.Name, 
                SignerTitle = signeeInfo.Position
            };

            SignatureLine signatureLine = builder.InsertSignatureLine(signatureLineOptions).SignatureLine;
            signatureLine.Id = signeeInfo.PersonId;

            // Innanzitutto, salveremo una versione non firmata del nostro documento.
            builder.Document.Save(dstDocumentPath);

            CertificateHolder certificateHolder = CertificateHolder.Create(certificatePath, certificatePassword);

            SignOptions signOptions = new SignOptions
            {
                SignatureLineId = signeeInfo.PersonId,
                SignatureLineImage = signeeInfo.Image
            };

            // Sovrascrivi il documento non firmato che abbiamo salvato in precedenza con una versione firmata utilizzando il certificato.
            DigitalSignatureUtil.Sign(dstDocumentPath, dstDocumentPath, certificateHolder, signOptions);
        }

#if NET48 || JAVA
        /// <summary>
        /// Converte un'immagine in un array di byte.
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

### Guarda anche

* spazio dei nomi [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
