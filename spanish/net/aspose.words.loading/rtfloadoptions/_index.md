---
title: RtfLoadOptions Class
linktitle: RtfLoadOptions
articleTitle: RtfLoadOptions
second_title: Aspose.Words para .NET
description: Descubra Aspose.Words.RtfLoadOptions para mejorar la carga de documentos RTF con configuraciones personalizables para una integración perfecta en sus proyectos.
type: docs
weight: 4170
url: /es/net/aspose.words.loading/rtfloadoptions/
---
## RtfLoadOptions class

Permite especificar opciones adicionales al cargarRtf documento en un[`Document`](../../aspose.words/document/) objeto.

Para obtener más información, visite el[Especificar opciones de carga](https://docs.aspose.com/words/net/specify-load-options/) Artículo de documentación.

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
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Obtiene o establece la cadena que se utilizará para resolver los URI relativos encontrados en el documento en URI absolutos cuando sea necesario. Puede ser`nulo` o cadena vacía. El valor predeterminado es`nulo` . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Obtiene o establece si se debe convertir el metarchivo(Wmf oEmf ) imágenes aPngformato de imagen. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Obtiene o establece si se deben convertir formas con EquationXML en objetos de Office Math. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Obtiene o establece la codificación que se utilizará para cargar un documento HTML, TXT o CHM si no se especifica la codificación dentro del documento. Puede ser`nulo` El valor predeterminado es`nulo` . |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Permite especificar la configuración de fuentes del documento. |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | Especifica si se deben ignorar los datos OLE. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Obtiene las preferencias de idioma que se utilizarán cuando se cargue el documento. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Especifica el formato del documento que se va a cargar. El valor predeterminado esAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Permite especificar que el proceso de carga del documento debe coincidir con una versión específica de MS Word. El valor predeterminado esWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Obtiene o establece la contraseña para abrir un documento cifrado. Puede ser`nulo` o cadena vacía. El valor predeterminado es`nulo` . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Obtiene o establece si se debe conservar el campo INCLUDEPICTURE al leer formatos de Microsoft Word. El valor predeterminado es`FALSO` . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Se llama durante la carga de un documento y acepta datos sobre el progreso de la carga. |
| [RecognizeUtf8Text](../../aspose.words.loading/rtfloadoptions/recognizeutf8text/) { get; set; } | Cuando se establece en`verdadero` , intentará detectar caracteres UTF8, se conservarán durante la importación. |
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

Muestra cómo detectar caracteres UTF-8 al cargar un documento RTF.

```csharp
// Crea un objeto "RtfLoadOptions" para modificar la forma en que cargamos un documento RTF.
RtfLoadOptions loadOptions = new RtfLoadOptions();

// Establezca la propiedad "RecognizeUtf8Text" en "falso" para asumir que el documento utiliza el juego de caracteres ISO 8859-1
// y carga cada carácter en el documento.
// Establezca la propiedad "RecognizeUtf8Text" en "verdadero" para analizar cualquier carácter de longitud variable que pueda aparecer en el texto.
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
