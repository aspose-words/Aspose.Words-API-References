---
title: GeneralFormat
linktitle: GeneralFormat
second_title: Aspose.Words for Java
description: Specifies a general format that is applied to a numeric text or any field result in Java.
type: docs
weight: 346
url: /java/com.aspose.words/generalformat/
---

**Inheritance:**
java.lang.Object
```
public class GeneralFormat
```

Specifies a general format that is applied to a numeric, text, or any field result. A field may have a combination of general formats.

 **Examples:** 

Shows how to format field results.

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
## Fields

| Field | Description |
| --- | --- |
| [AIUEO](#AIUEO) | Numeric formatting. |
| [ARABIC](#ARABIC) | Numeric formatting. |
| [ARABIC_ABJAD](#ARABIC-ABJAD) | Numeric formatting. |
| [ARABIC_ALPHA](#ARABIC-ALPHA) | Numeric formatting. |
| [ARABIC_DASH](#ARABIC-DASH) | Numeric formatting. |
| [BAHT_TEXT](#BAHT-TEXT) | Numeric formatting. |
| [CAPS](#CAPS) | Text formatting. |
| [CARD_TEXT](#CARD-TEXT) | Numeric formatting. |
| [CHAR_FORMAT](#CHAR-FORMAT) | Field result formatting. |
| [CHINESE_NUM_1](#CHINESE-NUM-1) | Numeric formatting. |
| [CHINESE_NUM_2](#CHINESE-NUM-2) | Numeric formatting. |
| [CHINESE_NUM_3](#CHINESE-NUM-3) | Numeric formatting. |
| [CHOSUNG](#CHOSUNG) | Numeric formatting. |
| [CIRCLE_NUM](#CIRCLE-NUM) | Numeric formatting. |
| [DB_CHAR](#DB-CHAR) |  |
| [DB_NUM_1](#DB-NUM-1) |  |
| [DB_NUM_2](#DB-NUM-2) |  |
| [DB_NUM_3](#DB-NUM-3) |  |
| [DB_NUM_4](#DB-NUM-4) |  |
| [DOLLAR_TEXT](#DOLLAR-TEXT) | Numeric formatting. |
| [FIRST_CAP](#FIRST-CAP) | Text formatting. |
| [GANADA](#GANADA) | Numeric formatting. |
| [GB_1](#GB-1) | Numeric formatting. |
| [GB_2](#GB-2) | Numeric formatting. |
| [GB_3](#GB-3) | Numeric formatting. |
| [GB_4](#GB-4) | Numeric formatting. |
| [HEBREW_1](#HEBREW-1) | Numeric formatting. |
| [HEBREW_2](#HEBREW-2) | Numeric formatting. |
| [HEX](#HEX) | Numeric formatting. |
| [HINDI_ARABIC](#HINDI-ARABIC) | Numeric formatting. |
| [HINDI_CARD_TEXT](#HINDI-CARD-TEXT) | Numeric formatting. |
| [HINDI_LETTER_1](#HINDI-LETTER-1) | Numeric formatting. |
| [HINDI_LETTER_2](#HINDI-LETTER-2) | Numeric formatting. |
| [IROHA](#IROHA) | Numeric formatting. |
| [KANJI_NUM_1](#KANJI-NUM-1) | Numeric formatting. |
| [KANJI_NUM_2](#KANJI-NUM-2) | Numeric formatting. |
| [KANJI_NUM_3](#KANJI-NUM-3) | Numeric formatting. |
| [LOWER](#LOWER) | Text formatting. |
| [LOWERCASE_ALPHABETIC](#LOWERCASE-ALPHABETIC) | Numeric formatting. |
| [LOWERCASE_ROMAN](#LOWERCASE-ROMAN) | Numeric formatting. |
| [MERGE_FORMAT](#MERGE-FORMAT) | Field result formatting. |
| [MERGE_FORMAT_INET](#MERGE-FORMAT-INET) | Field result formatting. |
| [NONE](#NONE) | Used to specify a missing general format. |
| [ORDINAL](#ORDINAL) | Numeric formatting. |
| [ORD_TEXT](#ORD-TEXT) | Numeric formatting. |
| [SB_CHAR](#SB-CHAR) |  |
| [THAI_ARABIC](#THAI-ARABIC) | Numeric formatting. |
| [THAI_CARD_TEXT](#THAI-CARD-TEXT) | Numeric formatting. |
| [THAI_LETTER](#THAI-LETTER) | Numeric formatting. |
| [UPPER](#UPPER) | Text formatting. |
| [UPPERCASE_ALPHABETIC](#UPPERCASE-ALPHABETIC) | Numeric formatting. |
| [UPPERCASE_ROMAN](#UPPERCASE-ROMAN) | Numeric formatting. |
| [VIET_CARD_TEXT](#VIET-CARD-TEXT) | Numeric formatting. |
| [ZODIAC_1](#ZODIAC-1) | Numeric formatting. |
| [ZODIAC_2](#ZODIAC-2) | Numeric formatting. |
| [ZODIAC_3](#ZODIAC-3) | Numeric formatting. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String generalFormatName)](#fromName-java.lang.String) |  |
| [getName(int generalFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int generalFormat)](#toString-int) |  |
### AIUEO {#AIUEO}
```
public static int AIUEO
```


Numeric formatting. Formats a numeric result using hiragana characters in the traditional a-i-u-e-o order.

### ARABIC {#ARABIC}
```
public static int ARABIC
```


Numeric formatting. Formats a numeric result using Arabic cardinal numerals.

### ARABIC_ABJAD {#ARABIC-ABJAD}
```
public static int ARABIC_ABJAD
```


Numeric formatting. Formats a numeric result using ascending Abjad numerals.

### ARABIC_ALPHA {#ARABIC-ALPHA}
```
public static int ARABIC_ALPHA
```


Numeric formatting. Formats a numeric result using characters in the Arabic alphabet.

### ARABIC_DASH {#ARABIC-DASH}
```
public static int ARABIC_DASH
```


Numeric formatting. Formats a numeric result using Arabic cardinal numerals, with a prefix of "- " and a suffix of " -".

### BAHT_TEXT {#BAHT-TEXT}
```
public static int BAHT_TEXT
```


Numeric formatting. Formats a numeric result in the Thai counting system.

### CAPS {#CAPS}
```
public static int CAPS
```


Text formatting. Capitalizes the first letter of each word.

### CARD_TEXT {#CARD-TEXT}
```
public static int CARD_TEXT
```


Numeric formatting. Cardinal text (One, Two, Three, ...).

### CHAR_FORMAT {#CHAR-FORMAT}
```
public static int CHAR_FORMAT
```


Field result formatting. The CHARFORMAT instruction.

### CHINESE_NUM_1 {#CHINESE-NUM-1}
```
public static int CHINESE_NUM_1
```


Numeric formatting. Formats a numeric result using ascending numbers from the appropriate counting system.

### CHINESE_NUM_2 {#CHINESE-NUM-2}
```
public static int CHINESE_NUM_2
```


Numeric formatting. Formats a numeric result using sequential numbers from the appropriate legal format.

### CHINESE_NUM_3 {#CHINESE-NUM-3}
```
public static int CHINESE_NUM_3
```


Numeric formatting. Formats a numeric result using sequential numbers from the appropriate counting thousand system.

### CHOSUNG {#CHOSUNG}
```
public static int CHOSUNG
```


Numeric formatting. Formats a numeric result using sequential numbers from the Korean Chosung format.

### CIRCLE_NUM {#CIRCLE-NUM}
```
public static int CIRCLE_NUM
```


Numeric formatting. Formats a numeric result using decimal numbering enclosed in a circle, using the enclosed alphanumeric glyph character for numbers in the range 1\\u201320.

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


Numeric formatting. Dollar text (One, Two, Three, ... + AND 55/100).

### FIRST_CAP {#FIRST-CAP}
```
public static int FIRST_CAP
```


Text formatting. Capitalizes the first letter of the first word.

### GANADA {#GANADA}
```
public static int GANADA
```


Numeric formatting. Formats a numeric result using sequential numbers from the Korean Ganada format.

### GB_1 {#GB-1}
```
public static int GB_1
```


Numeric formatting. Formats a numeric result using decimal numbering followed by a period, using the enclosed alphanumeric glyph character.

### GB_2 {#GB-2}
```
public static int GB_2
```


Numeric formatting. Formats a numeric result using decimal numbering enclosed in parenthesis, using the enclosed alphanumeric glyph character.

### GB_3 {#GB-3}
```
public static int GB_3
```


Numeric formatting. Formats a numeric result using decimal numbering enclosed in a circle, using the enclosed alphanumeric glyph character.

### GB_4 {#GB-4}
```
public static int GB_4
```


Numeric formatting. Formats a numeric result using decimal numbering enclosed in a circle, using the enclosed alphanumeric glyph character.

### HEBREW_1 {#HEBREW-1}
```
public static int HEBREW_1
```


Numeric formatting. Formats a numeric result using Hebrew numerals.

### HEBREW_2 {#HEBREW-2}
```
public static int HEBREW_2
```


Numeric formatting. Formats a numeric result using the Hebrew alphabet.

### HEX {#HEX}
```
public static int HEX
```


Numeric formatting. Formats the numeric result using uppercase hexadecimal digits.

### HINDI_ARABIC {#HINDI-ARABIC}
```
public static int HINDI_ARABIC
```


Numeric formatting. Formats a numeric result using Hindi numbers.

### HINDI_CARD_TEXT {#HINDI-CARD-TEXT}
```
public static int HINDI_CARD_TEXT
```


Numeric formatting. Formats a numeric result using sequential numbers from the Hindi counting system.

### HINDI_LETTER_1 {#HINDI-LETTER-1}
```
public static int HINDI_LETTER_1
```


Numeric formatting. Formats a numeric result using Hindi vowels.

### HINDI_LETTER_2 {#HINDI-LETTER-2}
```
public static int HINDI_LETTER_2
```


Numeric formatting. Formats a numeric result using Hindi consonants.

### IROHA {#IROHA}
```
public static int IROHA
```


Numeric formatting. Formats a numeric result using the Japanese iroha.

### KANJI_NUM_1 {#KANJI-NUM-1}
```
public static int KANJI_NUM_1
```


Numeric formatting. Formats a numeric result using a Japanese style using the appropriate counting system.

### KANJI_NUM_2 {#KANJI-NUM-2}
```
public static int KANJI_NUM_2
```


Numeric formatting. Formats a numeric result using the appropriate counting system.

### KANJI_NUM_3 {#KANJI-NUM-3}
```
public static int KANJI_NUM_3
```


Numeric formatting. Formats a numeric result using the appropriate counting system.

### LOWER {#LOWER}
```
public static int LOWER
```


Text formatting. All letters are lowercase.

### LOWERCASE_ALPHABETIC {#LOWERCASE-ALPHABETIC}
```
public static int LOWERCASE_ALPHABETIC
```


Numeric formatting. Formats a numeric result as one or more occurrences of an lowercase alphabetic Latin character.

### LOWERCASE_ROMAN {#LOWERCASE-ROMAN}
```
public static int LOWERCASE_ROMAN
```


Numeric formatting. Lowercase Roman (i, ii, iii, ...).

### MERGE_FORMAT {#MERGE-FORMAT}
```
public static int MERGE_FORMAT
```


Field result formatting. The MERGEFORMAT instruction.

### MERGE_FORMAT_INET {#MERGE-FORMAT-INET}
```
public static int MERGE_FORMAT_INET
```


Field result formatting. The MERGEFORMATINET instruction.

### NONE {#NONE}
```
public static int NONE
```


Used to specify a missing general format.

### ORDINAL {#ORDINAL}
```
public static int ORDINAL
```


Numeric formatting. Ordinal (1st, 2nd, 3rd, ...).

### ORD_TEXT {#ORD-TEXT}
```
public static int ORD_TEXT
```


Numeric formatting. Ordinal text (First, Second, Third, ...).

### SB_CHAR {#SB-CHAR}
```
public static int SB_CHAR
```


### THAI_ARABIC {#THAI-ARABIC}
```
public static int THAI_ARABIC
```


Numeric formatting. Formats a numeric result using Thai numbers.

### THAI_CARD_TEXT {#THAI-CARD-TEXT}
```
public static int THAI_CARD_TEXT
```


Numeric formatting. Formats a numeric result using sequential numbers from the Thai counting system.

### THAI_LETTER {#THAI-LETTER}
```
public static int THAI_LETTER
```


Numeric formatting. Formats a numeric result using Thai letters.

### UPPER {#UPPER}
```
public static int UPPER
```


Text formatting. All letters are uppercase.

### UPPERCASE_ALPHABETIC {#UPPERCASE-ALPHABETIC}
```
public static int UPPERCASE_ALPHABETIC
```


Numeric formatting. Formats a numeric result as one or more occurrences of an uppercase alphabetic Latin character.

### UPPERCASE_ROMAN {#UPPERCASE-ROMAN}
```
public static int UPPERCASE_ROMAN
```


Numeric formatting. Uppercase Roman (I, II, III, ...).

### VIET_CARD_TEXT {#VIET-CARD-TEXT}
```
public static int VIET_CARD_TEXT
```


Numeric formatting. Formats a numeric result using Vietnamese numerals.

### ZODIAC_1 {#ZODIAC-1}
```
public static int ZODIAC_1
```


Numeric formatting. Formats a numeric result using sequential numerical traditional ideographs.

### ZODIAC_2 {#ZODIAC-2}
```
public static int ZODIAC_2
```


Numeric formatting. Formats a numeric result using sequential zodiac ideographs.

### ZODIAC_3 {#ZODIAC-3}
```
public static int ZODIAC_3
```


Numeric formatting. Formats a numeric result using sequential traditional zodiac ideographs.

### length {#length}
```
public static int length
```


### fromName(String generalFormatName) {#fromName-java.lang.String}
```
public static int fromName(String generalFormatName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| generalFormatName | java.lang.String |  |

**Returns:**
int
### getName(int generalFormat) {#getName-int}
```
public static String getName(int generalFormat)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| generalFormat | int |  |

**Returns:**
java.lang.String
