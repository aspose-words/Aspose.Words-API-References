---
title: SdtCalendarType
second_title: Aspose.Words for Java API Reference
description: Specifies the possible types of calendars which can be used to specify  /  in an Office Open XML document.
type: docs
weight: 508
url: /java/com.aspose.words/sdtcalendartype/
---

**Inheritance:**
java.lang.Object
```
public class SdtCalendarType
```

Specifies the possible types of calendars which can be used to specify [StructuredDocumentTag.getCalendarType()](../../com.aspose.words/structureddocumenttag\#getCalendarType) / [StructuredDocumentTag.setCalendarType(int)](../../com.aspose.words/structureddocumenttag\#setCalendarType-int) in an Office Open XML document.
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
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String sdtCalendarTypeName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int sdtCalendarType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int sdtCalendarType)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Used as default value in OOXML. Equals [GREGORIAN](../../com.aspose.words/sdtcalendartype\#GREGORIAN).

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


Specifies that no calendar should be used. Usually in AW, None is the first and default value for enums, but not in this case. None is not default for OOXML, instead [GREGORIAN](../../com.aspose.words/sdtcalendartype\#GREGORIAN) is default and is first member of this enum.

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


### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
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
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
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
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
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
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

