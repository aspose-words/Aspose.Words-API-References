---
title: RtfLoadOptions
second_title: Referencia de API de Aspose.Words para .NET
description: Permite especificar opciones adicionales al cargarRtf documento en unDocument../aspose.words/document/ objeto.
type: docs
weight: 3510
url: /es/net/aspose.words.loading/rtfloadoptions/
---
## RtfLoadOptions class

Permite especificar opciones adicionales al cargarRtf documento en un[`Document`](../../aspose.words/document/) objeto.

```csharp
public class RtfLoadOptions : LoadOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [RtfLoadOptions](rtfloadoptions/)() | Inicializa una nueva instancia de esta clase con valores predeterminados. |

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
| [RecognizeUtf8Text](../../aspose.words.loading/rtfloadoptions/recognizeutf8text/) { get; set; } | Cuando se establece en verdadero,CharsetDetectorintentará detectar caracteres UTF8, se conservarán durante la importación. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Permite controlar cómo se cargan los recursos externos (imágenes, hojas de estilo) cuando se importa un documento desde HTML, MHTML. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Permite utilizar archivos temporales al leer un documento. Por defecto esta propiedad es`nulo` y no se utilizan archivos temporales. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Especifica si actualizar los campos con el`sucio` atributo. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Llamado durante una operación de carga, cuando se detecta un problema que podría provocar la pérdida de fidelidad de datos o formato. |

### Ejemplos

Muestra cómo detectar caracteres UTF-8 al cargar un documento RTF.

```csharp
// Crear un objeto "RtfLoadOptions" para modificar cómo cargamos un documento RTF.
RtfLoadOptions loadOptions = new RtfLoadOptions();

// Establezca la propiedad "RecognizeUtf8Text" en "false" para asumir que el documento usa el juego de caracteres ISO 8859-1
// y carga todos los caracteres del documento.
// Establezca la propiedad "RecognizeUtf8Text" en "true" para analizar cualquier carácter de longitud variable que pueda aparecer en el texto.
loadOptions.RecognizeUtf8Text = recognizeUtf8Text;

Document doc = new Document(MyDir + "UTF-8 characters.rtf", loadOptions);

Assert.AreEqual(
    recognizeUtf8Text
        ? "“John Doe´s list of currency symbols”™\r" +
          "€, ¢, £, ¥, ¤"
        : "â€œJohn DoeÂ´s list of currency symbolsâ€\u009dâ„¢\r" +
          "â‚¬, Â¢, Â£, Â¥, Â¤",
    doc.FirstSection.Body.GetText().Trim());
```

### Ver también

* class [LoadOptions](../loadoptions/)
* espacio de nombres [Aspose.Words.Loading](../../aspose.words.loading/)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
