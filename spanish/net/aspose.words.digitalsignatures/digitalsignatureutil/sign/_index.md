---
title: DigitalSignatureUtil.Sign
second_title: Referencia de API de Aspose.Words para .NET
description: DigitalSignatureUtil método. Firma el documento fuente utilizando lo indicadoCertificateHolder ySignOptions con firma digital y escribe el documento firmado en el flujo de destino.
type: docs
weight: 30
url: /es/net/aspose.words.digitalsignatures/digitalsignatureutil/sign/
---
## Sign(Stream, Stream, CertificateHolder, SignOptions) {#sign_1}

Firma el documento fuente utilizando lo indicado[`CertificateHolder`](../../certificateholder/) y[`SignOptions`](../../signoptions/) con firma digital y escribe el documento firmado en el flujo de destino.

El documento debe serDoc oDocx.

**La salida se escribirá al inicio de la transmisión y el tamaño de la transmisión se actualizará con la longitud del contenido.**

```csharp
public static void Sign(Stream srcStream, Stream dstStream, CertificateHolder certHolder, 
    SignOptions signOptions)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| srcStream | Stream | La secuencia que contiene el documento a firmar. |
| dstStream | Stream | La secuencia en la que se escribirá el documento firmado. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) objeto con certificado que se utilizó para firmar el archivo. El certificado en el titular DEBE contener claves privadas y tener establecido el indicador X509KeyStorageFlags.Exportable. |
| signOptions | SignOptions | [`SignOptions`](../../signoptions/) objeto con varias opciones de firma. |

### Ejemplos

Muestra cómo firmar documentos digitalmente.

```csharp
// Cree un certificado X.509 desde un almacén PKCS#12, que debe contener una clave privada.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// Crea un comentario y una fecha que se aplicará con nuestra nueva firma digital.
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// Tomar un documento sin firmar del sistema de archivos local a través de una secuencia de archivos,
// luego crea una copia firmada determinada por el nombre de archivo de la secuencia del archivo de salida.
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

### Ver también

* class [CertificateHolder](../../certificateholder/)
* class [SignOptions](../../signoptions/)
* class [DigitalSignatureUtil](../)
* espacio de nombres [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* asamblea [Aspose.Words](../../../)

---

## Sign(string, string, CertificateHolder, SignOptions) {#sign_3}

Firma el documento fuente utilizando lo indicado[`CertificateHolder`](../../certificateholder/) y[`SignOptions`](../../signoptions/) con firma digital y escribe el documento firmado en el archivo de destino.

El documento debe serDoc oDocx.

```csharp
public static void Sign(string srcFileName, string dstFileName, CertificateHolder certHolder, 
    SignOptions signOptions)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| srcFileName | String | El nombre del archivo del documento a firmar. |
| dstFileName | String | El nombre del archivo del documento firmado. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) objeto con certificado que se utilizó para firmar el archivo. El certificado en el titular DEBE contener claves privadas y tener establecido el indicador X509KeyStorageFlags.Exportable. |
| signOptions | SignOptions | [`SignOptions`](../../signoptions/) objeto con varias opciones de firma. |

### Ejemplos

Muestra cómo agregar una línea de firma a un documento y luego firmarlo usando un certificado digital.

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
        /// Crea una copia de un documento fuente firmado utilizando la información del firmante proporcionada y el certificado X509.
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

            // Sobrescribe el documento sin firmar que guardamos arriba con una versión firmada con el certificado.
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

* class [CertificateHolder](../../certificateholder/)
* class [SignOptions](../../signoptions/)
* class [DigitalSignatureUtil](../)
* espacio de nombres [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* asamblea [Aspose.Words](../../../)

---

## Sign(Stream, Stream, CertificateHolder) {#sign}

Firma el documento fuente utilizando lo indicado[`CertificateHolder`](../../certificateholder/)con firma digital y escribe el documento firmado en el flujo de destino.

El documento debe serDoc oDocx.

**La salida se escribirá al inicio de la transmisión y el tamaño de la transmisión se actualizará con la longitud del contenido.**

```csharp
public static void Sign(Stream srcStream, Stream dstStream, CertificateHolder certHolder)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| srcStream | Stream | La secuencia que contiene el documento a firmar. |
| dstStream | Stream | La secuencia en la que se escribirá el documento firmado. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) objeto con certificado que se utilizó para firmar el archivo. El certificado en el titular DEBE contener claves privadas y tener establecido el indicador X509KeyStorageFlags.Exportable. |

