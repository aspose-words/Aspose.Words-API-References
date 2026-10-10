---
title: "GeneralFormat"
linktitle: "GeneralFormat"
second_title: "Aspose.Words für Java"
description: "Gibt ein allgemeines Format an, das auf einen numerischen Text oder ein beliebiges Feldresultat in Java angewendet wird."
type: docs
weight: 355
url: /de/java/com.aspose.words/generalformat/
---

**Inheritance:**
java.lang.Object
```
public class GeneralFormat
```

Gibt ein allgemeines Format an, das auf ein numerisches, Text- oder beliebiges Feldresultat angewendet wird. Ein Feld kann eine Kombination aus allgemeinen Formaten haben.

 **Examples:** 

Zeigt, wie man Feldresultate formatiert.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [AIUEO](#AIUEO) | Numerische Formatierung. |
| [ARABIC](#ARABIC) | Numerische Formatierung. |
| [ARABIC_ABJAD](#ARABIC-ABJAD) | Numerische Formatierung. |
| [ARABIC_ALPHA](#ARABIC-ALPHA) | Numerische Formatierung. |
| [ARABIC_DASH](#ARABIC-DASH) | Numerische Formatierung. |
| [BAHT_TEXT](#BAHT-TEXT) | Numerische Formatierung. |
| [CAPS](#CAPS) | Textformatierung. |
| [CARD_TEXT](#CARD-TEXT) | Numerische Formatierung. |
| [CHAR_FORMAT](#CHAR-FORMAT) | Feldresultat-Formatierung. |
| [CHINESE_NUM_1](#CHINESE-NUM-1) | Numerische Formatierung. |
| [CHINESE_NUM_2](#CHINESE-NUM-2) | Numerische Formatierung. |
| [CHINESE_NUM_3](#CHINESE-NUM-3) | Numerische Formatierung. |
| [CHOSUNG](#CHOSUNG) | Numerische Formatierung. |
| [CIRCLE_NUM](#CIRCLE-NUM) | Numerische Formatierung. |
| [DB_CHAR](#DB-CHAR) |  |
| [DB_NUM_1](#DB-NUM-1) |  |
| [DB_NUM_2](#DB-NUM-2) |  |
| [DB_NUM_3](#DB-NUM-3) |  |
| [DB_NUM_4](#DB-NUM-4) |  |
| [DOLLAR_TEXT](#DOLLAR-TEXT) | Numerische Formatierung. |
| [FIRST_CAP](#FIRST-CAP) | Textformatierung. |
| [GANADA](#GANADA) | Numerische Formatierung. |
| [GB_1](#GB-1) | Numerische Formatierung. |
| [GB_2](#GB-2) | Numerische Formatierung. |
| [GB_3](#GB-3) | Numerische Formatierung. |
| [GB_4](#GB-4) | Numerische Formatierung. |
| [HEBREW_1](#HEBREW-1) | Numerische Formatierung. |
| [HEBREW_2](#HEBREW-2) | Numerische Formatierung. |
| [HEX](#HEX) | Numerische Formatierung. |
| [HINDI_ARABIC](#HINDI-ARABIC) | Numerische Formatierung. |
| [HINDI_CARD_TEXT](#HINDI-CARD-TEXT) | Numerische Formatierung. |
| [HINDI_LETTER_1](#HINDI-LETTER-1) | Numerische Formatierung. |
| [HINDI_LETTER_2](#HINDI-LETTER-2) | Numerische Formatierung. |
| [IROHA](#IROHA) | Numerische Formatierung. |
| [KANJI_NUM_1](#KANJI-NUM-1) | Numerische Formatierung. |
| [KANJI_NUM_2](#KANJI-NUM-2) | Numerische Formatierung. |
| [KANJI_NUM_3](#KANJI-NUM-3) | Numerische Formatierung. |
| [LOWER](#LOWER) | Textformatierung. |
| [LOWERCASE_ALPHABETIC](#LOWERCASE-ALPHABETIC) | Numerische Formatierung. |
| [LOWERCASE_ROMAN](#LOWERCASE-ROMAN) | Numerische Formatierung. |
| [MERGE_FORMAT](#MERGE-FORMAT) | Feldresultat-Formatierung. |
| [MERGE_FORMAT_INET](#MERGE-FORMAT-INET) | Feldresultat-Formatierung. |
| [NONE](#NONE) | Wird verwendet, um ein fehlendes allgemeines Format anzugeben. |
| [ORDINAL](#ORDINAL) | Numerische Formatierung. |
| [ORD_TEXT](#ORD-TEXT) | Numerische Formatierung. |
| [SB_CHAR](#SB-CHAR) |  |
| [THAI_ARABIC](#THAI-ARABIC) | Numerische Formatierung. |
| [THAI_CARD_TEXT](#THAI-CARD-TEXT) | Numerische Formatierung. |
| [THAI_LETTER](#THAI-LETTER) | Numerische Formatierung. |
| [UPPER](#UPPER) | Textformatierung. |
| [UPPERCASE_ALPHABETIC](#UPPERCASE-ALPHABETIC) | Numerische Formatierung. |
| [UPPERCASE_ROMAN](#UPPERCASE-ROMAN) | Numerische Formatierung. |
| [VIET_CARD_TEXT](#VIET-CARD-TEXT) | Numerische Formatierung. |
| [ZODIAC_1](#ZODIAC-1) | Numerische Formatierung. |
| [ZODIAC_2](#ZODIAC-2) | Numerische Formatierung. |
| [ZODIAC_3](#ZODIAC-3) | Numerische Formatierung. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String generalFormatName)](#fromName-java.lang.String) |  |
| [getName(int generalFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int generalFormat)](#toString-int) |  |
### AIUEO {#AIUEO}
```
public static int AIUEO
```


Numerische Formatierung. Formatiert ein numerisches Ergebnis mit Hiragana-Zeichen in der traditionellen a-i-u-e-o-Reihenfolge.

### ARABIC {#ARABIC}
```
public static int ARABIC
```


Numerische Formatierung. Formatiert ein numerisches Ergebnis mit arabischen Kardinalzahlen.

### ARABIC_ABJAD {#ARABIC-ABJAD}
```
public static int ARABIC_ABJAD
```


Numerische Formatierung. Formatiert ein numerisches Ergebnis mit aufsteigenden Abjad-Ziffern.

### ARABIC_ALPHA {#ARABIC-ALPHA}
```
public static int ARABIC_ALPHA
```


Numerische Formatierung. Formatiert ein numerisches Ergebnis mit Zeichen des arabischen Alphabets.

### ARABIC_DASH {#ARABIC-DASH}
```
public static int ARABIC_DASH
```


Numerische Formatierung. Formatiert ein numerisches Ergebnis mit arabischen Kardinalzahlen, mit dem Präfix "- " und dem Suffix " -".

### BAHT_TEXT {#BAHT-TEXT}
```
public static int BAHT_TEXT
```


Numerische Formatierung. Formatiert ein numerisches Ergebnis im thailändischen Zahlensystem.

### CAPS {#CAPS}
```
public static int CAPS
```


Textformatierung. Kapitalisiert den ersten Buchstaben jedes Wortes.

### CARD_TEXT {#CARD-TEXT}
```
public static int CARD_TEXT
```


Numerische Formatierung. Kardinaltext (Eins, Zwei, Drei, ...).

### CHAR_FORMAT {#CHAR-FORMAT}
```
public static int CHAR_FORMAT
```


Feldresultat-Formatierung. Die CHARFORMAT-Anweisung.

### CHINESE_NUM_1 {#CHINESE-NUM-1}
```
public static int CHINESE_NUM_1
```


Numerische Formatierung. Formatiert ein numerisches Ergebnis mit aufsteigenden Zahlen aus dem entsprechenden Zahlensystem.

### CHINESE_NUM_2 {#CHINESE-NUM-2}
```
public static int CHINESE_NUM_2
```


Numerische Formatierung. Formatiert ein numerisches Ergebnis mit fortlaufenden Zahlen aus dem entsprechenden rechtlichen Format.

### CHINESE_NUM_3 {#CHINESE-NUM-3}
```
public static int CHINESE_NUM_3
```


Numerische Formatierung. Formatiert ein numerisches Ergebnis mit fortlaufenden Zahlen aus dem entsprechenden Tausenderzählungssystem.

### CHOSUNG {#CHOSUNG}
```
public static int CHOSUNG
```


Numerische Formatierung. Formatiert ein numerisches Ergebnis mit fortlaufenden Zahlen aus dem koreanischen Chosung-Format.

### CIRCLE_NUM {#CIRCLE-NUM}
```
public static int CIRCLE_NUM
```


Numerische Formatierung. Formatiert ein numerisches Ergebnis mit dezimaler Nummerierung, die in einem Kreis eingeschlossen ist, wobei das eingeschlossene alphanumerische Glyphenzeichen für Zahlen im Bereich 1\u201320 verwendet wird.

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


Numerische Formatierung. Dollar-Text (One, Two, Three, ... + AND 55/100).

### FIRST_CAP {#FIRST-CAP}
```
public static int FIRST_CAP
```


Textformatierung. Großschreibt den ersten Buchstaben des ersten Wortes.

### GANADA {#GANADA}
```
public static int GANADA
```


Numerische Formatierung. Formatiert ein numerisches Ergebnis mit fortlaufenden Zahlen aus dem koreanischen Ganada-Format.

### GB_1 {#GB-1}
```
public static int GB_1
```


Numerische Formatierung. Formatiert ein numerisches Ergebnis mit dezimaler Nummerierung, gefolgt von einem Punkt, wobei das eingeschlossene alphanumerische Glyphenzeichen verwendet wird.

### GB_2 {#GB-2}
```
public static int GB_2
```


Numerische Formatierung. Formatiert ein numerisches Ergebnis mit dezimaler Nummerierung, die in Klammern eingeschlossen ist, wobei das eingeschlossene alphanumerische Glyphenzeichen verwendet wird.

### GB_3 {#GB-3}
```
public static int GB_3
```


Numerische Formatierung. Formatiert ein numerisches Ergebnis mit dezimaler Nummerierung, die in einem Kreis eingeschlossen ist, wobei das eingeschlossene alphanumerische Glyphenzeichen verwendet wird.

### GB_4 {#GB-4}
```
public static int GB_4
```


Numerische Formatierung. Formatiert ein numerisches Ergebnis mit dezimaler Nummerierung, die in einem Kreis eingeschlossen ist, wobei das eingeschlossene alphanumerische Glyphenzeichen verwendet wird.

### HEBREW_1 {#HEBREW-1}
```
public static int HEBREW_1
```


Numerische Formatierung. Formatiert ein numerisches Ergebnis mit hebräischen Ziffern.

### HEBREW_2 {#HEBREW-2}
```
public static int HEBREW_2
```


Numerische Formatierung. Formatiert ein numerisches Ergebnis mit dem hebräischen Alphabet.

### HEX {#HEX}
```
public static int HEX
```


Numerische Formatierung. Formatiert das numerische Ergebnis mit Großbuchstaben‑Hexadezimalziffern.

### HINDI_ARABIC {#HINDI-ARABIC}
```
public static int HINDI_ARABIC
```


Numerische Formatierung. Formatiert ein numerisches Ergebnis mit Hindi‑Ziffern.

### HINDI_CARD_TEXT {#HINDI-CARD-TEXT}
```
public static int HINDI_CARD_TEXT
```


Numerische Formatierung. Formatiert ein numerisches Ergebnis mit fortlaufenden Zahlen aus dem Hindi‑Zählsystem.

### HINDI_LETTER_1 {#HINDI-LETTER-1}
```
public static int HINDI_LETTER_1
```


Numerische Formatierung. Formatiert ein numerisches Ergebnis mit Hindi‑Vokalen.

### HINDI_LETTER_2 {#HINDI-LETTER-2}
```
public static int HINDI_LETTER_2
```


Numerische Formatierung. Formatiert ein numerisches Ergebnis mit Hindi‑Konsonanten.

### IROHA {#IROHA}
```
public static int IROHA
```


Numerische Formatierung. Formatiert ein numerisches Ergebnis mit dem japanischen Iroha.

### KANJI_NUM_1 {#KANJI-NUM-1}
```
public static int KANJI_NUM_1
```


Numerische Formatierung. Formatiert ein numerisches Ergebnis im japanischen Stil unter Verwendung des entsprechenden Zählsystems.

### KANJI_NUM_2 {#KANJI-NUM-2}
```
public static int KANJI_NUM_2
```


Numerische Formatierung. Formatiert ein numerisches Ergebnis mit dem entsprechenden Zählsystem.

### KANJI_NUM_3 {#KANJI-NUM-3}
```
public static int KANJI_NUM_3
```


Numerische Formatierung. Formatiert ein numerisches Ergebnis mit dem entsprechenden Zählsystem.

### LOWER {#LOWER}
```
public static int LOWER
```


Textformatierung. Alle Buchstaben sind klein geschrieben.

### LOWERCASE_ALPHABETIC {#LOWERCASE-ALPHABETIC}
```
public static int LOWERCASE_ALPHABETIC
```


Numerische Formatierung. Formatiert ein numerisches Ergebnis als ein oder mehrere Vorkommen eines klein geschriebenen alphabetischen lateinischen Zeichens.

### LOWERCASE_ROMAN {#LOWERCASE-ROMAN}
```
public static int LOWERCASE_ROMAN
```


Numerische Formatierung. Kleinbuchstaben‑Römisch (i, ii, iii, ...).

### MERGE_FORMAT {#MERGE-FORMAT}
```
public static int MERGE_FORMAT
```


Feld-Ergebnis-Formatierung. Die MERGEFORMAT‑Anweisung.

### MERGE_FORMAT_INET {#MERGE-FORMAT-INET}
```
public static int MERGE_FORMAT_INET
```


Feld-Ergebnis-Formatierung. Die MERGEFORMATINET‑Anweisung.

### NONE {#NONE}
```
public static int NONE
```


Wird verwendet, um ein fehlendes allgemeines Format anzugeben.

### ORDINAL {#ORDINAL}
```
public static int ORDINAL
```


Numerische Formatierung. Ordinalzahlen (1., 2., 3., ...).

### ORD_TEXT {#ORD-TEXT}
```
public static int ORD_TEXT
```


Numerische Formatierung. Ordinaltext (Erste, Zweite, Dritte, ...).

### SB_CHAR {#SB-CHAR}
```
public static int SB_CHAR
```


### THAI_ARABIC {#THAI-ARABIC}
```
public static int THAI_ARABIC
```


Numerische Formatierung. Formatiert ein numerisches Ergebnis mit thailändischen Zahlen.

### THAI_CARD_TEXT {#THAI-CARD-TEXT}
```
public static int THAI_CARD_TEXT
```


Numerische Formatierung. Formatiert ein numerisches Ergebnis mit fortlaufenden Zahlen aus dem thailändischen Zahlensystem.

### THAI_LETTER {#THAI-LETTER}
```
public static int THAI_LETTER
```


Numerische Formatierung. Formatiert ein numerisches Ergebnis mit thailändischen Buchstaben.

### UPPER {#UPPER}
```
public static int UPPER
```


Textformatierung. Alle Buchstaben sind großgeschrieben.

### UPPERCASE_ALPHABETIC {#UPPERCASE-ALPHABETIC}
```
public static int UPPERCASE_ALPHABETIC
```


Numerische Formatierung. Formatiert ein numerisches Ergebnis als ein oder mehrere Vorkommen eines großgeschriebenen lateinischen Buchstabens.

### UPPERCASE_ROMAN {#UPPERCASE-ROMAN}
```
public static int UPPERCASE_ROMAN
```


Numerische Formatierung. Römisch (I, II, III, ...).

### VIET_CARD_TEXT {#VIET-CARD-TEXT}
```
public static int VIET_CARD_TEXT
```


Numerische Formatierung. Formatiert ein numerisches Ergebnis mit vietnamesischen Ziffern.

### ZODIAC_1 {#ZODIAC-1}
```
public static int ZODIAC_1
```


Numerische Formatierung. Formatiert ein numerisches Ergebnis mit fortlaufenden traditionellen numerischen Ideogrammen.

### ZODIAC_2 {#ZODIAC-2}
```
public static int ZODIAC_2
```


Numerische Formatierung. Formatiert ein numerisches Ergebnis mit fortlaufenden Tierkreis-Ideogrammen.

### ZODIAC_3 {#ZODIAC-3}
```
public static int ZODIAC_3
```


Numerische Formatierung. Formatiert ein numerisches Ergebnis mit fortlaufenden traditionellen Tierkreis-Ideogrammen.

### length {#length}
```
public static int length
```


### fromName(String generalFormatName) {#fromName-java.lang.String}
```
public static int fromName(String generalFormatName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| generalFormatName | java.lang.String |  |

**Returns:**
int
### getName(int generalFormat) {#getName-int}
```
public static String getName(int generalFormat)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| generalFormat | int |  |

**Returns:**
java.lang.String
