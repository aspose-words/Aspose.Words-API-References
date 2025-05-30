---
title: FileFormatInfo.HasDigitalSignature
linktitle: HasDigitalSignature
articleTitle: HasDigitalSignature
second_title: Aspose.Words para .NET
description: Descubra la propiedad FileFormatInfo HasDigitalSignature verifique rápidamente si su documento incluye una firma digital, mejorando la seguridad y la autenticidad.
type: docs
weight: 20
url: /es/net/aspose.words/fileformatinfo/hasdigitalsignature/
---
## FileFormatInfo.HasDigitalSignature property

Devuelve`verdadero`Si este documento contiene una firma digital. Esta propiedad simplemente informa que hay una firma digital en un documento, pero no especifica si la firma es válida o no.

```csharp
public bool HasDigitalSignature { get; }
```

## Observaciones

Esta propiedad le ayuda a distinguir los documentos firmados digitalmente de los que no. Si usa Aspose.Words para modificar y guardar un documento firmado digitalmente, esta se perderá. Esto es intencional, ya que la firma digital existe para proteger la autenticidad de un documento. Con esta propiedad, puede detectar documentos firmados digitalmente antes de procesarlos, de la misma manera que los documentos normales, y tomar medidas para evitar perder la firma digital, por ejemplo, notificar al usuario.

## Ejemplos

Muestra cómo utilizar la clase FileFormatUtil para detectar el formato del documento y la presencia de firmas digitales.

```csharp
// Utilice una instancia de FileFormatInfo para verificar que un documento no esté firmado digitalmente.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.docx");

Assert.AreEqual(".docx", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.False(info.HasDigitalSignature);

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
SignOptions signOptions = new SignOptions() { SignTime = DateTime.Now };
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "File.DetectDigitalSignatures.docx",
    certificateHolder, signOptions);

// Utilice un nuevo FileFormatInstance para confirmar que está firmado.
info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDigitalSignatures.docx");

Assert.True(info.HasDigitalSignature);

//Podemos cargar y acceder a las firmas de un documento firmado en una colección como esta.
Assert.AreEqual(1, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "File.DetectDigitalSignatures.docx").Count);
```

### Ver también

* class [FileFormatInfo](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
