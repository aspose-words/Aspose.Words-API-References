---
title: DigitalSignatureCollection.IsValid
second_title: Referencia de API de Aspose.Words para .NET
description: DigitalSignatureCollection propiedad. Devolucionesverdadero si todas las firmas digitales de esta colección son válidas y el documento no ha sido manipulado También devuelveverdaderosi no hay firmas digitales. Devuelvefalso si al menos una firma digital no es válida.
type: docs
weight: 30
url: /es/net/aspose.words.digitalsignatures/digitalsignaturecollection/isvalid/
---
## DigitalSignatureCollection.IsValid property

Devoluciones`verdadero` si todas las firmas digitales de esta colección son válidas y el documento no ha sido manipulado También devuelve`verdadero`si no hay firmas digitales. Devuelve`falso` si al menos una firma digital no es válida.

```csharp
public bool IsValid { get; }
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

* class [DigitalSignatureCollection](../)
* espacio de nombres [Aspose.Words.DigitalSignatures](../../digitalsignaturecollection/)
* asamblea [Aspose.Words](../../../)


