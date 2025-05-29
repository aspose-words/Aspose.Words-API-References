---
title: DigitalSignature.CertificateHolder
linktitle: CertificateHolder
articleTitle: CertificateHolder
second_title: Aspose.Words para .NET
description: Descubra la propiedad DigitalSignature CertificateHolder, que recupera el objeto del titular del certificado para mejorar la seguridad y verificación de la firma de documentos.
type: docs
weight: 10
url: /es/net/aspose.words.digitalsignatures/digitalsignature/certificateholder/
---
## DigitalSignature.CertificateHolder property

Devuelve el objeto titular del certificado que contiene el certificado que se utilizó para firmar el documento.

```csharp
public CertificateHolder CertificateHolder { get; }
```

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
* class [DigitalSignature](../)
* espacio de nombres [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* asamblea [Aspose.Words](../../../)
