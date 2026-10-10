---
title: "SdtDateStorageFormat"
linktitle: "SdtDateStorageFormat"
second_title: "Aspose.Words para Java"
description: "Especifica cómo se almacena/recupera la fecha de un SDT de fecha cuando el SDT está vinculado a un nodo XML en el almacén de datos del documento en Java."
type: docs
weight: 601
url: /es/java/com.aspose.words/sdtdatestorageformat/
---

**Inheritance:**
java.lang.Object
```
public class SdtDateStorageFormat
```

Especifica cómo se almacena/recupera la fecha para un SDT de fecha cuando el SDT está vinculado a un nodo XML en el almacén de datos del documento.

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
| [DATE](#DATE) | El valor de fecha para un SDT de fecha se almacena como una fecha en el formato estándar de esquema XML Date. |
| [DATE_TIME](#DATE-TIME) | El valor de fecha para un SDT de fecha se almacena como una fecha en el formato estándar de esquema XML DateTime. |
| [DEFAULT](#DEFAULT) | Predeterminado a [DATE\_TIME](../../com.aspose.words/sdtdatestorageformat/\#DATE-TIME) |
| [TEXT](#TEXT) | El valor de fecha para un SDT de fecha se almacena como texto. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String sdtDateStorageFormatName)](#fromName-java.lang.String) |  |
| [getName(int sdtDateStorageFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sdtDateStorageFormat)](#toString-int) |  |
### DATE {#DATE}
```
public static int DATE
```


El valor de fecha para un SDT de fecha se almacena como una fecha en el formato estándar de esquema XML Date.

### DATE_TIME {#DATE-TIME}
```
public static int DATE_TIME
```


El valor de fecha para un SDT de fecha se almacena como una fecha en el formato estándar de esquema XML DateTime.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Predeterminado a [DATE\_TIME](../../com.aspose.words/sdtdatestorageformat/\#DATE-TIME)

### TEXT {#TEXT}
```
public static int TEXT
```


El valor de fecha para un SDT de fecha se almacena como texto.

### length {#length}
```
public static int length
```


### fromName(String sdtDateStorageFormatName) {#fromName-java.lang.String}
```
public static int fromName(String sdtDateStorageFormatName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| sdtDateStorageFormatName | java.lang.String |  |

**Returns:**
int
### getName(int sdtDateStorageFormat) {#getName-int}
```
public static String getName(int sdtDateStorageFormat)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| sdtDateStorageFormat | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int sdtDateStorageFormat) {#toString-int}
```
public static String toString(int sdtDateStorageFormat)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| sdtDateStorageFormat | int |  |

**Returns:**
java.lang.String
