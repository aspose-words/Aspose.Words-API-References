---
title: "GeneralFormat"
linktitle: "GeneralFormat"
second_title: "Aspose.Words para Java"
description: "Especifica un formato general que se aplica a un texto numérico o a cualquier resultado de campo en Java."
type: docs
weight: 355
url: /es/java/com.aspose.words/generalformat/
---

**Inheritance:**
java.lang.Object
```
public class GeneralFormat
```

Especifica un formato general que se aplica a un resultado numérico, de texto o de cualquier campo. Un campo puede tener una combinación de formatos generales.

 **Examples:** 

Muestra cómo formatear los resultados del campo.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [AIUEO](#AIUEO) | Formato numérico. |
| [ARABIC](#ARABIC) | Formato numérico. |
| [ARABIC_ABJAD](#ARABIC-ABJAD) | Formato numérico. |
| [ARABIC_ALPHA](#ARABIC-ALPHA) | Formato numérico. |
| [ARABIC_DASH](#ARABIC-DASH) | Formato numérico. |
| [BAHT_TEXT](#BAHT-TEXT) | Formato numérico. |
| [CAPS](#CAPS) | Formato de texto. |
| [CARD_TEXT](#CARD-TEXT) | Formato numérico. |
| [CHAR_FORMAT](#CHAR-FORMAT) | Formato del resultado del campo. |
| [CHINESE_NUM_1](#CHINESE-NUM-1) | Formato numérico. |
| [CHINESE_NUM_2](#CHINESE-NUM-2) | Formato numérico. |
| [CHINESE_NUM_3](#CHINESE-NUM-3) | Formato numérico. |
| [CHOSUNG](#CHOSUNG) | Formato numérico. |
| [CIRCLE_NUM](#CIRCLE-NUM) | Formato numérico. |
| [DB_CHAR](#DB-CHAR) |  |
| [DB_NUM_1](#DB-NUM-1) |  |
| [DB_NUM_2](#DB-NUM-2) |  |
| [DB_NUM_3](#DB-NUM-3) |  |
| [DB_NUM_4](#DB-NUM-4) |  |
| [DOLLAR_TEXT](#DOLLAR-TEXT) | Formato numérico. |
| [FIRST_CAP](#FIRST-CAP) | Formato de texto. |
| [GANADA](#GANADA) | Formato numérico. |
| [GB_1](#GB-1) | Formato numérico. |
| [GB_2](#GB-2) | Formato numérico. |
| [GB_3](#GB-3) | Formato numérico. |
| [GB_4](#GB-4) | Formato numérico. |
| [HEBREW_1](#HEBREW-1) | Formato numérico. |
| [HEBREW_2](#HEBREW-2) | Formato numérico. |
| [HEX](#HEX) | Formato numérico. |
| [HINDI_ARABIC](#HINDI-ARABIC) | Formato numérico. |
| [HINDI_CARD_TEXT](#HINDI-CARD-TEXT) | Formato numérico. |
| [HINDI_LETTER_1](#HINDI-LETTER-1) | Formato numérico. |
| [HINDI_LETTER_2](#HINDI-LETTER-2) | Formato numérico. |
| [IROHA](#IROHA) | Formato numérico. |
| [KANJI_NUM_1](#KANJI-NUM-1) | Formato numérico. |
| [KANJI_NUM_2](#KANJI-NUM-2) | Formato numérico. |
| [KANJI_NUM_3](#KANJI-NUM-3) | Formato numérico. |
| [LOWER](#LOWER) | Formato de texto. |
| [LOWERCASE_ALPHABETIC](#LOWERCASE-ALPHABETIC) | Formato numérico. |
| [LOWERCASE_ROMAN](#LOWERCASE-ROMAN) | Formato numérico. |
| [MERGE_FORMAT](#MERGE-FORMAT) | Formato del resultado del campo. |
| [MERGE_FORMAT_INET](#MERGE-FORMAT-INET) | Formato del resultado del campo. |
| [NONE](#NONE) | Se usa para especificar un formato general faltante. |
| [ORDINAL](#ORDINAL) | Formato numérico. |
| [ORD_TEXT](#ORD-TEXT) | Formato numérico. |
| [SB_CHAR](#SB-CHAR) |  |
| [THAI_ARABIC](#THAI-ARABIC) | Formato numérico. |
| [THAI_CARD_TEXT](#THAI-CARD-TEXT) | Formato numérico. |
| [THAI_LETTER](#THAI-LETTER) | Formato numérico. |
| [UPPER](#UPPER) | Formato de texto. |
| [UPPERCASE_ALPHABETIC](#UPPERCASE-ALPHABETIC) | Formato numérico. |
| [UPPERCASE_ROMAN](#UPPERCASE-ROMAN) | Formato numérico. |
| [VIET_CARD_TEXT](#VIET-CARD-TEXT) | Formato numérico. |
| [ZODIAC_1](#ZODIAC-1) | Formato numérico. |
| [ZODIAC_2](#ZODIAC-2) | Formato numérico. |
| [ZODIAC_3](#ZODIAC-3) | Formato numérico. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String generalFormatName)](#fromName-java.lang.String) |  |
| [getName(int generalFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int generalFormat)](#toString-int) |  |
### AIUEO {#AIUEO}
```
public static int AIUEO
```


Formato numérico. Formatea un resultado numérico usando caracteres hiragana en el orden tradicional a-i-u-e-o.

### ARABIC {#ARABIC}
```
public static int ARABIC
```


Formato numérico. Formatea un resultado numérico usando numerales cardinales árabes.

### ARABIC_ABJAD {#ARABIC-ABJAD}
```
public static int ARABIC_ABJAD
```


Formato numérico. Formatea un resultado numérico usando numerales Abjad ascendentes.

### ARABIC_ALPHA {#ARABIC-ALPHA}
```
public static int ARABIC_ALPHA
```


Formato numérico. Formatea un resultado numérico usando caracteres del alfabeto árabe.

### ARABIC_DASH {#ARABIC-DASH}
```
public static int ARABIC_DASH
```


Formato numérico. Formatea un resultado numérico usando numerales cardinales árabes, con un prefijo de "- " y un sufijo de " -".

### BAHT_TEXT {#BAHT-TEXT}
```
public static int BAHT_TEXT
```


Formato numérico. Formatea un resultado numérico en el sistema de numeración tailandés.

### CAPS {#CAPS}
```
public static int CAPS
```


Formato de texto. Capitaliza la primera letra de cada palabra.

### CARD_TEXT {#CARD-TEXT}
```
public static int CARD_TEXT
```


Formato numérico. Texto cardinal (Uno, Dos, Tres, ...).

### CHAR_FORMAT {#CHAR-FORMAT}
```
public static int CHAR_FORMAT
```


Formato del resultado del campo. La instrucción CHARFORMAT.

### CHINESE_NUM_1 {#CHINESE-NUM-1}
```
public static int CHINESE_NUM_1
```


Formato numérico. Formatea un resultado numérico usando números ascendentes del sistema de numeración apropiado.

### CHINESE_NUM_2 {#CHINESE-NUM-2}
```
public static int CHINESE_NUM_2
```


Formato numérico. Formatea un resultado numérico usando números secuenciales del formato legal apropiado.

### CHINESE_NUM_3 {#CHINESE-NUM-3}
```
public static int CHINESE_NUM_3
```


Formato numérico. Formatea un resultado numérico usando números secuenciales del sistema de conteo de miles apropiado.

### CHOSUNG {#CHOSUNG}
```
public static int CHOSUNG
```


Formato numérico. Formatea un resultado numérico usando números secuenciales del formato Chosung coreano.

### CIRCLE_NUM {#CIRCLE-NUM}
```
public static int CIRCLE_NUM
```


Formato numérico. Formatea un resultado numérico usando numeración decimal encerrada en un círculo, usando el carácter glifo alfanumérico encerrado para números en el rango 1\\u201320.

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


Formato numérico. Texto en dólares (Uno, Dos, Tres, ... + Y 55/100).

### FIRST_CAP {#FIRST-CAP}
```
public static int FIRST_CAP
```


Formato de texto. Capitaliza la primera letra de la primera palabra.

### GANADA {#GANADA}
```
public static int GANADA
```


Formato numérico. Formatea un resultado numérico usando números secuenciales del formato coreano Ganada.

### GB_1 {#GB-1}
```
public static int GB_1
```


Formato numérico. Formatea un resultado numérico usando numeración decimal seguida de un punto, utilizando el carácter glifo alfanumérico incluido.

### GB_2 {#GB-2}
```
public static int GB_2
```


Formato numérico. Formatea un resultado numérico usando numeración decimal entre paréntesis, utilizando el carácter glifo alfanumérico incluido.

### GB_3 {#GB-3}
```
public static int GB_3
```


Formato numérico. Formatea un resultado numérico usando numeración decimal dentro de un círculo, utilizando el carácter glifo alfanumérico incluido.

### GB_4 {#GB-4}
```
public static int GB_4
```


Formato numérico. Formatea un resultado numérico usando numeración decimal dentro de un círculo, utilizando el carácter glifo alfanumérico incluido.

### HEBREW_1 {#HEBREW-1}
```
public static int HEBREW_1
```


Formato numérico. Formatea un resultado numérico usando numerales hebreos.

### HEBREW_2 {#HEBREW-2}
```
public static int HEBREW_2
```


Formato numérico. Formatea un resultado numérico usando el alfabeto hebreo.

### HEX {#HEX}
```
public static int HEX
```


Formato numérico. Formatea el resultado numérico usando dígitos hexadecimales en mayúsculas.

### HINDI_ARABIC {#HINDI-ARABIC}
```
public static int HINDI_ARABIC
```


Formato numérico. Formatea un resultado numérico usando números hindi.

### HINDI_CARD_TEXT {#HINDI-CARD-TEXT}
```
public static int HINDI_CARD_TEXT
```


Formato numérico. Formatea un resultado numérico usando números secuenciales del sistema de numeración hindi.

### HINDI_LETTER_1 {#HINDI-LETTER-1}
```
public static int HINDI_LETTER_1
```


Formato numérico. Formatea un resultado numérico usando vocales hindi.

### HINDI_LETTER_2 {#HINDI-LETTER-2}
```
public static int HINDI_LETTER_2
```


Formato numérico. Formatea un resultado numérico usando consonantes hindi.

### IROHA {#IROHA}
```
public static int IROHA
```


Formato numérico. Formatea un resultado numérico usando el iroha japonés.

### KANJI_NUM_1 {#KANJI-NUM-1}
```
public static int KANJI_NUM_1
```


Formato numérico. Formatea un resultado numérico usando un estilo japonés con el sistema de numeración apropiado.

### KANJI_NUM_2 {#KANJI-NUM-2}
```
public static int KANJI_NUM_2
```


Formato numérico. Formatea un resultado numérico usando el sistema de numeración apropiado.

### KANJI_NUM_3 {#KANJI-NUM-3}
```
public static int KANJI_NUM_3
```


Formato numérico. Formatea un resultado numérico usando el sistema de numeración apropiado.

### LOWER {#LOWER}
```
public static int LOWER
```


Formato de texto. Todas las letras están en minúsculas.

### LOWERCASE_ALPHABETIC {#LOWERCASE-ALPHABETIC}
```
public static int LOWERCASE_ALPHABETIC
```


Formato numérico. Formatea un resultado numérico como una o más ocurrencias de un carácter alfabético latino en minúscula.

### LOWERCASE_ROMAN {#LOWERCASE-ROMAN}
```
public static int LOWERCASE_ROMAN
```


Formato numérico. Números romanos en minúscula (i, ii, iii, ...).

### MERGE_FORMAT {#MERGE-FORMAT}
```
public static int MERGE_FORMAT
```


Formato de resultado de campo. La instrucción MERGEFORMAT.

### MERGE_FORMAT_INET {#MERGE-FORMAT-INET}
```
public static int MERGE_FORMAT_INET
```


Formato de resultado de campo. La instrucción MERGEFORMATINET.

### NONE {#NONE}
```
public static int NONE
```


Se usa para especificar un formato general faltante.

### ORDINAL {#ORDINAL}
```
public static int ORDINAL
```


Formato numérico. Ordinal (1.º, 2.º, 3.º, ...).

### ORD_TEXT {#ORD-TEXT}
```
public static int ORD_TEXT
```


Formato numérico. Texto ordinal (Primero, Segundo, Tercero, ...).

### SB_CHAR {#SB-CHAR}
```
public static int SB_CHAR
```


### THAI_ARABIC {#THAI-ARABIC}
```
public static int THAI_ARABIC
```


Formato numérico. Formatea un resultado numérico usando números tailandeses.

### THAI_CARD_TEXT {#THAI-CARD-TEXT}
```
public static int THAI_CARD_TEXT
```


Formato numérico. Formatea un resultado numérico usando números secuenciales del sistema de numeración tailandés.

### THAI_LETTER {#THAI-LETTER}
```
public static int THAI_LETTER
```


Formato numérico. Formatea un resultado numérico usando letras tailandesas.

### UPPER {#UPPER}
```
public static int UPPER
```


Formato de texto. Todas las letras están en mayúsculas.

### UPPERCASE_ALPHABETIC {#UPPERCASE-ALPHABETIC}
```
public static int UPPERCASE_ALPHABETIC
```


Formato numérico. Formatea un resultado numérico como una o más ocurrencias de un carácter alfabético latino en mayúsculas.

### UPPERCASE_ROMAN {#UPPERCASE-ROMAN}
```
public static int UPPERCASE_ROMAN
```


Formato numérico. Números romanos en mayúsculas (I, II, III, ...).

### VIET_CARD_TEXT {#VIET-CARD-TEXT}
```
public static int VIET_CARD_TEXT
```


Formato numérico. Formatea un resultado numérico usando numerales vietnamitas.

### ZODIAC_1 {#ZODIAC-1}
```
public static int ZODIAC_1
```


Formato numérico. Formatea un resultado numérico usando ideogramas tradicionales numéricos secuenciales.

### ZODIAC_2 {#ZODIAC-2}
```
public static int ZODIAC_2
```


Formato numérico. Formatea un resultado numérico usando ideogramas del zodíaco secuenciales.

### ZODIAC_3 {#ZODIAC-3}
```
public static int ZODIAC_3
```


Formato numérico. Formatea un resultado numérico usando ideogramas tradicionales del zodíaco secuenciales.

### length {#length}
```
public static int length
```


### fromName(String generalFormatName) {#fromName-java.lang.String}
```
public static int fromName(String generalFormatName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| generalFormatName | java.lang.String |  |

**Returns:**
int
### getName(int generalFormat) {#getName-int}
```
public static String getName(int generalFormat)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| generalFormat | int |  |

**Returns:**
java.lang.String
