---
title: CertificateHolder Class
linktitle: CertificateHolder
articleTitle: CertificateHolder
second_title: Aspose.Words för .NET
description: Aspose.Words.DigitalSignatures.CertificateHolder klass. Representerar en innehavare avX509Certifikat2 instans i C#.
type: docs
weight: 370
url: /sv/net/aspose.words.digitalsignatures/certificateholder/
---
## CertificateHolder class

Representerar en innehavare av**X509Certifikat2** instans.

För att lära dig mer, besök[Arbeta med digitala signaturer](https://docs.aspose.com/words/net/working-with-digital-signatures/) dokumentationsartikel.

```csharp
public class CertificateHolder
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Certificate](../../aspose.words.digitalsignatures/certificateholder/certificate/) { get; } | Returnerar instansen av**X509Certifikat2** som har privata, offentliga nycklar och certifikatkedja. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create)(*byte[], SecureString*) | Skapar`CertificateHolder` objekt som använder byte-arrayen i PKCS12-arkivet och dess lösenord. |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create_1)(*byte[], string*) | Skapar`CertificateHolder` objekt som använder byte-arrayen i PKCS12-arkivet och dess lösenord. |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create_2)(*string, string*) | Skapar`CertificateHolder` objekt som använder sökvägen till PKCS12-butiken och dess lösenord. |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create_3)(*string, string, string*) | Skapar`CertificateHolder` objekt som använder sökvägen till PKCS12-arkivet, dess lösenord och alias genom att använda vilken privat nyckel och certifikat som kommer att hittas. |

## Anmärkningar

`CertificateHolder` kan endast skapas med statiska fabriksmetoder. Den innehåller en instans av**X509Certifikat2** som används för att introducera privata, offentliga nycklar och certifikatkedjor i systemet. Denna klass tillämpas i[`DigitalSignatureUtil`](../digitalsignatureutil/) och[`PdfDigitalSignatureDetails`](../../aspose.words.saving/pdfdigitalsignaturedetails/) istället för föråldrade metoder med X509Certificate2 som parametrar.

## Exempel

Visar hur man signerar krypterad dokumentfil.

```csharp
// Skapa ett X.509-certifikat från en PKCS#12-butik, som bör innehålla en privat nyckel.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Skapa en kommentar, datum och dekrypteringslösenord som kommer att tillämpas med vår nya digitala signatur.
SignOptions signOptions = new SignOptions
{
    Comments = "Comment",
    SignTime = DateTime.Now,
    DecryptionPassword = "docPassword"
};

// Ställ in ett lokalt systemfilnamn för det osignerade indatadokumentet och ett utdatafilnamn för dess nya digitalt signerade kopia.
string inputFileName = MyDir + "Encrypted.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.DecryptionPassword.docx";

DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

Visar hur man digitalt signerar dokument.

```csharp
// Skapa ett X.509-certifikat från en PKCS#12-butik, som bör innehålla en privat nyckel.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Skapa en kommentar och ett datum som kommer att tillämpas med vår nya digitala signatur.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Ta ett osignerat dokument från det lokala filsystemet via en filström,
// skapa sedan en signerad kopia av den som bestäms av filnamnet på utdatafilströmmen.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

Visar hur man lägger till en signaturrad i ett dokument och sedan signerar den med ett digitalt certifikat.

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
        /// Skapar en kopia av ett källdokument som är signerat med den angivna signatärinformationen och X509-certifikatet.
        /// </summary>
        private static void SignDocument(string srcDocumentPath, string dstDocumentPath,
            Signee signeeInfo, string certificatePath, string certificatePassword)
        {
            Document document = new Document(srcDocumentPath);
            DocumentBuilder builder = new DocumentBuilder(document);

            // Konfigurera och infoga en signaturrad, ett objekt i dokumentet som kommer att visa en signatur som vi signerar det med.
            SignatureLineOptions signatureLineOptions = new SignatureLineOptions
            {
                Signer = signeeInfo.Name, 
                SignerTitle = signeeInfo.Position
            };

            SignatureLine signatureLine = builder.InsertSignatureLine(signatureLineOptions).SignatureLine;
            signatureLine.Id = signeeInfo.PersonId;

            // Först kommer vi att spara en osignerad version av vårt dokument.
            builder.Document.Save(dstDocumentPath);

            CertificateHolder certificateHolder = CertificateHolder.Create(certificatePath, certificatePassword);

            SignOptions signOptions = new SignOptions
            {
                SignatureLineId = signeeInfo.PersonId,
                SignatureLineImage = signeeInfo.Image
            };

            // Skriv över det osignerade dokumentet vi sparade ovan med en version signerad med certifikatet.
            DigitalSignatureUtil.Sign(dstDocumentPath, dstDocumentPath, certificateHolder, signOptions);
        }

#if NET48 || JAVA
        /// <summary>
        /// Konverterar en bild till en byte-array.
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

### Se även

* namnutrymme [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* hopsättning [Aspose.Words](../../)
