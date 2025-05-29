---
title: OoxmlSaveOptions.CompressionLevel
linktitle: CompressionLevel
articleTitle: CompressionLevel
second_title: Aspose.Words para .NET
description: Descubra la propiedad OoxmlSaveOptions CompressionLevel para optimizar el guardado de documentos con niveles de compresión personalizables para un mejor rendimiento.
type: docs
weight: 30
url: /es/net/aspose.words.saving/ooxmlsaveoptions/compressionlevel/
---
## OoxmlSaveOptions.CompressionLevel property

Especifica el nivel de compresión utilizado para guardar el documento. El valor predeterminado esNormal .

```csharp
public CompressionLevel CompressionLevel { get; set; }
```

## Ejemplos

Muestra cómo especificar el nivel de compresión a utilizar al guardar un documento OOXML.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// Cuando guardamos el documento en un formato OOXML, podemos crear un objeto OoxmlSaveOptions
// y luego pasarlo al método de guardar del documento para modificar la forma en que guardamos el documento.
// Establezca la propiedad "CompressionLevel" en "CompressionLevel.Maximum" para aplicar la compresión más fuerte y más lenta.
// Establezca la propiedad "CompressionLevel" en "CompressionLevel.Normal" para aplicar
// la compresión predeterminada que utiliza Aspose.Words al guardar documentos OOXML.
// Establezca la propiedad "CompressionLevel" en "CompressionLevel.Fast" para aplicar una compresión más rápida y más débil.
// Establezca la propiedad "CompressionLevel" en "CompressionLevel.SuperFast" para aplicar
// la compresión predeterminada que utiliza Microsoft Word.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(SaveFormat.Docx);
saveOptions.CompressionLevel = compressionLevel;

Stopwatch st = Stopwatch.StartNew();
doc.Save(ArtifactsDir + "OoxmlSaveOptions.DocumentCompression.docx", saveOptions);
st.Stop();

FileInfo fileInfo = new FileInfo(ArtifactsDir + "OoxmlSaveOptions.DocumentCompression.docx");

Console.WriteLine($"Saving operation done using the \"{compressionLevel}\" compression level:");
Console.WriteLine($"\tDuration:\t{st.ElapsedMilliseconds} ms");
Console.WriteLine($"\tFile Size:\t{fileInfo.Length} bytes");
```

### Ver también

* enum [CompressionLevel](../../compressionlevel/)
* class [OoxmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
