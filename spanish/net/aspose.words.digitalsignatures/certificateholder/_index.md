---
title: CertificateHolder
second_title: Referencia de API de Aspose.Words para .NET
description: Representa a un titular de X509Certificado2 instancia.
type: docs
weight: 360
url: /es/net/aspose.words.digitalsignatures/certificateholder/
---
## CertificateHolder class

Representa a un titular de **X509Certificado2** instancia.

```csharp
public class CertificateHolder
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Certificate](../../aspose.words.digitalsignatures/certificateholder/certificate) { get; } | Devuelve la instancia de **X509Certificado2** que contiene claves públicas y privadas y cadena de certificados. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create#create)(byte[], SecureString) | Crea el objeto CertificateHolder utilizando la matriz de bytes del almacén PKCS12 y su contraseña. |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create#create_1)(byte[], string) | Crea el objeto CertificateHolder utilizando la matriz de bytes del almacén PKCS12 y su contraseña. |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create#create_2)(string, string) | Crea el objeto CertificateHolder usando la ruta al almacén PKCS12 y su contraseña. |
| static [Create](../../aspose.words.digitalsignatures/certificateholder/create#create_3)(string, string, string) | Crea el objeto CertificateHolder usando la ruta al almacén PKCS12, su contraseña y el alias mediante el cual se encontrará la clave privada y el certificado. |

### Observaciones

**Titular del certificado** solo se puede crear mediante métodos de fábrica estáticos. Contiene una instancia de **X509Certificado2** que se utiliza para introducir claves privadas y públicas y cadenas de certificados en el sistema. Esta clase se aplica en[`DigitalSignatureUtil`](../digitalsignatureutil) y[`PdfDigitalSignatureDetails`](../../aspose.words.saving/pdfdigitalsignaturedetails) en lugar de métodos obsoletos con X509Certificate2 como parámetros.

### Ejemplos

Muestra cómo firmar un archivo de documento cifrado.

```csharp
// Cree un certificado X.509 desde un almacén PKCS#12, que debe contener una clave privada.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Cree un comentario, fecha y contraseña de descifrado que se aplicará con nuestra nueva firma digital.
SignOptions signOptions = new SignOptions
{
    Comments = "Comment",
    SignTime = DateTime.Now,
    DecryptionPassword = "docPassword"
};

// Establecer un nombre de archivo del sistema local para el documento de entrada sin firmar y un nombre de archivo de salida para su nueva copia firmada digitalmente.
string inputFileName = MyDir + "Encrypted.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.DecryptionPassword.docx";

DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

Muestra cómo firmar documentos digitalmente.

```csharp
// Cree un certificado X.509 desde un almacén PKCS#12, que debe contener una clave privada.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Cree un comentario y una fecha que se aplicará con nuestra nueva firma digital.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Tome un documento sin firmar del sistema de archivos local a través de un flujo de archivos,
// luego cree una copia firmada determinada por el nombre de archivo de la secuencia del archivo de salida.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

Muestra cómo agregar una línea de firma a un documento y luego firmarlo con un certificado digital.

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
        /// Crea una copia de un documento de origen firmado con la información del firmante proporcionada y el certificado X509.
        /// </summary>
        private static void SignDocument(string srcDocumentPath, string dstDocumentPath,
            Signee signeeInfo, string certificatePath, string certificatePassword)
        {
            Document document = new Document(srcDocumentPath);
            DocumentBuilder builder = new DocumentBuilder(document);

            // Configurar e insertar una línea de firma, un objeto en el documento que mostrará una firma con la que lo firmamos.
            SignatureLineOptions signatureLineOptions = new SignatureLineOptions
            {
                Signer = signeeInfo.Name, 
                SignerTitle = signeeInfo.Position
            };

            SignatureLine signatureLine = builder.InsertSignatureLine(signatureLineOptions).SignatureLine;
            signatureLine.Id = signeeInfo.PersonId;

            // Primero, guardaremos una versión sin firmar de nuestro documento.
            builder.Document.Save(dstDocumentPath);

            CertificateHolder certificateHolder = CertificateHolder.Create(certificatePath, certificatePassword);

            SignOptions signOptions = new SignOptions
            {
                SignatureLineId = signeeInfo.PersonId,
                SignatureLineImage = signeeInfo.Image
            };

            // Sobrescribir el documento sin firmar que guardamos anteriormente con una versión firmada con el certificado.
            DigitalSignatureUtil.Sign(dstDocumentPath, dstDocumentPath, certificateHolder, signOptions);
        }

#if NET48 || JAVA
        /// <summary>
        /// Convierte una imagen en una matriz de bytes.
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

### Ver también

* espacio de nombres [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
