---
title: LoadOptions
second_title: Referencia de API de Aspose.Words para .NET
description: Permite especificar opciones adicionales como contraseña o URI base al cargar un documento en unDocument../aspose.words/document/ objeto.
type: docs
weight: 3460
url: /es/net/aspose.words.loading/loadoptions/
---
## LoadOptions class

Permite especificar opciones adicionales (como contraseña o URI base) al cargar un documento en un[`Document`](../../aspose.words/document/) objeto.

```csharp
public class LoadOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [LoadOptions](loadoptions/#constructor)() | Inicializa una nueva instancia de esta clase con valores predeterminados. |
| [LoadOptions](loadoptions/#constructor_2)(string) | Un atajo para inicializar una nueva instancia de esta clase con la contraseña especificada para cargar un documento encriptado. |
| [LoadOptions](loadoptions/#constructor_1)(LoadFormat, string, string) | Un atajo para inicializar una nueva instancia de esta clase con propiedades establecidas en los valores especificados. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Obtiene o establece la cadena que se usará para convertir los URI relativos encontrados en el documento en URI absolutos cuando sea necesario. Puede ser una cadena nula o vacía. El valor predeterminado es nulo. |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Obtiene o establece si convertir el metarchivo (Wmf oEmf ) imágenes aPng formato de imagen. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Obtiene o establece si convertir formas con EquationXML en objetos de Office Math. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Obtiene o establece la codificación que se usará para cargar un documento HTML, TXT o CHM si la codificación no se especifica dentro del documento. Puede ser nulo. El valor predeterminado es nulo. |
| [FlatOpcXmlMappingOnly](../../aspose.words.loading/loadoptions/flatopcxmlmappingonly/) { get; set; } | Obtiene o establece el valor que determina qué formatos de documento pueden ser asignados por[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Solo por defectoFlatOpc se permite mapear el formato del documento. |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Permite especificar la configuración de la fuente del documento. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Obtiene las preferencias de idioma que se usarán cuando se cargue el documento. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Especifica el formato del documento que se cargará. El valor predeterminado esAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Permite especificar que el proceso de carga del documento debe coincidir con una versión específica de MS Word. El valor predeterminado esWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Obtiene o establece la contraseña para abrir un documento cifrado. Puede ser una cadena nula o vacía. El valor predeterminado es nulo. |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Obtiene o establece si se debe conservar el campo INCLUDEPICTURE al leer formatos de Microsoft Word. El valor predeterminado es false. |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Llamado durante la carga de un documento y acepta datos sobre el progreso de la carga. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Permite controlar cómo se cargan los recursos externos (imágenes, hojas de estilo) cuando se importa un documento desde HTML, MHTML. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Permite utilizar archivos temporales al leer un documento. Por defecto esta propiedad es`nulo` y no se utilizan archivos temporales. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Especifica si actualizar los campos con el`sucio` atributo. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Llamado durante una operación de carga, cuando se detecta un problema que podría provocar la pérdida de fidelidad de datos o formato. |

### Ejemplos

Muestra cómo cargar un documento cifrado de Microsoft Word.

```csharp
Document doc;

// Aspose.Words lanza una excepción si intentamos abrir un documento encriptado sin su contraseña.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// Al cargar un documento de este tipo, la contraseña se pasa al constructor del documento mediante un objeto LoadOptions.
LoadOptions options = new LoadOptions("docPassword");

// Hay dos formas de cargar un documento cifrado con un objeto LoadOptions.
// 1 - Cargar el documento desde el sistema de archivos local por nombre de archivo:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - Cargar el documento desde un stream:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
```

### Ver también

* espacio de nombres [Aspose.Words.Loading](../../aspose.words.loading/)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
