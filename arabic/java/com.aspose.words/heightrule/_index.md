---
title: "HeightRule"
linktitle: "HeightRule"
second_title: "Aspose.Words لـ Java"
description: "يحدد القاعدة لتحديد ارتفاع كائن في Java."
type: docs
weight: 373
url: /ar/java/com.aspose.words/heightrule/
---

**Inheritance:**
java.lang.Object
```
public class HeightRule
```

يحدد القاعدة لتحديد ارتفاع الكائن.

 **Examples:** 

يوضح كيفية تنسيق الصفوف باستخدام DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Start a second row, and then configure its height. The builder will apply these settings to
 // its current row, as well as any new rows it creates afterwards.
 builder.endRow();

 RowFormat rowFormat = builder.getRowFormat();
 rowFormat.setHeight(100.0);
 rowFormat.setHeightRule(HeightRule.EXACTLY);

 builder.insertCell();
 builder.write("Row 2, cell 1.");
 builder.endTable();

 // The first row was unaffected by the padding reconfiguration and still holds the default values.
 Assert.assertEquals(0.0d, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());

 Assert.assertEquals(100.0d, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());

 doc.save(getArtifactsDir() + "DocumentBuilder.SetRowFormatting.docx");
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [AT_LEAST](#AT-LEAST) | سيكون الارتفاع على الأقل بالارتفاع المحدد بالنقاط. |
| [AUTO](#AUTO) | سيزداد الارتفاع تلقائيًا لاستيعاب كل النص داخل الكائن. |
| [EXACTLY](#EXACTLY) | يتم تحديد الارتفاع بدقة بالنقاط. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String heightRuleName)](#fromName-java.lang.String) |  |
| [getName(int heightRule)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int heightRule)](#toString-int) |  |
### AT_LEAST {#AT-LEAST}
```
public static int AT_LEAST
```


سيكون الارتفاع على الأقل بالارتفاع المحدد بالنقاط. سيتزايد إذا لزم الأمر لاستيعاب كل النص داخل الكائن.

### AUTO {#AUTO}
```
public static int AUTO
```


سيزداد الارتفاع تلقائيًا لاستيعاب كل النص داخل الكائن.

### EXACTLY {#EXACTLY}
```
public static int EXACTLY
```


يتم تحديد الارتفاع بدقة بالنقاط. يرجى ملاحظة أنه إذا لم يتسع النص داخل الكائن بهذا الارتفاع، فسيظهر مقطوعًا.

### length {#length}
```
public static int length
```


### fromName(String heightRuleName) {#fromName-java.lang.String}
```
public static int fromName(String heightRuleName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| heightRuleName | java.lang.String |  |

**Returns:**
int
### getName(int heightRule) {#getName-int}
```
public static String getName(int heightRule)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| heightRule | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int heightRule) {#toString-int}
```
public static String toString(int heightRule)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| heightRule | int |  |

**Returns:**
java.lang.String
