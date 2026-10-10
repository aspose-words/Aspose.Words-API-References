---
title: "SdtDateStorageFormat"
linktitle: "SdtDateStorageFormat"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie das Datum für ein date SDT gespeichert/abgerufen wird, wenn das SDT an einen XML‑Knoten im Dokumentdaten‑Store in Java gebunden ist."
type: docs
weight: 601
url: /de/java/com.aspose.words/sdtdatestorageformat/
---

**Inheritance:**
java.lang.Object
```
public class SdtDateStorageFormat
```

Gibt an, wie das Datum für ein Datums‑SDT gespeichert/abgerufen wird, wenn das SDT an einen XML‑Knoten im Datenspeicher des Dokuments gebunden ist.

 **Examples:** 

Zeigt, wie der Benutzer aufgefordert wird, ein Datum mit einem strukturierten Dokument-Tag einzugeben.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [DATE](#DATE) | Der Datumswert für ein date SDT wird als Datum im Standard‑XML‑Schema‑Date‑Format gespeichert. |
| [DATE_TIME](#DATE-TIME) | Der Datumswert für ein date SDT wird als Datum im Standard‑XML‑Schema‑DateTime‑Format gespeichert. |
| [DEFAULT](#DEFAULT) | Standardmäßig auf [DATE\_TIME](../../com.aspose.words/sdtdatestorageformat/\#DATE-TIME) |
| [TEXT](#TEXT) | Der Datumswert für ein date SDT wird als Text gespeichert. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String sdtDateStorageFormatName)](#fromName-java.lang.String) |  |
| [getName(int sdtDateStorageFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sdtDateStorageFormat)](#toString-int) |  |
### DATE {#DATE}
```
public static int DATE
```


Der Datumswert für ein date SDT wird als Datum im Standard‑XML‑Schema‑Date‑Format gespeichert.

### DATE_TIME {#DATE-TIME}
```
public static int DATE_TIME
```


Der Datumswert für ein date SDT wird als Datum im Standard‑XML‑Schema‑DateTime‑Format gespeichert.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Standardmäßig auf [DATE\_TIME](../../com.aspose.words/sdtdatestorageformat/\#DATE-TIME)

### TEXT {#TEXT}
```
public static int TEXT
```


Der Datumswert für ein date SDT wird als Text gespeichert.

### length {#length}
```
public static int length
```


### fromName(String sdtDateStorageFormatName) {#fromName-java.lang.String}
```
public static int fromName(String sdtDateStorageFormatName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sdtDateStorageFormatName | java.lang.String |  |

**Returns:**
int
### getName(int sdtDateStorageFormat) {#getName-int}
```
public static String getName(int sdtDateStorageFormat)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sdtDateStorageFormat | int |  |

**Returns:**
java.lang.String
