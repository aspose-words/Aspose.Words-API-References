---
title: FileFormatUtil Class
linktitle: FileFormatUtil
articleTitle: FileFormatUtil
second_title: Aspose.Words para .NET
description: Gestione fácilmente los formatos de archivo con Aspose.Words.FileFormatUtil. Detecte formatos y convierta extensiones sin problemas para una mayor productividad.
type: docs
weight: 3230
url: /es/net/aspose.words/fileformatutil/
---
## FileFormatUtil class

Proporciona métodos de utilidad para trabajar con formatos de archivo, como detectar el formato de archivo o convertir extensiones de archivo a/desde enumeraciones de formato de archivo.

Para obtener más información, visite el[Detectar formato de archivo y comprobar compatibilidad de formatos](https://docs.aspose.com/words/net/detect-file-format-and-check-format-compatibility/) Artículo de documentación.

```csharp
public static class FileFormatUtil
```

## Métodos

| Nombre | Descripción |
| --- | --- |
| static [ContentTypeToLoadFormat](../../aspose.words/fileformatutil/contenttypetoloadformat/)(*string*) | Convierte el tipo de contenido de IANA en un valor enumerado con formato de carga. |
| static [ContentTypeToSaveFormat](../../aspose.words/fileformatutil/contenttypetosaveformat/)(*string*) | Convierte el tipo de contenido de IANA en un valor enumerado en formato guardado. |
| static [DetectFileFormat](../../aspose.words/fileformatutil/detectfileformat/#detectfileformat)(*Stream*) | Detecta y devuelve la información sobre el formato de un documento almacenado en una secuencia. |
| static [DetectFileFormat](../../aspose.words/fileformatutil/detectfileformat/#detectfileformat_1)(*string*) | Detecta y devuelve la información sobre el formato de un documento almacenado en un archivo de disco. |
| static [ExtensionToSaveFormat](../../aspose.words/fileformatutil/extensiontosaveformat/)(*string*) | Convierte una extensión de nombre de archivo en una[`SaveFormat`](../saveformat/) valor. |
| static [ImageTypeToExtension](../../aspose.words/fileformatutil/imagetypetoextension/)(*[ImageType](../../aspose.words.drawing/imagetype/)*) | Convierte un valor enumerado de tipo de imagen Aspose.Words en una extensión de archivo. La extensión devuelta es una cadena en minúsculas con un punto inicial. |
| static [LoadFormatToExtension](../../aspose.words/fileformatutil/loadformattoextension/)(*[LoadFormat](../loadformat/)*) | Convierte un valor enumerado del formato de carga en una extensión de archivo. La extensión devuelta es una cadena en minúsculas con un punto inicial. |
| static [LoadFormatToSaveFormat](../../aspose.words/fileformatutil/loadformattosaveformat/)(*[LoadFormat](../loadformat/)*) | Convierte un[`LoadFormat`](../loadformat/) valor para un[`SaveFormat`](../saveformat/) valor si es posible. |
| static [SaveFormatToExtension](../../aspose.words/fileformatutil/saveformattoextension/)(*[SaveFormat](../saveformat/)*) | Convierte un valor enumerado en formato de guardado en una extensión de archivo. La extensión devuelta es una cadena en minúsculas con un punto inicial. |
| static [SaveFormatToLoadFormat](../../aspose.words/fileformatutil/saveformattoloadformat/)(*[SaveFormat](../saveformat/)*) | Convierte un[`SaveFormat`](../saveformat/) valor para un[`LoadFormat`](../loadformat/) valor si es posible. |

## Ejemplos

Muestra cómo detectar la codificación en un archivo html.

```csharp
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.html");

Assert.AreEqual(LoadFormat.Html, info.LoadFormat);

// La propiedad Encoding se utiliza solo cuando creamos un objeto FileFormatInfo para un documento html.
Assert.AreEqual("Western European (Windows)", info.Encoding.EncodingName);
Assert.AreEqual(1252, info.Encoding.CodePage);
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
