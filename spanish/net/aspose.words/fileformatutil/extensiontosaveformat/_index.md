---
title: FileFormatUtil.ExtensionToSaveFormat
second_title: Referencia de API de Aspose.Words para .NET
description: FileFormatUtil método. Convierte una extensión de nombre de archivo en unSaveFormat valor.
type: docs
weight: 40
url: /es/net/aspose.words/fileformatutil/extensiontosaveformat/
---
## FileFormatUtil.ExtensionToSaveFormat method

Convierte una extensión de nombre de archivo en un[`SaveFormat`](../../saveformat/) valor.

```csharp
public static SaveFormat ExtensionToSaveFormat(string extension)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| extension | String | La extensión del archivo. Puede ser con o sin punto inicial. No distingue entre mayúsculas y minúsculas. |

### Excepciones

| excepción | condición |
| --- | --- |
| ArgumentNullException | Lanza si el parámetro es`nulo`. |

### Observaciones

Si la extensión no se puede reconocer, regresaUnknown.

### Ejemplos

Muestra cómo utilizar los métodos FileFormatUtil para detectar el formato de un documento.

```csharp
// Cargue un documento desde un archivo al que le falta una extensión de archivo y luego detecte su formato de archivo.
using (FileStream docStream = File.OpenRead(MyDir + "Word document with missing file extension"))
{
    FileFormatInfo info = FileFormatUtil.DetectFileFormat(docStream);
    LoadFormat loadFormat = info.LoadFormat;

    Assert.AreEqual(LoadFormat.Doc, loadFormat);

    // A continuación se muestran dos métodos para convertir un LoadFormat a su SaveFormat correspondiente.
    // 1 - Obtenga la cadena de extensión del archivo para LoadFormat, luego obtenga el SaveFormat correspondiente de esa cadena:
    string fileExtension = FileFormatUtil.LoadFormatToExtension(loadFormat);
    SaveFormat saveFormat = FileFormatUtil.ExtensionToSaveFormat(fileExtension);

    // 2 - Convertir LoadFormat directamente a su SaveFormat:
    saveFormat = FileFormatUtil.LoadFormatToSaveFormat(loadFormat);

    // Cargue un documento de la secuencia y luego guárdelo en la extensión de archivo detectada automáticamente.
    Document doc = new Document(docStream);

    Assert.AreEqual(".doc", FileFormatUtil.SaveFormatToExtension(saveFormat));

    doc.Save(ArtifactsDir + "File.SaveToDetectedFileFormat" + FileFormatUtil.SaveFormatToExtension(saveFormat));
}
```

### Ver también

* enum [SaveFormat](../../saveformat/)
* class [FileFormatUtil](../)
* espacio de nombres [Aspose.Words](../../fileformatutil/)
* asamblea [Aspose.Words](../../../)


