---
title: "Aspose::Words::SaveFormat enum"
linktitle: "SaveFormat"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::SaveFormat enum. Indica el formato en el que se guarda el documento en C++."
type: docs
weight: 114000
url: /es/cpp/aspose.words/saveformat/
---
## SaveFormat enum


Indica el formato en el que se guarda el documento.

```cpp
enum class SaveFormat
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Desconocido | 0 | Predeterminado, valor no válido para el formato de archivo. |
| Doc | 10 | Guarda el documento en el formato Microsoft Word 97 - 2007 [Document](../document/). |
| Dot | 11 | Guarda el documento en el formato Plantilla Microsoft Word 97 - 2007. |
| Docx | 20 | Guarda el documento como un [Document](../document/) Office Open XML WordprocessingML (sin macros). |
| Docm | 21 | Guarda el documento como un Office Open XML WordprocessingML con macros habilitadas [Document](../document/). |
| Dotx | 22 | Guarda el documento como una plantilla Office Open XML WordprocessingML (sin macros). |
| Dotm | 23 | Guarda el documento como una plantilla Office Open XML WordprocessingML con macros habilitadas. |
| FlatOpc | 24 | Guarda el documento como un Office Open XML WordprocessingML almacenado en un archivo XML plano en lugar de un paquete ZIP. |
| FlatOpcMacroEnabled | 25 | Guarda el documento como un Office Open XML WordprocessingML con macros habilitadas [Document](../document/) almacenado en un archivo XML plano en lugar de un paquete ZIP. |
| FlatOpcTemplate | 26 | Guarda el documento como una plantilla Office Open XML WordprocessingML (sin macros) almacenada en un archivo XML plano en lugar de un paquete ZIP. |
| FlatOpcTemplateMacroEnabled | 27 | Guarda el documento como una plantilla Office Open XML WordprocessingML con macros habilitadas almacenada en un archivo XML plano en lugar de un paquete ZIP. |
| Rtf | 30 | Guarda el documento en formato RTF. Todos los caracteres de más de 7 bits se escapan como caracteres hexadecimales o Unicode. |
| WordML | 31 | Guarda el documento en el formato Microsoft Word 2003 WordprocessingML. |
| Pdf | 40 | Guarda el documento en formato PDF (Adobe Portable [Document](../document/)). |
| Xps | 41 | Guarda el documento en el formato XPS (XML Paper Specification). |
| XamlFixed | 42 | Guarda el documento en el formato Extensible Application [Markup](../../aspose.words.markup/) Language (XAML) como documento fijo. |
| Svg | 44 | Guarda el documento en el formato Svg (Scalable Vector Graphics). |
| HtmlFixed | 45 | Guarda el documento en el formato HTML usando elementos posicionados absolutamente. |
| OpenXps | 46 | Guarda el documento en el formato OpenXPS (Ecma-388). |
| Ps | 47 | Guarda el documento en el formato PS (PostScript). |
| Pcl | 48 | Guarda el documento en el formato PCL (Printer Control Language). |
| Html | 50 | Guarda el documento en el formato HTML. |
| Mhtml | 51 | Guarda el documento en el formato MHTML (Web archive). |
| Epub | 52 | Guarda el documento en el formato EPUB. |
| Azw3 | 53 | Guarda el documento en el formato AZW3. |
| Mobi | 54 | Guarda el documento en el formato MOBI. |
| Odt | 60 | Guarda el documento como un documento de texto ODF [Document](../document/). |
| Ott | 61 | Guarda el documento como una plantilla de documento de texto ODF [Document](../document/). |
| Text | 70 | Guarda el documento en el formato de texto plano. |
| XamlFlow | 71 | **Beta.** Guarda el documento en el formato Extensible Application [Markup](../../aspose.words.markup/) Language (XAML) como documento de flujo. |
| XamlFlowPack | 72 | **Beta.** Guarda el documento en el formato de paquete Extensible Application [Markup](../../aspose.words.markup/) Language (XAML) como documento de flujo. |
| Markdown | 73 | Guarda el documento en el formato Markdown. |
| Xlsx | 80 | Guarda el documento como un [Document](../document/) SpreadsheetML de Office Open XML (sin macros). |
| Docling | 81 | Guarda el documento en el formato Docling JSON. |
| Tiff | 100 | Renderiza una página o varias del documento y las guarda en un archivo TIFF único o multipágina. |
| Png | 101 | Renderiza una página del documento y la guarda como un archivo PNG. |
| Bmp | 102 | Renderiza una página del documento y la guarda como un archivo BMP. |
| Emf | 103 | Renderiza una página del documento y la guarda como un archivo vectorial EMF (Enhanced Meta File). |
| Jpeg | 104 | Renderiza una página del documento y la guarda como un archivo JPEG. |
| Gif | 105 | Renderiza una página del documento y la guarda como un archivo GIF. |
| Eps | 106 | Renderiza una página del documento y la guarda como un archivo EPS. |


## Ejemplos



Muestra cómo convertir de formato DOCX a HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

doc->Save(get_ArtifactsDir() + u"Document.ConvertToHtml.html", Aspose::Words::SaveFormat::Html);
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
