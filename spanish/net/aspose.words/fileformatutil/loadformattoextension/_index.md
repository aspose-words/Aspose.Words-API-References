---
title: FileFormatUtil.LoadFormatToExtension
linktitle: LoadFormatToExtension
articleTitle: LoadFormatToExtension
second_title: Aspose.Words para .NET
description: Transforma fácilmente los valores de formato de carga en extensiones de archivo con el método LoadFormatToExtension de FileFormatUtil. ¡Obtén extensiones precisas en minúsculas fácilmente!
type: docs
weight: 60
url: /es/net/aspose.words/fileformatutil/loadformattoextension/
---
## FileFormatUtil.LoadFormatToExtension method

Convierte un valor enumerado del formato de carga en una extensión de archivo. La extensión devuelta es una cadena en minúsculas con un punto inicial.

```csharp
public static string LoadFormatToExtension(LoadFormat loadFormat)
```

### Excepciones

| excepción | condición |
| --- | --- |
| ArgumentException | Se lanza cuando no se puede convertir. |

## Observaciones

ElWordML El valor se convierte a ".wml".

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

* enum [LoadFormat](../../loadformat/)
* class [FileFormatUtil](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
