---
title: "HtmlInsertOptions"
linktitle: "HtmlInsertOptions"
second_title: "Aspose.Words لـ Java"
description: "يحدد الخيارات للطريقة MAspose.Words.DocumentBuilder.InsertHtmlSystem.StringAspose.Words.HtmlInsertOptions في Java."
type: docs
weight: 381
url: /ar/java/com.aspose.words/htmlinsertoptions/
---

**Inheritance:**
java.lang.Object
```
public class HtmlInsertOptions
```

يحدد الخيارات للطريقة **M:Aspose.Words.DocumentBuilder.InsertHtml(System.String,Aspose.Words.HtmlInsertOptions)**.

 **Examples:** 

يعرض كيفية تحسين الحفاظ على الحدود والهوامش المرئية.

```

 final String HTML = "\n                \n                    \n                    \n                        paragraph 1\n                        paragraph 2\n                    \n                    \n                ";

 // Set the new mode of import HTML block-level elements.
 int insertOptions = HtmlInsertOptions.PRESERVE_BLOCKS;

 DocumentBuilder builder = new DocumentBuilder();
 builder.insertHtml(HTML, insertOptions);
 builder.getDocument().save(getArtifactsDir() + "DocumentBuilder.PreserveBlocks.docx");
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [NONE](#NONE) | استخدم الخيارات الافتراضية عند إدراج HTML. |
| [PRESERVE_BLOCKS](#PRESERVE-BLOCKS) | حافظ على خصائص العناصر على مستوى الكتلة. |
| [REMOVE_LAST_EMPTY_PARAGRAPH](#REMOVE-LAST-EMPTY-PARAGRAPH) | أزل الفقرة الفارغة التي تُدرج عادةً بعد HTML الذي ينتهي بعنصر على مستوى الكتلة. |
| [USE_BUILDER_FORMATTING](#USE-BUILDER-FORMATTING) | استخدم تنسيق الخط والفقرة المحدد في [DocumentBuilder](../../com.aspose.words/documentbuilder/) كتنسيق أساسي للنص المُدرج من HTML. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String htmlInsertOptionsName)](#fromName-java.lang.String) |  |
| [fromNames(Set htmlInsertOptionsNames)](#fromNames-java.util.Set) |  |
| [getName(int htmlInsertOptions)](#getName-int) |  |
| [getNames(int htmlInsertOptions)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int htmlInsertOptions)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### NONE {#NONE}
```
public static int NONE
```


استخدم الخيارات الافتراضية عند إدراج HTML.

### PRESERVE_BLOCKS {#PRESERVE-BLOCKS}
```
public static int PRESERVE_BLOCKS
```


حافظ على خصائص العناصر على مستوى الكتلة.

 **Remarks:** 

بشكل افتراضي، يتم دمج خصائص الكتل الأم وتخزينها على العناصر الفرعية لها (مثل الفقرات أو الجداول). إذا تم تحديد هذا الخيار، تُخزن خصائص كل كتلة بشكل منفصل في بنية منطقية خاصة. ونتيجة لذلك، يتيح هذا الخيار الحفاظ بشكل أفضل على الحدود والهوامش الفردية الموجودة في مستند HTML والحصول على نتائج تحويل أفضل. الجانب السلبي هو أن المستند الناتج يصبح أصعب في التعديل، لأن الحدود والهوامش المخزنة في البنية المنطقية غير متاحة للتحرير.

يتم الحفاظ فقط على الهوامش والحدود لعناصر HTML 'body' و 'div' و 'blockquote'. تُخزن خصائص كل عنصر HTML بشكل منفصل.

إذا تم تحديد هذا الخيار، فإن Aspose.Words يحاكي سلوك MS Word فيما يتعلق باستيراد خصائص الكتل.

### REMOVE_LAST_EMPTY_PARAGRAPH {#REMOVE-LAST-EMPTY-PARAGRAPH}
```
public static int REMOVE_LAST_EMPTY_PARAGRAPH
```


أزل الفقرة الفارغة التي تُدرج عادةً بعد HTML الذي ينتهي بعنصر على مستوى الكتلة.

 **Remarks:** 

بشكل افتراضي، يضمن [DocumentBuilder](../../com.aspose.words/documentbuilder/) إغلاق العنصر الأخير على مستوى الكتلة المستورد من HTML بعد الاستيراد وإدراج فاصل فقرة بعد العنصر. يفصل فاصل الفقرة هذا بين المحتوى المستورد من HTML ومحتوى مستند القالب. ومع ذلك، إذا تم إدراج قطعة HTML في فقرة فارغة، فإن فاصل الفقرة سيخلق فقرة فارغة إضافية. إذا كان هذا السلوك غير مرغوب فيه، حدد هذا الخيار.

### USE_BUILDER_FORMATTING {#USE-BUILDER-FORMATTING}
```
public static int USE_BUILDER_FORMATTING
```


استخدم تنسيق الخط والفقرة المحدد في [DocumentBuilder](../../com.aspose.words/documentbuilder/) كتنسيق أساسي للنص المُدرج من HTML.

 **Remarks:** 

إذا لم يتم تحديد هذا الخيار، يتم تجاهل تنسيق [DocumentBuilder](../../com.aspose.words/documentbuilder/) ويتم إدراج النص بتنسيق HTML الافتراضي. ونتيجة لذلك، يظهر النص كما يُعرض في المتصفحات.

إذا تم تحديد هذا الخيار، يعتمد تنسيق النص المُدرج على التنسيق المحدد في [DocumentBuilder](../../com.aspose.words/documentbuilder/)، ويظهر النص كما لو أنه تم إدراجه باستخدام [DocumentBuilder.write(java.lang.String)](../../com.aspose.words/documentbuilder/\#write-java.lang.String).

### length {#length}
```
public static int length
```


### fromName(String htmlInsertOptionsName) {#fromName-java.lang.String}
```
public static int fromName(String htmlInsertOptionsName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| htmlInsertOptionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set htmlInsertOptionsNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set htmlInsertOptionsNames)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| htmlInsertOptionsNames | java.util.Set |  |

**Returns:**
int
### getName(int htmlInsertOptions) {#getName-int}
```
public static String getName(int htmlInsertOptions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| htmlInsertOptions | int |  |

**Returns:**
java.lang.String
### getNames(int htmlInsertOptions) {#getNames-int}
```
public static Set getNames(int htmlInsertOptions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| htmlInsertOptions | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int htmlInsertOptions) {#toString-int}
```
public static String toString(int htmlInsertOptions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| htmlInsertOptions | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
