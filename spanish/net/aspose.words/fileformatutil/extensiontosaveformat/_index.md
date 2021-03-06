---
title: ExtensionToSaveFormat
second_title: Referencia de API de Aspose.Words para .NET
description: Convierte una extensión de nombre de archivo en unaSaveFormataspose.words/saveformat valor.
type: docs
weight: 40
url: /es/net/aspose.words/fileformatutil/extensiontosaveformat/
---
## FileFormatUtil.ExtensionToSaveFormat method

Convierte una extensión de nombre de archivo en una[`SaveFormat`](../../saveformat) valor.

```csharp
public static SaveFormat ExtensionToSaveFormat(string extension)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| extension | String | La extensión del archivo. Puede ser con o sin punto inicial. No distingue entre mayúsculas y minúsculas. |

### Excepciones

| excepción | condición |
| --- | --- |
| ArgumentNullException | Se lanza si el parámetro es nulo. |

### Observaciones

Si la extensión no puede ser reconocida, regresaUnknown.

### Ejemplos

Muestra cómo usar los métodos FileFormatUtil para detectar el formato de un documento.

```csharp
// Cargue un documento de un archivo al que le falta una extensión de archivo y luego detecte su formato de archivo.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // A continuación se muestran dos métodos para convertir un LoadFormat a su SaveFormat correspondiente.
    // 1 - Obtenga la cadena de extensión de archivo para LoadFormat, luego obtenga el SaveFormat correspondiente de esa cadena:
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - Convertir el LoadFormat directamente a su SaveFormat:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // Cargue un documento de la secuencia y luego guárdelo en la extensión de archivo detectada automáticamente.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### Ver también

* enum [SaveFormat](../../saveformat)
* class [FileFormatUtil](../../fileformatutil)
* espacio de nombres [Aspose.Words](../../fileformatutil)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
