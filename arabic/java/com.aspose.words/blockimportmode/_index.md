---
title: "BlockImportMode"
linktitle: "BlockImportMode"
second_title: "Aspose.Words لـ Java"
description: "يحدد كيف يتم استيراد خصائص العناصر ذات المستوى الكتلي من المستندات المستندة إلى HTML في Java."
type: docs
weight: 39
url: /ar/java/com.aspose.words/blockimportmode/
---

**Inheritance:**
java.lang.Object
```
public class BlockImportMode
```

يحدد كيفية استيراد خصائص العناصر على مستوى الكتلة من المستندات القائمة على HTML.

 **Examples:** 

يعرض كيف يتم استيراد خصائص العناصر ذات المستوى الكتلي من المستندات المستندة إلى HTML.

```

 final String html = "\n\n \n \n paragraph 1\n paragraph 2\n\n\n";

 HtmlLoadOptions loadOptions = new HtmlLoadOptions();
 // Set the new mode of import HTML block-level elements.
 loadOptions.setBlockImportMode(blockImportMode);

 Document doc = new Document(new ByteArrayInputStream(html.getBytes(StandardCharsets.UTF_8)), loadOptions);
 doc.save(getArtifactsDir() + "HtmlLoadOptions.BlockImport.docx");
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [MERGE](#MERGE) | يتم دمج خصائص الكتل الأصلية وتخزينها على العناصر الفرعية (مثلاً |
| [PRESERVE](#PRESERVE) | يتم استيراد خصائص الكتل الأصلية إلى بنية منطقية خاصة وتُخزن بشكل منفصل عن عقد المستند. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String blockImportModeName)](#fromName-java.lang.String) |  |
| [getName(int blockImportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int blockImportMode)](#toString-int) |  |
### MERGE {#MERGE}
```
public static int MERGE
```


يتم دمج خصائص الكتل الأصلية وتخزينها على العناصر الفرعية (مثلاً الفقرات أو الجداول).

 **Remarks:** 

يتم دمج خصائص الكتل الأصلية كما يلي: تُضاف الهوامش معًا؛ تُهمل حدود الكتل ذات المستوى الأعلى وتُحافظ فقط على حدود المستوى الداخلي الأكثر. نتيجةً لذلك، عندما يُحدد هذا الوضع، سيُفقد بعض تنسيق الكتل من المستند الأصلي.

من ناحية أخرى، بما أن جميع خصائص الكتل المدمجة تُخزن على عقد المستند، فإن جميع التنسيقات في المستند الناتج ستكون متاحة للتعديل.

### PRESERVE {#PRESERVE}
```
public static int PRESERVE
```


يتم استيراد خصائص الكتل الأصلية إلى بنية منطقية خاصة وتُخزن بشكل منفصل عن عقد المستند.

 **Remarks:** 

يتم استيراد الهوامش والحدود فقط لعناصر HTML 'body' و 'div' و 'blockquote'. تُخزن خصائص كل عنصر HTML بشكل فردي.

يسمح هذا الوضع بالحفاظ بشكل أفضل على الحدود والهوامش الموجودة في مستند HTML والحصول على نتائج تحويل أفضل. الجانب السلبي هو أن المستند الناتج يصبح أصعب في التعديل، لأن الحدود والهوامش المخزنة في البنية المنطقية غير متاحة للتحرير.

هذا الوضع يحاكي سلوك MS Word فيما يتعلق باستيراد خصائص الكتل.

### length {#length}
```
public static int length
```


### fromName(String blockImportModeName) {#fromName-java.lang.String}
```
public static int fromName(String blockImportModeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| blockImportModeName | java.lang.String |  |

**Returns:**
int
### getName(int blockImportMode) {#getName-int}
```
public static String getName(int blockImportMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| blockImportMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int blockImportMode) {#toString-int}
```
public static String toString(int blockImportMode)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| blockImportMode | int |  |

**Returns:**
java.lang.String
