---
title: GeneralFormat
second_title: Aspose.Words for Java API Reference
description: Specifies a general format that is applied to a numeric text or any field result.
type: docs
weight: 304
url: /java/com.aspose.words/generalformat/
---

**Inheritance:**
java.lang.Object
```
public class GeneralFormat
```

Specifies a general format that is applied to a numeric, text, or any field result. A field may have a combination of general formats.
## Fields

| Field | Description |
| --- | --- |
| [NONE](#NONE) | Used to specify a missing general format. |
| [AIUEO](#AIUEO) | Numeric formatting. |
| [UPPERCASE_ALPHABETIC](#UPPERCASE-ALPHABETIC) | Numeric formatting. |
| [LOWERCASE_ALPHABETIC](#LOWERCASE-ALPHABETIC) | Numeric formatting. |
| [ARABIC](#ARABIC) | Numeric formatting. |
| [ARABIC_ABJAD](#ARABIC-ABJAD) | Numeric formatting. |
| [ARABIC_ALPHA](#ARABIC-ALPHA) | Numeric formatting. |
| [ARABIC_DASH](#ARABIC-DASH) | Numeric formatting. |
| [BAHT_TEXT](#BAHT-TEXT) | Numeric formatting. |
| [CARD_TEXT](#CARD-TEXT) | Numeric formatting. |
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
| [ORDINAL](#ORDINAL) | Numeric formatting. |
| [ORD_TEXT](#ORD-TEXT) | Numeric formatting. |
| [UPPERCASE_ROMAN](#UPPERCASE-ROMAN) | Numeric formatting. |
| [LOWERCASE_ROMAN](#LOWERCASE-ROMAN) | Numeric formatting. |
| [SB_CHAR](#SB-CHAR) |  |
| [THAI_ARABIC](#THAI-ARABIC) | Numeric formatting. |
| [THAI_CARD_TEXT](#THAI-CARD-TEXT) | Numeric formatting. |
| [THAI_LETTER](#THAI-LETTER) | Numeric formatting. |
| [VIET_CARD_TEXT](#VIET-CARD-TEXT) | Numeric formatting. |
| [ZODIAC_1](#ZODIAC-1) | Numeric formatting. |
| [ZODIAC_2](#ZODIAC-2) | Numeric formatting. |
| [ZODIAC_3](#ZODIAC-3) | Numeric formatting. |
| [CAPS](#CAPS) | Text formatting. |
| [FIRST_CAP](#FIRST-CAP) | Text formatting. |
| [LOWER](#LOWER) | Text formatting. |
| [UPPER](#UPPER) | Text formatting. |
| [CHAR_FORMAT](#CHAR-FORMAT) | Field result formatting. |
| [MERGE_FORMAT](#MERGE-FORMAT) | Field result formatting. |
| [MERGE_FORMAT_INET](#MERGE-FORMAT-INET) | Field result formatting. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int generalFormat)](#getName-int-) |  |
| [toString(int generalFormat)](#toString-int-) |  |
| [fromName(String generalFormatName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### NONE {#NONE}
```
public static int NONE
```


Used to specify a missing general format.

### AIUEO {#AIUEO}
```
public static int AIUEO
```


Numeric formatting. Formats a numeric result using hiragana characters in the traditional a-i-u-e-o order.

### UPPERCASE_ALPHABETIC {#UPPERCASE-ALPHABETIC}
```
public static int UPPERCASE_ALPHABETIC
```


Numeric formatting. Formats a numeric result as one or more occurrences of an uppercase alphabetic Latin character.

### LOWERCASE_ALPHABETIC {#LOWERCASE-ALPHABETIC}
```
public static int LOWERCASE_ALPHABETIC
```


Numeric formatting. Formats a numeric result as one or more occurrences of an lowercase alphabetic Latin character.

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

### CARD_TEXT {#CARD-TEXT}
```
public static int CARD_TEXT
```


Numeric formatting. Cardinal text (One, Two, Three, ...).

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

### UPPERCASE_ROMAN {#UPPERCASE-ROMAN}
```
public static int UPPERCASE_ROMAN
```


Numeric formatting. Uppercase Roman (I, II, III, ...).

### LOWERCASE_ROMAN {#LOWERCASE-ROMAN}
```
public static int LOWERCASE_ROMAN
```


Numeric formatting. Lowercase Roman (i, ii, iii, ...).

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

### CAPS {#CAPS}
```
public static int CAPS
```


Text formatting. Capitalizes the first letter of each word.

### FIRST_CAP {#FIRST-CAP}
```
public static int FIRST_CAP
```


Text formatting. Capitalizes the first letter of the first word.

### LOWER {#LOWER}
```
public static int LOWER
```


Text formatting. All letters are lowercase.

### UPPER {#UPPER}
```
public static int UPPER
```


Text formatting. All letters are uppercase.

### CHAR_FORMAT {#CHAR-FORMAT}
```
public static int CHAR_FORMAT
```


Field result formatting. The CHARFORMAT instruction.

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

### length {#length}
```
public static int length
```


### getName(int generalFormat) {#getName-int-}
```
public static String getName(int generalFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| generalFormat | int |  |

**Returns:**
java.lang.String
### toString(int generalFormat) {#toString-int-}
```
public static String toString(int generalFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| generalFormat | int |  |

**Returns:**
java.lang.String
### fromName(String generalFormatName) {#fromName-java.lang.String-}
```
public static int fromName(String generalFormatName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| generalFormatName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
