---
title: "NumSpacing"
linktitle: "NumSpacing"
second_title: "Aspose.Words Java için"
description: "Java'da sayı aralığının gösterilebileceği olası değerleri belirtir."
type: docs
weight: 484
url: /tr/java/com.aspose.words/numspacing/
---

**Inheritance:**
java.lang.Object
```
public class NumSpacing
```

Sayısal aralığın görüntülenebileceği olası değerleri belirtir.

 **Examples:** 

Sayının aralık tipinin nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // This effect is only supported in newer versions of MS Word.
 doc.getCompatibilityOptions().optimizeFor(MsWordVersion.WORD_2019);

 builder.write("1 ");
 builder.write("This is an example");

 Run run = doc.getFirstSection().getBody().getFirstParagraph().getRuns().get(0);
 if (run.getFont().getNumberSpacing() == NumSpacing.DEFAULT)
     run.getFont().setNumberSpacing(NumSpacing.PROPORTIONAL);

 doc.save(getArtifactsDir() + "Fonts.NumberSpacing.docx");
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [DEFAULT](#DEFAULT) | Sayıların, fontun varsayılan biçiminde gösterileceğini belirtir. |
| [PROPORTIONAL](#PROPORTIONAL) | Font tarafından destekleniyorsa, sayılarının orantılı aralıklı olarak tasarlanmış biçimlerinin gösterileceğini belirtir. |
| [TABULAR](#TABULAR) | Font tarafından destekleniyorsa, sayılarının tablo şeklinde tasarlanmış biçimlerinin gösterileceğini belirtir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String numSpacingName)](#fromName-java.lang.String) |  |
| [getName(int numSpacing)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int numSpacing)](#toString-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Sayıların, fontun varsayılan biçiminde gösterileceğini belirtir.

### PROPORTIONAL {#PROPORTIONAL}
```
public static int PROPORTIONAL
```


Font tarafından destekleniyorsa, sayılarının orantılı aralıklı olarak tasarlanmış biçimlerinin gösterileceğini belirtir.

### TABULAR {#TABULAR}
```
public static int TABULAR
```


Font tarafından destekleniyorsa, sayılarının tablo şeklinde tasarlanmış biçimlerinin gösterileceğini belirtir.

### length {#length}
```
public static int length
```


### fromName(String numSpacingName) {#fromName-java.lang.String}
```
public static int fromName(String numSpacingName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| numSpacingName | java.lang.String |  |

**Returns:**
int
### getName(int numSpacing) {#getName-int}
```
public static String getName(int numSpacing)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| numSpacing | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int numSpacing) {#toString-int}
```
public static String toString(int numSpacing)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| numSpacing | int |  |

**Returns:**
java.lang.String
