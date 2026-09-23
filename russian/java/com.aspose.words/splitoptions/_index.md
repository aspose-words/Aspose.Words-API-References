---
title: "SplitOptions"
linktitle: "SplitOptions"
second_title: "Aspose.Words для Java"
description: "Указывает параметры, как документ разбивается на части в Java."
type: docs
weight: 630
url: /ru/java/com.aspose.words/splitoptions/
---

**Inheritance:**
java.lang.Object
```
public class SplitOptions
```

Указывает параметры, как документ разбивается на части.
## Методы

| Метод | Описание |
| --- | --- |
| [getSplitCriteria()](#getSplitCriteria) | Указывает критерии разбивки документа на части. |
| [getSplitStyle()](#getSplitStyle) | Указывает стиль абзаца для разбивки документа на части, когда используется [SplitCriteria.STYLE](../../com.aspose.words/splitcriteria/\#STYLE). |
| [setSplitCriteria(int value)](#setSplitCriteria-int) | Указывает критерии разбивки документа на части. |
| [setSplitStyle(String value)](#setSplitStyle-java.lang.String) | Указывает стиль абзаца для разбивки документа на части, когда используется [SplitCriteria.STYLE](../../com.aspose.words/splitcriteria/\#STYLE). |
### getSplitCriteria() {#getSplitCriteria}
```
public int getSplitCriteria()
```


Указывает критерии разбивки документа на части.

 **Examples:** 

Показывает, как разбить документ по страницам.

```

 String doc = getMyDir() + "Big document.docx";

 SplitOptions options = new SplitOptions();
 options.setSplitCriteria(SplitCriteria.PAGE);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.1.docx", options);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.2.docx", SaveFormat.DOCX, options);
 
```

**Returns:**
int - Соответствующее  int  значение. Возвращаемое значение является одной из констант [SplitCriteria](../../com.aspose.words/splitcriteria/).
### getSplitStyle() {#getSplitStyle}
```
public String getSplitStyle()
```


Указывает стиль абзаца для разбивки документа на части, когда используется [SplitCriteria.STYLE](../../com.aspose.words/splitcriteria/\#STYLE).

**Returns:**
java.lang.String - Соответствующее значение java.lang.String.
### setSplitCriteria(int value) {#setSplitCriteria-int}
```
public void setSplitCriteria(int value)
```


Указывает критерии разбивки документа на части.

 **Examples:** 

Показывает, как разбить документ по страницам.

```

 String doc = getMyDir() + "Big document.docx";

 SplitOptions options = new SplitOptions();
 options.setSplitCriteria(SplitCriteria.PAGE);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.1.docx", options);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.2.docx", SaveFormat.DOCX, options);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее  int  значение. Значение должно быть одной из констант [SplitCriteria](../../com.aspose.words/splitcriteria/). |

### setSplitStyle(String value) {#setSplitStyle-java.lang.String}
```
public void setSplitStyle(String value)
```


Указывает стиль абзаца для разбивки документа на части, когда используется [SplitCriteria.STYLE](../../com.aspose.words/splitcriteria/\#STYLE).

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| значение | java.lang.String | Соответствующее значение java.lang.String. |

