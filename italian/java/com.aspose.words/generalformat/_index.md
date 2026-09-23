---
title: "GeneralFormat"
linktitle: "GeneralFormat"
second_title: "Aspose.Words per Java"
description: "Specifica un formato generale che viene applicato a un testo numerico o a qualsiasi risultato di campo in Java."
type: docs
weight: 355
url: /it/java/com.aspose.words/generalformat/
---

**Inheritance:**
java.lang.Object
```
public class GeneralFormat
```

Specifica un formato generale che viene applicato a un valore numerico, testuale o a qualsiasi risultato di campo. Un campo può avere una combinazione di formati generali.

 **Examples:** 

Mostra come formattare i risultati del campo.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [AIUEO](#AIUEO) | Formattazione numerica. |
| [ARABIC](#ARABIC) | Formattazione numerica. |
| [ARABIC_ABJAD](#ARABIC-ABJAD) | Formattazione numerica. |
| [ARABIC_ALPHA](#ARABIC-ALPHA) | Formattazione numerica. |
| [ARABIC_DASH](#ARABIC-DASH) | Formattazione numerica. |
| [BAHT_TEXT](#BAHT-TEXT) | Formattazione numerica. |
| [CAPS](#CAPS) | Formattazione del testo. |
| [CARD_TEXT](#CARD-TEXT) | Formattazione numerica. |
| [CHAR_FORMAT](#CHAR-FORMAT) | Formattazione del risultato di campo. |
| [CHINESE_NUM_1](#CHINESE-NUM-1) | Formattazione numerica. |
| [CHINESE_NUM_2](#CHINESE-NUM-2) | Formattazione numerica. |
| [CHINESE_NUM_3](#CHINESE-NUM-3) | Formattazione numerica. |
| [CHOSUNG](#CHOSUNG) | Formattazione numerica. |
| [CIRCLE_NUM](#CIRCLE-NUM) | Formattazione numerica. |
| [DB_CHAR](#DB-CHAR) |  |
| [DB_NUM_1](#DB-NUM-1) |  |
| [DB_NUM_2](#DB-NUM-2) |  |
| [DB_NUM_3](#DB-NUM-3) |  |
| [DB_NUM_4](#DB-NUM-4) |  |
| [DOLLAR_TEXT](#DOLLAR-TEXT) | Formattazione numerica. |
| [FIRST_CAP](#FIRST-CAP) | Formattazione del testo. |
| [GANADA](#GANADA) | Formattazione numerica. |
| [GB_1](#GB-1) | Formattazione numerica. |
| [GB_2](#GB-2) | Formattazione numerica. |
| [GB_3](#GB-3) | Formattazione numerica. |
| [GB_4](#GB-4) | Formattazione numerica. |
| [HEBREW_1](#HEBREW-1) | Formattazione numerica. |
| [HEBREW_2](#HEBREW-2) | Formattazione numerica. |
| [HEX](#HEX) | Formattazione numerica. |
| [HINDI_ARABIC](#HINDI-ARABIC) | Formattazione numerica. |
| [HINDI_CARD_TEXT](#HINDI-CARD-TEXT) | Formattazione numerica. |
| [HINDI_LETTER_1](#HINDI-LETTER-1) | Formattazione numerica. |
| [HINDI_LETTER_2](#HINDI-LETTER-2) | Formattazione numerica. |
| [IROHA](#IROHA) | Formattazione numerica. |
| [KANJI_NUM_1](#KANJI-NUM-1) | Formattazione numerica. |
| [KANJI_NUM_2](#KANJI-NUM-2) | Formattazione numerica. |
| [KANJI_NUM_3](#KANJI-NUM-3) | Formattazione numerica. |
| [LOWER](#LOWER) | Formattazione del testo. |
| [LOWERCASE_ALPHABETIC](#LOWERCASE-ALPHABETIC) | Formattazione numerica. |
| [LOWERCASE_ROMAN](#LOWERCASE-ROMAN) | Formattazione numerica. |
| [MERGE_FORMAT](#MERGE-FORMAT) | Formattazione del risultato di campo. |
| [MERGE_FORMAT_INET](#MERGE-FORMAT-INET) | Formattazione del risultato di campo. |
| [NONE](#NONE) | Utilizzato per specificare un formato generale mancante. |
| [ORDINAL](#ORDINAL) | Formattazione numerica. |
| [ORD_TEXT](#ORD-TEXT) | Formattazione numerica. |
| [SB_CHAR](#SB-CHAR) |  |
| [THAI_ARABIC](#THAI-ARABIC) | Formattazione numerica. |
| [THAI_CARD_TEXT](#THAI-CARD-TEXT) | Formattazione numerica. |
| [THAI_LETTER](#THAI-LETTER) | Formattazione numerica. |
| [UPPER](#UPPER) | Formattazione del testo. |
| [UPPERCASE_ALPHABETIC](#UPPERCASE-ALPHABETIC) | Formattazione numerica. |
| [UPPERCASE_ROMAN](#UPPERCASE-ROMAN) | Formattazione numerica. |
| [VIET_CARD_TEXT](#VIET-CARD-TEXT) | Formattazione numerica. |
| [ZODIAC_1](#ZODIAC-1) | Formattazione numerica. |
| [ZODIAC_2](#ZODIAC-2) | Formattazione numerica. |
| [ZODIAC_3](#ZODIAC-3) | Formattazione numerica. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String generalFormatName)](#fromName-java.lang.String) |  |
| [getName(int generalFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int generalFormat)](#toString-int) |  |
### AIUEO {#AIUEO}
```
public static int AIUEO
```


Formattazione numerica. Formatta un risultato numerico usando caratteri hiragana nell'ordine tradizionale a-i-u-e-o.

### ARABIC {#ARABIC}
```
public static int ARABIC
```


Formattazione numerica. Formatta un risultato numerico usando numeri cardinali arabi.

### ARABIC_ABJAD {#ARABIC-ABJAD}
```
public static int ARABIC_ABJAD
```


Formattazione numerica. Formatta un risultato numerico usando numeri Abjad ascendente.

### ARABIC_ALPHA {#ARABIC-ALPHA}
```
public static int ARABIC_ALPHA
```


Formattazione numerica. Formatta un risultato numerico usando caratteri dell'alfabeto arabo.

### ARABIC_DASH {#ARABIC-DASH}
```
public static int ARABIC_DASH
```


Formattazione numerica. Formatta un risultato numerico usando numeri cardinali arabi, con un prefisso di "- " e un suffisso di " -".

### BAHT_TEXT {#BAHT-TEXT}
```
public static int BAHT_TEXT
```


Formattazione numerica. Formatta un risultato numerico nel sistema di numerazione tailandese.

### CAPS {#CAPS}
```
public static int CAPS
```


Formattazione del testo. Capitalizza la prima lettera di ogni parola.

### CARD_TEXT {#CARD-TEXT}
```
public static int CARD_TEXT
```


Formattazione numerica. Testo cardinale (Uno, Due, Tre, ...).

### CHAR_FORMAT {#CHAR-FORMAT}
```
public static int CHAR_FORMAT
```


Formattazione del risultato di campo. L'istruzione CHARFORMAT.

### CHINESE_NUM_1 {#CHINESE-NUM-1}
```
public static int CHINESE_NUM_1
```


Formattazione numerica. Formatta un risultato numerico usando numeri ascendente dal sistema di numerazione appropriato.

### CHINESE_NUM_2 {#CHINESE-NUM-2}
```
public static int CHINESE_NUM_2
```


Formattazione numerica. Formatta un risultato numerico usando numeri sequenziali dal formato legale appropriato.

### CHINESE_NUM_3 {#CHINESE-NUM-3}
```
public static int CHINESE_NUM_3
```


Formattazione numerica. Formatta un risultato numerico usando numeri sequenziali dal sistema di conteggio delle migliaia appropriato.

### CHOSUNG {#CHOSUNG}
```
public static int CHOSUNG
```


Formattazione numerica. Formatta un risultato numerico usando numeri sequenziali dal formato Chosung coreano.

### CIRCLE_NUM {#CIRCLE-NUM}
```
public static int CIRCLE_NUM
```


Formattazione numerica. Formatta un risultato numerico usando numerazione decimale racchiusa in un cerchio, usando il glifo alfanumerico racchiuso per i numeri nell'intervallo 1\u201320.

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


Formattazione numerica. Testo in dollari (Uno, Due, Tre, ... + E 55/100).

### FIRST_CAP {#FIRST-CAP}
```
public static int FIRST_CAP
```


Formattazione del testo. Converte in maiuscolo la prima lettera della prima parola.

### GANADA {#GANADA}
```
public static int GANADA
```


Formattazione numerica. Formatta un risultato numerico usando numeri sequenziali dal formato coreano Ganada.

### GB_1 {#GB-1}
```
public static int GB_1
```


Formattazione numerica. Formatta un risultato numerico usando numerazione decimale seguita da un punto, utilizzando il carattere glifo alfanumerico racchiuso.

### GB_2 {#GB-2}
```
public static int GB_2
```


Formattazione numerica. Formatta un risultato numerico usando numerazione decimale racchiusa tra parentesi, utilizzando il carattere glifo alfanumerico racchiuso.

### GB_3 {#GB-3}
```
public static int GB_3
```


Formattazione numerica. Formatta un risultato numerico usando numerazione decimale racchiusa in un cerchio, utilizzando il carattere glifo alfanumerico racchiuso.

### GB_4 {#GB-4}
```
public static int GB_4
```


Formattazione numerica. Formatta un risultato numerico usando numerazione decimale racchiusa in un cerchio, utilizzando il carattere glifo alfanumerico racchiuso.

### HEBREW_1 {#HEBREW-1}
```
public static int HEBREW_1
```


Formattazione numerica. Formatta un risultato numerico usando numeri ebraici.

### HEBREW_2 {#HEBREW-2}
```
public static int HEBREW_2
```


Formattazione numerica. Formatta un risultato numerico usando l'alfabeto ebraico.

### HEX {#HEX}
```
public static int HEX
```


Formattazione numerica. Formatta il risultato numerico usando cifre esadecimali maiuscole.

### HINDI_ARABIC {#HINDI-ARABIC}
```
public static int HINDI_ARABIC
```


Formattazione numerica. Formatta un risultato numerico usando numeri hindi.

### HINDI_CARD_TEXT {#HINDI-CARD-TEXT}
```
public static int HINDI_CARD_TEXT
```


Formattazione numerica. Formatta un risultato numerico usando numeri sequenziali dal sistema di conteggio hindi.

### HINDI_LETTER_1 {#HINDI-LETTER-1}
```
public static int HINDI_LETTER_1
```


Formattazione numerica. Formatta un risultato numerico usando vocali hindi.

### HINDI_LETTER_2 {#HINDI-LETTER-2}
```
public static int HINDI_LETTER_2
```


Formattazione numerica. Formatta un risultato numerico usando consonanti hindi.

### IROHA {#IROHA}
```
public static int IROHA
```


Formattazione numerica. Formatta un risultato numerico usando l'iroha giapponese.

### KANJI_NUM_1 {#KANJI-NUM-1}
```
public static int KANJI_NUM_1
```


Formattazione numerica. Formatta un risultato numerico usando uno stile giapponese con il sistema di conteggio appropriato.

### KANJI_NUM_2 {#KANJI-NUM-2}
```
public static int KANJI_NUM_2
```


Formattazione numerica. Formatta un risultato numerico usando il sistema di conteggio appropriato.

### KANJI_NUM_3 {#KANJI-NUM-3}
```
public static int KANJI_NUM_3
```


Formattazione numerica. Formatta un risultato numerico usando il sistema di conteggio appropriato.

### LOWER {#LOWER}
```
public static int LOWER
```


Formattazione del testo. Tutte le lettere sono minuscole.

### LOWERCASE_ALPHABETIC {#LOWERCASE-ALPHABETIC}
```
public static int LOWERCASE_ALPHABETIC
```


Formattazione numerica. Formatta un risultato numerico come una o più occorrenze di un carattere alfabetico latino minuscolo.

### LOWERCASE_ROMAN {#LOWERCASE-ROMAN}
```
public static int LOWERCASE_ROMAN
```


Formattazione numerica. Numeri romani minuscoli (i, ii, iii, ...).

### MERGE_FORMAT {#MERGE-FORMAT}
```
public static int MERGE_FORMAT
```


Formattazione del risultato del campo. L'istruzione MERGEFORMAT.

### MERGE_FORMAT_INET {#MERGE-FORMAT-INET}
```
public static int MERGE_FORMAT_INET
```


Formattazione del risultato del campo. L'istruzione MERGEFORMATINET.

### NONE {#NONE}
```
public static int NONE
```


Utilizzato per specificare un formato generale mancante.

### ORDINAL {#ORDINAL}
```
public static int ORDINAL
```


Formattazione numerica. Ordinale (1°, 2°, 3°, ...).

### ORD_TEXT {#ORD-TEXT}
```
public static int ORD_TEXT
```


Formattazione numerica. Testo ordinale (Primo, Secondo, Terzo, ...).

### SB_CHAR {#SB-CHAR}
```
public static int SB_CHAR
```


### THAI_ARABIC {#THAI-ARABIC}
```
public static int THAI_ARABIC
```


Formattazione numerica. Formatta un risultato numerico usando numeri tailandesi.

### THAI_CARD_TEXT {#THAI-CARD-TEXT}
```
public static int THAI_CARD_TEXT
```


Formattazione numerica. Formatta un risultato numerico usando numeri sequenziali dal sistema di conteggio tailandese.

### THAI_LETTER {#THAI-LETTER}
```
public static int THAI_LETTER
```


Formattazione numerica. Formatta un risultato numerico usando lettere tailandesi.

### UPPER {#UPPER}
```
public static int UPPER
```


Formattazione del testo. Tutte le lettere sono maiuscole.

### UPPERCASE_ALPHABETIC {#UPPERCASE-ALPHABETIC}
```
public static int UPPERCASE_ALPHABETIC
```


Formattazione numerica. Formatta un risultato numerico come una o più occorrenze di un carattere alfabetico latino maiuscolo.

### UPPERCASE_ROMAN {#UPPERCASE-ROMAN}
```
public static int UPPERCASE_ROMAN
```


Formattazione numerica. Numeri romani maiuscoli (I, II, III, ...).

### VIET_CARD_TEXT {#VIET-CARD-TEXT}
```
public static int VIET_CARD_TEXT
```


Formattazione numerica. Formatta un risultato numerico usando numeri vietnamiti.

### ZODIAC_1 {#ZODIAC-1}
```
public static int ZODIAC_1
```


Formattazione numerica. Formatta un risultato numerico usando ideogrammi tradizionali numerici sequenziali.

### ZODIAC_2 {#ZODIAC-2}
```
public static int ZODIAC_2
```


Formattazione numerica. Formatta un risultato numerico usando ideogrammi zodiacali sequenziali.

### ZODIAC_3 {#ZODIAC-3}
```
public static int ZODIAC_3
```


Formattazione numerica. Formatta un risultato numerico usando ideogrammi zodiacali tradizionali sequenziali.

### length {#length}
```
public static int length
```


### fromName(String generalFormatName) {#fromName-java.lang.String}
```
public static int fromName(String generalFormatName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| generalFormatName | java.lang.String |  |

**Returns:**
int
### getName(int generalFormat) {#getName-int}
```
public static String getName(int generalFormat)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| generalFormat | int |  |

**Returns:**
java.lang.String
