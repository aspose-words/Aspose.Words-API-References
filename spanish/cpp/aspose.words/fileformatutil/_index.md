---
title: "Aspose::Words::FileFormatUtil clase"
linktitle: "FileFormatUtil"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::FileFormatUtil clase. Proporciona métodos utilitarios para trabajar con formatos de archivo, como detectar el formato de archivo o convertir extensiones de archivo a/de enumeraciones de formatos de archivo. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 28000
url: /es/cpp/aspose.words/fileformatutil/
---
## FileFormatUtil class


Proporciona métodos utilitarios para trabajar con formatos de archivo, como detectar el formato de archivo o convertir extensiones de archivo a/de enumeraciones de formatos de archivo. Para obtener más información, visite el artículo de documentación [Detect File Format and Check Format Compatibility](https://docs.aspose.com/words/cpp/detect-file-format-and-check-format-compatibility/).

```cpp
class FileFormatUtil
```

## Métodos

| Método | Descripción |
| --- | --- |
| static [ContentTypeToLoadFormat](./contenttypetoloadformat/)(const System::String\&) | Convierte el tipo de contenido IANA en un valor enumerado de formato de carga. |
| static [ContentTypeToSaveFormat](./contenttypetosaveformat/)(const System::String\&) | Convierte el tipo de contenido IANA en un valor enumerado de formato de guardado. |
| static [DetectFileFormat](./detectfileformat/)(const System::String\&) | Detecta y devuelve la información sobre el formato de un documento almacenado en un archivo en disco. |
| static [DetectFileFormat](./detectfileformat/)(const System::SharedPtr\<System::IO::Stream\>\&) | Detecta y devuelve la información sobre el formato de un documento almacenado en un flujo. |
| static [DetectFileFormat](./detectfileformat/)(std::basic_istream\<CharType, Traits\>\&) |  |
| static [ExtensionToSaveFormat](./extensiontosaveformat/)(const System::String\&) | Convierte una extensión de nombre de archivo en un valor de [SaveFormat](../saveformat/). |
| [FileFormatUtil](./fileformatutil/)() |  |
| static [ImageTypeToExtension](./imagetypetoextension/)(Aspose::Words::Drawing::ImageType) | Convierte un valor enumerado de tipo de imagen de Aspose.Words en una extensión de archivo. La extensión devuelta es una cadena en minúsculas con un punto inicial. |
| static [LoadFormatToExtension](./loadformattoextension/)(Aspose::Words::LoadFormat) | Convierte un valor enumerado de formato de carga en una extensión de archivo. La extensión devuelta es una cadena en minúsculas con un punto inicial. |
| static [LoadFormatToSaveFormat](./loadformattosaveformat/)(Aspose::Words::LoadFormat) | Convierte un valor de [LoadFormat](../loadformat/) a un valor de [SaveFormat](../saveformat/) si es posible. |
| static [SaveFormatToExtension](./saveformattoextension/)(Aspose::Words::SaveFormat) | Convierte un valor enumerado de formato de guardado en una extensión de archivo. La extensión devuelta es una cadena en minúsculas con un punto inicial. |
| static [SaveFormatToLoadFormat](./saveformattoloadformat/)(Aspose::Words::SaveFormat) | Convierte un valor de [SaveFormat](../saveformat/) a un valor de [LoadFormat](../loadformat/) si es posible. |

## Ejemplos



Muestra cómo detectar la codificación en un archivo html.
```cpp
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.html");

ASSERT_EQ(Aspose::Words::LoadFormat::Html, info->get_LoadFormat());

// La propiedad Encoding se usa solo cuando creamos un objeto FileFormatInfo para un documento html.
ASSERT_EQ(u"Western European (Windows)", info->get_Encoding()->get_EncodingName());
ASSERT_EQ(1252, info->get_Encoding()->get_CodePage());
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
