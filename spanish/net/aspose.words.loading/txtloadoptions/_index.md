---
title: Class TxtLoadOptions
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Loading.TxtLoadOptions clase. Permite especificar opciones adicionales al cargarText documento en unDocument objeto.
type: docs
weight: 3530
url: /es/net/aspose.words.loading/txtloadoptions/
---
## TxtLoadOptions class

Permite especificar opciones adicionales al cargarText documento en un[`Document`](../../aspose.words/document/) objeto.

```csharp
public class TxtLoadOptions : LoadOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [TxtLoadOptions](txtloadoptions/)() | Inicializa una nueva instancia de esta clase con valores predeterminados. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Obtiene o establece la cadena que se usará para convertir los URI relativos encontrados en el documento en URI absolutos cuando sea necesario. Puede ser una cadena nula o vacía. El valor predeterminado es nulo. |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Obtiene o establece si convertir el metarchivo (Wmf oEmf ) imágenes aPng formato de imagen. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Obtiene o establece si convertir formas con EquationXML en objetos de Office Math. |
| [DetectNumberingWithWhitespaces](../../aspose.words.loading/txtloadoptions/detectnumberingwithwhitespaces/) { get; set; } | Permite especificar cómo se reconocen los elementos de la lista numerada cuando el documento se importa desde formato de texto sin formato. El valor predeterminado es verdadero. |
| [DocumentDirection](../../aspose.words.loading/txtloadoptions/documentdirection/) { get; set; } | Obtiene o establece la dirección de un documento. El valor predeterminado esLeftToRight . |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Obtiene o establece la codificación que se usará para cargar un documento HTML, TXT o CHM si la codificación no se especifica dentro del documento. Puede ser nulo. El valor predeterminado es nulo. |
| [FlatOpcXmlMappingOnly](../../aspose.words.loading/loadoptions/flatopcxmlmappingonly/) { get; set; } | Obtiene o establece el valor que determina qué formatos de documento pueden ser asignados por[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Solo por defectoFlatOpc se permite mapear el formato del documento. |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Permite especificar la configuración de la fuente del documento. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Obtiene las preferencias de idioma que se usarán cuando se cargue el documento. |
| [LeadingSpacesOptions](../../aspose.words.loading/txtloadoptions/leadingspacesoptions/) { get; set; } | Obtiene o establece la opción preferida de manejo de un espacio inicial. El valor predeterminado esConvertToIndent . |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Especifica el formato del documento que se cargará. El valor predeterminado esAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Permite especificar que el proceso de carga del documento debe coincidir con una versión específica de MS Word. El valor predeterminado esWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Obtiene o establece la contraseña para abrir un documento cifrado. Puede ser una cadena nula o vacía. El valor predeterminado es nulo. |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Obtiene o establece si se debe conservar el campo INCLUDEPICTURE al leer formatos de Microsoft Word. El valor predeterminado es false. |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Llamado durante la carga de un documento y acepta datos sobre el progreso de la carga. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Permite controlar cómo se cargan los recursos externos (imágenes, hojas de estilo) cuando se importa un documento desde HTML, MHTML. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Permite utilizar archivos temporales al leer un documento. Por defecto esta propiedad es`nulo` y no se utilizan archivos temporales. |
| [TrailingSpacesOptions](../../aspose.words.loading/txtloadoptions/trailingspacesoptions/) { get; set; } | Obtiene o establece la opción preferida de un manejo de espacio final. El valor predeterminado esTrim . |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Especifica si actualizar los campos con el`sucio` atributo. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Llamado durante una operación de carga, cuando se detecta un problema que podría provocar la pérdida de fidelidad de datos o formato. |

### Ver también

* class [LoadOptions](../loadoptions/)
* espacio de nombres [Aspose.Words.Loading](../../aspose.words.loading/)
* asamblea [Aspose.Words](../../)


