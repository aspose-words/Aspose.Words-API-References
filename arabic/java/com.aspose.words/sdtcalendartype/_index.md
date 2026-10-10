---
title: "SdtCalendarType"
linktitle: "SdtCalendarType"
second_title: "Aspose.Words لـ Java"
description: "يحدد أنواع التقويم الممكنة التي يمكن استخدامها لتحديد StructuredDocumentTag.getCalendarType / StructuredDocumentTag.setCalendarTypeint في مستند Office Open XML بلغة Java."
type: docs
weight: 600
url: /ar/java/com.aspose.words/sdtcalendartype/
---

**Inheritance:**
java.lang.Object
```
public class SdtCalendarType
```

يحدد أنواع التقويم الممكنة التي يمكن استخدامها لتحديد [StructuredDocumentTag.getCalendarType()](../../com.aspose.words/structureddocumenttag/\#getCalendarType) / [StructuredDocumentTag.setCalendarType(int)](../../com.aspose.words/structureddocumenttag/\#setCalendarType-int) في مستند Office Open XML.

 **Examples:** 

يعرض كيفية مطالبة المستخدم بإدخال تاريخ باستخدام علامة مستند منسقة.

```

 Document doc = new Document();

 // Insert a structured document tag that prompts the user to enter a date.
 // In Microsoft Word, this element is known as a "Date picker content control".
 // When we click on the arrow on the right end of this tag in Microsoft Word,
 // we will see a pop up in the form of a clickable calendar.
 // We can use that popup to select a date that the tag will display.
 StructuredDocumentTag sdtDate = new StructuredDocumentTag(doc, SdtType.DATE, MarkupLevel.INLINE);

 // Display the date, according to the Saudi Arabian Arabic locale.
 sdtDate.setDateDisplayLocale(1025);

 // Set the format with which to display the date.
 sdtDate.setDateDisplayFormat("dd MMMM, yyyy");
 sdtDate.setDateStorageFormat(SdtDateStorageFormat.DATE_TIME);

 // Display the date according to the Hijri calendar.
 sdtDate.setCalendarType(SdtCalendarType.HIJRI);

 // Before the user chooses a date in Microsoft Word, the tag will display the text "Click here to enter a date.".
 // According to the tag's calendar, set the "FullDate" property to get the tag to display a default date.
 Calendar cal = Calendar.getInstance();
 cal.set(1440, 10, 20);
 sdtDate.setFullDate(cal.getTime());

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.insertNode(sdtDate);

 doc.save(getArtifactsDir() + "StructuredDocumentTag.Date.docx");
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [DEFAULT](#DEFAULT) | يُستخدم كقيمة افتراضية في OOXML. |
| [GREGORIAN](#GREGORIAN) | يحدد أنه يجب استخدام التقويم الغريغوري، كما هو معرف في ISO 8601. |
| [GREGORIAN_ARABIC](#GREGORIAN-ARABIC) | يحدد أنه يجب استخدام التقويم الغريغوري، كما هو معرف في ISO 8601. |
| [GREGORIAN_ME_FRENCH](#GREGORIAN-ME-FRENCH) | يحدد أنه يجب استخدام التقويم الغريغوري، كما هو معرف في ISO 8601. |
| [GREGORIAN_US](#GREGORIAN-US) | يحدد أنه يجب استخدام التقويم الغريغوري، كما هو معرف في ISO 8601. |
| [GREGORIAN_XLIT_ENGLISH](#GREGORIAN-XLIT-ENGLISH) | يحدد أنه يجب استخدام التقويم الغريغوري، كما هو معرف في ISO 8601. |
| [GREGORIAN_XLIT_FRENCH](#GREGORIAN-XLIT-FRENCH) | يحدد أنه يجب استخدام التقويم الغريغوري، كما هو معرف في ISO 8601. |
| [HEBREW](#HEBREW) | يحدد أنه يجب استخدام التقويم العبري القمري، كما هو موضح بصيغة غاوس لعيد الفصح [CITATION] والبيان الكامل للقانون الشفهي (مشنه توراه). |
| [HIJRI](#HIJRI) | يحدد أنه يجب استخدام التقويم الهجري القمري، كما هو موضح من قبل المملكة العربية السعودية، وزارة الشؤون الإسلامية، الوقف، الدعوة والإرشاد. |
| [JAPAN](#JAPAN) | يحدد أنه يجب استخدام تقويم عصر الإمبراطور الياباني، كما هو موضح في المعيار الصناعي الياباني JIS X 0301. |
| [KOREA](#KOREA) | يحدد أنه يجب استخدام تقويم عصر تانغون الكوري، كما هو موضح في قانون كوريا رقم. |
| [NONE](#NONE) | يحدد أنه لا يجب استخدام أي تقويم. |
| [SAKA](#SAKA) | يحدد أنه يجب استخدام تقويم عصر سكا، كما هو موضح من قبل لجنة إصلاح التقويم في الهند، كجزء من التقويم الهندي والمرشد الملاحي. |
| [TAIWAN](#TAIWAN) | يحدد أنه يجب استخدام التقويم التايواني، كما هو معرف في المعيار الوطني الصيني CNS 7648. |
| [THAI](#THAI) | يحدد أنه يجب استخدام التقويم التايلاندي، كما هو معرف في المرسوم الملكي لجلالة الملك. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String sdtCalendarTypeName)](#fromName-java.lang.String) |  |
| [getName(int sdtCalendarType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sdtCalendarType)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


يُستخدم كقيمة افتراضية في OOXML. يساوي [GREGORIAN](../../com.aspose.words/sdtcalendartype/\#GREGORIAN).

### GREGORIAN {#GREGORIAN}
```
public static int GREGORIAN
```


يحدد أنه يجب استخدام التقويم الغريغوري، كما هو معرف في ISO 8601. يجب تعريب هذا التقويم إلى اللغة المناسبة.

### GREGORIAN_ARABIC {#GREGORIAN-ARABIC}
```
public static int GREGORIAN_ARABIC
```


يحدد أنه يجب استخدام التقويم الغريغوري، كما هو معرف في ISO 8601. يجب عرض قيم هذا التقويم باللغة العربية.

### GREGORIAN_ME_FRENCH {#GREGORIAN-ME-FRENCH}
```
public static int GREGORIAN_ME_FRENCH
```


يحدد أنه يجب استخدام التقويم الغريغوري، كما هو معرف في ISO 8600. يجب عرض قيم هذا التقويم بالفرنسية المستخدمة في الشرق الأوسط.

### GREGORIAN_US {#GREGORIAN-US}
```
public static int GREGORIAN_US
```


يحدد أنه يجب استخدام التقويم الغريغوري، كما هو معرف في ISO 8601. يجب عرض قيم هذا التقويم باللغة الإنجليزية.

### GREGORIAN_XLIT_ENGLISH {#GREGORIAN-XLIT-ENGLISH}
```
public static int GREGORIAN_XLIT_ENGLISH
```


يحدد أنه يجب استخدام التقويم الغريغوري، كما هو معرف في ISO 8601. يجب أن تكون قيم هذا التقويم تمثيل السلاسل الإنجليزية بأحرف عربية مكافئة (التحويل الصوتي العربي للإنجليزية للتقويم الغريغوري).

### GREGORIAN_XLIT_FRENCH {#GREGORIAN-XLIT-FRENCH}
```
public static int GREGORIAN_XLIT_FRENCH
```


يحدد أنه يجب استخدام التقويم الغريغوري، كما هو معرف في ISO 8601. يجب أن تكون قيم هذا التقويم تمثيل السلاسل الفرنسية بأحرف عربية مكافئة (التحويل الصوتي العربي للفرنسية للتقويم الغريغوري).

### HEBREW {#HEBREW}
```
public static int HEBREW
```


يحدد أنه يجب استخدام التقويم العبري القمري، كما هو موضح بصيغة غاوس لعيد الفصح [CITATION] والبيان الكامل للقانون الشفهي (مشنه توراه).

### HIJRI {#HIJRI}
```
public static int HIJRI
```


يحدد أنه يجب استخدام التقويم الهجري القمري، كما هو موضح من قبل المملكة العربية السعودية، وزارة الشؤون الإسلامية، الوقف، الدعوة والإرشاد.

### JAPAN {#JAPAN}
```
public static int JAPAN
```


يحدد أنه يجب استخدام تقويم عصر الإمبراطور الياباني، كما هو موضح في المعيار الصناعي الياباني JIS X 0301.

### KOREA {#KOREA}
```
public static int KOREA
```


يحدد أنه يجب استخدام تقويم عصر تانغون الكوري، كما هو موضح في قانون كوريا رقم 4.

### NONE {#NONE}
```
public static int NONE
```


يحدد أنه لا يجب استخدام أي تقويم.

 **Remarks:** 

عادةً في AW، تكون القيمة None هي الأولى والقيمة الافتراضية للتعدادات، لكن ليس في هذه الحالة. القيمة None ليست افتراضية في OOXML، بل [GREGORIAN](../../com.aspose.words/sdtcalendartype/\#GREGORIAN) هي الافتراضية وتُعد أول عنصر في هذا التعداد.

### SAKA {#SAKA}
```
public static int SAKA
```


يحدد أنه يجب استخدام تقويم عصر سكا، كما هو موضح من قبل لجنة إصلاح التقويم في الهند، كجزء من التقويم الهندي والمرشد الملاحي.

### TAIWAN {#TAIWAN}
```
public static int TAIWAN
```


يحدد أنه يجب استخدام التقويم التايواني، كما هو معرف في المعيار الوطني الصيني CNS 7648.

### THAI {#THAI}
```
public static int THAI
```


يحدد أنه يجب استخدام التقويم التايلاندي، كما هو معرف في المرسوم الملكي لجلالة الملك فاجيرافود (راما السادس) في الجريدة الملكية ب. هـ 2456 (1913 م) وبحسب مرسوم رئيس الوزراء فيبونسونغكرام (1941 م) لبدء السنة في 1 يناير الغريغوري وربط السنة الصفرية بالسنة الغريغورية 543 قبل الميلاد.

### length {#length}
```
public static int length
```


### fromName(String sdtCalendarTypeName) {#fromName-java.lang.String}
```
public static int fromName(String sdtCalendarTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| sdtCalendarTypeName | java.lang.String |  |

**Returns:**
int
### getName(int sdtCalendarType) {#getName-int}
```
public static String getName(int sdtCalendarType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| sdtCalendarType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int sdtCalendarType) {#toString-int}
```
public static String toString(int sdtCalendarType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| sdtCalendarType | int |  |

**Returns:**
java.lang.String
