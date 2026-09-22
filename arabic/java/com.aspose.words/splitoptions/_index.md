---
title: "SplitOptions"
linktitle: "SplitOptions"
second_title: "Aspose.Words لـ Java"
description: "يحدد الخيارات لكيفية تقسيم المستند إلى أجزاء في Java."
type: docs
weight: 630
url: /ar/java/com.aspose.words/splitoptions/
---

**Inheritance:**
java.lang.Object
```
public class SplitOptions
```

يحدد خيارات كيفية تقسيم المستند إلى أجزاء.
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getSplitCriteria()](#getSplitCriteria) | يحدد معايير تقسيم المستند إلى أجزاء. |
| [getSplitStyle()](#getSplitStyle) | يحدد نمط الفقرة لتقسيم المستند إلى أجزاء عندما يتم استخدام [SplitCriteria.STYLE](../../com.aspose.words/splitcriteria/\#STYLE). |
| [setSplitCriteria(int value)](#setSplitCriteria-int) | يحدد معايير تقسيم المستند إلى أجزاء. |
| [setSplitStyle(String value)](#setSplitStyle-java.lang.String) | يحدد نمط الفقرة لتقسيم المستند إلى أجزاء عندما يتم استخدام [SplitCriteria.STYLE](../../com.aspose.words/splitcriteria/\#STYLE). |
### getSplitCriteria() {#getSplitCriteria}
```
public int getSplitCriteria()
```


يحدد معايير تقسيم المستند إلى أجزاء.

 **Examples:** 

يوضح كيفية تقسيم المستند حسب الصفحات.

```

 String doc = getMyDir() + "Big document.docx";

 SplitOptions options = new SplitOptions();
 options.setSplitCriteria(SplitCriteria.PAGE);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.1.docx", options);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.2.docx", SaveFormat.DOCX, options);
 
```

**Returns:**
int - القيمة int المقابلة. القيمة المرجعة هي واحدة من ثوابت [SplitCriteria](../../com.aspose.words/splitcriteria/).
### getSplitStyle() {#getSplitStyle}
```
public String getSplitStyle()
```


يحدد نمط الفقرة لتقسيم المستند إلى أجزاء عندما يتم استخدام [SplitCriteria.STYLE](../../com.aspose.words/splitcriteria/\#STYLE).

**Returns:**
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### setSplitCriteria(int value) {#setSplitCriteria-int}
```
public void setSplitCriteria(int value)
```


يحدد معايير تقسيم المستند إلى أجزاء.

 **Examples:** 

يوضح كيفية تقسيم المستند حسب الصفحات.

```

 String doc = getMyDir() + "Big document.docx";

 SplitOptions options = new SplitOptions();
 options.setSplitCriteria(SplitCriteria.PAGE);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.1.docx", options);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.2.docx", SaveFormat.DOCX, options);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | القيمة int المقابلة. يجب أن تكون القيمة واحدة من ثوابت [SplitCriteria](../../com.aspose.words/splitcriteria/). |

### setSplitStyle(String value) {#setSplitStyle-java.lang.String}
```
public void setSplitStyle(String value)
```


يحدد نمط الفقرة لتقسيم المستند إلى أجزاء عندما يتم استخدام [SplitCriteria.STYLE](../../com.aspose.words/splitcriteria/\#STYLE).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | القيمة المقابلة من نوع java.lang.String. |

