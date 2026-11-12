---
title: "GeneralFormat"
linktitle: "GeneralFormat"
second_title: "Aspose.Words для Java"
description: "Указывает общий формат, который применяется к числовому тексту или любому результату поля в Java."
type: docs
weight: 355
url: /ru/java/com.aspose.words/generalformat/
---

**Inheritance:**
java.lang.Object
```
public class GeneralFormat
```

Указывает общий формат, который применяется к числовому, текстовому или любому результату поля. Поле может иметь комбинацию общих форматов.

 **Examples:** 

Показывает, как форматировать результаты полей.

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
## Поля

| Поле | Описание |
| --- | --- |
| [AIUEO](#AIUEO) | Числовое форматирование. |
| [ARABIC](#ARABIC) | Числовое форматирование. |
| [ARABIC_ABJAD](#ARABIC-ABJAD) | Числовое форматирование. |
| [ARABIC_ALPHA](#ARABIC-ALPHA) | Числовое форматирование. |
| [ARABIC_DASH](#ARABIC-DASH) | Числовое форматирование. |
| [BAHT_TEXT](#BAHT-TEXT) | Числовое форматирование. |
| [CAPS](#CAPS) | Текстовое форматирование. |
| [CARD_TEXT](#CARD-TEXT) | Числовое форматирование. |
| [CHAR_FORMAT](#CHAR-FORMAT) | Форматирование результата поля. |
| [CHINESE_NUM_1](#CHINESE-NUM-1) | Числовое форматирование. |
| [CHINESE_NUM_2](#CHINESE-NUM-2) | Числовое форматирование. |
| [CHINESE_NUM_3](#CHINESE-NUM-3) | Числовое форматирование. |
| [CHOSUNG](#CHOSUNG) | Числовое форматирование. |
| [CIRCLE_NUM](#CIRCLE-NUM) | Числовое форматирование. |
| [DB_CHAR](#DB-CHAR) |  |
| [DB_NUM_1](#DB-NUM-1) |  |
| [DB_NUM_2](#DB-NUM-2) |  |
| [DB_NUM_3](#DB-NUM-3) |  |
| [DB_NUM_4](#DB-NUM-4) |  |
| [DOLLAR_TEXT](#DOLLAR-TEXT) | Числовое форматирование. |
| [FIRST_CAP](#FIRST-CAP) | Текстовое форматирование. |
| [GANADA](#GANADA) | Числовое форматирование. |
| [GB_1](#GB-1) | Числовое форматирование. |
| [GB_2](#GB-2) | Числовое форматирование. |
| [GB_3](#GB-3) | Числовое форматирование. |
| [GB_4](#GB-4) | Числовое форматирование. |
| [HEBREW_1](#HEBREW-1) | Числовое форматирование. |
| [HEBREW_2](#HEBREW-2) | Числовое форматирование. |
| [HEX](#HEX) | Числовое форматирование. |
| [HINDI_ARABIC](#HINDI-ARABIC) | Числовое форматирование. |
| [HINDI_CARD_TEXT](#HINDI-CARD-TEXT) | Числовое форматирование. |
| [HINDI_LETTER_1](#HINDI-LETTER-1) | Числовое форматирование. |
| [HINDI_LETTER_2](#HINDI-LETTER-2) | Числовое форматирование. |
| [IROHA](#IROHA) | Числовое форматирование. |
| [KANJI_NUM_1](#KANJI-NUM-1) | Числовое форматирование. |
| [KANJI_NUM_2](#KANJI-NUM-2) | Числовое форматирование. |
| [KANJI_NUM_3](#KANJI-NUM-3) | Числовое форматирование. |
| [LOWER](#LOWER) | Текстовое форматирование. |
| [LOWERCASE_ALPHABETIC](#LOWERCASE-ALPHABETIC) | Числовое форматирование. |
| [LOWERCASE_ROMAN](#LOWERCASE-ROMAN) | Числовое форматирование. |
| [MERGE_FORMAT](#MERGE-FORMAT) | Форматирование результата поля. |
| [MERGE_FORMAT_INET](#MERGE-FORMAT-INET) | Форматирование результата поля. |
| [NONE](#NONE) | Используется для указания отсутствующего общего формата. |
| [ORDINAL](#ORDINAL) | Числовое форматирование. |
| [ORD_TEXT](#ORD-TEXT) | Числовое форматирование. |
| [SB_CHAR](#SB-CHAR) |  |
| [THAI_ARABIC](#THAI-ARABIC) | Числовое форматирование. |
| [THAI_CARD_TEXT](#THAI-CARD-TEXT) | Числовое форматирование. |
| [THAI_LETTER](#THAI-LETTER) | Числовое форматирование. |
| [UPPER](#UPPER) | Текстовое форматирование. |
| [UPPERCASE_ALPHABETIC](#UPPERCASE-ALPHABETIC) | Числовое форматирование. |
| [UPPERCASE_ROMAN](#UPPERCASE-ROMAN) | Числовое форматирование. |
| [VIET_CARD_TEXT](#VIET-CARD-TEXT) | Числовое форматирование. |
| [ZODIAC_1](#ZODIAC-1) | Числовое форматирование. |
| [ZODIAC_2](#ZODIAC-2) | Числовое форматирование. |
| [ZODIAC_3](#ZODIAC-3) | Числовое форматирование. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String generalFormatName)](#fromName-java.lang.String) |  |
| [getName(int generalFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int generalFormat)](#toString-int) |  |
### AIUEO {#AIUEO}
```
public static int AIUEO
```


Числовое форматирование. Форматирует числовой результат, используя символы хираганы в традиционном порядке a-i-u-e-o.

### ARABIC {#ARABIC}
```
public static int ARABIC
```


Числовое форматирование. Форматирует числовой результат, используя арабские количественные цифры.

### ARABIC_ABJAD {#ARABIC-ABJAD}
```
public static int ARABIC_ABJAD
```


Числовое форматирование. Форматирует числовой результат, используя восходящие цифры абджад.

### ARABIC_ALPHA {#ARABIC-ALPHA}
```
public static int ARABIC_ALPHA
```


Числовое форматирование. Форматирует числовой результат, используя символы арабского алфавита.

### ARABIC_DASH {#ARABIC-DASH}
```
public static int ARABIC_DASH
```


Числовое форматирование. Форматирует числовой результат, используя арабские количественные цифры, с префиксом "- " и суффиксом " -".

### BAHT_TEXT {#BAHT-TEXT}
```
public static int BAHT_TEXT
```


Числовое форматирование. Форматирует числовой результат в тайской системе счисления.

### CAPS {#CAPS}
```
public static int CAPS
```


Текстовое форматирование. Делает заглавной первую букву каждого слова.

### CARD_TEXT {#CARD-TEXT}
```
public static int CARD_TEXT
```


Числовое форматирование. Количественный текст (One, Two, Three, ...).

### CHAR_FORMAT {#CHAR-FORMAT}
```
public static int CHAR_FORMAT
```


Форматирование результата поля. Инструкция CHARFORMAT.

### CHINESE_NUM_1 {#CHINESE-NUM-1}
```
public static int CHINESE_NUM_1
```


Числовое форматирование. Форматирует числовой результат, используя восходящие числа из соответствующей системы счисления.

### CHINESE_NUM_2 {#CHINESE-NUM-2}
```
public static int CHINESE_NUM_2
```


Числовое форматирование. Форматирует числовой результат, используя последовательные числа из соответствующего юридического формата.

### CHINESE_NUM_3 {#CHINESE-NUM-3}
```
public static int CHINESE_NUM_3
```


Числовое форматирование. Форматирует числовой результат, используя последовательные числа из соответствующей тысячной системы счисления.

### CHOSUNG {#CHOSUNG}
```
public static int CHOSUNG
```


Числовое форматирование. Форматирует числовой результат, используя последовательные числа из корейского формата Чосунг.

### CIRCLE_NUM {#CIRCLE-NUM}
```
public static int CIRCLE_NUM
```


Числовое форматирование. Форматирует числовой результат, используя десятичную нумерацию, заключённую в круг, используя заключённый буквенно-цифровой глиф для чисел в диапазоне 1\u201320.

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


Числовое форматирование. Текст в долларах (One, Two, Three, ... + AND 55/100).

### FIRST_CAP {#FIRST-CAP}
```
public static int FIRST_CAP
```


Форматирование текста. Делает заглавной первую букву первого слова.

### GANADA {#GANADA}
```
public static int GANADA
```


Числовое форматирование. Форматирует числовой результат, используя последовательные числа из корейского формата Ганада.

### GB_1 {#GB-1}
```
public static int GB_1
```


Числовое форматирование. Форматирует числовой результат, используя десятичную нумерацию с точкой, используя заключённый буквенно-цифровой глиф.

### GB_2 {#GB-2}
```
public static int GB_2
```


Числовое форматирование. Форматирует числовой результат, используя десятичную нумерацию в скобках, используя заключённый буквенно-цифровой глиф.

### GB_3 {#GB-3}
```
public static int GB_3
```


Числовое форматирование. Форматирует числовой результат, используя десятичную нумерацию в круге, используя заключённый буквенно-цифровой глиф.

### GB_4 {#GB-4}
```
public static int GB_4
```


Числовое форматирование. Форматирует числовой результат, используя десятичную нумерацию в круге, используя заключённый буквенно-цифровой глиф.

### HEBREW_1 {#HEBREW-1}
```
public static int HEBREW_1
```


Числовое форматирование. Форматирует числовой результат, используя еврейские цифры.

### HEBREW_2 {#HEBREW-2}
```
public static int HEBREW_2
```


Числовое форматирование. Форматирует числовой результат, используя еврейский алфавит.

### HEX {#HEX}
```
public static int HEX
```


Числовое форматирование. Форматирует числовой результат, используя заглавные шестнадцатеричные цифры.

### HINDI_ARABIC {#HINDI-ARABIC}
```
public static int HINDI_ARABIC
```


Числовое форматирование. Форматирует числовой результат, используя хинди-цифры.

### HINDI_CARD_TEXT {#HINDI-CARD-TEXT}
```
public static int HINDI_CARD_TEXT
```


Числовое форматирование. Форматирует числовой результат, используя последовательные числа из хинди-счётной системы.

### HINDI_LETTER_1 {#HINDI-LETTER-1}
```
public static int HINDI_LETTER_1
```


Числовое форматирование. Форматирует числовой результат, используя хинди-гласные.

### HINDI_LETTER_2 {#HINDI-LETTER-2}
```
public static int HINDI_LETTER_2
```


Числовое форматирование. Форматирует числовой результат, используя хинди-согласные.

### IROHA {#IROHA}
```
public static int IROHA
```


Числовое форматирование. Форматирует числовой результат, используя японскую ироха.

### KANJI_NUM_1 {#KANJI-NUM-1}
```
public static int KANJI_NUM_1
```


Числовое форматирование. Форматирует числовой результат в японском стиле, используя соответствующую счётную систему.

### KANJI_NUM_2 {#KANJI-NUM-2}
```
public static int KANJI_NUM_2
```


Числовое форматирование. Форматирует числовой результат, используя соответствующую счётную систему.

### KANJI_NUM_3 {#KANJI-NUM-3}
```
public static int KANJI_NUM_3
```


Числовое форматирование. Форматирует числовой результат, используя соответствующую счётную систему.

### LOWER {#LOWER}
```
public static int LOWER
```


Форматирование текста. Все буквы в нижнем регистре.

### LOWERCASE_ALPHABETIC {#LOWERCASE-ALPHABETIC}
```
public static int LOWERCASE_ALPHABETIC
```


Числовое форматирование. Форматирует числовой результат как одно или несколько вхождений строчной латинской буквы.

### LOWERCASE_ROMAN {#LOWERCASE-ROMAN}
```
public static int LOWERCASE_ROMAN
```


Числовое форматирование. Строчные римские (i, ii, iii, ...).

### MERGE_FORMAT {#MERGE-FORMAT}
```
public static int MERGE_FORMAT
```


Форматирование результата поля. Инструкция MERGEFORMAT.

### MERGE_FORMAT_INET {#MERGE-FORMAT-INET}
```
public static int MERGE_FORMAT_INET
```


Форматирование результата поля. Инструкция MERGEFORMATINET.

### NONE {#NONE}
```
public static int NONE
```


Используется для указания отсутствующего общего формата.

### ORDINAL {#ORDINAL}
```
public static int ORDINAL
```


Числовое форматирование. Порядковые (1‑й, 2‑й, 3‑й, ...).

### ORD_TEXT {#ORD-TEXT}
```
public static int ORD_TEXT
```


Числовое форматирование. Порядковый текст (Первый, Второй, Третий, ...).

### SB_CHAR {#SB-CHAR}
```
public static int SB_CHAR
```


### THAI_ARABIC {#THAI-ARABIC}
```
public static int THAI_ARABIC
```


Числовое форматирование. Форматирует числовой результат, используя тайские цифры.

### THAI_CARD_TEXT {#THAI-CARD-TEXT}
```
public static int THAI_CARD_TEXT
```


Числовое форматирование. Форматирует числовой результат, используя последовательные числа из тайской счётной системы.

### THAI_LETTER {#THAI-LETTER}
```
public static int THAI_LETTER
```


Числовое форматирование. Форматирует числовой результат, используя тайские буквы.

### UPPER {#UPPER}
```
public static int UPPER
```


Форматирование текста. Все буквы заглавные.

### UPPERCASE_ALPHABETIC {#UPPERCASE-ALPHABETIC}
```
public static int UPPERCASE_ALPHABETIC
```


Числовое форматирование. Форматирует числовой результат как одно или несколько вхождений заглавного латинского буквенного символа.

### UPPERCASE_ROMAN {#UPPERCASE-ROMAN}
```
public static int UPPERCASE_ROMAN
```


Числовое форматирование. Заглавные римские цифры (I, II, III, ...).

### VIET_CARD_TEXT {#VIET-CARD-TEXT}
```
public static int VIET_CARD_TEXT
```


Числовое форматирование. Форматирует числовой результат с использованием вьетнамских цифр.

### ZODIAC_1 {#ZODIAC-1}
```
public static int ZODIAC_1
```


Числовое форматирование. Форматирует числовой результат с использованием последовательных традиционных числовых иероглифов.

### ZODIAC_2 {#ZODIAC-2}
```
public static int ZODIAC_2
```


Числовое форматирование. Форматирует числовой результат с использованием последовательных зодиакальных иероглифов.

### ZODIAC_3 {#ZODIAC-3}
```
public static int ZODIAC_3
```


Числовое форматирование. Форматирует числовой результат с использованием последовательных традиционных зодиакальных иероглифов.

### length {#length}
```
public static int length
```


### fromName(String generalFormatName) {#fromName-java.lang.String}
```
public static int fromName(String generalFormatName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| generalFormatName | java.lang.String |  |

**Returns:**
int
### getName(int generalFormat) {#getName-int}
```
public static String getName(int generalFormat)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| generalFormat | int |  |

**Returns:**
java.lang.String
