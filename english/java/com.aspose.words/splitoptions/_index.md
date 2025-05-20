---
title: SplitOptions
linktitle: SplitOptions
second_title: Aspose.Words for Java
description: Specifies options how the document is split into parts in Java.
type: docs
weight: 621
url: /java/com.aspose.words/splitoptions/
---

**Inheritance:**
java.lang.Object
```
public class SplitOptions
```

Specifies options how the document is split into parts.
## Methods

| Method | Description |
| --- | --- |
| [getSplitCriteria()](#getSplitCriteria) | Specifies the criteria for splitting the document into parts. |
| [getSplitStyle()](#getSplitStyle) | Specifies the paragraph style for splitting the document into parts when [SplitCriteria.STYLE](../../com.aspose.words/splitcriteria/\#STYLE) is used. |
| [setSplitCriteria(int value)](#setSplitCriteria-int) | Specifies the criteria for splitting the document into parts. |
| [setSplitStyle(String value)](#setSplitStyle-java.lang.String) | Specifies the paragraph style for splitting the document into parts when [SplitCriteria.STYLE](../../com.aspose.words/splitcriteria/\#STYLE) is used. |
### getSplitCriteria() {#getSplitCriteria}
```
public int getSplitCriteria()
```


Specifies the criteria for splitting the document into parts.

 **Examples:** 

Shows how to split document by pages.

```

 String doc = getMyDir() + "Big document.docx";

 SplitOptions options = new SplitOptions();
 options.setSplitCriteria(SplitCriteria.PAGE);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.1.docx", options);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.2.docx", SaveFormat.DOCX, options);
 
```

**Returns:**
int - The corresponding  int  value. The returned value is one of [SplitCriteria](../../com.aspose.words/splitcriteria/) constants.
### getSplitStyle() {#getSplitStyle}
```
public String getSplitStyle()
```


Specifies the paragraph style for splitting the document into parts when [SplitCriteria.STYLE](../../com.aspose.words/splitcriteria/\#STYLE) is used.

**Returns:**
java.lang.String - The corresponding java.lang.String value.
### setSplitCriteria(int value) {#setSplitCriteria-int}
```
public void setSplitCriteria(int value)
```


Specifies the criteria for splitting the document into parts.

 **Examples:** 

Shows how to split document by pages.

```

 String doc = getMyDir() + "Big document.docx";

 SplitOptions options = new SplitOptions();
 options.setSplitCriteria(SplitCriteria.PAGE);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.1.docx", options);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.2.docx", SaveFormat.DOCX, options);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [SplitCriteria](../../com.aspose.words/splitcriteria/) constants. |

### setSplitStyle(String value) {#setSplitStyle-java.lang.String}
```
public void setSplitStyle(String value)
```


Specifies the paragraph style for splitting the document into parts when [SplitCriteria.STYLE](../../com.aspose.words/splitcriteria/\#STYLE) is used.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The corresponding java.lang.String value. |

