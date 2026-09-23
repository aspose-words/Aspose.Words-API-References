---
title: "SdtCalendarType"
linktitle: "SdtCalendarType"
second_title: "Aspose.Words per Java"
description: "Specifica i possibili tipi di calendari che possono essere usati per specificare StructuredDocumentTag.getCalendarType / StructuredDocumentTag.setCalendarTypeint in un documento Office Open XML in Java."
type: docs
weight: 600
url: /it/java/com.aspose.words/sdtcalendartype/
---

**Inheritance:**
java.lang.Object
```
public class SdtCalendarType
```

Specifica i possibili tipi di calendari che possono essere usati per specificare [StructuredDocumentTag.getCalendarType()](../../com.aspose.words/structureddocumenttag/\#getCalendarType) / [StructuredDocumentTag.setCalendarType(int)](../../com.aspose.words/structureddocumenttag/\#setCalendarType-int) in un documento Office Open XML.

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
| [DEFAULT](#DEFAULT) | Usato come valore predefinito in OOXML. |
| [GREGORIAN](#GREGORIAN) | Specifica che il calendario gregoriano, così definito nello ISO 8601, deve essere utilizzato. |
| [GREGORIAN_ARABIC](#GREGORIAN-ARABIC) | Specifica che il calendario gregoriano, così definito nello ISO 8601, deve essere utilizzato. |
| [GREGORIAN_ME_FRENCH](#GREGORIAN-ME-FRENCH) | Specifica che il calendario gregoriano, così definito nello ISO 8601, deve essere utilizzato. |
| [GREGORIAN_US](#GREGORIAN-US) | Specifica che il calendario gregoriano, così definito nello ISO 8601, deve essere utilizzato. |
| [GREGORIAN_XLIT_ENGLISH](#GREGORIAN-XLIT-ENGLISH) | Specifica che il calendario gregoriano, così definito nello ISO 8601, deve essere utilizzato. |
| [GREGORIAN_XLIT_FRENCH](#GREGORIAN-XLIT-FRENCH) | Specifica che il calendario gregoriano, così definito nello ISO 8601, deve essere utilizzato. |
| [HEBREW](#HEBREW) | Specifica che il calendario lunare ebraico, così descritto dalla formula di Gauss per la Pasqua [CITATION] e dal Complete Restatement of Oral Law (Mishneh Torah), deve essere usato. |
| [HIJRI](#HIJRI) | Specifica che il calendario lunare Hijri, così descritto dal Regno dell'Arabia Saudita, Ministero degli Affari Islamici, Endowments, Da‘wah e Guidance, deve essere usato. |
| [JAPAN](#JAPAN) | Specifica che il calendario dell'era dell'Imperatore giapponese, così descritto dallo Japanese Industrial Standard JIS X 0301, deve essere usato. |
| [KOREA](#KOREA) | Specifica che il calendario dell'era Tangun coreana, così descritto dal Korean Law Enactment No., deve essere usato. |
| [NONE](#NONE) | Specifica che non deve essere usato alcun calendario. |
| [SAKA](#SAKA) | Specifica che il calendario dell'era Saka, così descritto dal Calendar Reform Committee of India, come parte dell'Indian Ephemeris and Nautical Almanac, deve essere usato. |
| [TAIWAN](#TAIWAN) | Specifica che il calendario taiwanese, così definito dallo Chinese National Standard CNS 7648, deve essere usato. |
| [THAI](#THAI) | Specifica che il calendario tailandese, così definito dal Royal Decree of H.M., deve essere usato. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String sdtCalendarTypeName)](#fromName-java.lang.String) |  |
| [getName(int sdtCalendarType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sdtCalendarType)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Usato come valore predefinito in OOXML. È uguale a [GREGORIAN](../../com.aspose.words/sdtcalendartype/\#GREGORIAN).

### GREGORIAN {#GREGORIAN}
```
public static int GREGORIAN
```


Specifica che il calendario gregoriano, così definito nello ISO 8601, deve essere usato. Questo calendario dovrebbe essere localizzato nella lingua appropriata.

### GREGORIAN_ARABIC {#GREGORIAN-ARABIC}
```
public static int GREGORIAN_ARABIC
```


Specifica che il calendario gregoriano, così definito nello ISO 8601, deve essere usato. I valori per questo calendario dovrebbero essere presentati in arabo.

### GREGORIAN_ME_FRENCH {#GREGORIAN-ME-FRENCH}
```
public static int GREGORIAN_ME_FRENCH
```


Specifica che il calendario gregoriano, così definito nello ISO 8601, deve essere usato. I valori per questo calendario dovrebbero essere presentati in francese del Medio Oriente.

### GREGORIAN_US {#GREGORIAN-US}
```
public static int GREGORIAN_US
```


Specifica che il calendario gregoriano, così definito nello ISO 8601, deve essere usato. I valori per questo calendario dovrebbero essere presentati in inglese.

### GREGORIAN_XLIT_ENGLISH {#GREGORIAN-XLIT-ENGLISH}
```
public static int GREGORIAN_XLIT_ENGLISH
```


Specifica che il calendario gregoriano, così definito nello ISO 8601, deve essere usato. I valori per questo calendario dovrebbero essere la rappresentazione delle stringhe inglesi nei corrispondenti caratteri arabi (la traslitterazione araba dell'inglese per il calendario gregoriano).

### GREGORIAN_XLIT_FRENCH {#GREGORIAN-XLIT-FRENCH}
```
public static int GREGORIAN_XLIT_FRENCH
```


Specifica che il calendario gregoriano, così definito nello ISO 8601, deve essere usato. I valori per questo calendario dovrebbero essere la rappresentazione delle stringhe francesi nei corrispondenti caratteri arabi (la traslitterazione araba del francese per il calendario gregoriano).

### HEBREW {#HEBREW}
```
public static int HEBREW
```


Specifica che il calendario lunare ebraico, così descritto dalla formula di Gauss per la Pasqua [CITATION] e dal Complete Restatement of Oral Law (Mishneh Torah), deve essere usato.

### HIJRI {#HIJRI}
```
public static int HIJRI
```


Specifica che il calendario lunare Hijri, così descritto dal Regno dell'Arabia Saudita, Ministero degli Affari Islamici, Endowments, Da‘wah e Guidance, deve essere usato.

### JAPAN {#JAPAN}
```
public static int JAPAN
```


Specifica che il calendario dell'era dell'Imperatore giapponese, così descritto dallo Japanese Industrial Standard JIS X 0301, deve essere usato.

### KOREA {#KOREA}
```
public static int KOREA
```


Specifica che il calendario dell'era Tangun coreana, così descritto dal Korean Law Enactment No. 4, deve essere usato.

### NONE {#NONE}
```
public static int NONE
```


Specifica che non deve essere usato alcun calendario.

 **Remarks:** 

Di solito in AW, None è il primo e valore predefinito per gli enum, ma non in questo caso. None non è il valore predefinito per OOXML, invece [GREGORIAN](../../com.aspose.words/sdtcalendartype/\#GREGORIAN) è predefinito ed è il primo membro di questo enum.

### SAKA {#SAKA}
```
public static int SAKA
```


Specifica che il calendario dell'era Saka, così descritto dal Calendar Reform Committee of India, come parte dell'Indian Ephemeris and Nautical Almanac, deve essere usato.

### TAIWAN {#TAIWAN}
```
public static int TAIWAN
```


Specifica che il calendario taiwanese, così definito dallo Chinese National Standard CNS 7648, deve essere usato.

### THAI {#THAI}
```
public static int THAI
```


Specifica che il calendario tailandese, così definito dal Royal Decree of H.M. King Vajiravudh (Rama VI) nella Royal Gazette B. E. 2456 (1913 d.C.) e dal decreto del Primo Ministro Phibunsongkhram (1941 d.C.) per iniziare l'anno il 1 gennaio gregoriano e per mappare l'anno zero all'anno gregoriano 543 a.C., deve essere usato.

### length {#length}
```
public static int length
```


### fromName(String sdtCalendarTypeName) {#fromName-java.lang.String}
```
public static int fromName(String sdtCalendarTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sdtCalendarTypeName | java.lang.String |  |

**Returns:**
int
### getName(int sdtCalendarType) {#getName-int}
```
public static String getName(int sdtCalendarType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sdtCalendarType | int |  |

**Returns:**
java.lang.String
