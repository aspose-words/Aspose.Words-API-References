---
title: Class FileFormatUtil
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.FileFormatUtil clase. Proporciona métodos de utilidad para trabajar con formatos de archivo como detectar el formato de archivo o convertir extensiones de archivo a/desde enumeraciones de formato de archivo.
type: docs
weight: 2640
url: /es/net/aspose.words/fileformatutil/
---
## FileFormatUtil class

Proporciona métodos de utilidad para trabajar con formatos de archivo, como detectar el formato de archivo o convertir extensiones de archivo a/desde enumeraciones de formato de archivo.

```csharp
public static class FileFormatUtil
```

## Métodos

| Nombre | Descripción |
| --- | --- |
| static [ContentTypeToLoadFormat](../../aspose.words/fileformatutil/contenttypetoloadformat/)(string) | Convierte el tipo de contenido de IANA en un valor enumerado de formato de carga. |
| static [ContentTypeToSaveFormat](../../aspose.words/fileformatutil/contenttypetosaveformat/)(string) | Convierte el tipo de contenido de IANA en un valor enumerado de formato guardado. |
| static [DetectFileFormat](../../aspose.words/fileformatutil/detectfileformat/#detectfileformat)(Stream) | Detecta y devuelve la información sobre un formato de un documento almacenado en un flujo. |
| static [DetectFileFormat](../../aspose.words/fileformatutil/detectfileformat/#detectfileformat_1)(string) | Detecta y devuelve la información sobre un formato de un documento almacenado en un archivo de disco. |
| static [ExtensionToSaveFormat](../../aspose.words/fileformatutil/extensiontosaveformat/)(string) | Convierte una extensión de nombre de archivo en una[`SaveFormat`](../saveformat/) valor. |
| static [ImageTypeToExtension](../../aspose.words/fileformatutil/imagetypetoextension/)(ImageType) | Convierte un valor enumerado de tipo de imagen de Aspose.Words en una extensión de archivo. La extensión devuelta es una cadena en minúsculas con un punto inicial. |
| static [LoadFormatToExtension](../../aspose.words/fileformatutil/loadformattoextension/)(LoadFormat) | Convierte un valor enumerado de formato de carga en una extensión de archivo. La extensión devuelta es una cadena en minúsculas con un punto inicial. |
| static [LoadFormatToSaveFormat](../../aspose.words/fileformatutil/loadformattosaveformat/)(LoadFormat) | Convierte un[`LoadFormat`](../loadformat/) valor a un[`SaveFormat`](../saveformat/) valor si es posible. |
| static [SaveFormatToExtension](../../aspose.words/fileformatutil/saveformattoextension/)(SaveFormat) | Convierte un valor enumerado de formato guardado en una extensión de archivo. La extensión devuelta es una cadena en minúsculas con un punto inicial. |
| static [SaveFormatToLoadFormat](../../aspose.words/fileformatutil/saveformattoloadformat/)(SaveFormat) | Convierte un[`SaveFormat`](../saveformat/) valor a un[`LoadFormat`](../loadformat/) valor si es posible. |

### Ejemplos

Muestra cómo detectar la codificación en un archivo html.

```csharp
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.html");

Assert.AreEqual(LoadFormat.Html, info.LoadFormat);

// La propiedad Encoding se usa solo cuando creamos un objeto FileFormatInfo para un documento html.
Assert.AreEqual("Western European (Windows)", info.Encoding.EncodingName);
Assert.AreEqual(1252, info.Encoding.CodePage);
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)


