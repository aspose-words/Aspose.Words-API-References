---
title: "PreferredWidthType"
linktitle: "PreferredWidthType"
second_title: "Aspose.Words لـ Java"
description: "يحدد وحدة القياس للعرض المفضل لجدول أو خلية في Java."
type: docs
weight: 551
url: /ar/java/com.aspose.words/preferredwidthtype/
---

**Inheritance:**
java.lang.Object
```
public class PreferredWidthType
```

يحدد وحدة القياس للعرض المفضل لجدول أو خلية.

 **Examples:** 

يعرض كيفية التحقق من نوع العرض المفضل وقيمته لخلية جدول.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 Table table = doc.getFirstSection().getBody().getTables().get(0);
 Cell firstCell = table.getFirstRow().getFirstCell();

 Assert.assertEquals(PreferredWidthType.PERCENT, firstCell.getCellFormat().getPreferredWidth().getType());
 Assert.assertEquals(11.16d, firstCell.getCellFormat().getPreferredWidth().getValue());
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [AUTO](#AUTO) | العرض المفضل غير محدد. |
| [PERCENT](#PERCENT) | قِس عرض العنصر الحالي باستخدام نسبة مئوية محددة. |
| [POINTS](#POINTS) | قِس عرض العنصر الحالي باستخدام عدد محدد من النقاط (1/72 بوصة). |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String preferredWidthTypeName)](#fromName-java.lang.String) |  |
| [getName(int preferredWidthType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int preferredWidthType)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


العرض المفضل غير محدد. العرض الفعلي للجدول أو الخلية إما يتم تحديده باستخدام العرض الصريح أو سيُحدد تلقائيًا بواسطة خوارزمية تخطيط الجدول عند عرض الجدول، اعتمادًا على إعداد التلاؤم التلقائي للجدول.

### PERCENT {#PERCENT}
```
public static int PERCENT
```


قِس عرض العنصر الحالي باستخدام نسبة مئوية محددة.

### POINTS {#POINTS}
```
public static int POINTS
```


قِس عرض العنصر الحالي باستخدام عدد محدد من النقاط (1/72 بوصة).

### length {#length}
```
public static int length
```


### fromName(String preferredWidthTypeName) {#fromName-java.lang.String}
```
public static int fromName(String preferredWidthTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| preferredWidthTypeName | java.lang.String |  |

**Returns:**
int
### getName(int preferredWidthType) {#getName-int}
```
public static String getName(int preferredWidthType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| preferredWidthType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int preferredWidthType) {#toString-int}
```
public static String toString(int preferredWidthType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| preferredWidthType | int |  |

**Returns:**
java.lang.String
