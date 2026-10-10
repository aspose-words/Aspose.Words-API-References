---
title: "GeneralFormat"
linktitle: "GeneralFormat"
second_title: "Aspose.Words لـ Java"
description: "يحدد تنسيقًا عامًا يُطبق على نص رقمي أو أي نتيجة حقل في Java."
type: docs
weight: 355
url: /ar/java/com.aspose.words/generalformat/
---

**Inheritance:**
java.lang.Object
```
public class GeneralFormat
```

يحدد تنسيقًا عامًا يُطبق على نتيجة رقمية أو نصية أو أي حقل. قد يحتوي الحقل على مجموعة من التنسيقات العامة.

 **Examples:** 

يوضح كيفية تنسيق نتائج الحقول.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [AIUEO](#AIUEO) | تنسيق رقمي. |
| [ARABIC](#ARABIC) | تنسيق رقمي. |
| [ARABIC_ABJAD](#ARABIC-ABJAD) | تنسيق رقمي. |
| [ARABIC_ALPHA](#ARABIC-ALPHA) | تنسيق رقمي. |
| [ARABIC_DASH](#ARABIC-DASH) | تنسيق رقمي. |
| [BAHT_TEXT](#BAHT-TEXT) | تنسيق رقمي. |
| [CAPS](#CAPS) | تنسيق نص. |
| [CARD_TEXT](#CARD-TEXT) | تنسيق رقمي. |
| [CHAR_FORMAT](#CHAR-FORMAT) | تنسيق نتيجة الحقل. |
| [CHINESE_NUM_1](#CHINESE-NUM-1) | تنسيق رقمي. |
| [CHINESE_NUM_2](#CHINESE-NUM-2) | تنسيق رقمي. |
| [CHINESE_NUM_3](#CHINESE-NUM-3) | تنسيق رقمي. |
| [CHOSUNG](#CHOSUNG) | تنسيق رقمي. |
| [CIRCLE_NUM](#CIRCLE-NUM) | تنسيق رقمي. |
| [DB_CHAR](#DB-CHAR) |  |
| [DB_NUM_1](#DB-NUM-1) |  |
| [DB_NUM_2](#DB-NUM-2) |  |
| [DB_NUM_3](#DB-NUM-3) |  |
| [DB_NUM_4](#DB-NUM-4) |  |
| [DOLLAR_TEXT](#DOLLAR-TEXT) | تنسيق رقمي. |
| [FIRST_CAP](#FIRST-CAP) | تنسيق نص. |
| [GANADA](#GANADA) | تنسيق رقمي. |
| [GB_1](#GB-1) | تنسيق رقمي. |
| [GB_2](#GB-2) | تنسيق رقمي. |
| [GB_3](#GB-3) | تنسيق رقمي. |
| [GB_4](#GB-4) | تنسيق رقمي. |
| [HEBREW_1](#HEBREW-1) | تنسيق رقمي. |
| [HEBREW_2](#HEBREW-2) | تنسيق رقمي. |
| [HEX](#HEX) | تنسيق رقمي. |
| [HINDI_ARABIC](#HINDI-ARABIC) | تنسيق رقمي. |
| [HINDI_CARD_TEXT](#HINDI-CARD-TEXT) | تنسيق رقمي. |
| [HINDI_LETTER_1](#HINDI-LETTER-1) | تنسيق رقمي. |
| [HINDI_LETTER_2](#HINDI-LETTER-2) | تنسيق رقمي. |
| [IROHA](#IROHA) | تنسيق رقمي. |
| [KANJI_NUM_1](#KANJI-NUM-1) | تنسيق رقمي. |
| [KANJI_NUM_2](#KANJI-NUM-2) | تنسيق رقمي. |
| [KANJI_NUM_3](#KANJI-NUM-3) | تنسيق رقمي. |
| [LOWER](#LOWER) | تنسيق نص. |
| [LOWERCASE_ALPHABETIC](#LOWERCASE-ALPHABETIC) | تنسيق رقمي. |
| [LOWERCASE_ROMAN](#LOWERCASE-ROMAN) | تنسيق رقمي. |
| [MERGE_FORMAT](#MERGE-FORMAT) | تنسيق نتيجة الحقل. |
| [MERGE_FORMAT_INET](#MERGE-FORMAT-INET) | تنسيق نتيجة الحقل. |
| [NONE](#NONE) | يُستخدم لتحديد تنسيق عام مفقود. |
| [ORDINAL](#ORDINAL) | تنسيق رقمي. |
| [ORD_TEXT](#ORD-TEXT) | تنسيق رقمي. |
| [SB_CHAR](#SB-CHAR) |  |
| [THAI_ARABIC](#THAI-ARABIC) | تنسيق رقمي. |
| [THAI_CARD_TEXT](#THAI-CARD-TEXT) | تنسيق رقمي. |
| [THAI_LETTER](#THAI-LETTER) | تنسيق رقمي. |
| [UPPER](#UPPER) | تنسيق نص. |
| [UPPERCASE_ALPHABETIC](#UPPERCASE-ALPHABETIC) | تنسيق رقمي. |
| [UPPERCASE_ROMAN](#UPPERCASE-ROMAN) | تنسيق رقمي. |
| [VIET_CARD_TEXT](#VIET-CARD-TEXT) | تنسيق رقمي. |
| [ZODIAC_1](#ZODIAC-1) | تنسيق رقمي. |
| [ZODIAC_2](#ZODIAC-2) | تنسيق رقمي. |
| [ZODIAC_3](#ZODIAC-3) | تنسيق رقمي. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String generalFormatName)](#fromName-java.lang.String) |  |
| [getName(int generalFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int generalFormat)](#toString-int) |  |
### AIUEO {#AIUEO}
```
public static int AIUEO
```


تنسيق رقمي. ينسق نتيجة رقمية باستخدام أحرف الهيراغانا بالترتيب التقليدي a-i-u-e-o.

### ARABIC {#ARABIC}
```
public static int ARABIC
```


تنسيق رقمي. ينسق نتيجة رقمية باستخدام الأرقام العربية الترتيبية.

### ARABIC_ABJAD {#ARABIC-ABJAD}
```
public static int ARABIC_ABJAD
```


تنسيق رقمي. ينسق نتيجة رقمية باستخدام أرقام أبجد تصاعدية.

### ARABIC_ALPHA {#ARABIC-ALPHA}
```
public static int ARABIC_ALPHA
```


تنسيق رقمي. ينسق نتيجة رقمية باستخدام أحرف الأبجدية العربية.

### ARABIC_DASH {#ARABIC-DASH}
```
public static int ARABIC_DASH
```


تنسيق رقمي. ينسق نتيجة رقمية باستخدام الأرقام العربية الترتيبية، مع بادئة "- " ولاحقة " -".

### BAHT_TEXT {#BAHT-TEXT}
```
public static int BAHT_TEXT
```


تنسيق رقمي. ينسق نتيجة رقمية بنظام العد التايلاندي.

### CAPS {#CAPS}
```
public static int CAPS
```


تنسيق نص. يضع الحرف الأول من كل كلمة بحرف كبير.

### CARD_TEXT {#CARD-TEXT}
```
public static int CARD_TEXT
```


تنسيق رقمي. نص ترتيبي (One, Two, Three, ...).

### CHAR_FORMAT {#CHAR-FORMAT}
```
public static int CHAR_FORMAT
```


تنسيق نتيجة الحقل. تعليمة CHARFORMAT.

### CHINESE_NUM_1 {#CHINESE-NUM-1}
```
public static int CHINESE_NUM_1
```


تنسيق رقمي. ينسق نتيجة رقمية باستخدام أرقام تصاعدية من نظام العد المناسب.

### CHINESE_NUM_2 {#CHINESE-NUM-2}
```
public static int CHINESE_NUM_2
```


تنسيق رقمي. ينسق نتيجة رقمية باستخدام أرقام متسلسلة من التنسيق القانوني المناسب.

### CHINESE_NUM_3 {#CHINESE-NUM-3}
```
public static int CHINESE_NUM_3
```


تنسيق رقمي. ينسق نتيجة رقمية باستخدام أرقام متسلسلة من نظام العد بالألف المناسب.

### CHOSUNG {#CHOSUNG}
```
public static int CHOSUNG
```


تنسيق رقمي. ينسق نتيجة رقمية باستخدام أرقام متسلسلة من تنسيق Chosung الكوري.

### CIRCLE_NUM {#CIRCLE-NUM}
```
public static int CIRCLE_NUM
```


تنسيق رقمي. ينسق نتيجة رقمية باستخدام ترقيم عشري محاط بدائرة، باستخدام حرف رمزي أبجدي رقمي محاط للأرقام في النطاق 1\\\\u201320.

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


تنسيق رقمي. نص الدولار (One, Two, Three, ... + AND 55/100).

### FIRST_CAP {#FIRST-CAP}
```
public static int FIRST_CAP
```


تنسيق النص. يضع الحرف الأول من الكلمة الأولى بحرف كبير.

### GANADA {#GANADA}
```
public static int GANADA
```


تنسيق رقمي. ينسق نتيجة رقمية باستخدام أرقام متسلسلة من تنسيق كانادا الكوري.

### GB_1 {#GB-1}
```
public static int GB_1
```


تنسيق رقمي. ينسق نتيجة رقمية باستخدام ترقيم عشري يتبعه نقطة، باستخدام حرف رمزي أبجدي مضمّن.

### GB_2 {#GB-2}
```
public static int GB_2
```


تنسيق رقمي. ينسق نتيجة رقمية باستخدام ترقيم عشري محاط بأقواس، باستخدام حرف رمزي أبجدي مضمّن.

### GB_3 {#GB-3}
```
public static int GB_3
```


تنسيق رقمي. ينسق نتيجة رقمية باستخدام ترقيم عشري محاط بدائرة، باستخدام حرف رمزي أبجدي مضمّن.

### GB_4 {#GB-4}
```
public static int GB_4
```


تنسيق رقمي. ينسق نتيجة رقمية باستخدام ترقيم عشري محاط بدائرة، باستخدام حرف رمزي أبجدي مضمّن.

### HEBREW_1 {#HEBREW-1}
```
public static int HEBREW_1
```


تنسيق رقمي. ينسق نتيجة رقمية باستخدام أرقام عبريّة.

### HEBREW_2 {#HEBREW-2}
```
public static int HEBREW_2
```


تنسيق رقمي. ينسق نتيجة رقمية باستخدام الأبجدية العبرية.

### HEX {#HEX}
```
public static int HEX
```


تنسيق رقمي. ينسق النتيجة الرقمية باستخدام أرقام سداسية عشرية بحروف كبيرة.

### HINDI_ARABIC {#HINDI-ARABIC}
```
public static int HINDI_ARABIC
```


تنسيق رقمي. ينسق نتيجة رقمية باستخدام أرقام هندية.

### HINDI_CARD_TEXT {#HINDI-CARD-TEXT}
```
public static int HINDI_CARD_TEXT
```


تنسيق رقمي. ينسق نتيجة رقمية باستخدام أرقام متسلسلة من نظام العد الهندي.

### HINDI_LETTER_1 {#HINDI-LETTER-1}
```
public static int HINDI_LETTER_1
```


تنسيق رقمي. ينسق نتيجة رقمية باستخدام حروف العلة الهندية.

### HINDI_LETTER_2 {#HINDI-LETTER-2}
```
public static int HINDI_LETTER_2
```


تنسيق رقمي. ينسق نتيجة رقمية باستخدام حروف الساكنة الهندية.

### IROHA {#IROHA}
```
public static int IROHA
```


تنسيق رقمي. ينسق نتيجة رقمية باستخدام إروها اليابانية.

### KANJI_NUM_1 {#KANJI-NUM-1}
```
public static int KANJI_NUM_1
```


تنسيق رقمي. ينسق نتيجة رقمية باستخدام نمط ياباني مع نظام العد المناسب.

### KANJI_NUM_2 {#KANJI-NUM-2}
```
public static int KANJI_NUM_2
```


تنسيق رقمي. ينسق نتيجة رقمية باستخدام نظام العد المناسب.

### KANJI_NUM_3 {#KANJI-NUM-3}
```
public static int KANJI_NUM_3
```


تنسيق رقمي. ينسق نتيجة رقمية باستخدام نظام العد المناسب.

### LOWER {#LOWER}
```
public static int LOWER
```


تنسيق النص. جميع الأحرف صغيرة.

### LOWERCASE_ALPHABETIC {#LOWERCASE-ALPHABETIC}
```
public static int LOWERCASE_ALPHABETIC
```


تنسيق رقمي. ينسق نتيجة رقمية كواحد أو أكثر من تكرارات حرف لاتيني أبجدي صغير.

### LOWERCASE_ROMAN {#LOWERCASE-ROMAN}
```
public static int LOWERCASE_ROMAN
```


تنسيق رقمي. أرقام رومانية صغيرة (i, ii, iii, ...).

### MERGE_FORMAT {#MERGE-FORMAT}
```
public static int MERGE_FORMAT
```


تنسيق نتيجة الحقل. تعليمة MERGEFORMAT.

### MERGE_FORMAT_INET {#MERGE-FORMAT-INET}
```
public static int MERGE_FORMAT_INET
```


تنسيق نتيجة الحقل. تعليمة MERGEFORMATINET.

### NONE {#NONE}
```
public static int NONE
```


يُستخدم لتحديد تنسيق عام مفقود.

### ORDINAL {#ORDINAL}
```
public static int ORDINAL
```


تنسيق رقمي. ترتيبي (1st, 2nd, 3rd, ...).

### ORD_TEXT {#ORD-TEXT}
```
public static int ORD_TEXT
```


تنسيق رقمي. نص ترتيبي (First, Second, Third, ...).

### SB_CHAR {#SB-CHAR}
```
public static int SB_CHAR
```


### THAI_ARABIC {#THAI-ARABIC}
```
public static int THAI_ARABIC
```


تنسيق رقمي. ينسق نتيجة رقمية باستخدام أرقام تايلاندية.

### THAI_CARD_TEXT {#THAI-CARD-TEXT}
```
public static int THAI_CARD_TEXT
```


تنسيق رقمي. ينسق نتيجة رقمية باستخدام أرقام متسلسلة من نظام العد التايلاندي.

### THAI_LETTER {#THAI-LETTER}
```
public static int THAI_LETTER
```


تنسيق رقمي. ينسق نتيجة رقمية باستخدام حروف تايلاندية.

### UPPER {#UPPER}
```
public static int UPPER
```


تنسيق النص. جميع الأحرف بأحرف كبيرة.

### UPPERCASE_ALPHABETIC {#UPPERCASE-ALPHABETIC}
```
public static int UPPERCASE_ALPHABETIC
```


تنسيق رقمي. ينسق نتيجة رقمية كواحد أو أكثر من ظهور حرف أبجدي لاتيني كبير.

### UPPERCASE_ROMAN {#UPPERCASE-ROMAN}
```
public static int UPPERCASE_ROMAN
```


تنسيق رقمي. أرقام رومانية بأحرف كبيرة (I, II, III, ...).

### VIET_CARD_TEXT {#VIET-CARD-TEXT}
```
public static int VIET_CARD_TEXT
```


تنسيق رقمي. ينسق نتيجة رقمية باستخدام الأرقام الفيتنامية.

### ZODIAC_1 {#ZODIAC-1}
```
public static int ZODIAC_1
```


تنسيق رقمي. ينسق نتيجة رقمية باستخدام الأحرف التقليدية الرقمية المتسلسلة.

### ZODIAC_2 {#ZODIAC-2}
```
public static int ZODIAC_2
```


تنسيق رقمي. ينسق نتيجة رقمية باستخدام الأحرف المتسلسلة لأبراج الزودياك.

### ZODIAC_3 {#ZODIAC-3}
```
public static int ZODIAC_3
```


تنسيق رقمي. ينسق نتيجة رقمية باستخدام الأحرف التقليدية المتسلسلة لأبراج الزودياك.

### length {#length}
```
public static int length
```


### fromName(String generalFormatName) {#fromName-java.lang.String}
```
public static int fromName(String generalFormatName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| generalFormatName | java.lang.String |  |

**Returns:**
int
### getName(int generalFormat) {#getName-int}
```
public static String getName(int generalFormat)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| generalFormat | int |  |

**Returns:**
java.lang.String
