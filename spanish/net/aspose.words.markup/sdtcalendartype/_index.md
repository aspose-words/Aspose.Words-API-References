---
title: SdtCalendarType Enum
linktitle: SdtCalendarType
articleTitle: SdtCalendarType
second_title: Aspose.Words para .NET
description: Explore la enumeración Aspose.Words.Markup.SdtCalendarType para mejorar sus documentos Office Open XML con opciones de calendario versátiles para una mejor eficiencia del flujo de trabajo.
type: docs
weight: 4690
url: /es/net/aspose.words.markup/sdtcalendartype/
---
## SdtCalendarType enumeration

Especifica los posibles tipos de calendarios que se pueden utilizar para especificar[`CalendarType`](../structureddocumenttag/calendartype/) en un documento Office Open XML.

```csharp
public enum SdtCalendarType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Default | `0` | Se usa como valor predeterminado en OOXML. Es igual aGregorian . |
| Gregorian | `0` | Especifica que se utilizará el calendario gregoriano, tal como se define en la norma ISO 8601. Este calendario debe estar localizado en el idioma apropiado. |
| GregorianArabic | `1` | Especifica que se utilizará el calendario gregoriano, tal como se define en ISO 8601. Los valores de este calendario deben presentarse en árabe. |
| GregorianMeFrench | `2` | Especifica que se utilizará el calendario gregoriano, tal como se define en la norma ISO 8601. Los valores de este calendario deben presentarse en francés de Oriente Medio. |
| GregorianUs | `3` | Especifica que se utilizará el calendario gregoriano, tal como se define en ISO 8601. Los valores de este calendario deben presentarse en inglés. |
| GregorianXlitEnglish | `4` | Especifica que se debe utilizar el calendario gregoriano, tal como se define en ISO 8601. Los valores para este calendario deben ser la representación de las cadenas en inglés en los caracteres árabes correspondientes (la transliteración árabe del inglés para el calendario gregoriano). |
| GregorianXlitFrench | `5` | Especifica que se debe utilizar el calendario gregoriano, tal como se define en ISO 8601. Los valores para este calendario deben ser la representación de las cadenas francesas en los caracteres árabes correspondientes (la transliteración árabe del francés para el calendario gregoriano). |
| Hebrew | `6` | Especifica que se utilizará el calendario lunar hebreo, tal como se describe en la fórmula de Gauss para la Pascua [CITA] y La Redeclaración Completa de la Ley Oral (Mishneh Torá). |
| Hijri | `7` | Especifica que se utilizará el calendario lunar Hijri, según lo descrito por el Reino de Arabia Saudita, Ministerio de Asuntos Islámicos, Dotaciones, Da'wah y Orientación. |
| Japan | `8` | Especifica que se utilizará el calendario de la era del emperador japonés, tal como se describe en la norma industrial japonesa JIS X 0301. |
| Korea | `9` | Especifica que se utilizará el calendario coreano de la era Tangun, tal como se describe en la Ley Coreana N.° 4. |
| None | `10` | Especifica que no se debe utilizar ningún calendario. |
| Saka | `11` | Especifica que se utilizará el calendario de la Era Saka, tal como lo describe el Comité de Reforma del Calendario de la India, como parte de las Efemérides de la India y el Almanaque Náutico. |
| Taiwan | `12` | Especifica que se utilizará el calendario taiwanés, según lo define la Norma Nacional China CNS 7648. |
| Thai | `13` | Especifica que se utilizará el calendario tailandés, tal como lo define el Decreto Real de Su Majestad el Rey Vajiravudh (Rama VI) en la Gaceta Real BE 2456 (1913 d. C.) y por el decreto del Primer Ministro Phibunsongkhram (1941 d. C.) para comenzar el año el 1 de enero gregoriano y asignar el año cero al año gregoriano 543 a. C. |

## Ejemplos

Muestra cómo solicitar al usuario que ingrese una fecha con una etiqueta de documento estructurado.

```csharp
Document doc = new Document();

// Inserte una etiqueta de documento estructurado que solicite al usuario que ingrese una fecha.
// En Microsoft Word, este elemento se conoce como "control de contenido del selector de fecha".
// Cuando hacemos clic en la flecha en el extremo derecho de esta etiqueta en Microsoft Word,
//Veremos una ventana emergente en forma de calendario en el que podemos hacer clic.
//Podemos usar esa ventana emergente para seleccionar una fecha que se mostrará en la etiqueta.
StructuredDocumentTag sdtDate = new StructuredDocumentTag(doc, SdtType.Date, MarkupLevel.Inline);

// Muestra la fecha, según la configuración regional del árabe de Arabia Saudita.
sdtDate.DateDisplayLocale = CultureInfo.GetCultureInfo("ar-SA").LCID;

// Establezca el formato con el que se mostrará la fecha.
sdtDate.DateDisplayFormat = "dd MMMM, yyyy";
sdtDate.DateStorageFormat = SdtDateStorageFormat.DateTime;

// Muestra la fecha según el calendario Hijri.
sdtDate.CalendarType = SdtCalendarType.Hijri;

// Antes de que el usuario elija una fecha en Microsoft Word, la etiqueta mostrará el texto "Haga clic aquí para ingresar una fecha".
// Según el calendario de la etiqueta, configure la propiedad "FullDate" para que la etiqueta muestre una fecha predeterminada.
sdtDate.FullDate = new DateTime(1440, 10, 20);

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(sdtDate);

doc.Save(ArtifactsDir + "StructuredDocumentTag.Date.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Markup](../../aspose.words.markup/)
* asamblea [Aspose.Words](../../)
