---
title: FileFormatUtil.DetectFileFormat
linktitle: DetectFileFormat
articleTitle: DetectFileFormat
second_title: Aspose.Words para .NET
description: Identifique rápidamente los formatos de documentos con el método DetectFileFormat de FileFormatUtil. Obtenga información precisa sobre el formato para una gestión eficiente de archivos.
type: docs
weight: 30
url: /es/net/aspose.words/fileformatutil/detectfileformat/
---
## DetectFileFormat(*string*) {#detectfileformat_1}

Detecta y devuelve la información sobre el formato de un documento almacenado en un archivo de disco.

```csharp
public static FileFormatInfo DetectFileFormat(string fileName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| fileName | String | El nombre del archivo. |

### Valor_devuelto

A[`FileFormatInfo`](../../fileformatinfo/) objeto que contiene la información detectada.

## Observaciones

Aunque este método detecte el formato del documento, no garantiza su validez. Este método solo detecta el formato leyendo datos suficientes para la detección. Para verificar completamente la validez de un documento, debe cargarlo en un...[`Document`](../../document/) objeto.

Este método lanza[`FileCorruptedException`](../../filecorruptedexception/) cuando se reconoce el formato , pero la detección no puede completarse debido a la corrupción.

## Ejemplos

Muestra cómo utilizar la clase FileFormatUtil para detectar el formato y el cifrado del documento.

```csharp
Document doc = new Document();

// Configurar un objeto SaveOptions para cifrar el documento
// con una contraseña cuando lo guardamos y luego guardamos el documento.
OdtSaveOptions saveOptions = new OdtSaveOptions(SaveFormat.Odt);
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "File.DetectDocumentEncryption.odt", saveOptions);

//Verificar el tipo de archivo de nuestro documento, y su estado de cifrado.
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

* class [FileFormatInfo](../../fileformatinfo/)
* class [FileFormatUtil](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)

---

## DetectFileFormat(*Stream*) {#detectfileformat}

Detecta y devuelve la información sobre el formato de un documento almacenado en una secuencia.

```csharp
public static FileFormatInfo DetectFileFormat(Stream stream)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| stream | Stream | El arroyo. |

### Valor_devuelto

A[`FileFormatInfo`](../../fileformatinfo/) objeto que contiene la información detectada.

## Observaciones

El stream debe estar posicionado al inicio del documento.

Cuando este método regresa, la posición en el flujo se restaura a la posición original.

Aunque este método detecte el formato del documento, no garantiza su validez. Este método solo detecta el formato leyendo datos suficientes para la detección. Para verificar completamente la validez de un documento, debe cargarlo en un...[`Document`](../../document/) objeto.

Este método lanza[`FileCorruptedException`](../../filecorruptedexception/) cuando se reconoce el formato , pero la detección no puede completarse debido a la corrupción.

## Ejemplos

Muestra cómo utilizar los métodos FileFormatUtil para detectar el formato de un documento.

```csharp
// Cargue un documento desde un archivo al que le falta una extensión de archivo y luego detecte su formato de archivo.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // A continuación se muestran dos métodos para convertir un LoadFormat a su SaveFormat correspondiente.
    // 1 - Obtenga la cadena de extensión de archivo para LoadFormat, luego obtenga el SaveFormat correspondiente de esa cadena:
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - Convierte el LoadFormat directamente a su SaveFormat:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // Cargue un documento desde la secuencia y luego guárdelo en la extensión de archivo detectada automáticamente.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### Ver también

* class [FileFormatInfo](../../fileformatinfo/)
* class [FileFormatUtil](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
