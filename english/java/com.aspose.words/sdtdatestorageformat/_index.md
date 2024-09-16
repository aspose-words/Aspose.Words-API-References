---
title: SdtDateStorageFormat
linktitle: SdtDateStorageFormat
second_title: Aspose.Words for Java
description: Specifies how the date for a date SDT is stored/retrieved when the SDT is bound to an XML node in the documents data store in Java.
type: docs
weight: 560
url: /java/com.aspose.words/sdtdatestorageformat/
---

**Inheritance:**
java.lang.Object
```
public class SdtDateStorageFormat
```

Specifies how the date for a date SDT is stored/retrieved when the SDT is bound to an XML node in the document's data store.

 **Examples:** 

Shows how to prompt the user to enter a date with a structured document tag.

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
## Fields

| Field | Description |
| --- | --- |
| [DATE](#DATE) | The date value for a date SDT is stored as a date in the standard XML Schema Date format. |
| [DATE_TIME](#DATE-TIME) | The date value for a date SDT is stored as a date in the standard XML Schema DateTime format. |
| [DEFAULT](#DEFAULT) | Defaults to [DATE\_TIME](../../com.aspose.words/sdtdatestorageformat/\#DATE-TIME) |
| [TEXT](#TEXT) | The date value for a date SDT is stored as text. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String sdtDateStorageFormatName)](#fromName-java.lang.String) |  |
| [getName(int sdtDateStorageFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sdtDateStorageFormat)](#toString-int) |  |
### DATE {#DATE}
```
public static int DATE
```


The date value for a date SDT is stored as a date in the standard XML Schema Date format.

### DATE_TIME {#DATE-TIME}
```
public static int DATE_TIME
```


The date value for a date SDT is stored as a date in the standard XML Schema DateTime format.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Defaults to [DATE\_TIME](../../com.aspose.words/sdtdatestorageformat/\#DATE-TIME)

### TEXT {#TEXT}
```
public static int TEXT
```


The date value for a date SDT is stored as text.

### length {#length}
```
public static int length
```


### fromName(String sdtDateStorageFormatName) {#fromName-java.lang.String}
```
public static int fromName(String sdtDateStorageFormatName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sdtDateStorageFormatName | java.lang.String |  |

**Returns:**
int
### getName(int sdtDateStorageFormat) {#getName-int}
```
public static String getName(int sdtDateStorageFormat)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| sdtDateStorageFormat | int |  |

**Returns:**
java.lang.String
