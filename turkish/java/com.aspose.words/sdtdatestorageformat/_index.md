---
title: "SdtDateStorageFormat"
linktitle: "SdtDateStorageFormat"
second_title: "Aspose.Words Java için"
description: "Bir tarih SDT'sinin tarihinin, SDT bir XML düğümüne bağlandığında Java'daki belge veri deposunda nasıl saklandığını/geri alındığını belirtir."
type: docs
weight: 601
url: /tr/java/com.aspose.words/sdtdatestorageformat/
---

**Inheritance:**
java.lang.Object
```
public class SdtDateStorageFormat
```

SDT bir belgenin veri deposundaki bir XML düğümüne bağlandığında tarih SDT'sinin tarihinin nasıl saklandığını/geri alındığını belirtir.

 **Examples:** 

Kullanıcıyı yapılandırılmış belge etiketiyle bir tarih girmeye istemeyi gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [DATE](#DATE) | Bir tarih SDT'sinin tarih değeri, standart XML Şema Tarih formatında tarih olarak saklanır. |
| [DATE_TIME](#DATE-TIME) | Bir tarih SDT'sinin tarih değeri, standart XML Şema TarihSaat formatında tarih olarak saklanır. |
| [DEFAULT](#DEFAULT) | Varsayılan olarak [DATE\\_TIME](../../com.aspose.words/sdtdatestorageformat/\\#DATE-TIME) |
| [TEXT](#TEXT) | Bir tarih SDT'sinin tarih değeri metin olarak saklanır. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String sdtDateStorageFormatName)](#fromName-java.lang.String) |  |
| [getName(int sdtDateStorageFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sdtDateStorageFormat)](#toString-int) |  |
### DATE {#DATE}
```
public static int DATE
```


Bir tarih SDT'sinin tarih değeri, standart XML Şema Tarih formatında tarih olarak saklanır.

### DATE_TIME {#DATE-TIME}
```
public static int DATE_TIME
```


Bir tarih SDT'sinin tarih değeri, standart XML Şema TarihSaat formatında tarih olarak saklanır.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Varsayılan olarak [DATE\\_TIME](../../com.aspose.words/sdtdatestorageformat/\\#DATE-TIME)

### TEXT {#TEXT}
```
public static int TEXT
```


Bir tarih SDT'sinin tarih değeri metin olarak saklanır.

### length {#length}
```
public static int length
```


### fromName(String sdtDateStorageFormatName) {#fromName-java.lang.String}
```
public static int fromName(String sdtDateStorageFormatName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sdtDateStorageFormatName | java.lang.String |  |

**Returns:**
int
### getName(int sdtDateStorageFormat) {#getName-int}
```
public static String getName(int sdtDateStorageFormat)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sdtDateStorageFormat | int |  |

**Returns:**
java.lang.String
