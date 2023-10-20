---
title: FileFormatInfo.HasDigitalSignature
linktitle: HasDigitalSignature
articleTitle: HasDigitalSignature
second_title: Aspose.Words para .NET
description: FileFormatInfo HasDigitalSignature propiedad. Devolucionesverdaderosi este documento contiene firma digital. Esta propiedad simplemente informa que hay una firma digital presente en un documento pero no especifica si la firma es válida o no en C#.
type: docs
weight: 20
url: /es/net/aspose.words/fileformatinfo/hasdigitalsignature/
---
## FileFormatInfo.HasDigitalSignature property

Devoluciones`verdadero`si este documento contiene firma digital. Esta propiedad simplemente informa que hay una firma digital presente en un documento, pero no especifica si la firma es válida o no.

```csharp
public bool HasDigitalSignature { get; }
```

## Observaciones

Esta propiedad existe para ayudarle a clasificar los documentos que están firmados digitalmente de los que no. Si utiliza Aspose.Words para modificar y guardar un documento que está firmado digitalmente, entonces la firma digital se perderá. Esto se debe a su diseño porque existe una firma digital para proteger la autenticidad de un documento. Con esta propiedad puede detectar documentos firmados digitalmente antes de procesarlos de la misma manera que los documentos normales y tomar alguna medida para evitar la pérdida de la firma digital, por ejemplo, notificar al usuario.

## Ejemplos

Muestra cómo utilizar la clase FileFormatUtil para detectar el formato del documento y la presencia de firmas digitales.

```csharp
// Utilice una instancia de FileFormatInfo para verificar que un documento no esté firmado digitalmente.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.docx");

Assert.AreEqual(".docx", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.False(info.HasDigitalSignature);

CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "File.DetectDigitalSignatures.docx",
    certificateHolder, new SignOptions() { SignTime = DateTime.Now });

// Utilice un nuevo FileFormatInstance para confirmar que está firmado.
info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDigitalSignatures.docx");

Assert.True(info.HasDigitalSignature);

// Podemos cargar y acceder a las firmas de un documento firmado en una colección como esta.
Assert.AreEqual(1, DigitalSignatureUtil.LoadSignatures(ArtifactsDir + "File.DetectDigitalSignatures.docx").Count);
```

### Ver también

* class [FileFormatInfo](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
