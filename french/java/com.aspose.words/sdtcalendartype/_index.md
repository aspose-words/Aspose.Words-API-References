---
title: "SdtCalendarType"
linktitle: "SdtCalendarType"
second_title: "Aspose.Words pour Java"
description: "Spécifie les types possibles de calendriers qui peuvent être utilisés pour spécifier StructuredDocumentTag.getCalendarType / StructuredDocumentTag.setCalendarTypeint dans un document Office Open XML en Java."
type: docs
weight: 600
url: /fr/java/com.aspose.words/sdtcalendartype/
---

**Inheritance:**
java.lang.Object
```
public class SdtCalendarType
```

Spécifie les types possibles de calendriers qui peuvent être utilisés pour spécifier [StructuredDocumentTag.getCalendarType()](../../com.aspose.words/structureddocumenttag/#getCalendarType) / [StructuredDocumentTag.setCalendarType(int)](../../com.aspose.words/structureddocumenttag/#setCalendarType-int) dans un document Office Open XML.

 **Examples:** 

Montre comment inviter l'utilisateur à saisir une date avec une balise de document structuré.

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
## Champs

| Champ | Description |
| --- | --- |
| [DEFAULT](#DEFAULT) | Utilisé comme valeur par défaut dans OOXML. |
| [GREGORIAN](#GREGORIAN) | Spécifie que le calendrier grégorien, tel que défini dans ISO 8601, doit être utilisé. |
| [GREGORIAN_ARABIC](#GREGORIAN-ARABIC) | Spécifie que le calendrier grégorien, tel que défini dans ISO 8601, doit être utilisé. |
| [GREGORIAN_ME_FRENCH](#GREGORIAN-ME-FRENCH) | Spécifie que le calendrier grégorien, tel que défini dans ISO 8601, doit être utilisé. |
| [GREGORIAN_US](#GREGORIAN-US) | Spécifie que le calendrier grégorien, tel que défini dans ISO 8601, doit être utilisé. |
| [GREGORIAN_XLIT_ENGLISH](#GREGORIAN-XLIT-ENGLISH) | Spécifie que le calendrier grégorien, tel que défini dans ISO 8601, doit être utilisé. |
| [GREGORIAN_XLIT_FRENCH](#GREGORIAN-XLIT-FRENCH) | Spécifie que le calendrier grégorien, tel que défini dans ISO 8601, doit être utilisé. |
| [HEBREW](#HEBREW) | Spécifie que le calendrier lunaire hébreu, tel que décrit par la formule de Gauss pour la Pâque [CITATION] et le Complete Restatement of Oral Law (Mishneh Torah), doit être utilisé. |
| [HIJRI](#HIJRI) | Spécifie que le calendrier lunaire hijri, tel que décrit par le Royaume d'Arabie Saoudite, le Ministère des Affaires Islamiques, des Endowments, Da‘wah et Guidance, doit être utilisé. |
| [JAPAN](#JAPAN) | Spécifie que le calendrier de l'ère de l'empereur japonais, tel que décrit par la norme industrielle japonaise JIS X 0301, doit être utilisé. |
| [KOREA](#KOREA) | Spécifie que le calendrier de l'ère Tangun coréenne, tel que décrit par la loi coréenne No. |
| [NONE](#NONE) | Spécifie qu'aucun calendrier ne doit être utilisé. |
| [SAKA](#SAKA) | Spécifie que le calendrier de l'ère Saka, tel que décrit par le Comité de réforme du calendrier de l'Inde, dans le cadre de l'Éphéméride indienne et de l'Almanach nautique, doit être utilisé. |
| [TAIWAN](#TAIWAN) | Spécifie que le calendrier taïwanais, tel que défini par la norme nationale chinoise CNS 7648, doit être utilisé. |
| [THAI](#THAI) | Spécifie que le calendrier thaïlandais, tel que défini par le décret royal de H.M. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String sdtCalendarTypeName)](#fromName-java.lang.String) |  |
| [getName(int sdtCalendarType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sdtCalendarType)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Utilisé comme valeur par défaut dans OOXML. Égal à [GREGORIAN](../../com.aspose.words/sdtcalendartype/#GREGORIAN).

### GREGORIAN {#GREGORIAN}
```
public static int GREGORIAN
```


Spécifie que le calendrier grégorien, tel que défini dans ISO 8601, doit être utilisé. Ce calendrier doit être localisé dans la langue appropriée.

### GREGORIAN_ARABIC {#GREGORIAN-ARABIC}
```
public static int GREGORIAN_ARABIC
```


Spécifie que le calendrier grégorien, tel que défini dans ISO 8601, doit être utilisé. Les valeurs de ce calendrier doivent être présentées en arabe.

### GREGORIAN_ME_FRENCH {#GREGORIAN-ME-FRENCH}
```
public static int GREGORIAN_ME_FRENCH
```


Spécifie que le calendrier grégorien, tel que défini dans ISO 8601, doit être utilisé. Les valeurs de ce calendrier doivent être présentées en français du Moyen-Orient.

### GREGORIAN_US {#GREGORIAN-US}
```
public static int GREGORIAN_US
```


Spécifie que le calendrier grégorien, tel que défini dans ISO 8601, doit être utilisé. Les valeurs de ce calendrier doivent être présentées en anglais.

### GREGORIAN_XLIT_ENGLISH {#GREGORIAN-XLIT-ENGLISH}
```
public static int GREGORIAN_XLIT_ENGLISH
```


Spécifie que le calendrier grégorien, tel que défini dans ISO 8601, doit être utilisé. Les valeurs de ce calendrier doivent être la représentation des chaînes anglaises en caractères arabes correspondants (la translittération arabe de l'anglais pour le calendrier grégorien).

### GREGORIAN_XLIT_FRENCH {#GREGORIAN-XLIT-FRENCH}
```
public static int GREGORIAN_XLIT_FRENCH
```


Spécifie que le calendrier grégorien, tel que défini dans ISO 8601, doit être utilisé. Les valeurs de ce calendrier doivent être la représentation des chaînes françaises en caractères arabes correspondants (la translittération arabe du français pour le calendrier grégorien).

### HEBREW {#HEBREW}
```
public static int HEBREW
```


Spécifie que le calendrier lunaire hébreu, tel que décrit par la formule de Gauss pour la Pâque [CITATION] et le Complete Restatement of Oral Law (Mishneh Torah), doit être utilisé.

### HIJRI {#HIJRI}
```
public static int HIJRI
```


Spécifie que le calendrier lunaire hijri, tel que décrit par le Royaume d'Arabie Saoudite, le Ministère des Affaires Islamiques, des Endowments, Da‘wah et Guidance, doit être utilisé.

### JAPAN {#JAPAN}
```
public static int JAPAN
```


Spécifie que le calendrier de l'ère de l'empereur japonais, tel que décrit par la norme industrielle japonaise JIS X 0301, doit être utilisé.

### KOREA {#KOREA}
```
public static int KOREA
```


Spécifie que le calendrier de l'ère Tangun coréenne, tel que décrit par la loi coréenne No. 4, doit être utilisé.

### NONE {#NONE}
```
public static int NONE
```


Spécifie qu'aucun calendrier ne doit être utilisé.

 **Remarks:** 

Habituellement dans AW, None est la première et la valeur par défaut pour les énumérations, mais pas dans ce cas. None n'est pas la valeur par défaut pour OOXML, à la place [GREGORIAN](../../com.aspose.words/sdtcalendartype/#GREGORIAN) est la valeur par défaut et le premier membre de cette énumération.

### SAKA {#SAKA}
```
public static int SAKA
```


Spécifie que le calendrier de l'ère Saka, tel que décrit par le Comité de réforme du calendrier de l'Inde, dans le cadre de l'Éphéméride indienne et de l'Almanach nautique, doit être utilisé.

### TAIWAN {#TAIWAN}
```
public static int TAIWAN
```


Spécifie que le calendrier taïwanais, tel que défini par la norme nationale chinoise CNS 7648, doit être utilisé.

### THAI {#THAI}
```
public static int THAI
```


Spécifie que le calendrier thaïlandais, tel que défini par le décret royal de H.M. le roi Vajiravudh (Rama VI) dans le Journal officiel B. E. 2456 (1913 A.D.) et par le décret du Premier ministre Phibunsongkhram (1941 A.D.) pour commencer l'année le 1er janvier grégorien et mapper l'année zéro à l'année grégorienne 543 B.C., doit être utilisé.

### length {#length}
```
public static int length
```


### fromName(String sdtCalendarTypeName) {#fromName-java.lang.String}
```
public static int fromName(String sdtCalendarTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| sdtCalendarTypeName | java.lang.String |  |

**Returns:**
int
### getName(int sdtCalendarType) {#getName-int}
```
public static String getName(int sdtCalendarType)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| sdtCalendarType | int |  |

**Returns:**
java.lang.String
