---
title: "SdtDateStorageFormat"
linktitle: "SdtDateStorageFormat"
second_title: "Aspose.Words per Java"
description: "Specifica come la data per un SDT di tipo data viene memorizzata/recuperata quando l'SDT è associato a un nodo XML nell'archivio dati del documento in Java."
type: docs
weight: 601
url: /it/java/com.aspose.words/sdtdatestorageformat/
---

**Inheritance:**
java.lang.Object
```
public class SdtDateStorageFormat
```

Specifica come la data per un SDT di tipo data viene memorizzata/recuperata quando lo SDT è collegato a un nodo XML nell'archivio dati del documento.

 **Examples:** 

Mostra come richiedere all'utente di inserire una data con un tag di documento strutturato.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [DATE](#DATE) | Il valore della data per un SDT di tipo data è memorizzato come data nel formato standard XML Schema Date. |
| [DATE_TIME](#DATE-TIME) | Il valore della data per un SDT di tipo data è memorizzato come data nel formato standard XML Schema DateTime. |
| [DEFAULT](#DEFAULT) | Predefinito a [DATE\_TIME](../../com.aspose.words/sdtdatestorageformat/\#DATE-TIME) |
| [TEXT](#TEXT) | Il valore della data per un SDT di tipo data è memorizzato come testo. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String sdtDateStorageFormatName)](#fromName-java.lang.String) |  |
| [getName(int sdtDateStorageFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sdtDateStorageFormat)](#toString-int) |  |
### DATE {#DATE}
```
public static int DATE
```


Il valore della data per un SDT di tipo data è memorizzato come data nel formato standard XML Schema Date.

### DATE_TIME {#DATE-TIME}
```
public static int DATE_TIME
```


Il valore della data per un SDT di tipo data è memorizzato come data nel formato standard XML Schema DateTime.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Predefinito a [DATE\_TIME](../../com.aspose.words/sdtdatestorageformat/\#DATE-TIME)

### TEXT {#TEXT}
```
public static int TEXT
```


Il valore della data per un SDT di tipo data è memorizzato come testo.

### length {#length}
```
public static int length
```


### fromName(String sdtDateStorageFormatName) {#fromName-java.lang.String}
```
public static int fromName(String sdtDateStorageFormatName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sdtDateStorageFormatName | java.lang.String |  |

**Returns:**
int
### getName(int sdtDateStorageFormat) {#getName-int}
```
public static String getName(int sdtDateStorageFormat)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sdtDateStorageFormat | int |  |

**Returns:**
java.lang.String
