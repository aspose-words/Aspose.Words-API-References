---
title: DigitalSignature.IssuerName
second_title: Referencia de API de Aspose.Words para .NET
description: DigitalSignature propiedad. Devuelve el nombre distinguido del sujeto del emisor del certificado.
type: docs
weight: 30
url: /es/net/aspose.words.digitalsignatures/digitalsignature/issuername/
---
## DigitalSignature.IssuerName property

Devuelve el nombre distinguido del sujeto del emisor del certificado.

```csharp
public string IssuerName { get; }
```

### Ejemplos

Muestra cómo firmar documentos con certificados X.509.

```csharp
// Verifica que un documento no esté firmado.
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// Crear un objeto CertificateHolder a partir de un archivo PKCS12, que usaremos para firmar el documento.
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// Hay dos formas de guardar una copia firmada de un documento en el sistema de archivos local:
// 1 - Designar un documento por un nombre de archivo del sistema local y guardar una copia firmada en una ubicación especificada por otro nombre de archivo.
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx", 
    certificateHolder, new SignOptions() { SignTime = DateTime.Now } );

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - Tome un documento de un flujo y guarde una copia firmada en otro flujo.
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

* class [DigitalSignature](../)
* espacio de nombres [Aspose.Words.DigitalSignatures](../../digitalsignature/)
* asamblea [Aspose.Words](../../../)


