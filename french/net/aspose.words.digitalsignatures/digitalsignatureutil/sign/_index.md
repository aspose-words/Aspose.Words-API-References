---
title: DigitalSignatureUtil.Sign
second_title: Référence de l'API Aspose.Words pour .NET
description: DigitalSignatureUtil méthode. Signe le document source en utilisantCertificateHolder etSignOptions avec signature numérique et écrit le document signé dans le flux de destination.
type: docs
weight: 30
url: /fr/net/aspose.words.digitalsignatures/digitalsignatureutil/sign/
---
## Sign(Stream, Stream, CertificateHolder, SignOptions) {#sign_1}

Signe le document source en utilisant[`CertificateHolder`](../../certificateholder/) et[`SignOptions`](../../signoptions/) avec signature numérique et écrit le document signé dans le flux de destination.

Le document doit être soitDoc ouDocx.

**La sortie sera écrite au début du flux et la taille du flux sera mise à jour avec la longueur du contenu.**

```csharp
public static void Sign(Stream srcStream, Stream dstStream, CertificateHolder certHolder, 
    SignOptions signOptions)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| srcStream | Stream | Le flux qui contient le document à signer. |
| dstStream | Stream | Le flux dans lequel le document signé sera écrit. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) objet avec certificat utilisé pour signer le fichier. Le certificat du détenteur DOIT contenir des clés privées et avoir l'indicateur X509KeyStorageFlags.Exportable défini. |
| signOptions | SignOptions | [`SignOptions`](../../signoptions/) objet avec diverses options de signature. |

### Exemples

Montre comment signer numériquement des documents.

```csharp
// Crée un certificat X.509 à partir d'un magasin PKCS#12, qui doit contenir une clé privée.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Créez un commentaire et une date qui seront appliqués avec notre nouvelle signature numérique.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Prend un document non signé du système de fichiers local via un flux de fichiers,
// puis créez une copie signée de celui-ci déterminée par le nom de fichier du flux de fichier de sortie.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

### Voir également

* class [CertificateHolder](../../certificateholder/)
* class [SignOptions](../../signoptions/)
* class [DigitalSignatureUtil](../)
* espace de noms [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* Assemblée [Aspose.Words](../../../)

---

## Sign(string, string, CertificateHolder, SignOptions) {#sign_3}

Signe le document source en utilisant[`CertificateHolder`](../../certificateholder/) et[`SignOptions`](../../signoptions/) avec signature numérique et écrit le document signé dans le fichier de destination.

Le document doit être soitDoc ouDocx.

```csharp
public static void Sign(string srcFileName, string dstFileName, CertificateHolder certHolder, 
    SignOptions signOptions)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| srcFileName | String | Le nom de fichier du document à signer. |
| dstFileName | String | Le nom de fichier de la sortie du document signé. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) objet avec certificat utilisé pour signer le fichier. Le certificat du détenteur DOIT contenir des clés privées et avoir l'indicateur X509KeyStorageFlags.Exportable défini. |
| signOptions | SignOptions | [`SignOptions`](../../signoptions/) objet avec diverses options de signature. |

### Exemples

Montre comment ajouter une ligne de signature à un document, puis le signer à l'aide d'un certificat numérique.

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
        /// Crée une copie d'un document source signé à l'aide des informations de signataire fournies et du certificat X509.
        /// </summary>
        private static void SignDocument(string srcDocumentPath, string dstDocumentPath,
            Signee signeeInfo, string certificatePath, string certificatePassword)
        {
            Document document = new Document(srcDocumentPath);
            DocumentBuilder builder = new DocumentBuilder(document);

            // Configurez et insérez une ligne de signature, un objet dans le document qui affichera une signature avec laquelle nous le signerons.
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
        /// Convertit une image en un tableau d'octets.
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

* class [CertificateHolder](../../certificateholder/)
* class [SignOptions](../../signoptions/)
* class [DigitalSignatureUtil](../)
* espace de noms [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* Assemblée [Aspose.Words](../../../)

---

## Sign(Stream, Stream, CertificateHolder) {#sign}

Signe le document source en utilisant[`CertificateHolder`](../../certificateholder/)avec la signature numérique et écrit le document signé dans le flux de destination.

Le document doit être soitDoc ouDocx.

**La sortie sera écrite au début du flux et la taille du flux sera mise à jour avec la longueur du contenu.**

```csharp
public static void Sign(Stream srcStream, Stream dstStream, CertificateHolder certHolder)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| srcStream | Stream | Le flux qui contient le document à signer. |
| dstStream | Stream | Le flux dans lequel le document signé sera écrit. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) objet avec certificat utilisé pour signer le fichier. Le certificat du détenteur DOIT contenir des clés privées et avoir l'indicateur X509KeyStorageFlags.Exportable défini. |

