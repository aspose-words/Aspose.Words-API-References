---
title: MarkdownLoadOptions Class
linktitle: MarkdownLoadOptions
articleTitle: MarkdownLoadOptions
second_title: Aspose.Words para .NET
description: Descubre Aspose.Words.MarkdownLoadOptions para mejorar la carga de documentos Markdown. Personaliza las opciones para una integración perfecta en tus proyectos.
type: docs
weight: 4120
url: /es/net/aspose.words.loading/markdownloadoptions/
---
## MarkdownLoadOptions class

Permite especificar opciones adicionales al cargarMarkdown documento en un[`Document`](../../aspose.words/document/) objeto.

```csharp
public class MarkdownLoadOptions : LoadOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [MarkdownLoadOptions](markdownloadoptions/)() | Inicializa una nueva instancia de`MarkdownLoadOptions` clase. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Obtiene o establece la cadena que se utilizará para resolver los URI relativos encontrados en el documento en URI absolutos cuando sea necesario. Puede ser`nulo` o cadena vacía. El valor predeterminado es`nulo` . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Obtiene o establece si se debe convertir el metarchivo(Wmf oEmf ) imágenes aPngformato de imagen. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Obtiene o establece si se deben convertir formas con EquationXML en objetos de Office Math. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Obtiene o establece la codificación que se utilizará para cargar un documento HTML, TXT o CHM si no se especifica la codificación dentro del documento. Puede ser`nulo` El valor predeterminado es`nulo` . |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Permite especificar la configuración de fuentes del documento. |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | Especifica si se deben ignorar los datos OLE. |
| [ImportUnderlineFormatting](../../aspose.words.loading/markdownloadoptions/importunderlineformatting/) { get; set; } | Obtiene o establece un valor booleano que indica si se debe reconocer una secuencia de dos caracteres más "++" como formato de texto subrayado. El valor predeterminado es`FALSO` . |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Obtiene las preferencias de idioma que se utilizarán cuando se cargue el documento. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Especifica el formato del documento que se va a cargar. El valor predeterminado esAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Permite especificar que el proceso de carga del documento debe coincidir con una versión específica de MS Word. El valor predeterminado esWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Obtiene o establece la contraseña para abrir un documento cifrado. Puede ser`nulo` o cadena vacía. El valor predeterminado es`nulo` . |
| [PreserveEmptyLines](../../aspose.words.loading/markdownloadoptions/preserveemptylines/) { get; set; } | Obtiene o establece un valor booleano que indica si se deben conservar las líneas vacías mientras se carga unMarkdown document. El valor predeterminado es`FALSO` . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Obtiene o establece si se debe conservar el campo INCLUDEPICTURE al leer formatos de Microsoft Word. El valor predeterminado es`FALSO` . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Se llama durante la carga de un documento y acepta datos sobre el progreso de la carga. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Permite controlar cómo se cargan los recursos externos (imágenes, hojas de estilo) cuando se importa un documento desde HTML, MHTML. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Permite utilizar archivos temporales al leer el documento. Por defecto esta propiedad es`nulo` y no se utilizan archivos temporales. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Especifica si se deben actualizar los campos con el`sucio` atributo. |
| [UseSystemLcid](../../aspose.words.loading/loadoptions/usesystemlcid/) { get; set; } | Obtiene o establece si se debe utilizar el valor LCID obtenido del registro de Windows para determinar los márgenes predeterminados de configuración de página. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Se llama durante una operación de carga, cuando se detecta un problema que podría provocar pérdida de fidelidad de datos o formato. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(*object*) | Determina si el objeto especificado es igual en valor al objeto actual. |

## Ejemplos

Muestra cómo conservar una línea vacía mientras se carga un documento.

```csharp
string mdText = $"{Environment.NewLine}Line1{Environment.NewLine}{Environment.NewLine}Line2{Environment.NewLine}{Environment.NewLine}";
using (MemoryStream stream = new MemoryStream(Encoding.UTF8.GetBytes(mdText)))
{
    MarkdownLoadOptions loadOptions = new MarkdownLoadOptions() { PreserveEmptyLines = true };
    Document doc = new Document(stream, loadOptions);

    Assert.AreEqual("\rLine1\r\rLine2\r\f", doc.GetText());
}
```

### Ver también

* class [LoadOptions](../loadoptions/)
* espacio de nombres [Aspose.Words.Loading](../../aspose.words.loading/)
* asamblea [Aspose.Words](../../)
