---
title: "GeneralFormat"
linktitle: "GeneralFormat"
second_title: "Aspose.Words pour Java"
description: "Spécifie un format général qui est appliqué à un texte numérique ou à tout résultat de champ en Java."
type: docs
weight: 355
url: /fr/java/com.aspose.words/generalformat/
---

**Inheritance:**
java.lang.Object
```
public class GeneralFormat
```

Spécifie un format général qui est appliqué à un numérique, un texte ou tout résultat de champ. Un champ peut avoir une combinaison de formats généraux.

 **Examples:** 

Montre comment formater les résultats de champ.

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
## Champs

| Champ | Description |
| --- | --- |
| [AIUEO](#AIUEO) | Mise en forme numérique. |
| [ARABIC](#ARABIC) | Mise en forme numérique. |
| [ARABIC_ABJAD](#ARABIC-ABJAD) | Mise en forme numérique. |
| [ARABIC_ALPHA](#ARABIC-ALPHA) | Mise en forme numérique. |
| [ARABIC_DASH](#ARABIC-DASH) | Mise en forme numérique. |
| [BAHT_TEXT](#BAHT-TEXT) | Mise en forme numérique. |
| [CAPS](#CAPS) | Mise en forme de texte. |
| [CARD_TEXT](#CARD-TEXT) | Mise en forme numérique. |
| [CHAR_FORMAT](#CHAR-FORMAT) | Mise en forme du résultat de champ. |
| [CHINESE_NUM_1](#CHINESE-NUM-1) | Mise en forme numérique. |
| [CHINESE_NUM_2](#CHINESE-NUM-2) | Mise en forme numérique. |
| [CHINESE_NUM_3](#CHINESE-NUM-3) | Mise en forme numérique. |
| [CHOSUNG](#CHOSUNG) | Mise en forme numérique. |
| [CIRCLE_NUM](#CIRCLE-NUM) | Mise en forme numérique. |
| [DB_CHAR](#DB-CHAR) |  |
| [DB_NUM_1](#DB-NUM-1) |  |
| [DB_NUM_2](#DB-NUM-2) |  |
| [DB_NUM_3](#DB-NUM-3) |  |
| [DB_NUM_4](#DB-NUM-4) |  |
| [DOLLAR_TEXT](#DOLLAR-TEXT) | Mise en forme numérique. |
| [FIRST_CAP](#FIRST-CAP) | Mise en forme de texte. |
| [GANADA](#GANADA) | Mise en forme numérique. |
| [GB_1](#GB-1) | Mise en forme numérique. |
| [GB_2](#GB-2) | Mise en forme numérique. |
| [GB_3](#GB-3) | Mise en forme numérique. |
| [GB_4](#GB-4) | Mise en forme numérique. |
| [HEBREW_1](#HEBREW-1) | Mise en forme numérique. |
| [HEBREW_2](#HEBREW-2) | Mise en forme numérique. |
| [HEX](#HEX) | Mise en forme numérique. |
| [HINDI_ARABIC](#HINDI-ARABIC) | Mise en forme numérique. |
| [HINDI_CARD_TEXT](#HINDI-CARD-TEXT) | Mise en forme numérique. |
| [HINDI_LETTER_1](#HINDI-LETTER-1) | Mise en forme numérique. |
| [HINDI_LETTER_2](#HINDI-LETTER-2) | Mise en forme numérique. |
| [IROHA](#IROHA) | Mise en forme numérique. |
| [KANJI_NUM_1](#KANJI-NUM-1) | Mise en forme numérique. |
| [KANJI_NUM_2](#KANJI-NUM-2) | Mise en forme numérique. |
| [KANJI_NUM_3](#KANJI-NUM-3) | Mise en forme numérique. |
| [LOWER](#LOWER) | Mise en forme de texte. |
| [LOWERCASE_ALPHABETIC](#LOWERCASE-ALPHABETIC) | Mise en forme numérique. |
| [LOWERCASE_ROMAN](#LOWERCASE-ROMAN) | Mise en forme numérique. |
| [MERGE_FORMAT](#MERGE-FORMAT) | Mise en forme du résultat de champ. |
| [MERGE_FORMAT_INET](#MERGE-FORMAT-INET) | Mise en forme du résultat de champ. |
| [NONE](#NONE) | Utilisé pour spécifier un format général manquant. |
| [ORDINAL](#ORDINAL) | Mise en forme numérique. |
| [ORD_TEXT](#ORD-TEXT) | Mise en forme numérique. |
| [SB_CHAR](#SB-CHAR) |  |
| [THAI_ARABIC](#THAI-ARABIC) | Mise en forme numérique. |
| [THAI_CARD_TEXT](#THAI-CARD-TEXT) | Mise en forme numérique. |
| [THAI_LETTER](#THAI-LETTER) | Mise en forme numérique. |
| [UPPER](#UPPER) | Mise en forme de texte. |
| [UPPERCASE_ALPHABETIC](#UPPERCASE-ALPHABETIC) | Mise en forme numérique. |
| [UPPERCASE_ROMAN](#UPPERCASE-ROMAN) | Mise en forme numérique. |
| [VIET_CARD_TEXT](#VIET-CARD-TEXT) | Mise en forme numérique. |
| [ZODIAC_1](#ZODIAC-1) | Mise en forme numérique. |
| [ZODIAC_2](#ZODIAC-2) | Mise en forme numérique. |
| [ZODIAC_3](#ZODIAC-3) | Mise en forme numérique. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String generalFormatName)](#fromName-java.lang.String) |  |
| [getName(int generalFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int generalFormat)](#toString-int) |  |
### AIUEO {#AIUEO}
```
public static int AIUEO
```


Mise en forme numérique. Formate un résultat numérique en utilisant des caractères hiragana dans l'ordre traditionnel a-i-u-e-o.

### ARABIC {#ARABIC}
```
public static int ARABIC
```


Mise en forme numérique. Formate un résultat numérique en utilisant des chiffres cardinaux arabes.

### ARABIC_ABJAD {#ARABIC-ABJAD}
```
public static int ARABIC_ABJAD
```


Mise en forme numérique. Formate un résultat numérique en utilisant des chiffres Abjad croissants.

### ARABIC_ALPHA {#ARABIC-ALPHA}
```
public static int ARABIC_ALPHA
```


Mise en forme numérique. Formate un résultat numérique en utilisant des caractères de l'alphabet arabe.

### ARABIC_DASH {#ARABIC-DASH}
```
public static int ARABIC_DASH
```


Mise en forme numérique. Formate un résultat numérique en utilisant des chiffres cardinaux arabes, avec un préfixe de "- " et un suffixe de " -".

### BAHT_TEXT {#BAHT-TEXT}
```
public static int BAHT_TEXT
```


Mise en forme numérique. Formate un résultat numérique selon le système de comptage thaï.

### CAPS {#CAPS}
```
public static int CAPS
```


Mise en forme de texte. Met en majuscule la première lettre de chaque mot.

### CARD_TEXT {#CARD-TEXT}
```
public static int CARD_TEXT
```


Mise en forme numérique. Texte cardinal (Un, Deux, Trois, ...).

### CHAR_FORMAT {#CHAR-FORMAT}
```
public static int CHAR_FORMAT
```


Mise en forme du résultat de champ. L'instruction CHARFORMAT.

### CHINESE_NUM_1 {#CHINESE-NUM-1}
```
public static int CHINESE_NUM_1
```


Mise en forme numérique. Formate un résultat numérique en utilisant des nombres croissants du système de comptage approprié.

### CHINESE_NUM_2 {#CHINESE-NUM-2}
```
public static int CHINESE_NUM_2
```


Mise en forme numérique. Formate un résultat numérique en utilisant des nombres séquentiels du format légal approprié.

### CHINESE_NUM_3 {#CHINESE-NUM-3}
```
public static int CHINESE_NUM_3
```


Mise en forme numérique. Formate un résultat numérique en utilisant des nombres séquentiels du système de comptage des milliers approprié.

### CHOSUNG {#CHOSUNG}
```
public static int CHOSUNG
```


Mise en forme numérique. Formate un résultat numérique en utilisant des nombres séquentiels du format Chosung coréen.

### CIRCLE_NUM {#CIRCLE-NUM}
```
public static int CIRCLE_NUM
```


Mise en forme numérique. Formate un résultat numérique en utilisant une numérotation décimale enfermée dans un cercle, en utilisant le glyphe alphanumérique enfermé pour les nombres dans la plage 1\\u201320.

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


Mise en forme numérique. Texte en dollars (Un, Deux, Trois, ... + ET 55/100).

### FIRST_CAP {#FIRST-CAP}
```
public static int FIRST_CAP
```


Mise en forme du texte. Met en majuscule la première lettre du premier mot.

### GANADA {#GANADA}
```
public static int GANADA
```


Mise en forme numérique. Formate un résultat numérique en utilisant des nombres séquentiels du format coréen Ganada.

### GB_1 {#GB-1}
```
public static int GB_1
```


Mise en forme numérique. Formate un résultat numérique en utilisant une numérotation décimale suivie d’un point, en utilisant le caractère glyphe alphanumérique encadré.

### GB_2 {#GB-2}
```
public static int GB_2
```


Mise en forme numérique. Formate un résultat numérique en utilisant une numérotation décimale entre parenthèses, en utilisant le caractère glyphe alphanumérique encadré.

### GB_3 {#GB-3}
```
public static int GB_3
```


Mise en forme numérique. Formate un résultat numérique en utilisant une numérotation décimale entourée d’un cercle, en utilisant le caractère glyphe alphanumérique encadré.

### GB_4 {#GB-4}
```
public static int GB_4
```


Mise en forme numérique. Formate un résultat numérique en utilisant une numérotation décimale entourée d’un cercle, en utilisant le caractère glyphe alphanumérique encadré.

### HEBREW_1 {#HEBREW-1}
```
public static int HEBREW_1
```


Mise en forme numérique. Formate un résultat numérique en utilisant des chiffres hébreux.

### HEBREW_2 {#HEBREW-2}
```
public static int HEBREW_2
```


Mise en forme numérique. Formate un résultat numérique en utilisant l’alphabet hébreu.

### HEX {#HEX}
```
public static int HEX
```


Mise en forme numérique. Formate le résultat numérique en utilisant des chiffres hexadécimaux majuscules.

### HINDI_ARABIC {#HINDI-ARABIC}
```
public static int HINDI_ARABIC
```


Mise en forme numérique. Formate un résultat numérique en utilisant les chiffres hindi.

### HINDI_CARD_TEXT {#HINDI-CARD-TEXT}
```
public static int HINDI_CARD_TEXT
```


Mise en forme numérique. Formate un résultat numérique en utilisant des nombres séquentiels du système de comptage hindi.

### HINDI_LETTER_1 {#HINDI-LETTER-1}
```
public static int HINDI_LETTER_1
```


Mise en forme numérique. Formate un résultat numérique en utilisant les voyelles hindi.

### HINDI_LETTER_2 {#HINDI-LETTER-2}
```
public static int HINDI_LETTER_2
```


Mise en forme numérique. Formate un résultat numérique en utilisant les consonnes hindi.

### IROHA {#IROHA}
```
public static int IROHA
```


Mise en forme numérique. Formate un résultat numérique en utilisant l’iroha japonais.

### KANJI_NUM_1 {#KANJI-NUM-1}
```
public static int KANJI_NUM_1
```


Mise en forme numérique. Formate un résultat numérique en utilisant un style japonais avec le système de comptage approprié.

### KANJI_NUM_2 {#KANJI-NUM-2}
```
public static int KANJI_NUM_2
```


Mise en forme numérique. Formate un résultat numérique en utilisant le système de comptage approprié.

### KANJI_NUM_3 {#KANJI-NUM-3}
```
public static int KANJI_NUM_3
```


Mise en forme numérique. Formate un résultat numérique en utilisant le système de comptage approprié.

### LOWER {#LOWER}
```
public static int LOWER
```


Mise en forme du texte. Toutes les lettres sont en minuscules.

### LOWERCASE_ALPHABETIC {#LOWERCASE-ALPHABETIC}
```
public static int LOWERCASE_ALPHABETIC
```


Mise en forme numérique. Formate un résultat numérique comme une ou plusieurs occurrences d’un caractère alphabétique latin minuscule.

### LOWERCASE_ROMAN {#LOWERCASE-ROMAN}
```
public static int LOWERCASE_ROMAN
```


Mise en forme numérique. Romains minuscules (i, ii, iii, …).

### MERGE_FORMAT {#MERGE-FORMAT}
```
public static int MERGE_FORMAT
```


Mise en forme du résultat de champ. L’instruction MERGEFORMAT.

### MERGE_FORMAT_INET {#MERGE-FORMAT-INET}
```
public static int MERGE_FORMAT_INET
```


Mise en forme du résultat de champ. L’instruction MERGEFORMATINET.

### NONE {#NONE}
```
public static int NONE
```


Utilisé pour spécifier un format général manquant.

### ORDINAL {#ORDINAL}
```
public static int ORDINAL
```


Mise en forme numérique. Ordinal (1ᵉʳ, 2ᵉ, 3ᵉ, …).

### ORD_TEXT {#ORD-TEXT}
```
public static int ORD_TEXT
```


Mise en forme numérique. Texte ordinal (Premier, Deuxième, Troisième, …).

### SB_CHAR {#SB-CHAR}
```
public static int SB_CHAR
```


### THAI_ARABIC {#THAI-ARABIC}
```
public static int THAI_ARABIC
```


Mise en forme numérique. Formate un résultat numérique en utilisant les chiffres thaï.

### THAI_CARD_TEXT {#THAI-CARD-TEXT}
```
public static int THAI_CARD_TEXT
```


Mise en forme numérique. Formate un résultat numérique en utilisant des nombres séquentiels du système de comptage thaï.

### THAI_LETTER {#THAI-LETTER}
```
public static int THAI_LETTER
```


Mise en forme numérique. Formate un résultat numérique en utilisant les lettres thaï.

### UPPER {#UPPER}
```
public static int UPPER
```


Mise en forme du texte. Toutes les lettres sont en majuscules.

### UPPERCASE_ALPHABETIC {#UPPERCASE-ALPHABETIC}
```
public static int UPPERCASE_ALPHABETIC
```


Mise en forme numérique. Formate un résultat numérique sous forme d'une ou plusieurs occurrences d'un caractère alphabétique latin majuscule.

### UPPERCASE_ROMAN {#UPPERCASE-ROMAN}
```
public static int UPPERCASE_ROMAN
```


Mise en forme numérique. Romain majuscule (I, II, III, ...).

### VIET_CARD_TEXT {#VIET-CARD-TEXT}
```
public static int VIET_CARD_TEXT
```


Mise en forme numérique. Formate un résultat numérique en utilisant les chiffres vietnamiens.

### ZODIAC_1 {#ZODIAC-1}
```
public static int ZODIAC_1
```


Mise en forme numérique. Formate un résultat numérique en utilisant des idéogrammes traditionnels numériques séquentiels.

### ZODIAC_2 {#ZODIAC-2}
```
public static int ZODIAC_2
```


Mise en forme numérique. Formate un résultat numérique en utilisant des idéogrammes du zodiaque séquentiels.

### ZODIAC_3 {#ZODIAC-3}
```
public static int ZODIAC_3
```


Mise en forme numérique. Formate un résultat numérique en utilisant des idéogrammes traditionnels du zodiaque séquentiels.

### length {#length}
```
public static int length
```


### fromName(String generalFormatName) {#fromName-java.lang.String}
```
public static int fromName(String generalFormatName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| generalFormatName | java.lang.String |  |

**Returns:**
int
### getName(int generalFormat) {#getName-int}
```
public static String getName(int generalFormat)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| generalFormat | int |  |

**Returns:**
java.lang.String
