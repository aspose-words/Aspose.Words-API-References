---
title: SaveFormat Enum
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words para .NET
description: Aspose.Words.SaveFormat enumeración. Indica el formato en el que se guarda el documento en C#.
type: docs
weight: 4840
url: /es/net/aspose.words/saveformat/
---
## SaveFormat enumeration

Indica el formato en el que se guarda el documento.

```csharp
public enum SaveFormat
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Unknown | `0` | Valor predeterminado no válido para el formato de archivo. |
| Doc | `10` | Guarda el documento en el formato de documento Microsoft Word 97 - 2007. |
| Dot | `11` | Guarda el documento en el formato de plantilla de Microsoft Word 97 - 2007. |
| Docx | `20` | Guarda el documento como un documento Office Open XML WordprocessingML (sin macros). |
| Docm | `21` | Guarda el documento como un documento habilitado para macros de Office Open XML WordprocessingML. |
| Dotx | `22` | Guarda el documento como una plantilla Office Open XML WordprocessingML (sin macros). |
| Dotm | `23` | Guarda el documento como una plantilla habilitada para macros de Office Open XML WordprocessingML. |
| FlatOpc | `24` | Guarda el documento como un procesamiento de textos XML abierto de Office ML almacenado en un archivo XML plano en lugar de un paquete ZIP. |
| FlatOpcMacroEnabled | `25` | Guarda el documento como un documento habilitado para macros de Office Open XML WordprocessingML almacenado en un archivo XML plano en lugar de un paquete ZIP. |
| FlatOpcTemplate | `26` | Guarda el documento como una plantilla Office Open XML WordprocessingML (sin macros) almacenada en un archivo XML plano en lugar de un paquete ZIP. |
| FlatOpcTemplateMacroEnabled | `27` | Guarda el documento como una plantilla habilitada para macros de Office Open XML WordprocessingML almacenada en un archivo XML plano en lugar de un paquete ZIP. |
| Rtf | `30` | Guarda el documento en formato RTF. Todos los caracteres superiores a 7 bits se utilizan como caracteres de escape como caracteres hexadecimales o Unicode. |
| WordML | `31` | Guarda el documento en formato Microsoft Word 2003 WordprocessingML. |
| Pdf | `40` | Guarda el documento en formato PDF (Adobe Portable Document). |
| Xps | `41` | Guarda el documento en formato XPS (Especificación de papel XML). |
| XamlFixed | `42` | Guarda el documento en formato XAML (Extensible Application Markup Language) como un documento fijo. |
| Svg | `44` | Guarda el documento en formato SVG (Gráficos vectoriales escalables). |
| HtmlFixed | `45` | Guarda el documento en formato HTML utilizando elementos posicionados absolutamente |
| OpenXps | `46` | Guarda el documento en formato OpenXPS (Ecma-388). |
| Ps | `47` | Guarda el documento en formato PS (PostScript). |
| Pcl | `48` | Guarda el documento en formato PCL (Lenguaje de control de impresora). |
| Html | `50` | Guarda el documento en formato HTML. |
| Mhtml | `51` | Guarda el documento en formato MHTML (archivo web). |
| Epub | `52` | Guarda el documento en formato EPUB. |
| Azw3 | `53` | Guarda el documento en formato AZW3. |
| Mobi | `54` | Guarda el documento en formato MOBI. |
| Odt | `60` | Guarda el documento como documento de texto ODF. |
| Ott | `61` | Guarda el documento como una plantilla de documento de texto ODF. |
| Text | `70` | Guarda el documento en formato de texto sin formato. |
| XamlFlow | `71` | **Beta.** Guarda el documento en formato XAML (Lenguaje de marcado de aplicaciones extensible) como un documento de flujo. |
| XamlFlowPack | `72` | **Beta.** Guarda el documento en el formato de paquete de lenguaje de marcado de aplicaciones extensible (XAML) como un documento de flujo. |
| Markdown | `73` | Guarda el documento en formato Markdown. |
| Xlsx | `80` | Guarda el documento como un documento Office Open XML SpreadsheetML (sin macros). |
| Tiff | `100` | Representa una página o páginas del documento y las guarda en un archivo TIFF de una o varias páginas. |
| Png | `101` | Representa una página del documento y la guarda como un archivo PNG. |
| Bmp | `102` | Representa una página del documento y la guarda como un archivo BMP. |
| Emf | `103` | Representa una página del documento y la guarda como un archivo vectorial EMF (Enhanced Meta File). |
| Jpeg | `104` | Representa una página del documento y la guarda como un archivo JPEG. |
| Gif | `105` | Representa una página del documento y la guarda como un archivo GIF. |
| Eps | `106` | Representa una página del documento y la guarda como un archivo EPS. |

## Ejemplos

Muestra cómo convertir de formato DOCX a HTML.

```csharp
Document doc = new Document(MyDir + "Document.docx");

doc.Save(ArtifactsDir + "Document.ConvertToHtml.html", SaveFormat.Html);
```

### Ver también

* method [Save](../document/save/)
* class [SaveOptions](../../aspose.words.saving/saveoptions/)
* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
