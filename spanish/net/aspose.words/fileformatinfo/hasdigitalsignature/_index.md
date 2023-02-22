---
title: FileFormatInfo.HasDigitalSignature
second_title: Referencia de API de Aspose.Words para .NET
description: FileFormatInfo propiedad. Devuelve verdadero si este documento contiene una firma digital. Esta propiedad simplemente informa que una firma digital está presente en un documento pero no especifica si la firma es válida o no.
type: docs
weight: 20
url: /es/net/aspose.words/fileformatinfo/hasdigitalsignature/
---
## FileFormatInfo.HasDigitalSignature property

Devuelve verdadero si este documento contiene una firma digital. Esta propiedad simplemente informa que una firma digital está presente en un documento, pero no especifica si la firma es válida o no.

```csharp
public bool HasDigitalSignature { get; }
```

### Observaciones

Esta propiedad existe para ayudarlo a clasificar los documentos que están firmados digitalmente de los que no lo están. Si usa Aspose.Words para modificar y guardar un documento que está firmado digitalmente, entonces la firma digital se perderá. Esto es por diseño porque existe una firma digital para proteger la autenticidad de un documento. Al usar esta propiedad, puede detectar documentos firmados digitalmente antes de procesarlos de la misma manera que los documentos normales y tomar alguna acción para evitar perder la firma digital, por ejemplo, notificar al usuario.

### Ejemplos

Muestra cómo usar la clase FileFormatUtil para detectar el formato del documento y la presencia de firmas digitales.

```csharp
// Use una instancia de FileFormatInfo para verificar que un documento no esté firmado digitalmente.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.docx");

Assert.AreEqual(".docx", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.False(info.HasDigitalSignature);

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "File.DetectDigitalSignatures.docx",
    certificateHolder, new SignOptions() { SignTime = DateTime.Now });

// Use un nuevo FileFormatInstance para confirmar que está firmado.
info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDigitalSignatures.docx");

Assert.True(info.HasDigitalSignature);

// Podemos cargar y acceder a las firmas de un documento firmado en una colección como esta.
Assert.AreEqual(1, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "File.DetectDigitalSignatures.docx").Count);
```

### Ver también

* class [FileFormatInfo](../)
* espacio de nombres [Aspose.Words](../../fileformatinfo/)
* asamblea [Aspose.Words](../../../)