### Exemples

Montre comment signer des documents avec des certificats X.509.

```csharp
// Vérifie qu'un document n'est pas signé.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Crée un objet CertificateHolder à partir d'un fichier PKCS12, que nous utiliserons pour signer le document.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Il existe deux manières d'enregistrer une copie signée d'un document dans le système de fichiers local :
// 1 - Désignez un document par un nom de fichier système local et enregistrez une copie signée à un emplacement spécifié par un autre nom de fichier.
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx", 
    certificateHolder, new SignOptions() { SignTime = DateTime.Now } );

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - Extraire un document d'un flux et enregistrer une copie signée dans un autre flux.
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// Veuillez vérifier que toutes les signatures numériques du document sont valides et vérifiez leurs détails.
Document signedDoc = new Document(ArtifactsDir + "Document.DigitalSignature.docx");
DigitalSignatureCollection digitalSignatureCollection = signedDoc.DigitalSignatures;

Assert.True(digitalSignatureCollection.IsValid);
Assert.AreEqual(1, digitalSignatureCollection.Count);
Assert.AreEqual(DigitalSignatureType.XmlDsig, digitalSignatureCollection[0].SignatureType);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].IssuerName);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].SubjectName);
```

### Voir également

* class [CertificateHolder](../../certificateholder/)
* class [DigitalSignatureUtil](../)
* espace de noms [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* Assemblée [Aspose.Words](../../../)

---

## Sign(string, string, CertificateHolder) {#sign_2}

Signe le document source en utilisant[`CertificateHolder`](../../certificateholder/) avec signature numérique et écrit le document signé dans le fichier de destination.

Le document doit être soitDoc ouDocx.

```csharp
public static void Sign(string srcFileName, string dstFileName, CertificateHolder certHolder)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| srcFileName | String | Le nom de fichier du document à signer. |
| dstFileName | String | Le nom de fichier de la sortie du document signé. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) objet avec certificat utilisé pour signer le fichier. Le certificat du détenteur DOIT contenir des clés privées et avoir l'indicateur X509KeyStorageFlags.Exportable défini. |

### Exemples

Montre comment signer des documents avec des certificats X.509.

```csharp
// Vérifie qu'un document n'est pas signé.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Crée un objet CertificateHolder à partir d'un fichier PKCS12, que nous utiliserons pour signer le document.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Il existe deux manières d'enregistrer une copie signée d'un document dans le système de fichiers local :
// 1 - Désignez un document par un nom de fichier système local et enregistrez une copie signée à un emplacement spécifié par un autre nom de fichier.
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx", 
    certificateHolder, new SignOptions() { SignTime = DateTime.Now } );

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - Extraire un document d'un flux et enregistrer une copie signée dans un autre flux.
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// Veuillez vérifier que toutes les signatures numériques du document sont valides et vérifiez leurs détails.
Document signedDoc = new Document(ArtifactsDir + "Document.DigitalSignature.docx");
DigitalSignatureCollection digitalSignatureCollection = signedDoc.DigitalSignatures;

Assert.True(digitalSignatureCollection.IsValid);
Assert.AreEqual(1, digitalSignatureCollection.Count);
Assert.AreEqual(DigitalSignatureType.XmlDsig, digitalSignatureCollection[0].SignatureType);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].IssuerName);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].SubjectName);
```

### Voir également

* class [CertificateHolder](../../certificateholder/)
* class [DigitalSignatureUtil](../)
* espace de noms [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* Assemblée [Aspose.Words](../../../)


