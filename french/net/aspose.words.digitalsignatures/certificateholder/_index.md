---
title: Class CertificateHolder
second_title: Référence de l'API Aspose.Words pour .NET
description: Aspose.Words.DigitalSignatures.CertificateHolder classe. Représente un titulaire de X509Certificat2 instance.
type: docs
weight: 370
url: /fr/net/aspose.words.digitalsignatures/certificateholder/
---
## CertificateHolder class

Représente un titulaire de **X509Certificat2** instance.

Pour en savoir plus, visitez le[Travailler avec des signatures numériques](https://docs.aspose.com/words/net/working-with-digital-signatures/) article documentaire.

```csharp
public class CertificateHolder
```

## Propriétés

| Nom | La description |
| --- | --- |
| [Certificate](../../aspose.words.digitalsignatures/certificateholder/certificate/) { get; } | Renvoie l'instance de **X509Certificat2** qui contient les clés privées et publiques et la chaîne de certificats. |

## Méthodes

| Nom | La description |
| --- | --- |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create)(byte[], SecureString) | Crée`CertificateHolder` objet utilisant un tableau d'octets du magasin PKCS12 et son mot de passe. |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create_1)(byte[], string) | Crée`CertificateHolder` objet utilisant un tableau d'octets du magasin PKCS12 et son mot de passe. |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create_2)(string, string) | Crée`CertificateHolder` objet utilisant le chemin d'accès au magasin PKCS12 et son mot de passe. |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create/#create_3)(string, string, string) | Crée`CertificateHolder` objet utilisant le chemin d'accès au magasin PKCS12, son mot de passe et l'alias à l'aide duquel la clé privée et le certificat seront trouvés. |

### Remarques

`CertificateHolder` peut être créé uniquement par des méthodes de fabrique statiques. Il contient une instance de **X509Certificat2** qui est utilisé pour introduire des clés privées et publiques et des chaînes de certificats dans le système. Cette classe est appliquée dans[`DigitalSignatureUtil`](../digitalsignatureutil/) et[`PdfDigitalSignatureDetails`](../../aspose.words.saving/pdfdigitalsignaturedetails/) au lieu de méthodes obsolètes avec X509Certificate2 comme paramètres.

### Exemples

Montre comment signer un fichier de document crypté.

```csharp
// Créez un certificat X.509 à partir d'un magasin PKCS#12, qui doit contenir une clé privée.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Créez un commentaire, une date et un mot de passe de décryptage qui seront appliqués avec notre nouvelle signature numérique.
SignOptions signOptions = new SignOptions
{
    Comments = "Comment",
    SignTime = DateTime.Now,
    DecryptionPassword = "docPassword"
};

// Définit un nom de fichier système local pour le document d'entrée non signé et un nom de fichier de sortie pour sa nouvelle copie signée numériquement.
string inputFileName = MyDir + "Encrypted.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.DecryptionPassword.docx";

DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

Montre comment signer numériquement des documents.

```csharp
// Créez un certificat X.509 à partir d'un magasin PKCS#12, qui doit contenir une clé privée.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Créez un commentaire et une date qui seront appliqués avec notre nouvelle signature numérique.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Récupère un document non signé du système de fichiers local via un flux de fichiers,
// puis créez une copie signée de celui-ci déterminée par le nom de fichier du flux de fichier de sortie.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

Montre comment ajouter une ligne de signature à un document, puis le signer à l'aide d'un certificat numérique.

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
        /// Crée une copie d'un document source signé à l'aide des informations de signataire fournies et du certificat X509.
        /// </summary>
        private static void SignDocument(string srcDocumentPath, string dstDocumentPath,
            Signee signeeInfo, string certificatePath, string certificatePassword)
        {
            Document document = new Document(srcDocumentPath);
            DocumentBuilder builder = new DocumentBuilder(document);

            // Configurer et insérer une ligne de signature, un objet dans le document qui affichera une signature avec laquelle nous le signons.
            SignatureLineOptions signatureLineOptions = new SignatureLineOptions
            {
                Signer = signeeInfo.Name, 
                SignerTitle = signeeInfo.Position
            };

            SignatureLine signatureLine = builder.InsertSignatureLine(signatureLineOptions).SignatureLine;
            signatureLine.Id = signeeInfo.PersonId;

            // Tout d'abord, nous allons enregistrer une version non signée de notre document.
            builder.Document.Save(dstDocumentPath);

            CertificateHolder certificateHolder = CertificateHolder.Create(certificatePath, certificatePassword);

            SignOptions signOptions = new SignOptions
            {
                SignatureLineId = signeeInfo.PersonId,
                SignatureLineImage = signeeInfo.Image
            };

            // Remplacez le document non signé que nous avons enregistré ci-dessus par une version signée à l'aide du certificat.
            DigitalSignatureUtil.Sign(dstDocumentPath, dstDocumentPath, certificateHolder, signOptions);
        }

#if NET48 || JAVA
        /// <summary>
        /// Convertit une image en tableau d'octets.
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

### Voir également

* espace de noms [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* Assemblée [Aspose.Words](../../)


