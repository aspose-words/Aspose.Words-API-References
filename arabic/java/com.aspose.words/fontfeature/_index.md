---
title: "FontFeature"
linktitle: "FontFeature"
second_title: "Aspose.Words لـ Java"
description: "توفر الميزات معلومات حول كيفية استخدام الحروف في الخط لتصيير النص في Java."
type: docs
weight: 325
url: /ar/java/com.aspose.words/fontfeature/
---

**Inheritance:**
java.lang.Object
```
public class FontFeature
```

توفر الميزات معلومات حول كيفية استخدام الحروف في الخط لتصيير النص. https://docs.microsoft.com/en-us/typography/opentype/spec/featuretags
## الحقول

| حقل | الوصف |
| --- | --- |
| [CONTEXTUAL_LIGATURES](#CONTEXTUAL-LIGATURES) | يستبدل تسلسلًا من الحروف بحرف واحد يُفضَّل لأغراض الطباعة. |
| [DISCRETIONARY_LIGATURES](#DISCRETIONARY-LIGATURES) | يستبدل تسلسلًا من الحروف بحرف واحد يُفضَّل لأغراض الطباعة. |
| [GLYPH_COMPOSITION_DECOMPOSITION](#GLYPH-COMPOSITION-DECOMPOSITION) | لتقليل عدد بدائل الرموز، قد يكون من المرغوب أحيانًا تفكيك الرمز الافتراضي لحرف ما إلى رمزين أو أكثر. |
| [HISTORICAL_LIGATURES](#HISTORICAL-LIGATURES) | كانت بعض الأحرف المتصلة شائعة الاستخدام في الماضي، لكنها تبدو قديمة اليوم. |
| [KERNING](#KERNING) | يضبط مقدار المسافة بين الرموز، عادةً لتوفير تباعد بصري متسق بين الرموز. |
| [LINING_FIGURES](#LINING-FIGURES) | تقوم هذه الميزة بتحويل الأرقام غير المتراصة المختارة إلى أرقام متراصة. |
| [OLDSTYLE_FIGURES](#OLDSTYLE-FIGURES) | تقوم هذه الميزة بتحويل الأرقام المختارة من النمط الافتراضي أو المتراص إلى الشكل القديم. |
| [PROPORTIONAL_FIGURES](#PROPORTIONAL-FIGURES) | يستبدل رموز الأرقام التي تم ضبطها على عرض موحد (جدولي) بالرموز المقابلة التي تم ضبطها على عرض خاص بالرمز (متناسب). |
| [REQUIRED_LIGATURES](#REQUIRED-LIGATURES) | يستبدل تسلسلًا من الحروف بحرف واحد يُفضَّل لأغراض الطباعة. |
| [STANDARD_LIGATURES](#STANDARD-LIGATURES) | يستبدل تسلسلًا من الحروف بحرف واحد يُفضَّل لأغراض الطباعة. |
| [STYLISTIC_SET_01](#STYLISTIC-SET-01) | مجموعة نمطية 1 بالإضافة إلى أو بدلاً من البدائل النمطية للرموز الفردية (انظر ميزة 'salt')، قد تحتوي بعض الخطوط على مجموعات من رموز نمطية بديلة تتطابق مع أجزاء من مجموعة الأحرف، على سبيل المثال. |
| [STYLISTIC_SET_02](#STYLISTIC-SET-02) | مجموعة نمطية 2 العلامة المكافئة في OpenType: 'ss02' |
| [STYLISTIC_SET_03](#STYLISTIC-SET-03) | مجموعة نمطية 3 العلامة المكافئة في OpenType: 'ss03' |
| [STYLISTIC_SET_04](#STYLISTIC-SET-04) | مجموعة نمطية 4 العلامة المكافئة في OpenType: 'ss04' |
| [STYLISTIC_SET_05](#STYLISTIC-SET-05) | مجموعة نمطية 5 العلامة المكافئة في OpenType: 'ss05' |
| [STYLISTIC_SET_06](#STYLISTIC-SET-06) | مجموعة نمطية 6 العلامة المكافئة في OpenType: 'ss06' |
| [STYLISTIC_SET_07](#STYLISTIC-SET-07) | مجموعة نمطية 7 العلامة المكافئة في OpenType: 'ss07' |
| [STYLISTIC_SET_08](#STYLISTIC-SET-08) | مجموعة نمطية 8 العلامة المكافئة في OpenType: 'ss08' |
| [STYLISTIC_SET_09](#STYLISTIC-SET-09) | مجموعة نمطية 9 العلامة المكافئة في OpenType: 'ss09' |
| [STYLISTIC_SET_10](#STYLISTIC-SET-10) | مجموعة نمطية 10 العلامة المكافئة في OpenType: 'ss10' |
| [STYLISTIC_SET_11](#STYLISTIC-SET-11) | مجموعة نمطية 11 العلامة المكافئة في OpenType: 'ss11' |
| [STYLISTIC_SET_12](#STYLISTIC-SET-12) | مجموعة نمطية 12 العلامة المكافئة في OpenType: 'ss12' |
| [STYLISTIC_SET_13](#STYLISTIC-SET-13) | مجموعة نمطية 13 العلامة المكافئة في OpenType: 'ss13' |
| [STYLISTIC_SET_14](#STYLISTIC-SET-14) | مجموعة نمطية 14 العلامة المكافئة في OpenType: 'ss14' |
| [STYLISTIC_SET_15](#STYLISTIC-SET-15) | مجموعة نمطية 15 العلامة المكافئة في OpenType: 'ss15' |
| [STYLISTIC_SET_16](#STYLISTIC-SET-16) | مجموعة نمطية 16 العلامة المكافئة في OpenType: 'ss16' |
| [STYLISTIC_SET_17](#STYLISTIC-SET-17) | مجموعة نمطية 17 العلامة المكافئة في OpenType: 'ss17' |
| [STYLISTIC_SET_18](#STYLISTIC-SET-18) | مجموعة نمطية 18 العلامة المكافئة في OpenType: 'ss18' |
| [STYLISTIC_SET_19](#STYLISTIC-SET-19) | مجموعة نمطية 19 العلامة المكافئة في OpenType: 'ss19' |
| [STYLISTIC_SET_20](#STYLISTIC-SET-20) | مجموعة الأنماط 20 ما يعادل وسم OpenType: 'ss20' |
| [TABULAR_FIGURES](#TABULAR-FIGURES) | يستبدل رموز الأرقام المضبوطة على عرض نسبي بالرموز المقابلة المضبوطة على عرض موحد (جدولي). |
| [VERTICAL_ALTERNATES](#VERTICAL-ALTERNATES) | يحوّل الرموز الافتراضية إلى رموز مناسبة للعرض العمودي في وضع الكتابة العمودية. |
| [VERTICAL_ALTERNATES_AND_ROTATION](#VERTICAL-ALTERNATES-AND-ROTATION) | يستبدل بعض الرموز ذات العرض الثابت (نصف، ثلث أو ربع العرض) أو الرموز ذات العرض النسبي (معظمها لاتينية أو كاتاكانا) بأشكال مناسبة للكتابة العمودية (أي، مُدوَّرة 90 درجة باتجاه عقارب الساعة). |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String fontFeatureName)](#fromName-java.lang.String) |  |
| [getName(int fontFeature)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int fontFeature)](#toString-int) |  |
### CONTEXTUAL_LIGATURES {#CONTEXTUAL-LIGATURES}
```
public static int CONTEXTUAL_LIGATURES
```


يستبدل تسلسلًا من الرموز برمز واحد يُفضَّل لأغراض الطباعة. على عكس ميزات الحروف المتصلة الأخرى، 'clig' يحدد السياق الذي يُنصح فيه باستخدام الحرف المتصل. هذه القدرة مهمة في بعض تصاميم الخطوط وللحروف المتصلة المزخرفة. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ae\#clig ما يعادل وسم OpenType: 'clig'

### DISCRETIONARY_LIGATURES {#DISCRETIONARY-LIGATURES}
```
public static int DISCRETIONARY_LIGATURES
```


يستبدل تسلسلًا من الرموز برمز واحد يُفضَّل لأغراض الطباعة. تغطي هذه الميزة الحروف المتصلة التي قد تُستَخدم لتأثير خاص، حسب تفضيل المستخدم\u2019s. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ae\#dlig ما يعادل وسم OpenType: 'dlig'

### GLYPH_COMPOSITION_DECOMPOSITION {#GLYPH-COMPOSITION-DECOMPOSITION}
```
public static int GLYPH_COMPOSITION_DECOMPOSITION
```


لتقليل عدد البدائل للرموز، قد يكون من المرغوب أحيانًا تفكيك الرمز الافتراضي لحرف إلى رمزين أو أكثر. بالإضافة إلى ذلك، قد يكون من الأفضل تجميع الرموز الافتراضية لحرفين أو أكثر في رمز واحد لتحسين معالجة الرموز. تسمح هذه الميزة بمثل هذا التجميع/التفكيك. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ae\#ccmp ما يعادل وسم OpenType: 'ccmp'

### HISTORICAL_LIGATURES {#HISTORICAL-LIGATURES}
```
public static int HISTORICAL_LIGATURES
```


كانت بعض الحروف المتصلة شائعة الاستخدام في الماضي، لكنها تبدو قديمة اليوم. بعض الخطوط تتضمن الأشكال التاريخية كبدائل، بحيث يمكن استخدامها لتأثير العصر. تستبدل هذه الميزة الأشكال الافتراضية (الحالية) بالبدائل التاريخية. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_fj\#hlig ما يعادل وسم OpenType: 'hlig'

### KERNING {#KERNING}
```
public static int KERNING
```


يضبط مقدار المسافة بين الرموز، عادةً لتوفير تباعد بصري متسق بين الرموز. على الرغم من أن الخط المصمم جيدًا يمتلك تباعدًا متسقًا بين الرموز بشكل عام، إلا أن بعض تركيبات الرموز تتطلب تعديلًا لتحسين القابلية للقراءة. إلى جانب الضبط القياسي في الاتجاه الأفقي، يمكن لهذه الميزة توفير بيانات تباعد تعتمد على الحجم عبر جداول الأجهزة، وتباعد عبر التدفق في اتجاه النص Y، وضبط موضع الرموز بشكل مستقل عن ضبط التقدم. لاحظ أن هذه الميزة قد تُطبق على سلاسل تتجاوز رمزين، ولن تُستخدم في الخطوط ذات العرض الأحادي. كما لاحظ أن هذه الميزة لا تُطبق على النص المُضبط عموديًا. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ko\#kern ما يعادل وسم OpenType: 'kern'

### LINING_FIGURES {#LINING-FIGURES}
```
public static int LINING_FIGURES
```


تغيّر هذه الميزة الأرقام غير الخطية المختارة إلى أرقام خطية. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ko\#lnum ما يعادل وسم OpenType: 'lnum'

### OLDSTYLE_FIGURES {#OLDSTYLE-FIGURES}
```
public static int OLDSTYLE_FIGURES
```


تغيّر هذه الميزة الأرقام المختارة من النمط الافتراضي أو الخطية إلى الشكل القديم. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ko\#onum ما يعادل وسم OpenType: 'onum'

### PROPORTIONAL_FIGURES {#PROPORTIONAL-FIGURES}
```
public static int PROPORTIONAL_FIGURES
```


يستبدل رموز الأرقام المضبوطة على عرض موحد (جدولي) بالرموز المقابلة المضبوطة على عرض خاص بالرمز (نسبي). https://docs.microsoft.com/en-us/typography/opentype/spec/features\_pt\#tag-pnum ما يعادل وسم OpenType: 'pnum'

### REQUIRED_LIGATURES {#REQUIRED-LIGATURES}
```
public static int REQUIRED_LIGATURES
```


يستبدل تسلسلًا من الرموز برمز واحد يُفضَّل لأغراض الطباعة. تغطي هذه الميزة تلك الحروف المتصلة التي يحدد النص أنها ضرورية للاستخدام في الظروف العادية. هذه الميزة مهمة لبعض النصوص لضمان تشكيل الرموز بشكل صحيح. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_pt\#rlig ما يعادل وسم OpenType: 'rlig'

### STANDARD_LIGATURES {#STANDARD-LIGATURES}
```
public static int STANDARD_LIGATURES
```


يستبدل تسلسل من الرموز برمز واحد يُفضَّل لأغراض الطباعة. يغطي هذا الميزة الأحرف المتصلة التي يقرر المصمم/الصانع أنه يجب استخدامها في الظروف العادية. علامة OpenType المكافئة: 'liga' https://docs.microsoft.com/en-us/typography/opentype/spec/features\_ko\#liga

### STYLISTIC_SET_01 {#STYLISTIC-SET-01}
```
public static int STYLISTIC_SET_01
```


مجموعة الأنماط 1 بالإضافة إلى، أو بدلاً من، البدائل الأنماطية للأحرف الفردية (انظر ميزة 'salt')، قد تحتوي بعض الخطوط على مجموعات من الأحرف المتغيرة الأنماطية التي تتCorrespond إلى أجزاء من مجموعة الأحرف، مثل عدة متغيرات للأحرف الصغيرة في خط لاتيني. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_pt\#tag-ss01---ss20 علامة OpenType المكافئة: 'ss01'

### STYLISTIC_SET_02 {#STYLISTIC-SET-02}
```
public static int STYLISTIC_SET_02
```


مجموعة نمطية 2 العلامة المكافئة في OpenType: 'ss02'

### STYLISTIC_SET_03 {#STYLISTIC-SET-03}
```
public static int STYLISTIC_SET_03
```


مجموعة نمطية 3 العلامة المكافئة في OpenType: 'ss03'

### STYLISTIC_SET_04 {#STYLISTIC-SET-04}
```
public static int STYLISTIC_SET_04
```


مجموعة نمطية 4 العلامة المكافئة في OpenType: 'ss04'

### STYLISTIC_SET_05 {#STYLISTIC-SET-05}
```
public static int STYLISTIC_SET_05
```


مجموعة نمطية 5 العلامة المكافئة في OpenType: 'ss05'

### STYLISTIC_SET_06 {#STYLISTIC-SET-06}
```
public static int STYLISTIC_SET_06
```


مجموعة نمطية 6 العلامة المكافئة في OpenType: 'ss06'

### STYLISTIC_SET_07 {#STYLISTIC-SET-07}
```
public static int STYLISTIC_SET_07
```


مجموعة نمطية 7 العلامة المكافئة في OpenType: 'ss07'

### STYLISTIC_SET_08 {#STYLISTIC-SET-08}
```
public static int STYLISTIC_SET_08
```


مجموعة نمطية 8 العلامة المكافئة في OpenType: 'ss08'

### STYLISTIC_SET_09 {#STYLISTIC-SET-09}
```
public static int STYLISTIC_SET_09
```


مجموعة نمطية 9 العلامة المكافئة في OpenType: 'ss09'

### STYLISTIC_SET_10 {#STYLISTIC-SET-10}
```
public static int STYLISTIC_SET_10
```


مجموعة نمطية 10 العلامة المكافئة في OpenType: 'ss10'

### STYLISTIC_SET_11 {#STYLISTIC-SET-11}
```
public static int STYLISTIC_SET_11
```


مجموعة نمطية 11 العلامة المكافئة في OpenType: 'ss11'

### STYLISTIC_SET_12 {#STYLISTIC-SET-12}
```
public static int STYLISTIC_SET_12
```


مجموعة نمطية 12 العلامة المكافئة في OpenType: 'ss12'

### STYLISTIC_SET_13 {#STYLISTIC-SET-13}
```
public static int STYLISTIC_SET_13
```


مجموعة نمطية 13 العلامة المكافئة في OpenType: 'ss13'

### STYLISTIC_SET_14 {#STYLISTIC-SET-14}
```
public static int STYLISTIC_SET_14
```


مجموعة نمطية 14 العلامة المكافئة في OpenType: 'ss14'

### STYLISTIC_SET_15 {#STYLISTIC-SET-15}
```
public static int STYLISTIC_SET_15
```


مجموعة نمطية 15 العلامة المكافئة في OpenType: 'ss15'

### STYLISTIC_SET_16 {#STYLISTIC-SET-16}
```
public static int STYLISTIC_SET_16
```


مجموعة نمطية 16 العلامة المكافئة في OpenType: 'ss16'

### STYLISTIC_SET_17 {#STYLISTIC-SET-17}
```
public static int STYLISTIC_SET_17
```


مجموعة نمطية 17 العلامة المكافئة في OpenType: 'ss17'

### STYLISTIC_SET_18 {#STYLISTIC-SET-18}
```
public static int STYLISTIC_SET_18
```


مجموعة نمطية 18 العلامة المكافئة في OpenType: 'ss18'

### STYLISTIC_SET_19 {#STYLISTIC-SET-19}
```
public static int STYLISTIC_SET_19
```


مجموعة نمطية 19 العلامة المكافئة في OpenType: 'ss19'

### STYLISTIC_SET_20 {#STYLISTIC-SET-20}
```
public static int STYLISTIC_SET_20
```


مجموعة الأنماط 20 ما يعادل وسم OpenType: 'ss20'

### TABULAR_FIGURES {#TABULAR-FIGURES}
```
public static int TABULAR_FIGURES
```


يستبدل رموز الأرقام التي تم ضبطها على عرض نسبي بالرموز المقابلة التي تم ضبطها على عرض موحد (جدولي). عادةً ما يكون العرض الجدولي هو الافتراضي، لكن لا يمكن الاعتماد على ذلك بأمان. بالطبع هذا الميزة لن تكون موجودة في التصاميم ذات العرض الأحادي. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_pt\#tag-tnum علامة OpenType المكافئة: 'tnum'

### VERTICAL_ALTERNATES {#VERTICAL-ALTERNATES}
```
public static int VERTICAL_ALTERNATES
```


يحوّل الرموز الافتراضية إلى رموز مناسبة للعرض العمودي في وضع الكتابة العمودية. https://docs.microsoft.com/en-us/typography/opentype/spec/features\_uz\#tag-vert علامة OpenType المكافئة: 'vert'

### VERTICAL_ALTERNATES_AND_ROTATION {#VERTICAL-ALTERNATES-AND-ROTATION}
```
public static int VERTICAL_ALTERNATES_AND_ROTATION
```


يستبدل بعض الرموز ذات العرض الثابت (نصف عرض، ثلث عرض أو ربع عرض) أو الرموز ذات العرض النسبي (معظمها لاتيني أو كاتاكانا) بأشكال مناسبة للكتابة العمودية (أي، مدورة 90 درجة باتجاه عقارب الساعة). https://docs.microsoft.com/en-us/typography/opentype/spec/features\_uz\#tag-vrt2 علامة OpenType المكافئة: 'vrt2'

### length {#length}
```
public static int length
```


### fromName(String fontFeatureName) {#fromName-java.lang.String}
```
public static int fromName(String fontFeatureName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fontFeatureName | java.lang.String |  |

**Returns:**
int
### getName(int fontFeature) {#getName-int}
```
public static String getName(int fontFeature)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fontFeature | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int fontFeature) {#toString-int}
```
public static String toString(int fontFeature)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| fontFeature | int |  |

**Returns:**
java.lang.String
