---
title: "SdtCalendarType"
linktitle: "SdtCalendarType"
second_title: "Aspose.Words Java için"
description: "Bir Office Open XML belgesinde Java için StructuredDocumentTag.getCalendarType / StructuredDocumentTag.setCalendarTypeint belirtmek için kullanılabilecek takvimlerin olası türlerini belirtir."
type: docs
weight: 600
url: /tr/java/com.aspose.words/sdtcalendartype/
---

**Inheritance:**
java.lang.Object
```
public class SdtCalendarType
```

Bir Office Open XML belgesinde kullanılabilecek takvimlerin olası türlerini, [StructuredDocumentTag.getCalendarType()](../../com.aspose.words/structureddocumenttag/\#getCalendarType) / [StructuredDocumentTag.setCalendarType(int)](../../com.aspose.words/structureddocumenttag/\#setCalendarType-int) belirtmek için belirtir.

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
| [DEFAULT](#DEFAULT) | OOXML'de varsayılan değer olarak kullanılır. |
| [GREGORIAN](#GREGORIAN) | ISO 8601'de tanımlandığı gibi Gregoryen takvimin kullanılacağını belirtir. |
| [GREGORIAN_ARABIC](#GREGORIAN-ARABIC) | ISO 8601'de tanımlandığı gibi Gregoryen takvimin kullanılacağını belirtir. |
| [GREGORIAN_ME_FRENCH](#GREGORIAN-ME-FRENCH) | ISO 8601'de tanımlandığı gibi Gregoryen takvimin kullanılacağını belirtir. |
| [GREGORIAN_US](#GREGORIAN-US) | ISO 8601'de tanımlandığı gibi Gregoryen takvimin kullanılacağını belirtir. |
| [GREGORIAN_XLIT_ENGLISH](#GREGORIAN-XLIT-ENGLISH) | ISO 8601'de tanımlandığı gibi Gregoryen takvimin kullanılacağını belirtir. |
| [GREGORIAN_XLIT_FRENCH](#GREGORIAN-XLIT-FRENCH) | ISO 8601'de tanımlandığı gibi Gregoryen takvimin kullanılacağını belirtir. |
| [HEBREW](#HEBREW) | Gauss formülüyle Passover için ve The Complete Restatement of Oral Law (Mishneh Torah) ile tanımlanan İbranice ay takviminin kullanılacağını belirtir. |
| [HIJRI](#HIJRI) | Suudi Arabistan Krallığı, İslam İşleri, Vakıflar, Da\u2018wah ve Rehberlik Bakanlığı tarafından tanımlanan Hicri ay takviminin kullanılacağını belirtir. |
| [JAPAN](#JAPAN) | Japon Endüstri Standardı JIS X 0301 tarafından tanımlanan Japon İmparatorluk Dönemi takviminin kullanılacağını belirtir. |
| [KOREA](#KOREA) | Kore Yasası No. tarafından tanımlanan Kore Tangun Dönemi takviminin kullanılacağını belirtir. |
| [NONE](#NONE) | Hiç takvim kullanılmaması gerektiğini belirtir. |
| [SAKA](#SAKA) | Hindistan Takvim Reform Komitesi tarafından, Hindistan Ephemeris ve Denizcilik Takvimi'nin bir parçası olarak tanımlanan Saka Dönemi takviminin kullanılacağını belirtir. |
| [TAIWAN](#TAIWAN) | Çin Ulusal Standardı CNS 7648 tarafından tanımlanan Tayvan takviminin kullanılacağını belirtir. |
| [THAI](#THAI) | HM'nin Kraliyet Kararnamesi tarafından tanımlanan Tayland takviminin kullanılacağını belirtir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String sdtCalendarTypeName)](#fromName-java.lang.String) |  |
| [getName(int sdtCalendarType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sdtCalendarType)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


OOXML'de varsayılan değer olarak kullanılır. Eşittir [GREGORIAN](../../com.aspose.words/sdtcalendartype/\#GREGORIAN).

### GREGORIAN {#GREGORIAN}
```
public static int GREGORIAN
```


ISO 8601'de tanımlandığı gibi Gregoryen takvimin kullanılacağını belirtir. Bu takvim uygun dile yerelleştirilmeli.

### GREGORIAN_ARABIC {#GREGORIAN-ARABIC}
```
public static int GREGORIAN_ARABIC
```


ISO 8601'de tanımlandığı gibi Gregoryen takvimin kullanılacağını belirtir. Bu takvimin değerleri Arapça olarak sunulmalıdır.

### GREGORIAN_ME_FRENCH {#GREGORIAN-ME-FRENCH}
```
public static int GREGORIAN_ME_FRENCH
```


ISO 8601'de tanımlandığı gibi Gregoryen takvimin kullanılacağını belirtir. Bu takvimin değerleri Orta Doğu Fransızcası olarak sunulmalıdır.

### GREGORIAN_US {#GREGORIAN-US}
```
public static int GREGORIAN_US
```


ISO 8601'de tanımlandığı gibi Gregoryen takvimin kullanılacağını belirtir. Bu takvimin değerleri İngilizce olarak sunulmalıdır.

### GREGORIAN_XLIT_ENGLISH {#GREGORIAN-XLIT-ENGLISH}
```
public static int GREGORIAN_XLIT_ENGLISH
```


ISO 8601'de tanımlandığı gibi Gregoryen takvimin kullanılacağını belirtir. Bu takvimin değerleri, İngilizce dizelerin ilgili Arapça karakterlerle temsili (Gregoryen takvim için İngilizce'nin Arapça transliterasyonu) olmalıdır.

### GREGORIAN_XLIT_FRENCH {#GREGORIAN-XLIT-FRENCH}
```
public static int GREGORIAN_XLIT_FRENCH
```


ISO 8601'de tanımlandığı gibi Gregoryen takvimin kullanılacağını belirtir. Bu takvimin değerleri, Fransızca dizelerin ilgili Arapça karakterlerle temsili (Gregoryen takvim için Fransızca'nın Arapça transliterasyonu) olmalıdır.

### HEBREW {#HEBREW}
```
public static int HEBREW
```


Gauss formülüyle Passover için ve The Complete Restatement of Oral Law (Mishneh Torah) ile tanımlanan İbranice ay takviminin kullanılacağını belirtir.

### HIJRI {#HIJRI}
```
public static int HIJRI
```


Suudi Arabistan Krallığı, İslam İşleri, Vakıflar, Da\u2018wah ve Rehberlik Bakanlığı tarafından tanımlanan Hicri ay takviminin kullanılacağını belirtir.

### JAPAN {#JAPAN}
```
public static int JAPAN
```


Japon Endüstri Standardı JIS X 0301 tarafından tanımlanan Japon İmparatorluk Dönemi takviminin kullanılacağını belirtir.

### KOREA {#KOREA}
```
public static int KOREA
```


Kore Yasası No. 4 tarafından tanımlanan Kore Tangun Dönemi takviminin kullanılacağını belirtir.

### NONE {#NONE}
```
public static int NONE
```


Hiç takvim kullanılmaması gerektiğini belirtir.

 **Remarks:** 

Genellikle AW'de, None enum'lar için ilk ve varsayılan değerdir, ancak bu durumda değil. None OOXML için varsayılan değildir, bunun yerine [GREGORIAN](../../com.aspose.words/sdtcalendartype/\#GREGORIAN) varsayılandır ve bu enum'un ilk üyesidir.

### SAKA {#SAKA}
```
public static int SAKA
```


Hindistan Takvim Reform Komitesi tarafından, Hindistan Ephemeris ve Denizcilik Takvimi'nin bir parçası olarak tanımlanan Saka Dönemi takviminin kullanılacağını belirtir.

### TAIWAN {#TAIWAN}
```
public static int TAIWAN
```


Çin Ulusal Standardı CNS 7648 tarafından tanımlanan Tayvan takviminin kullanılacağını belirtir.

### THAI {#THAI}
```
public static int THAI
```


HM Kralı Vajiravudh (Rama VI) tarafından Kraliyet Gazetesi B. E. 2456 (1913 AD) ve Başbakan Phibunsongkhram (1941 AD) kararnamesiyle Gregoryen Ocak 1'de yılı başlatmak ve yıl sıfırını Gregoryen 543 B.C. yılına eşlemek üzere tanımlanan Tayland takviminin kullanılacağını belirtir.

### length {#length}
```
public static int length
```


### fromName(String sdtCalendarTypeName) {#fromName-java.lang.String}
```
public static int fromName(String sdtCalendarTypeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sdtCalendarTypeName | java.lang.String |  |

**Returns:**
int
### getName(int sdtCalendarType) {#getName-int}
```
public static String getName(int sdtCalendarType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sdtCalendarType | int |  |

**Returns:**
java.lang.String
