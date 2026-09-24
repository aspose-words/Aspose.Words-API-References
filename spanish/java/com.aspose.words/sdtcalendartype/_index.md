---
title: "SdtCalendarType"
linktitle: "SdtCalendarType"
second_title: "Aspose.Words para Java"
description: "Especifica los tipos posibles de calendarios que pueden usarse para especificar StructuredDocumentTag.getCalendarType / StructuredDocumentTag.setCalendarTypeint en un documento Office Open XML en Java."
type: docs
weight: 600
url: /es/java/com.aspose.words/sdtcalendartype/
---

**Inheritance:**
java.lang.Object
```
public class SdtCalendarType
```

Especifica los tipos posibles de calendarios que pueden usarse para especificar [StructuredDocumentTag.getCalendarType()](../../com.aspose.words/structureddocumenttag/\#getCalendarType) / [StructuredDocumentTag.setCalendarType(int)](../../com.aspose.words/structureddocumenttag/\#setCalendarType-int) en un documento Office Open XML.

 **Examples:** 

Muestra cómo solicitar al usuario que introduzca una fecha con una etiqueta de documento estructurado.

```

 Document doc = new Document();

 // Insert a structured document tag that prompts the user to enter a date.
 // In Microsoft Word, this element is known as a "Date picker content control".
 // When we click on the arrow on the right end of this tag in Microsoft Word,
 // we will see a pop up in the form of a clickable calendar.
 // We can use that popup to select a date that the tag will display.
 StructuredDocumentTag sdtDate = new StructuredDocumentTag(doc, SdtType.DATE, MarkupLevel.INLINE);

 // Display the date, according to the Saudi Arabian Arabic locale.
 sdtDate.setDateDisplayLocale(1025);

 // Set the format with which to display the date.
 sdtDate.setDateDisplayFormat("dd MMMM, yyyy");
 sdtDate.setDateStorageFormat(SdtDateStorageFormat.DATE_TIME);

 // Display the date according to the Hijri calendar.
 sdtDate.setCalendarType(SdtCalendarType.HIJRI);

 // Before the user chooses a date in Microsoft Word, the tag will display the text "Click here to enter a date.".
 // According to the tag's calendar, set the "FullDate" property to get the tag to display a default date.
 Calendar cal = Calendar.getInstance();
 cal.set(1440, 10, 20);
 sdtDate.setFullDate(cal.getTime());

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertNode(sdtDate);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.Date.docx");
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [DEFAULT](#DEFAULT) | Usado como valor predeterminado en OOXML. |
| [GREGORIAN](#GREGORIAN) | Especifica que se debe usar el calendario gregoriano, tal como se define en ISO 8601. |
| [GREGORIAN_ARABIC](#GREGORIAN-ARABIC) | Especifica que se debe usar el calendario gregoriano, tal como se define en ISO 8601. |
| [GREGORIAN_ME_FRENCH](#GREGORIAN-ME-FRENCH) | Especifica que se debe usar el calendario gregoriano, tal como se define en ISO 8601. |
| [GREGORIAN_US](#GREGORIAN-US) | Especifica que se debe usar el calendario gregoriano, tal como se define en ISO 8601. |
| [GREGORIAN_XLIT_ENGLISH](#GREGORIAN-XLIT-ENGLISH) | Especifica que se debe usar el calendario gregoriano, tal como se define en ISO 8601. |
| [GREGORIAN_XLIT_FRENCH](#GREGORIAN-XLIT-FRENCH) | Especifica que se debe usar el calendario gregoriano, tal como se define en ISO 8601. |
| [HEBREW](#HEBREW) | Especifica que se debe usar el calendario lunar hebreo, según la fórmula de Gauss para la Pascua [CITATION] y The Complete Restatement of Oral Law (Mishneh Torah). |
| [HIJRI](#HIJRI) | Especifica que se debe usar el calendario lunar hijri, según el Reino de Arabia Saudita, Ministerio de Asuntos Islámicos, Endowments, Da‘wah y Guidance. |
| [JAPAN](#JAPAN) | Especifica que se debe usar el calendario de la era del emperador japonés, según la Norma Industrial Japonesa JIS X 0301. |
| [KOREA](#KOREA) | Especifica que se debe usar el calendario de la era Tangun coreana, según la Ley Coreana No. |
| [NONE](#NONE) | Especifica que no se debe usar ningún calendario. |
| [SAKA](#SAKA) | Especifica que se debe usar el calendario de la era Saka, según el Comité de Reforma del Calendario de la India, como parte del Efemérides y Almanaque Náutico de la India. |
| [TAIWAN](#TAIWAN) | Especifica que se debe usar el calendario taiwanés, según la Norma Nacional China CNS 7648. |
| [THAI](#THAI) | Especifica que se debe usar el calendario tailandés, según el Decreto Real de Su Majestad. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String sdtCalendarTypeName)](#fromName-java.lang.String) |  |
| [getName(int sdtCalendarType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sdtCalendarType)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Usado como valor predeterminado en OOXML. Equivale a [GREGORIAN](../../com.aspose.words/sdtcalendartype/\#GREGORIAN).

### GREGORIAN {#GREGORIAN}
```
public static int GREGORIAN
```


Especifica que se debe usar el calendario gregoriano, tal como se define en ISO 8601. Este calendario debe localizarse al idioma apropiado.

### GREGORIAN_ARABIC {#GREGORIAN-ARABIC}
```
public static int GREGORIAN_ARABIC
```


Especifica que se debe usar el calendario gregoriano, tal como se define en ISO 8601. Los valores de este calendario deben presentarse en árabe.

### GREGORIAN_ME_FRENCH {#GREGORIAN-ME-FRENCH}
```
public static int GREGORIAN_ME_FRENCH
```


Especifica que se debe usar el calendario gregoriano, tal como se define en ISO 8601. Los valores de este calendario deben presentarse en francés del Oriente Medio.

### GREGORIAN_US {#GREGORIAN-US}
```
public static int GREGORIAN_US
```


Especifica que se debe usar el calendario gregoriano, tal como se define en ISO 8601. Los valores de este calendario deben presentarse en inglés.

### GREGORIAN_XLIT_ENGLISH {#GREGORIAN-XLIT-ENGLISH}
```
public static int GREGORIAN_XLIT_ENGLISH
```


Especifica que se debe usar el calendario gregoriano, tal como se define en ISO 8601. Los valores de este calendario deben ser la representación de las cadenas en inglés con los caracteres árabes correspondientes (la transliteración al árabe del inglés para el calendario gregoriano).

### GREGORIAN_XLIT_FRENCH {#GREGORIAN-XLIT-FRENCH}
```
public static int GREGORIAN_XLIT_FRENCH
```


Especifica que se debe usar el calendario gregoriano, tal como se define en ISO 8601. Los valores de este calendario deben ser la representación de las cadenas en francés con los caracteres árabes correspondientes (la transliteración al árabe del francés para el calendario gregoriano).

### HEBREW {#HEBREW}
```
public static int HEBREW
```


Especifica que se debe usar el calendario lunar hebreo, según la fórmula de Gauss para la Pascua [CITATION] y The Complete Restatement of Oral Law (Mishneh Torah).

### HIJRI {#HIJRI}
```
public static int HIJRI
```


Especifica que se debe usar el calendario lunar hijri, según el Reino de Arabia Saudita, Ministerio de Asuntos Islámicos, Endowments, Da‘wah y Guidance.

### JAPAN {#JAPAN}
```
public static int JAPAN
```


Especifica que se debe usar el calendario de la era del emperador japonés, según la Norma Industrial Japonesa JIS X 0301.

### KOREA {#KOREA}
```
public static int KOREA
```


Especifica que se debe usar el calendario de la era Tangun coreana, según la Ley Coreana No. 4.

### NONE {#NONE}
```
public static int NONE
```


Especifica que no se debe usar ningún calendario.

 **Remarks:** 

Normalmente en AW, None es el primer valor predeterminado para los enumerados, pero no en este caso. None no es el predeterminado para OOXML, en su lugar [GREGORIAN](../../com.aspose.words/sdtcalendartype/\#GREGORIAN) es el predeterminado y es el primer miembro de este enumerado.

### SAKA {#SAKA}
```
public static int SAKA
```


Especifica que se debe usar el calendario de la era Saka, según el Comité de Reforma del Calendario de la India, como parte del Efemérides y Almanaque Náutico de la India.

### TAIWAN {#TAIWAN}
```
public static int TAIWAN
```


Especifica que se debe usar el calendario taiwanés, según la Norma Nacional China CNS 7648.

### THAI {#THAI}
```
public static int THAI
```


Especifica que se debe usar el calendario tailandés, según el Decreto Real de Su Majestad el Rey Vajiravudh (Rama VI) en la Gaceta Real B. E. 2456 (1913 d.C.) y por el decreto del Primer Ministro Phibunsongkhram (1941 d.C.) para iniciar el año el 1 de enero del calendario gregoriano y mapear el año cero al año gregoriano 543 a.C.

### length {#length}
```
public static int length
```


### fromName(String sdtCalendarTypeName) {#fromName-java.lang.String}
```
public static int fromName(String sdtCalendarTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| sdtCalendarTypeName | java.lang.String |  |

**Returns:**
int
### getName(int sdtCalendarType) {#getName-int}
```
public static String getName(int sdtCalendarType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| sdtCalendarType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int sdtCalendarType) {#toString-int}
```
public static String toString(int sdtCalendarType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| sdtCalendarType | int |  |

**Returns:**
java.lang.String
