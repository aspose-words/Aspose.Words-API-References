---
title: SdtCalendarType
linktitle: SdtCalendarType
second_title: Aspose.Words for Java
description: Specifies the possible types of calendars which can be used to specify StructuredDocumentTag.getCalendarType / StructuredDocumentTag.setCalendarTypeint in an Office Open XML document in Java.
type: docs
weight: 580
url: /java/com.aspose.words/sdtcalendartype/
---

**Inheritance:**
java.lang.Object
```
public class SdtCalendarType
```

Specifies the possible types of calendars which can be used to specify [StructuredDocumentTag.getCalendarType()](../../com.aspose.words/structureddocumenttag/\#getCalendarType) / [StructuredDocumentTag.setCalendarType(int)](../../com.aspose.words/structureddocumenttag/\#setCalendarType-int) in an Office Open XML document.

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
| [DEFAULT](#DEFAULT) | Used as default value in OOXML. |
| [GREGORIAN](#GREGORIAN) | Specifies that the Gregorian calendar, as defined in ISO 8601, shall be used. |
| [GREGORIAN_ARABIC](#GREGORIAN-ARABIC) | Specifies that the Gregorian calendar, as defined in ISO 8601, shall be used. |
| [GREGORIAN_ME_FRENCH](#GREGORIAN-ME-FRENCH) | Specifies that the Gregorian calendar, as defined in ISO 8601, shall be used. |
| [GREGORIAN_US](#GREGORIAN-US) | Specifies that the Gregorian calendar, as defined in ISO 8601, shall be used. |
| [GREGORIAN_XLIT_ENGLISH](#GREGORIAN-XLIT-ENGLISH) | Specifies that the Gregorian calendar, as defined in ISO 8601, shall be used. |
| [GREGORIAN_XLIT_FRENCH](#GREGORIAN-XLIT-FRENCH) | Specifies that the Gregorian calendar, as defined in ISO 8601, shall be used. |
| [HEBREW](#HEBREW) | Specifies that the Hebrew lunar calendar, as described by the Gauss formula for Passover [CITATION] and The Complete Restatement of Oral Law (Mishneh Torah),shall be used. |
| [HIJRI](#HIJRI) | Specifies that the Hijri lunar calendar, as described by the Kingdom of Saudi Arabia, Ministry of Islamic Affairs, Endowments, Da\\u2018wah and Guidance, shall be used. |
| [JAPAN](#JAPAN) | Specifies that the Japanese Emperor Era calendar, as described by Japanese Industrial Standard JIS X 0301, shall be used. |
| [KOREA](#KOREA) | Specifies that the Korean Tangun Era calendar, as described by Korean Law Enactment No. |
| [NONE](#NONE) | Specifies that no calendar should be used. |
| [SAKA](#SAKA) | Specifies that the Saka Era calendar, as described by the Calendar Reform Committee of India, as part of the Indian Ephemeris and Nautical Almanac, shall be used. |
| [TAIWAN](#TAIWAN) | Specifies that the Taiwanese calendar, as defined by the Chinese National Standard CNS 7648, shall be used. |
| [THAI](#THAI) | Specifies that the Thai calendar, as defined by the Royal Decree of H.M. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String sdtCalendarTypeName)](#fromName-java.lang.String) |  |
| [getName(int sdtCalendarType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sdtCalendarType)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Used as default value in OOXML. Equals [GREGORIAN](../../com.aspose.words/sdtcalendartype/\#GREGORIAN).

### GREGORIAN {#GREGORIAN}
```
public static int GREGORIAN
```


Specifies that the Gregorian calendar, as defined in ISO 8601, shall be used. This calendar should be localized into the appropriate language.

### GREGORIAN_ARABIC {#GREGORIAN-ARABIC}
```
public static int GREGORIAN_ARABIC
```


Specifies that the Gregorian calendar, as defined in ISO 8601, shall be used. The values for this calendar should be presented in Arabic.

### GREGORIAN_ME_FRENCH {#GREGORIAN-ME-FRENCH}
```
public static int GREGORIAN_ME_FRENCH
```


Specifies that the Gregorian calendar, as defined in ISO 8601, shall be used. The values for this calendar should be presented in Middle East French.

### GREGORIAN_US {#GREGORIAN-US}
```
public static int GREGORIAN_US
```


Specifies that the Gregorian calendar, as defined in ISO 8601, shall be used. The values for this calendar should be presented in English.

### GREGORIAN_XLIT_ENGLISH {#GREGORIAN-XLIT-ENGLISH}
```
public static int GREGORIAN_XLIT_ENGLISH
```


Specifies that the Gregorian calendar, as defined in ISO 8601, shall be used. The values for this calendar should be the representation of the English strings in the corresponding Arabic characters (the Arabic transliteration of the English for the Gregorian calendar).

### GREGORIAN_XLIT_FRENCH {#GREGORIAN-XLIT-FRENCH}
```
public static int GREGORIAN_XLIT_FRENCH
```


Specifies that the Gregorian calendar, as defined in ISO 8601, shall be used. The values for this calendar should be the representation of the French strings in the corresponding Arabic characters (the Arabic transliteration of the French for the Gregorian calendar).

### HEBREW {#HEBREW}
```
public static int HEBREW
```


Specifies that the Hebrew lunar calendar, as described by the Gauss formula for Passover [CITATION] and The Complete Restatement of Oral Law (Mishneh Torah),shall be used.

### HIJRI {#HIJRI}
```
public static int HIJRI
```


Specifies that the Hijri lunar calendar, as described by the Kingdom of Saudi Arabia, Ministry of Islamic Affairs, Endowments, Da\\u2018wah and Guidance, shall be used.

### JAPAN {#JAPAN}
```
public static int JAPAN
```


Specifies that the Japanese Emperor Era calendar, as described by Japanese Industrial Standard JIS X 0301, shall be used.

### KOREA {#KOREA}
```
public static int KOREA
```


Specifies that the Korean Tangun Era calendar, as described by Korean Law Enactment No. 4, shall be used.

### NONE {#NONE}
```
public static int NONE
```


Specifies that no calendar should be used.

 **Remarks:** 

Usually in AW, None is the first and default value for enums, but not in this case. None is not default for OOXML, instead [GREGORIAN](../../com.aspose.words/sdtcalendartype/\#GREGORIAN) is default and is first member of this enum.

### SAKA {#SAKA}
```
public static int SAKA
```


Specifies that the Saka Era calendar, as described by the Calendar Reform Committee of India, as part of the Indian Ephemeris and Nautical Almanac, shall be used.

### TAIWAN {#TAIWAN}
```
public static int TAIWAN
```


Specifies that the Taiwanese calendar, as defined by the Chinese National Standard CNS 7648, shall be used.

### THAI {#THAI}
```
public static int THAI
```


Specifies that the Thai calendar, as defined by the Royal Decree of H.M. King Vajiravudh (Rama VI) in Royal Gazette B. E. 2456 (1913 A.D.) and by the decree of Prime Minister Phibunsongkhram (1941 A.D.) to start the year on the Gregorian January 1 and to map year zero to Gregorian year 543 B.C., shall be used.

### length {#length}
```
public static int length
```


### fromName(String sdtCalendarTypeName) {#fromName-java.lang.String}
```
public static int fromName(String sdtCalendarTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sdtCalendarTypeName | java.lang.String |  |

**Returns:**
int
### getName(int sdtCalendarType) {#getName-int}
```
public static String getName(int sdtCalendarType)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| sdtCalendarType | int |  |

**Returns:**
java.lang.String