### Ejemplos

Muestra cómo firmar documentos con certificados X.509.

```csharp
// Verificar que un documento no esté firmado.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Crea un objeto CertificateHolder a partir de un archivo PKCS12, que usaremos para firmar el documento.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Hay dos formas de guardar una copia firmada de un documento en el sistema de archivos local:
// 1: designe un documento con un nombre de archivo del sistema local y guarde una copia firmada en una ubicación especificada con otro nombre de archivo.
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx", 
    certificateHolder, new SignOptions() { SignTime = DateTime.Now } );

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2: tomar un documento de una secuencia y guardar una copia firmada en otra secuencia.
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// Verifique que todas las firmas digitales del documento sean válidas y verifique sus detalles.
Document signedDoc = new Document(ArtifactsDir + "Document.DigitalSignature.docx");
DigitalSignatureCollection digitalSignatureCollection = signedDoc.DigitalSignatures;

Assert.True(digitalSignatureCollection.IsValid);
Assert.AreEqual(1, digitalSignatureCollection.Count);
Assert.AreEqual(DigitalSignatureType.XmlDsig, digitalSignatureCollection[0].SignatureType);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].IssuerName);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].SubjectName);
```

### Ver también

* class [CertificateHolder](../../certificateholder/)
* class [DigitalSignatureUtil](../)
* espacio de nombres [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* asamblea [Aspose.Words](../../../)

---

## Sign(string, string, CertificateHolder) {#sign_2}

Firma el documento fuente utilizando lo indicado[`CertificateHolder`](../../certificateholder/) con firma digital y escribe el documento firmado en el archivo de destino.

El documento debe serDoc oDocx.

```csharp
public static void Sign(string srcFileName, string dstFileName, CertificateHolder certHolder)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| srcFileName | String | El nombre del archivo del documento a firmar. |
| dstFileName | String | El nombre del archivo del documento firmado. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) objeto con certificado que se utilizó para firmar el archivo. El certificado en el titular DEBE contener claves privadas y tener establecido el indicador X509KeyStorageFlags.Exportable. |

### Ejemplos

Muestra cómo firmar documentos con certificados X.509.

```csharp
// Verificar que un documento no esté firmado.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Crea un objeto CertificateHolder a partir de un archivo PKCS12, que usaremos para firmar el documento.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Hay dos formas de guardar una copia firmada de un documento en el sistema de archivos local:
// 1: designe un documento con un nombre de archivo del sistema local y guarde una copia firmada en una ubicación especificada con otro nombre de archivo.
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx", 
    certificateHolder, new SignOptions() { SignTime = DateTime.Now } );

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2: tomar un documento de una secuencia y guardar una copia firmada en otra secuencia.
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// Verifique que todas las firmas digitales del documento sean válidas y verifique sus detalles.
Document signedDoc = new Document(ArtifactsDir + "Document.DigitalSignature.docx");
DigitalSignatureCollection digitalSignatureCollection = signedDoc.DigitalSignatures;

Assert.True(digitalSignatureCollection.IsValid);
Assert.AreEqual(1, digitalSignatureCollection.Count);
Assert.AreEqual(DigitalSignatureType.XmlDsig, digitalSignatureCollection[0].SignatureType);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].IssuerName);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].SubjectName);
```

### Ver también

* class [CertificateHolder](../../certificateholder/)
* class [DigitalSignatureUtil](../)
* espacio de nombres [Aspose.Words.DigitalSignatures](../../digitalsignatureutil/)
* asamblea [Aspose.Words](../../../)


