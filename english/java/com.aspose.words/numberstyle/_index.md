---
title: NumberStyle
linktitle: NumberStyle
second_title: Aspose.Words for Java
description: Specifies the number style for a list footnotes and endnotes page numbers in Java.
type: docs
weight: 479
url: /java/com.aspose.words/numberstyle/
---

**Inheritance:**
java.lang.Object
```
public class NumberStyle
```

Specifies the number style for a list, footnotes and endnotes, page numbers.

 **Examples:** 

Shows how to apply custom list formatting to paragraphs when using DocumentBuilder.

```

 Document doc = new Document();

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // Create a list from a Microsoft Word template, and customize the first two of its list levels.
 List docList = doc.getLists().add(ListTemplate.NUMBER_DEFAULT);

 ListLevel listLevel = docList.getListLevels().get(0);
 listLevel.getFont().setColor(Color.RED);
 listLevel.getFont().setSize(24.0);
 listLevel.setNumberStyle(NumberStyle.ORDINAL_TEXT);
 listLevel.setStartAt(21);
 listLevel.setNumberFormat(" ");

 listLevel.setNumberPosition(-36);
 listLevel.setTextPosition(144.0);
 listLevel.setTabPosition(144.0);

 listLevel = docList.getListLevels().get(1);
 listLevel.setAlignment(ListLevelAlignment.RIGHT);
 listLevel.setNumberStyle(NumberStyle.BULLET);
 listLevel.getFont().setName("Wingdings");
 listLevel.getFont().setColor(Color.BLUE);
 listLevel.getFont().setSize(24.0);

 // This NumberFormat value will create star-shaped bullet list symbols.
 listLevel.setNumberFormat("\uf0af");
 listLevel.setTrailingCharacter(ListTrailingCharacter.SPACE);
 listLevel.setNumberPosition(144.0);

 // Create paragraphs and apply both list levels of our custom list formatting to them.
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getListFormat().setList(docList);
 builder.writeln("The quick brown fox...");
 builder.writeln("The quick brown fox...");

 builder.getListFormat().listIndent();
 builder.writeln("jumped over the lazy dog.");
 builder.writeln("jumped over the lazy dog.");

 builder.getListFormat().listOutdent();
 builder.writeln("The quick brown fox...");

 builder.getListFormat().removeNumbers();

 builder.getDocument().save(getArtifactsDir() + "Lists.CreateCustomList.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [AIUEO](#AIUEO) | Aiueo full width |
| [AIUEO_HALF_WIDTH](#AIUEO-HALF-WIDTH) | Aiueo |
| [ARABIC](#ARABIC) | Arabic numbering (1, 2, 3, ...) |
| [ARABIC_1](#ARABIC-1) | Arabic alpha |
| [ARABIC_2](#ARABIC-2) | Arabic abjad |
| [ARABIC_FULL_WIDTH](#ARABIC-FULL-WIDTH) | Full-width Arabic: 1, 2, 3, 4 |
| [ARABIC_HALF_WIDTH](#ARABIC-HALF-WIDTH) | Half-width Arabic: 1, 2, 3, 4 |
| [BULLET](#BULLET) | Bullet (check the character code in the text) |
| [CHICAGO_MANUAL](#CHICAGO-MANUAL) | Chicago Manual of Style: \*, \\u2020, \\u2020 |
| [CHOSUNG](#CHOSUNG) | Korea Chosung |
| [CUSTOM](#CUSTOM) | Custom number format. |
| [DECIMAL_FULL_WIDTH](#DECIMAL-FULL-WIDTH) | Decimal full width: 1, 2, 3, 4 |
| [GANADA](#GANADA) | Korean Ganada |
| [GB_1](#GB-1) | Enclosed full stop |
| [GB_2](#GB-2) | Enclosed parenthesis |
| [GB_3](#GB-3) | Enclosed circle Chinese |
| [GB_4](#GB-4) | Ideograph enclosed circle |
| [HANGUL](#HANGUL) | Korea legal |
| [HANJA](#HANJA) | Korea digital2 |
| [HANJA_READ](#HANJA-READ) | Korean digital |
| [HANJA_READ_DIGIT](#HANJA-READ-DIGIT) | Korean counting |
| [HEBREW_1](#HEBREW-1) | Hebrew-1 |
| [HEBREW_2](#HEBREW-2) | Hebrew-2 |
| [HEX](#HEX) | Hexadecimal: 8, 9, A, B, C, D, E, F, 10, 11, 12 |
| [HINDI_ARABIC](#HINDI-ARABIC) | Hindi numbers |
| [HINDI_CARDINAL_TEXT](#HINDI-CARDINAL-TEXT) | Hindi descriptive (cardinals) |
| [HINDI_LETTER_1](#HINDI-LETTER-1) | Hindi vowels |
| [HINDI_LETTER_2](#HINDI-LETTER-2) | Hindi consonants |
| [IROHA](#IROHA) | Iroha full width |
| [IROHA_HALF_WIDTH](#IROHA-HALF-WIDTH) | Iroha |
| [KANJI](#KANJI) | Ideograph-digital |
| [KANJI_DIGIT](#KANJI-DIGIT) | Japanese counting |
| [KANJI_TRADITIONAL](#KANJI-TRADITIONAL) | Japanese legal |
| [KANJI_TRADITIONAL_2](#KANJI-TRADITIONAL-2) | Japanese digital ten thousand |
| [LEADING_ZERO](#LEADING-ZERO) | Leading Zero (01, 02,..., 09, 10, 11,..., 99, 100, 101,...) |
| [LOWERCASE_LETTER](#LOWERCASE-LETTER) | Lower case letter (a, b, c, ...) |
| [LOWERCASE_ROMAN](#LOWERCASE-ROMAN) | Lower case Roman (i, ii, iii, ...) |
| [LOWERCASE_RUSSIAN](#LOWERCASE-RUSSIAN) | Lowercase Russian alphabet |
| [NONE](#NONE) | No bullet or number. |
| [NUMBER](#NUMBER) | Numbered (One, Two, Three, ...) |
| [NUMBER_IN_CIRCLE](#NUMBER-IN-CIRCLE) | Enclosed circles |
| [NUMBER_IN_DASH](#NUMBER-IN-DASH) | Page number format: - 1 -, - 2 -, - 3 -, - 4 - |
| [ORDINAL](#ORDINAL) | Ordinal (1st, 2nd, 3rd, ...) |
| [ORDINAL_TEXT](#ORDINAL-TEXT) | Ordinal (text) (First, Second, Third, ...) |
| [SIMP_CHIN_NUM_1](#SIMP-CHIN-NUM-1) | Chinese counting |
| [SIMP_CHIN_NUM_2](#SIMP-CHIN-NUM-2) | Chinese legal simplified |
| [SIMP_CHIN_NUM_3](#SIMP-CHIN-NUM-3) | Chinese counting thousand |
| [SIMP_CHIN_NUM_4](#SIMP-CHIN-NUM-4) | Chinese (not implemented) |
| [THAI_ARABIC](#THAI-ARABIC) | Thai numbers |
| [THAI_CARDINAL_TEXT](#THAI-CARDINAL-TEXT) | Thai descriptive (cardinals) |
| [THAI_LETTER](#THAI-LETTER) | Thai letters |
| [TRAD_CHIN_NUM_1](#TRAD-CHIN-NUM-1) | Taiwanese counting |
| [TRAD_CHIN_NUM_2](#TRAD-CHIN-NUM-2) | Ideograph legal traditional |
| [TRAD_CHIN_NUM_3](#TRAD-CHIN-NUM-3) | Taiwanese counting thousand |
| [TRAD_CHIN_NUM_4](#TRAD-CHIN-NUM-4) | Taiwanese digital |
| [UPPERCASE_LETTER](#UPPERCASE-LETTER) | Upper case Letter (A, B, C, ...) |
| [UPPERCASE_ROMAN](#UPPERCASE-ROMAN) | Upper case Roman (I, II, III, ...) |
| [UPPERCASE_RUSSIAN](#UPPERCASE-RUSSIAN) | Uppercase Russian alphabet |
| [VIET_CARDINAL_TEXT](#VIET-CARDINAL-TEXT) | Vietnamese descriptive (cardinals) |
| [ZODIAC_1](#ZODIAC-1) | Ideograph traditional |
| [ZODIAC_2](#ZODIAC-2) | Ideograph Zodiac |
| [ZODIAC_3](#ZODIAC-3) | Ideograph Zodiac traditional |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String numberStyleName)](#fromName-java.lang.String) |  |
| [getName(int numberStyle)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int numberStyle)](#toString-int) |  |
### AIUEO {#AIUEO}
```
public static int AIUEO
```


Aiueo full width

### AIUEO_HALF_WIDTH {#AIUEO-HALF-WIDTH}
```
public static int AIUEO_HALF_WIDTH
```


Aiueo

### ARABIC {#ARABIC}
```
public static int ARABIC
```


Arabic numbering (1, 2, 3, ...)

### ARABIC_1 {#ARABIC-1}
```
public static int ARABIC_1
```


Arabic alpha

### ARABIC_2 {#ARABIC-2}
```
public static int ARABIC_2
```


Arabic abjad

### ARABIC_FULL_WIDTH {#ARABIC-FULL-WIDTH}
```
public static int ARABIC_FULL_WIDTH
```


Full-width Arabic: 1, 2, 3, 4

### ARABIC_HALF_WIDTH {#ARABIC-HALF-WIDTH}
```
public static int ARABIC_HALF_WIDTH
```


Half-width Arabic: 1, 2, 3, 4

### BULLET {#BULLET}
```
public static int BULLET
```


Bullet (check the character code in the text)

### CHICAGO_MANUAL {#CHICAGO-MANUAL}
```
public static int CHICAGO_MANUAL
```


Chicago Manual of Style: \*, \\u2020, \\u2020

### CHOSUNG {#CHOSUNG}
```
public static int CHOSUNG
```


Korea Chosung

### CUSTOM {#CUSTOM}
```
public static int CUSTOM
```


Custom number format. It is supported by DOCX format only.

### DECIMAL_FULL_WIDTH {#DECIMAL-FULL-WIDTH}
```
public static int DECIMAL_FULL_WIDTH
```


Decimal full width: 1, 2, 3, 4

### GANADA {#GANADA}
```
public static int GANADA
```


Korean Ganada

### GB_1 {#GB-1}
```
public static int GB_1
```


Enclosed full stop

### GB_2 {#GB-2}
```
public static int GB_2
```


Enclosed parenthesis

### GB_3 {#GB-3}
```
public static int GB_3
```


Enclosed circle Chinese

### GB_4 {#GB-4}
```
public static int GB_4
```


Ideograph enclosed circle

### HANGUL {#HANGUL}
```
public static int HANGUL
```


Korea legal

### HANJA {#HANJA}
```
public static int HANJA
```


Korea digital2

### HANJA_READ {#HANJA-READ}
```
public static int HANJA_READ
```


Korean digital

### HANJA_READ_DIGIT {#HANJA-READ-DIGIT}
```
public static int HANJA_READ_DIGIT
```


Korean counting

### HEBREW_1 {#HEBREW-1}
```
public static int HEBREW_1
```


Hebrew-1

### HEBREW_2 {#HEBREW-2}
```
public static int HEBREW_2
```


Hebrew-2

### HEX {#HEX}
```
public static int HEX
```


Hexadecimal: 8, 9, A, B, C, D, E, F, 10, 11, 12

### HINDI_ARABIC {#HINDI-ARABIC}
```
public static int HINDI_ARABIC
```


Hindi numbers

### HINDI_CARDINAL_TEXT {#HINDI-CARDINAL-TEXT}
```
public static int HINDI_CARDINAL_TEXT
```


Hindi descriptive (cardinals)

### HINDI_LETTER_1 {#HINDI-LETTER-1}
```
public static int HINDI_LETTER_1
```


Hindi vowels

### HINDI_LETTER_2 {#HINDI-LETTER-2}
```
public static int HINDI_LETTER_2
```


Hindi consonants

### IROHA {#IROHA}
```
public static int IROHA
```


Iroha full width

### IROHA_HALF_WIDTH {#IROHA-HALF-WIDTH}
```
public static int IROHA_HALF_WIDTH
```


Iroha

### KANJI {#KANJI}
```
public static int KANJI
```


Ideograph-digital

### KANJI_DIGIT {#KANJI-DIGIT}
```
public static int KANJI_DIGIT
```


Japanese counting

### KANJI_TRADITIONAL {#KANJI-TRADITIONAL}
```
public static int KANJI_TRADITIONAL
```


Japanese legal

### KANJI_TRADITIONAL_2 {#KANJI-TRADITIONAL-2}
```
public static int KANJI_TRADITIONAL_2
```


Japanese digital ten thousand

### LEADING_ZERO {#LEADING-ZERO}
```
public static int LEADING_ZERO
```


Leading Zero (01, 02,..., 09, 10, 11,..., 99, 100, 101,...)

### LOWERCASE_LETTER {#LOWERCASE-LETTER}
```
public static int LOWERCASE_LETTER
```


Lower case letter (a, b, c, ...)

### LOWERCASE_ROMAN {#LOWERCASE-ROMAN}
```
public static int LOWERCASE_ROMAN
```


Lower case Roman (i, ii, iii, ...)

### LOWERCASE_RUSSIAN {#LOWERCASE-RUSSIAN}
```
public static int LOWERCASE_RUSSIAN
```


Lowercase Russian alphabet

### NONE {#NONE}
```
public static int NONE
```


No bullet or number.

### NUMBER {#NUMBER}
```
public static int NUMBER
```


Numbered (One, Two, Three, ...)

### NUMBER_IN_CIRCLE {#NUMBER-IN-CIRCLE}
```
public static int NUMBER_IN_CIRCLE
```


Enclosed circles

### NUMBER_IN_DASH {#NUMBER-IN-DASH}
```
public static int NUMBER_IN_DASH
```


Page number format: - 1 -, - 2 -, - 3 -, - 4 -

### ORDINAL {#ORDINAL}
```
public static int ORDINAL
```


Ordinal (1st, 2nd, 3rd, ...)

### ORDINAL_TEXT {#ORDINAL-TEXT}
```
public static int ORDINAL_TEXT
```


Ordinal (text) (First, Second, Third, ...)

### SIMP_CHIN_NUM_1 {#SIMP-CHIN-NUM-1}
```
public static int SIMP_CHIN_NUM_1
```


Chinese counting

### SIMP_CHIN_NUM_2 {#SIMP-CHIN-NUM-2}
```
public static int SIMP_CHIN_NUM_2
```


Chinese legal simplified

### SIMP_CHIN_NUM_3 {#SIMP-CHIN-NUM-3}
```
public static int SIMP_CHIN_NUM_3
```


Chinese counting thousand

### SIMP_CHIN_NUM_4 {#SIMP-CHIN-NUM-4}
```
public static int SIMP_CHIN_NUM_4
```


Chinese (not implemented)

### THAI_ARABIC {#THAI-ARABIC}
```
public static int THAI_ARABIC
```


Thai numbers

### THAI_CARDINAL_TEXT {#THAI-CARDINAL-TEXT}
```
public static int THAI_CARDINAL_TEXT
```


Thai descriptive (cardinals)

### THAI_LETTER {#THAI-LETTER}
```
public static int THAI_LETTER
```


Thai letters

### TRAD_CHIN_NUM_1 {#TRAD-CHIN-NUM-1}
```
public static int TRAD_CHIN_NUM_1
```


Taiwanese counting

### TRAD_CHIN_NUM_2 {#TRAD-CHIN-NUM-2}
```
public static int TRAD_CHIN_NUM_2
```


Ideograph legal traditional

### TRAD_CHIN_NUM_3 {#TRAD-CHIN-NUM-3}
```
public static int TRAD_CHIN_NUM_3
```


Taiwanese counting thousand

### TRAD_CHIN_NUM_4 {#TRAD-CHIN-NUM-4}
```
public static int TRAD_CHIN_NUM_4
```


Taiwanese digital

### UPPERCASE_LETTER {#UPPERCASE-LETTER}
```
public static int UPPERCASE_LETTER
```


Upper case Letter (A, B, C, ...)

### UPPERCASE_ROMAN {#UPPERCASE-ROMAN}
```
public static int UPPERCASE_ROMAN
```


Upper case Roman (I, II, III, ...)

### UPPERCASE_RUSSIAN {#UPPERCASE-RUSSIAN}
```
public static int UPPERCASE_RUSSIAN
```


Uppercase Russian alphabet

### VIET_CARDINAL_TEXT {#VIET-CARDINAL-TEXT}
```
public static int VIET_CARDINAL_TEXT
```


Vietnamese descriptive (cardinals)

### ZODIAC_1 {#ZODIAC-1}
```
public static int ZODIAC_1
```


Ideograph traditional

### ZODIAC_2 {#ZODIAC-2}
```
public static int ZODIAC_2
```


Ideograph Zodiac

### ZODIAC_3 {#ZODIAC-3}
```
public static int ZODIAC_3
```


Ideograph Zodiac traditional

### length {#length}
```
public static int length
```


### fromName(String numberStyleName) {#fromName-java.lang.String}
```
public static int fromName(String numberStyleName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| numberStyleName | java.lang.String |  |

**Returns:**
int
### getName(int numberStyle) {#getName-int}
```
public static String getName(int numberStyle)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| numberStyle | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int numberStyle) {#toString-int}
```
public static String toString(int numberStyle)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| numberStyle | int |  |

**Returns:**
java.lang.String
