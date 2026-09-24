---
title: "HeightRule"
linktitle: "HeightRule"
second_title: "Aspose.Words Java için"
description: "Java'da bir nesnenin yüksekliğini belirleme kuralını belirtir."
type: docs
weight: 373
url: /tr/java/com.aspose.words/heightrule/
---

**Inheritance:**
java.lang.Object
```
public class HeightRule
```

Bir nesnenin yüksekliğini belirleme kuralını belirtir.

 **Examples:** 

DocumentBuilder ile satırların nasıl biçimlendirileceğini gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [AT_LEAST](#AT-LEAST) | Yükseklik, nokta cinsinden belirtilen yüksekliğin en azı kadar olacaktır. |
| [AUTO](#AUTO) | Yükseklik, bir nesnenin içindeki tüm metni barındıracak şekilde otomatik olarak artacaktır. |
| [EXACTLY](#EXACTLY) | Yükseklik, nokta cinsinden tam olarak belirtilir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String heightRuleName)](#fromName-java.lang.String) |  |
| [getName(int heightRule)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int heightRule)](#toString-int) |  |
### AT_LEAST {#AT-LEAST}
```
public static int AT_LEAST
```


Yükseklik, nokta cinsinden belirtilen yüksekliğin en azı kadar olacaktır. Gerekirse, bir nesnenin içindeki tüm metni barındıracak şekilde artacaktır.

### AUTO {#AUTO}
```
public static int AUTO
```


Yükseklik, bir nesnenin içindeki tüm metni barındıracak şekilde otomatik olarak artacaktır.

### EXACTLY {#EXACTLY}
```
public static int EXACTLY
```


Yükseklik, nokta cinsinden tam olarak belirtilir. Lütfen, metin bu yüksekliğe sahip nesneye sığmazsa kesileceğini unutmayın.

### length {#length}
```
public static int length
```


### fromName(String heightRuleName) {#fromName-java.lang.String}
```
public static int fromName(String heightRuleName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| heightRuleName | java.lang.String |  |

**Returns:**
int
### getName(int heightRule) {#getName-int}
```
public static String getName(int heightRule)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| heightRule | int |  |

**Returns:**
java.lang.String
