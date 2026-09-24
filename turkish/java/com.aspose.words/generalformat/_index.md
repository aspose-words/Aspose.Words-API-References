---
title: "GeneralFormat"
linktitle: "GeneralFormat"
second_title: "Aspose.Words Java için"
description: "Java'da sayısal metne veya herhangi bir alan sonucuna uygulanan genel bir formatı belirtir."
type: docs
weight: 355
url: /tr/java/com.aspose.words/generalformat/
---

**Inheritance:**
java.lang.Object
```
public class GeneralFormat
```

Sayısal, metin veya herhangi bir alan sonucuna uygulanan genel bir formatı belirtir. Bir alan, genel formatların bir kombinasyonuna sahip olabilir.

 **Examples:** 

Alan sonuçlarını nasıl biçimlendireceğinizi gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Use a document builder to insert a field that displays a result with no format applied.
 Field field = builder.insertField("= 2 + 3");

 Assert.assertEquals("= 2 + 3", field.getFieldCode());
 Assert.assertEquals("5", field.getResult());

 // We can apply a format to a field's result using the field's properties.
 // Below are three types of formats that we can apply to a field's result.
 // 1 -  Numeric format:
 FieldFormat format = field.getFormat();
 format.setNumericFormat("$###.00");
 field.update();

 Assert.assertEquals("= 2 + 3 \\# $###.00", field.getFieldCode());
 Assert.assertEquals("$  5.00", field.getResult());

 // 2 -  Date/time format:
 field = builder.insertField("DATE");
 format = field.getFormat();
 format.setDateTimeFormat("dddd, MMMM dd, yyyy");
 field.update();

 Assert.assertEquals("DATE \\@ \"dddd, MMMM dd, yyyy\"", field.getFieldCode());
 System.out.println("Today's date, in {format.DateTimeFormat} format:\n\t{field.Result}");

 // 3 -  General format:
 field = builder.insertField("= 25 + 33");
 format = field.getFormat();
 format.getGeneralFormats().add(GeneralFormat.LOWERCASE_ROMAN);
 format.getGeneralFormats().add(GeneralFormat.UPPER);
 field.update();

 int index = 0;
 Iterator generalFormatEnumerator = format.getGeneralFormats().iterator();
 while (generalFormatEnumerator.hasNext()) {
     int value = generalFormatEnumerator.next();
     System.out.println(MessageFormat.format("General format index {0}: {1}", index++, value));
 }

 Assert.assertEquals("= 25 + 33 \\* roman \\* Upper", field.getFieldCode());
 Assert.assertEquals("LVIII", field.getResult());
 Assert.assertEquals(2, format.getGeneralFormats().getCount());
 Assert.assertEquals(GeneralFormat.LOWERCASE_ROMAN, format.getGeneralFormats().get(0));

 // We can remove our formats to revert the field's result to its original form.
 format.getGeneralFormats().remove(GeneralFormat.LOWERCASE_ROMAN);
 format.getGeneralFormats().removeAt(0);
 Assert.assertEquals(0, format.getGeneralFormats().getCount());
 field.update();

 Assert.assertEquals("= 25 + 33  ", field.getFieldCode());
 Assert.assertEquals("58", field.getResult());
 Assert.assertEquals(0, format.getGeneralFormats().getCount());
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [AIUEO](#AIUEO) | Sayısal biçimlendirme. |
| [ARABIC](#ARABIC) | Sayısal biçimlendirme. |
| [ARABIC_ABJAD](#ARABIC-ABJAD) | Sayısal biçimlendirme. |
| [ARABIC_ALPHA](#ARABIC-ALPHA) | Sayısal biçimlendirme. |
| [ARABIC_DASH](#ARABIC-DASH) | Sayısal biçimlendirme. |
| [BAHT_TEXT](#BAHT-TEXT) | Sayısal biçimlendirme. |
| [CAPS](#CAPS) | Metin biçimlendirme. |
| [CARD_TEXT](#CARD-TEXT) | Sayısal biçimlendirme. |
| [CHAR_FORMAT](#CHAR-FORMAT) | Alan sonucu biçimlendirme. |
| [CHINESE_NUM_1](#CHINESE-NUM-1) | Sayısal biçimlendirme. |
| [CHINESE_NUM_2](#CHINESE-NUM-2) | Sayısal biçimlendirme. |
| [CHINESE_NUM_3](#CHINESE-NUM-3) | Sayısal biçimlendirme. |
| [CHOSUNG](#CHOSUNG) | Sayısal biçimlendirme. |
| [CIRCLE_NUM](#CIRCLE-NUM) | Sayısal biçimlendirme. |
| [DB_CHAR](#DB-CHAR) |  |
| [DB_NUM_1](#DB-NUM-1) |  |
| [DB_NUM_2](#DB-NUM-2) |  |
| [DB_NUM_3](#DB-NUM-3) |  |
| [DB_NUM_4](#DB-NUM-4) |  |
| [DOLLAR_TEXT](#DOLLAR-TEXT) | Sayısal biçimlendirme. |
| [FIRST_CAP](#FIRST-CAP) | Metin biçimlendirme. |
| [GANADA](#GANADA) | Sayısal biçimlendirme. |
| [GB_1](#GB-1) | Sayısal biçimlendirme. |
| [GB_2](#GB-2) | Sayısal biçimlendirme. |
| [GB_3](#GB-3) | Sayısal biçimlendirme. |
| [GB_4](#GB-4) | Sayısal biçimlendirme. |
| [HEBREW_1](#HEBREW-1) | Sayısal biçimlendirme. |
| [HEBREW_2](#HEBREW-2) | Sayısal biçimlendirme. |
| [HEX](#HEX) | Sayısal biçimlendirme. |
| [HINDI_ARABIC](#HINDI-ARABIC) | Sayısal biçimlendirme. |
| [HINDI_CARD_TEXT](#HINDI-CARD-TEXT) | Sayısal biçimlendirme. |
| [HINDI_LETTER_1](#HINDI-LETTER-1) | Sayısal biçimlendirme. |
| [HINDI_LETTER_2](#HINDI-LETTER-2) | Sayısal biçimlendirme. |
| [IROHA](#IROHA) | Sayısal biçimlendirme. |
| [KANJI_NUM_1](#KANJI-NUM-1) | Sayısal biçimlendirme. |
| [KANJI_NUM_2](#KANJI-NUM-2) | Sayısal biçimlendirme. |
| [KANJI_NUM_3](#KANJI-NUM-3) | Sayısal biçimlendirme. |
| [LOWER](#LOWER) | Metin biçimlendirme. |
| [LOWERCASE_ALPHABETIC](#LOWERCASE-ALPHABETIC) | Sayısal biçimlendirme. |
| [LOWERCASE_ROMAN](#LOWERCASE-ROMAN) | Sayısal biçimlendirme. |
| [MERGE_FORMAT](#MERGE-FORMAT) | Alan sonucu biçimlendirme. |
| [MERGE_FORMAT_INET](#MERGE-FORMAT-INET) | Alan sonucu biçimlendirme. |
| [NONE](#NONE) | Eksik bir genel formatı belirtmek için kullanılır. |
| [ORDINAL](#ORDINAL) | Sayısal biçimlendirme. |
| [ORD_TEXT](#ORD-TEXT) | Sayısal biçimlendirme. |
| [SB_CHAR](#SB-CHAR) |  |
| [THAI_ARABIC](#THAI-ARABIC) | Sayısal biçimlendirme. |
| [THAI_CARD_TEXT](#THAI-CARD-TEXT) | Sayısal biçimlendirme. |
| [THAI_LETTER](#THAI-LETTER) | Sayısal biçimlendirme. |
| [UPPER](#UPPER) | Metin biçimlendirme. |
| [UPPERCASE_ALPHABETIC](#UPPERCASE-ALPHABETIC) | Sayısal biçimlendirme. |
| [UPPERCASE_ROMAN](#UPPERCASE-ROMAN) | Sayısal biçimlendirme. |
| [VIET_CARD_TEXT](#VIET-CARD-TEXT) | Sayısal biçimlendirme. |
| [ZODIAC_1](#ZODIAC-1) | Sayısal biçimlendirme. |
| [ZODIAC_2](#ZODIAC-2) | Sayısal biçimlendirme. |
| [ZODIAC_3](#ZODIAC-3) | Sayısal biçimlendirme. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String generalFormatName)](#fromName-java.lang.String) |  |
| [getName(int generalFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int generalFormat)](#toString-int) |  |
### AIUEO {#AIUEO}
```
public static int AIUEO
```


Sayısal biçimlendirme. Sayısal bir sonucu geleneksel a-i-u-e-o sırasındaki hiragana karakterlerini kullanarak biçimler.

### ARABIC {#ARABIC}
```
public static int ARABIC
```


Sayısal biçimlendirme. Sayısal bir sonucu Arap kardinal rakamlarıyla biçimler.

### ARABIC_ABJAD {#ARABIC-ABJAD}
```
public static int ARABIC_ABJAD
```


Sayısal biçimlendirme. Sayısal bir sonucu artan Abjad rakamlarıyla biçimler.

### ARABIC_ALPHA {#ARABIC-ALPHA}
```
public static int ARABIC_ALPHA
```


Sayısal biçimlendirme. Sayısal bir sonucu Arap alfabesindeki karakterlerle biçimler.

### ARABIC_DASH {#ARABIC-DASH}
```
public static int ARABIC_DASH
```


Sayısal biçimlendirme. Sayısal bir sonucu Arap kardinal rakamlarıyla, "- " öneki ve " -" soneki ekleyerek biçimler.

### BAHT_TEXT {#BAHT-TEXT}
```
public static int BAHT_TEXT
```


Sayısal biçimlendirme. Sayısal bir sonucu Tayland sayma sisteminde biçimler.

### CAPS {#CAPS}
```
public static int CAPS
```


Metin biçimlendirme. Her kelimenin ilk harfini büyük yapar.

### CARD_TEXT {#CARD-TEXT}
```
public static int CARD_TEXT
```


Sayısal biçimlendirme. Kardinal metin (Bir, İki, Üç, ...).

### CHAR_FORMAT {#CHAR-FORMAT}
```
public static int CHAR_FORMAT
```


Alan sonucu biçimlendirme. CHARFORMAT talimatı.

### CHINESE_NUM_1 {#CHINESE-NUM-1}
```
public static int CHINESE_NUM_1
```


Sayısal biçimlendirme. Sayısal bir sonucu uygun sayma sisteminden artan sayılarla biçimler.

### CHINESE_NUM_2 {#CHINESE-NUM-2}
```
public static int CHINESE_NUM_2
```


Sayısal biçimlendirme. Sayısal bir sonucu uygun yasal formattan ardışık sayılarla biçimler.

### CHINESE_NUM_3 {#CHINESE-NUM-3}
```
public static int CHINESE_NUM_3
```


Sayısal biçimlendirme. Sayısal bir sonucu uygun binlik sayma sisteminden ardışık sayılarla biçimler.

### CHOSUNG {#CHOSUNG}
```
public static int CHOSUNG
```


Sayısal biçimlendirme. Sayısal bir sonucu Kore Chosung formatından ardışık sayılarla biçimler.

### CIRCLE_NUM {#CIRCLE-NUM}
```
public static int CIRCLE_NUM
```


Sayısal biçimlendirme. Sayısal bir sonucu bir daire içine alınmış ondalık numaralandırma ile, 1\\u201320 aralığındaki sayılar için kapsanan alfanümerik glif karakterini kullanarak biçimler.

### DB_CHAR {#DB-CHAR}
```
public static int DB_CHAR
```


### DB_NUM_1 {#DB-NUM-1}
```
public static int DB_NUM_1
```


### DB_NUM_2 {#DB-NUM-2}
```
public static int DB_NUM_2
```


### DB_NUM_3 {#DB-NUM-3}
```
public static int DB_NUM_3
```


### DB_NUM_4 {#DB-NUM-4}
```
public static int DB_NUM_4
```


### DOLLAR_TEXT {#DOLLAR-TEXT}
```
public static int DOLLAR_TEXT
```


Sayısal biçimlendirme. Dolar metni (Bir, İki, Üç, ... + VE 55/100).

### FIRST_CAP {#FIRST-CAP}
```
public static int FIRST_CAP
```


Metin biçimlendirme. İlk kelimenin ilk harfini büyük yapar.

### GANADA {#GANADA}
```
public static int GANADA
```


Sayısal biçimlendirme. Kore Ganada formatından sıralı sayılar kullanarak sayısal sonucu biçimler.

### GB_1 {#GB-1}
```
public static int GB_1
```


Sayısal biçimlendirme. Kapalı alfanümerik glif karakteri kullanarak nokta ile biten ondalık numaralandırma ile sayısal sonucu biçimler.

### GB_2 {#GB-2}
```
public static int GB_2
```


Sayısal biçimlendirme. Kapalı alfanümerik glif karakteri kullanarak parantez içinde ondalık numaralandırma ile sayısal sonucu biçimler.

### GB_3 {#GB-3}
```
public static int GB_3
```


Sayısal biçimlendirme. Kapalı alfanümerik glif karakteri kullanarak daire içinde ondalık numaralandırma ile sayısal sonucu biçimler.

### GB_4 {#GB-4}
```
public static int GB_4
```


Sayısal biçimlendirme. Kapalı alfanümerik glif karakteri kullanarak daire içinde ondalık numaralandırma ile sayısal sonucu biçimler.

### HEBREW_1 {#HEBREW-1}
```
public static int HEBREW_1
```


Sayısal biçimlendirme. İbranice rakamlar kullanarak sayısal sonucu biçimler.

### HEBREW_2 {#HEBREW-2}
```
public static int HEBREW_2
```


Sayısal biçimlendirme. İbranice alfabeyi kullanarak sayısal sonucu biçimler.

### HEX {#HEX}
```
public static int HEX
```


Sayısal biçimlendirme. Büyük harfli onaltılık basamakları kullanarak sayısal sonucu biçimler.

### HINDI_ARABIC {#HINDI-ARABIC}
```
public static int HINDI_ARABIC
```


Sayısal biçimlendirme. Hint rakamları kullanarak sayısal sonucu biçimler.

### HINDI_CARD_TEXT {#HINDI-CARD-TEXT}
```
public static int HINDI_CARD_TEXT
```


Sayısal biçimlendirme. Hint sayma sisteminden sıralı sayılar kullanarak sayısal sonucu biçimler.

### HINDI_LETTER_1 {#HINDI-LETTER-1}
```
public static int HINDI_LETTER_1
```


Sayısal biçimlendirme. Hint sesli harfleri kullanarak sayısal sonucu biçimler.

### HINDI_LETTER_2 {#HINDI-LETTER-2}
```
public static int HINDI_LETTER_2
```


Sayısal biçimlendirme. Hint sessiz harfleri kullanarak sayısal sonucu biçimler.

### IROHA {#IROHA}
```
public static int IROHA
```


Sayısal biçimlendirme. Japon iroha'sını kullanarak sayısal sonucu biçimler.

### KANJI_NUM_1 {#KANJI-NUM-1}
```
public static int KANJI_NUM_1
```


Sayısal biçimlendirme. Uygun sayma sistemini kullanan Japon tarzı ile sayısal sonucu biçimler.

### KANJI_NUM_2 {#KANJI-NUM-2}
```
public static int KANJI_NUM_2
```


Sayısal biçimlendirme. Uygun sayma sistemini kullanarak sayısal sonucu biçimler.

### KANJI_NUM_3 {#KANJI-NUM-3}
```
public static int KANJI_NUM_3
```


Sayısal biçimlendirme. Uygun sayma sistemini kullanarak sayısal sonucu biçimler.

### LOWER {#LOWER}
```
public static int LOWER
```


Metin biçimlendirme. Tüm harfler küçüktür.

### LOWERCASE_ALPHABETIC {#LOWERCASE-ALPHABETIC}
```
public static int LOWERCASE_ALPHABETIC
```


Sayısal biçimlendirme. Sayısal sonucu bir veya daha fazla küçük harfli Latin alfabesi karakteri olarak biçimler.

### LOWERCASE_ROMAN {#LOWERCASE-ROMAN}
```
public static int LOWERCASE_ROMAN
```


Sayısal biçimlendirme. Küçük harfli Roma rakamları (i, ii, iii, ...).

### MERGE_FORMAT {#MERGE-FORMAT}
```
public static int MERGE_FORMAT
```


Alan sonucu biçimlendirme. MERGEFORMAT talimatı.

### MERGE_FORMAT_INET {#MERGE-FORMAT-INET}
```
public static int MERGE_FORMAT_INET
```


Alan sonucu biçimlendirme. MERGEFORMATINET talimatı.

### NONE {#NONE}
```
public static int NONE
```


Eksik bir genel formatı belirtmek için kullanılır.

### ORDINAL {#ORDINAL}
```
public static int ORDINAL
```


Sayısal biçimlendirme. Sıralı (1., 2., 3., ...).

### ORD_TEXT {#ORD-TEXT}
```
public static int ORD_TEXT
```


Sayısal biçimlendirme. Sıralı metin (Birinci, İkinci, Üçüncü, ...).

### SB_CHAR {#SB-CHAR}
```
public static int SB_CHAR
```


### THAI_ARABIC {#THAI-ARABIC}
```
public static int THAI_ARABIC
```


Sayısal biçimlendirme. Tay rakamları kullanarak sayısal sonucu biçimler.

### THAI_CARD_TEXT {#THAI-CARD-TEXT}
```
public static int THAI_CARD_TEXT
```


Sayısal biçimlendirme. Tay sayma sisteminden sıralı sayılar kullanarak sayısal sonucu biçimler.

### THAI_LETTER {#THAI-LETTER}
```
public static int THAI_LETTER
```


Sayısal biçimlendirme. Tay harflerini kullanarak sayısal sonucu biçimler.

### UPPER {#UPPER}
```
public static int UPPER
```


Metin biçimlendirme. Tüm harfler büyük harf olarak.

### UPPERCASE_ALPHABETIC {#UPPERCASE-ALPHABETIC}
```
public static int UPPERCASE_ALPHABETIC
```


Sayısal biçimlendirme. Sayısal bir sonucu bir veya daha fazla büyük harf Latin alfabesi karakteri olarak biçimler.

### UPPERCASE_ROMAN {#UPPERCASE-ROMAN}
```
public static int UPPERCASE_ROMAN
```


Sayısal biçimlendirme. Büyük harf Roma rakamları (I, II, III, ...).

### VIET_CARD_TEXT {#VIET-CARD-TEXT}
```
public static int VIET_CARD_TEXT
```


Sayısal biçimlendirme. Sayısal bir sonucu Vietnam rakamlarıyla biçimler.

### ZODIAC_1 {#ZODIAC-1}
```
public static int ZODIAC_1
```


Sayısal biçimlendirme. Sayısal bir sonucu sıralı geleneksel ideogramlarla biçimler.

### ZODIAC_2 {#ZODIAC-2}
```
public static int ZODIAC_2
```


Sayısal biçimlendirme. Sayısal bir sonucu sıralı burç ideogramlarıyla biçimler.

### ZODIAC_3 {#ZODIAC-3}
```
public static int ZODIAC_3
```


Sayısal biçimlendirme. Sayısal bir sonucu sıralı geleneksel burç ideogramlarıyla biçimler.

### length {#length}
```
public static int length
```


### fromName(String generalFormatName) {#fromName-java.lang.String}
```
public static int fromName(String generalFormatName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| generalFormatName | java.lang.String |  |

**Returns:**
int
### getName(int generalFormat) {#getName-int}
```
public static String getName(int generalFormat)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| generalFormat | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int generalFormat) {#toString-int}
```
public static String toString(int generalFormat)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| generalFormat | int |  |

**Returns:**
java.lang.String
