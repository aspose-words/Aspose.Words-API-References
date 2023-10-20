---
title: FileFormatInfo Class
linktitle: FileFormatInfo
articleTitle: FileFormatInfo
second_title: Aspose.Words para .NET
description: Aspose.Words.FileFormatInfo clase. Contiene datos devueltos porFileFormatUtil métodos de detección de formato de documento en C#.
type: docs
weight: 2810
url: /es/net/aspose.words/fileformatinfo/
---
## FileFormatInfo class

Contiene datos devueltos por[`FileFormatUtil`](../fileformatutil/) métodos de detección de formato de documento.

Para obtener más información, visite el[Detectar formato de archivo y comprobar la compatibilidad del formato](https://docs.aspose.com/words/net/detect-file-format-and-check-format-compatibility/) artículo de documentación.

```csharp
public class FileFormatInfo
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Encoding](../../aspose.words/fileformatinfo/encoding/) { get; } | Obtiene la codificación detectada si corresponde al formato del documento actual. Por el momento detecta la codificación solo para documentos HTML. |
| [HasDigitalSignature](../../aspose.words/fileformatinfo/hasdigitalsignature/) { get; } | Devoluciones`verdadero`si este documento contiene firma digital. Esta propiedad simplemente informa que hay una firma digital presente en un documento, pero no especifica si la firma es válida o no. |
| [IsEncrypted](../../aspose.words/fileformatinfo/isencrypted/) { get; } | Devoluciones`verdadero` si el documento está cifrado y requiere una contraseña para abrirse. |
| [LoadFormat](../../aspose.words/fileformatinfo/loadformat/) { get; } | Obtiene el formato del documento detectado. |

## Observaciones

No crea instancias de esta clase directamente. Los objetos de esta clase son devueltos por [`DetectFileFormat`](../fileformatutil/detectfileformat/) métodos.

## Ejemplos

Muestra cómo utilizar la clase FileFormatUtil para detectar el formato y el cifrado del documento.

```csharp
Document doc = new Document();

// Configurar un objeto SaveOptions para cifrar el documento
// con una contraseña cuando lo guardamos, y luego guardamos el documento.
OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.Odt);
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "File.DetectDocumentEncryption.odt", saveOptions);

// Verificar el tipo de archivo de nuestro documento, y su estado de cifrado.
FileFormatInfo info = FileFormatUtil.DetectFileFormat(ArtifactsDir + "File.DetectDocumentEncryption.odt");

Assert.AreEqual(".odt", FileFormatUtil.LoadFormatToExtension(info.LoadFormat));
Assert.True(info.IsEncrypted);
```

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

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
