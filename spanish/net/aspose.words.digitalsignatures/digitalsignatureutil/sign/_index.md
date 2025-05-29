---
title: DigitalSignatureUtil.Sign
linktitle: Sign
articleTitle: Sign
second_title: Aspose.Words para .NET
description: Firme sus documentos fácilmente con el método Sign de DigitalSignatureUtil. Aplique firmas digitales de forma segura con CertificateHolder y SignOptions.
type: docs
weight: 30
url: /es/net/aspose.words.digitalsignatures/digitalsignatureutil/sign/
---
## Sign(*Stream, Stream, [CertificateHolder](../../certificateholder/), [SignOptions](../../signoptions/)*) {#sign_1}

Firma el documento fuente usando lo indicado[`CertificateHolder`](../../certificateholder/) y[`SignOptions`](../../signoptions/) con firma digital y escribe documento firmado en el flujo de destino.

Los formatos admitidos son: Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott.

**La salida se escribirá al inicio de la transmisión y el tamaño de la transmisión se actualizará con la longitud del contenido.**

```csharp
public static void Sign(Stream srcStream, Stream dstStream, CertificateHolder certHolder, 
    SignOptions signOptions)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| srcStream | Stream | El flujo que contiene el documento a firmar. |
| dstStream | Stream | El flujo en el que se escribirá el documento firmado. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) objeto con certificado utilizado para firmar el archivo. El certificado en el titular DEBE contener claves privadas y tener el indicador X509KeyStorageFlags.Exportable configurado. |
| signOptions | SignOptions | [`SignOptions`](../../signoptions/) objeto con varias opciones de firma. |

## Ejemplos

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

// Tome un documento sin firmar del sistema de archivos local a través de un flujo de archivos,
// luego crea una copia firmada determinada por el nombre del archivo de flujo de salida.
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
* espacio de nombres [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* asamblea [Aspose.Words](../../../)

---

## Sign(*string, string, [CertificateHolder](../../certificateholder/), [SignOptions](../../signoptions/)*) {#sign_3}

Firma el documento fuente usando lo indicado[`CertificateHolder`](../../certificateholder/) y[`SignOptions`](../../signoptions/) con firma digital y escribe documento firmado en archivo de destino.

Los formatos admitidos son: Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott.

```csharp
public static void Sign(string srcFileName, string dstFileName, CertificateHolder certHolder, 
    SignOptions signOptions)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| srcFileName | String | El nombre del archivo del documento a firmar. |
| dstFileName | String | El nombre del archivo de salida del documento firmado. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) objeto con certificado utilizado para firmar el archivo. El certificado en el titular DEBE contener claves privadas y tener el indicador X509KeyStorageFlags.Exportable configurado. |
| signOptions | SignOptions | [`SignOptions`](../../signoptions/) objeto con varias opciones de firma. |

## Ejemplos

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

    // Sobrescriba el documento sin firmar que guardamos arriba con una versión firmada usando el certificado.
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

### Ver también

* class [CertificateHolder](../../certificateholder/)
* class [SignOptions](../../signoptions/)
* class [DigitalSignatureUtil](../)
* espacio de nombres [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* asamblea [Aspose.Words](../../../)

---

## Sign(*Stream, Stream, [CertificateHolder](../../certificateholder/)*) {#sign}

Firma el documento fuente usando lo indicado[`CertificateHolder`](../../certificateholder/) con firma digital y escribe el documento firmado en el flujo de destino.

Los formatos admitidos son: Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott.

**La salida se escribirá al inicio de la transmisión y el tamaño de la transmisión se actualizará con la longitud del contenido.**

```csharp
public static void Sign(Stream srcStream, Stream dstStream, CertificateHolder certHolder)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| srcStream | Stream | El flujo que contiene el documento a firmar. |
| dstStream | Stream | El flujo en el que se escribirá el documento firmado. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) objeto con certificado utilizado para firmar el archivo. El certificado en el titular DEBE contener claves privadas y tener el indicador X509KeyStorageFlags.Exportable configurado. |

## Ejemplos

Muestra cómo firmar documentos con certificados X.509.

```csharp
// Verificar que un documento no esté firmado.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Crea un objeto CertificateHolder a partir de un archivo PKCS12, que usaremos para firmar el documento.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Hay dos formas de guardar una copia firmada de un documento en el sistema de archivos local:
// 1 - Designa un documento con un nombre de archivo del sistema local y guarda una copia firmada en una ubicación especificada por otro nombre de archivo.
SignOptions signOptions = new SignOptions { SignTime = DateTime.Now };
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx",
    certificateHolder, signOptions);

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - Toma un documento de una secuencia y guarda una copia firmada en otra secuencia.
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

//Por favor verifique que todas las firmas digitales del documento sean válidas y verifique sus detalles.
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
* espacio de nombres [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* asamblea [Aspose.Words](../../../)

---

## Sign(*string, string, [CertificateHolder](../../certificateholder/)*) {#sign_2}

Firma el documento fuente usando lo indicado[`CertificateHolder`](../../certificateholder/) con firma digital y escribe el documento firmado en el archivo de destino.

Los formatos admitidos son: Doc , Dot , Docx , Dotx , Docm , Dotm , Odt , Ott.

```csharp
public static void Sign(string srcFileName, string dstFileName, CertificateHolder certHolder)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| srcFileName | String | El nombre del archivo del documento a firmar. |
| dstFileName | String | El nombre del archivo de salida del documento firmado. |
| certHolder | CertificateHolder | [`CertificateHolder`](../../certificateholder/) objeto con certificado utilizado para firmar el archivo. El certificado en el titular DEBE contener claves privadas y tener el indicador X509KeyStorageFlags.Exportable configurado. |

## Ejemplos

Muestra cómo firmar documentos con certificados X.509.

```csharp
// Verificar que un documento no esté firmado.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Crea un objeto CertificateHolder a partir de un archivo PKCS12, que usaremos para firmar el documento.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Hay dos formas de guardar una copia firmada de un documento en el sistema de archivos local:
// 1 - Designa un documento con un nombre de archivo del sistema local y guarda una copia firmada en una ubicación especificada por otro nombre de archivo.
SignOptions signOptions = new SignOptions { SignTime = DateTime.Now };
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx",
    certificateHolder, signOptions);

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - Toma un documento de una secuencia y guarda una copia firmada en otra secuencia.
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

//Por favor verifique que todas las firmas digitales del documento sean válidas y verifique sus detalles.
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
* espacio de nombres [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* asamblea [Aspose.Words](../../../)
