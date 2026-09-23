---
title: "SdtCalendarType"
linktitle: "SdtCalendarType"
second_title: "Aspose.Words für Java"
description: "Gibt die möglichen Kalendertypen an, die verwendet werden können, um StructuredDocumentTag.getCalendarType / StructuredDocumentTag.setCalendarTypeint in einem Office Open XML‑Dokument in Java zu spezifizieren."
type: docs
weight: 600
url: /de/java/com.aspose.words/sdtcalendartype/
---

**Inheritance:**
java.lang.Object
```
public class SdtCalendarType
```

Gibt die möglichen Kalendertypen an, die verwendet werden können, um [StructuredDocumentTag.getCalendarType()](../../com.aspose.words/structureddocumenttag/\#getCalendarType) / [StructuredDocumentTag.setCalendarType(int)](../../com.aspose.words/structureddocumenttag/\#setCalendarType-int) in einem Office Open XML‑Dokument zu spezifizieren.

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
| [DEFAULT](#DEFAULT) | Wird als Standardwert in OOXML verwendet. |
| [GREGORIAN](#GREGORIAN) | Gibt an, dass der gregorianische Kalender, wie in ISO 8601 definiert, verwendet werden soll. |
| [GREGORIAN_ARABIC](#GREGORIAN-ARABIC) | Gibt an, dass der gregorianische Kalender, wie in ISO 8601 definiert, verwendet werden soll. |
| [GREGORIAN_ME_FRENCH](#GREGORIAN-ME-FRENCH) | Gibt an, dass der gregorianische Kalender, wie in ISO 8601 definiert, verwendet werden soll. |
| [GREGORIAN_US](#GREGORIAN-US) | Gibt an, dass der gregorianische Kalender, wie in ISO 8601 definiert, verwendet werden soll. |
| [GREGORIAN_XLIT_ENGLISH](#GREGORIAN-XLIT-ENGLISH) | Gibt an, dass der gregorianische Kalender, wie in ISO 8601 definiert, verwendet werden soll. |
| [GREGORIAN_XLIT_FRENCH](#GREGORIAN-XLIT-FRENCH) | Gibt an, dass der gregorianische Kalender, wie in ISO 8601 definiert, verwendet werden soll. |
| [HEBREW](#HEBREW) | Gibt an, dass der hebräische Mondkalender, wie beschrieben durch die Gaußsche Formel für das Passah [CITATION] und die vollständige Wiederholung des mündlichen Rechts (Mishneh Torah), verwendet werden soll. |
| [HIJRI](#HIJRI) | Gibt an, dass der hijri Mondkalender, wie beschrieben vom Königreich Saudi-Arabien, Ministerium für Islamische Angelegenheiten, Stiftungen, Da\\u2018wah und Führung, verwendet werden soll. |
| [JAPAN](#JAPAN) | Gibt an, dass der japanische Kaiserzeit-Kalender, wie beschrieben durch den Japanischen Industrie-Standard JIS X 0301, verwendet werden soll. |
| [KOREA](#KOREA) | Gibt an, dass der koreanische Tangun-Ära-Kalender, wie beschrieben durch das koreanische Gesetzesdekret Nr., verwendet werden soll. |
| [NONE](#NONE) | Gibt an, dass kein Kalender verwendet werden soll. |
| [SAKA](#SAKA) | Gibt an, dass der Saka-Ära-Kalender, wie beschrieben durch das Kalenderreformkomitee Indiens, als Teil des indischen Ephemeriden- und Nautikalmanachs, verwendet werden soll. |
| [TAIWAN](#TAIWAN) | Gibt an, dass der taiwanesische Kalender, wie definiert durch den chinesischen Nationalstandard CNS 7648, verwendet werden soll. |
| [THAI](#THAI) | Gibt an, dass der thailändische Kalender, wie definiert durch das königliche Dekret von H.M., verwendet werden soll. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String sdtCalendarTypeName)](#fromName-java.lang.String) |  |
| [getName(int sdtCalendarType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sdtCalendarType)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Wird als Standardwert in OOXML verwendet. Entspricht [GREGORIAN](../../com.aspose.words/sdtcalendartype/#GREGORIAN).

### GREGORIAN {#GREGORIAN}
```
public static int GREGORIAN
```


Gibt an, dass der gregorianische Kalender, wie definiert in ISO 8601, verwendet werden soll. Dieser Kalender sollte in die entsprechende Sprache lokalisiert werden.

### GREGORIAN_ARABIC {#GREGORIAN-ARABIC}
```
public static int GREGORIAN_ARABIC
```


Gibt an, dass der gregorianische Kalender, wie definiert in ISO 8601, verwendet werden soll. Die Werte für diesen Kalender sollten in Arabisch dargestellt werden.

### GREGORIAN_ME_FRENCH {#GREGORIAN-ME-FRENCH}
```
public static int GREGORIAN_ME_FRENCH
```


Gibt an, dass der gregorianische Kalender, wie definiert in ISO 8601, verwendet werden soll. Die Werte für diesen Kalender sollten in französisch für den Nahen Osten dargestellt werden.

### GREGORIAN_US {#GREGORIAN-US}
```
public static int GREGORIAN_US
```


Gibt an, dass der gregorianische Kalender, wie definiert in ISO 8601, verwendet werden soll. Die Werte für diesen Kalender sollten in Englisch dargestellt werden.

### GREGORIAN_XLIT_ENGLISH {#GREGORIAN-XLIT-ENGLISH}
```
public static int GREGORIAN_XLIT_ENGLISH
```


Gibt an, dass der gregorianische Kalender, wie definiert in ISO 8601, verwendet werden soll. Die Werte für diesen Kalender sollten die Darstellung der englischen Zeichenketten in den entsprechenden arabischen Zeichen sein (die arabische Transliteration des Englischen für den gregorianischen Kalender).

### GREGORIAN_XLIT_FRENCH {#GREGORIAN-XLIT-FRENCH}
```
public static int GREGORIAN_XLIT_FRENCH
```


Gibt an, dass der gregorianische Kalender, wie definiert in ISO 8601, verwendet werden soll. Die Werte für diesen Kalender sollten die Darstellung der französischen Zeichenketten in den entsprechenden arabischen Zeichen sein (die arabische Transliteration des Französischen für den gregorianischen Kalender).

### HEBREW {#HEBREW}
```
public static int HEBREW
```


Gibt an, dass der hebräische Mondkalender, wie beschrieben durch die Gaußsche Formel für das Passah [CITATION] und die vollständige Wiederholung des mündlichen Rechts (Mishneh Torah), verwendet werden soll.

### HIJRI {#HIJRI}
```
public static int HIJRI
```


Gibt an, dass der hijri Mondkalender, wie beschrieben vom Königreich Saudi-Arabien, Ministerium für Islamische Angelegenheiten, Stiftungen, Da\\u2018wah und Führung, verwendet werden soll.

### JAPAN {#JAPAN}
```
public static int JAPAN
```


Gibt an, dass der japanische Kaiserzeit-Kalender, wie beschrieben durch den Japanischen Industrie-Standard JIS X 0301, verwendet werden soll.

### KOREA {#KOREA}
```
public static int KOREA
```


Gibt an, dass der koreanische Tangun-Ära-Kalender, wie beschrieben durch das koreanische Gesetzesdekret Nr. 4, verwendet werden soll.

### NONE {#NONE}
```
public static int NONE
```


Gibt an, dass kein Kalender verwendet werden soll.

 **Remarks:** 

Normalerweise ist in AW None der erste und Standardwert für Aufzählungen, aber nicht in diesem Fall. None ist nicht der Standard für OOXML, stattdessen ist [GREGORIAN](../../com.aspose.words/sdtcalendartype/#GREGORIAN) der Standard und das erste Element dieser Aufzählung.

### SAKA {#SAKA}
```
public static int SAKA
```


Gibt an, dass der Saka-Ära-Kalender, wie beschrieben durch das Kalenderreformkomitee Indiens, als Teil des indischen Ephemeriden- und Nautikalmanachs, verwendet werden soll.

### TAIWAN {#TAIWAN}
```
public static int TAIWAN
```


Gibt an, dass der taiwanesische Kalender, wie definiert durch den chinesischen Nationalstandard CNS 7648, verwendet werden soll.

### THAI {#THAI}
```
public static int THAI
```


Gibt an, dass der thailändische Kalender, wie definiert durch das königliche Dekret von H.M. König Vajiravudh (Rama VI) im Royal Gazette B. E. 2456 (1913 n. Chr.) und durch das Dekret des Premierministers Phibunsongkhram (1941 n. Chr.), das Jahr am gregorianischen 1. Januar beginnen und das Jahr Null auf das gregorianische Jahr 543 v. Chr. abbilden soll, verwendet werden soll.

### length {#length}
```
public static int length
```


### fromName(String sdtCalendarTypeName) {#fromName-java.lang.String}
```
public static int fromName(String sdtCalendarTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sdtCalendarTypeName | java.lang.String |  |

**Returns:**
int
### getName(int sdtCalendarType) {#getName-int}
```
public static String getName(int sdtCalendarType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sdtCalendarType | int |  |

**Returns:**
java.lang.String
