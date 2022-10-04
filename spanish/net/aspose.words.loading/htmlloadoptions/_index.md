---
title: HtmlLoadOptions
second_title: Referencia de API de Aspose.Words para .NET
description: Permite especificar opciones adicionales al cargar un documento HTML en unDocument../aspose.words/document/ objeto.
type: docs
weight: 3420
url: /es/net/aspose.words.loading/htmlloadoptions/
---
## HtmlLoadOptions class

Permite especificar opciones adicionales al cargar un documento HTML en un[`Document`](../../aspose.words/document/) objeto.

```csharp
public class HtmlLoadOptions : LoadOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [HtmlLoadOptions](htmlloadoptions/#constructor)() | Inicializa una nueva instancia de esta clase con valores predeterminados. |
| [HtmlLoadOptions](htmlloadoptions/#constructor_2)(string) | Un atajo para inicializar una nueva instancia de esta clase con la contraseña especificada para cargar un documento encriptado. |
| [HtmlLoadOptions](htmlloadoptions/#constructor_1)(LoadFormat, string, string) | Un atajo para inicializar una nueva instancia de esta clase con propiedades establecidas en los valores especificados. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Obtiene o establece la cadena que se usará para convertir los URI relativos encontrados en el documento en URI absolutos cuando sea necesario. Puede ser una cadena nula o vacía. El valor predeterminado es nulo. |
| [BlockImportMode](../../aspose.words.loading/htmlloadoptions/blockimportmode/) { get; set; } | Obtiene o establece un valor que especifica cómo se importan las propiedades de los elementos a nivel de bloque. El valor predeterminado esMerge . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Obtiene o establece si convertir el metarchivo (Wmf oEmf ) imágenes aPng formato de imagen. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Obtiene o establece si convertir formas con EquationXML en objetos de Office Math. |
| [ConvertSvgToEmf](../../aspose.words.loading/htmlloadoptions/convertsvgtoemf/) { get; set; } | Obtiene o establece un valor que indica si se deben convertir las imágenes SVG cargadas al formato EMF. El valor predeterminado es`falso` y, si es posible, las imágenes SVG cargadas se almacenan tal cual sin conversión. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Obtiene o establece la codificación que se usará para cargar un documento HTML, TXT o CHM si la codificación no se especifica dentro del documento. Puede ser nulo. El valor predeterminado es nulo. |
| [FlatOpcXmlMappingOnly](../../aspose.words.loading/loadoptions/flatopcxmlmappingonly/) { get; set; } | Obtiene o establece el valor que determina qué formatos de documento pueden ser asignados por[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Solo por defectoFlatOpc se permite mapear el formato del documento. |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Permite especificar la configuración de la fuente del documento. |
| [IgnoreNoscriptElements](../../aspose.words.loading/htmlloadoptions/ignorenoscriptelements/) { get; set; } | Obtiene o establece un valor que indica si se deben ignorar los elementos HTML &lt;noscript&gt;. El valor predeterminado es`falso` . |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Obtiene las preferencias de idioma que se usarán cuando se cargue el documento. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Especifica el formato del documento que se cargará. El valor predeterminado esAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Permite especificar que el proceso de carga del documento debe coincidir con una versión específica de MS Word. El valor predeterminado esWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Obtiene o establece la contraseña para abrir un documento cifrado. Puede ser una cadena nula o vacía. El valor predeterminado es nulo. |
| [PreferredControlType](../../aspose.words.loading/htmlloadoptions/preferredcontroltype/) { get; set; } | Obtiene o establece el tipo preferido de nodos de documento que representarán los elementos &lt;input&gt; y &lt;select&gt; importados. El valor predeterminado esFormField . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Obtiene o establece si se debe conservar el campo INCLUDEPICTURE al leer formatos de Microsoft Word. El valor predeterminado es false. |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Llamado durante la carga de un documento y acepta datos sobre el progreso de la carga. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Permite controlar cómo se cargan los recursos externos (imágenes, hojas de estilo) cuando se importa un documento desde HTML, MHTML. |
| [SupportVml](../../aspose.words.loading/htmlloadoptions/supportvml/) { get; set; } | Obtiene o establece un valor que indica si se admiten imágenes VML. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Permite utilizar archivos temporales al leer un documento. Por defecto esta propiedad es`nulo` y no se utilizan archivos temporales. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Especifica si actualizar los campos con el`sucio` atributo. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Llamado durante una operación de carga, cuando se detecta un problema que podría provocar la pérdida de fidelidad de datos o formato. |
| [WebRequestTimeout](../../aspose.words.loading/htmlloadoptions/webrequesttimeout/) { get; set; } | El número de milisegundos a esperar antes de que se agote el tiempo de espera de la solicitud web. El valor predeterminado es 100000 milisegundos (100 segundos). |

### Ver también

* class [LoadOptions](../loadoptions/)
* espacio de nombres [Aspose.Words.Loading](../../aspose.words.loading/)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
