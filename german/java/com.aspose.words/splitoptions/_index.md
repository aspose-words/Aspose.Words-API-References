---
title: "SplitOptions"
linktitle: "SplitOptions"
second_title: "Aspose.Words für Java"
description: "Gibt Optionen an, wie das Dokument in Java in Teile aufgeteilt wird."
type: docs
weight: 630
url: /de/java/com.aspose.words/splitoptions/
---

**Inheritance:**
java.lang.Object
```
public class SplitOptions
```

Gibt Optionen an, wie das Dokument in Teile aufgeteilt wird.
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getSplitCriteria()](#getSplitCriteria) | Gibt die Kriterien für das Aufteilen des Dokuments in Teile an. |
| [getSplitStyle()](#getSplitStyle) | Gibt den Absatzstil für das Aufteilen des Dokuments in Teile an, wenn [SplitCriteria.STYLE](../../com.aspose.words/splitcriteria/\#STYLE) verwendet wird. |
| [setSplitCriteria(int value)](#setSplitCriteria-int) | Gibt die Kriterien für das Aufteilen des Dokuments in Teile an. |
| [setSplitStyle(String value)](#setSplitStyle-java.lang.String) | Gibt den Absatzstil für das Aufteilen des Dokuments in Teile an, wenn [SplitCriteria.STYLE](../../com.aspose.words/splitcriteria/\#STYLE) verwendet wird. |
### getSplitCriteria() {#getSplitCriteria}
```
public int getSplitCriteria()
```


Gibt die Kriterien für das Aufteilen des Dokuments in Teile an.

 **Examples:** 

Zeigt, wie das Dokument nach Seiten aufgeteilt wird.

```

 String doc = getMyDir() + "Big document.docx";

 SplitOptions options = new SplitOptions();
 options.setSplitCriteria(SplitCriteria.PAGE);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.1.docx", options);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.2.docx", SaveFormat.DOCX, options);
 
```

**Returns:**
int - Der entsprechende int‑Wert. Der zurückgegebene Wert ist einer der [SplitCriteria](../../com.aspose.words/splitcriteria/) Konstanten.
### getSplitStyle() {#getSplitStyle}
```
public String getSplitStyle()
```


Gibt den Absatzstil für das Aufteilen des Dokuments in Teile an, wenn [SplitCriteria.STYLE](../../com.aspose.words/splitcriteria/\#STYLE) verwendet wird.

**Returns:**
java.lang.String - Der entsprechende java.lang.String-Wert.
### setSplitCriteria(int value) {#setSplitCriteria-int}
```
public void setSplitCriteria(int value)
```


Gibt die Kriterien für das Aufteilen des Dokuments in Teile an.

 **Examples:** 

Zeigt, wie das Dokument nach Seiten aufgeteilt wird.

```

 String doc = getMyDir() + "Big document.docx";

 SplitOptions options = new SplitOptions();
 options.setSplitCriteria(SplitCriteria.PAGE);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.1.docx", options);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.2.docx", SaveFormat.DOCX, options);
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Der entsprechende int‑Wert. Der Wert muss einer der [SplitCriteria](../../com.aspose.words/splitcriteria/) Konstanten sein. |

### setSplitStyle(String value) {#setSplitStyle-java.lang.String}
```
public void setSplitStyle(String value)
```


Gibt den Absatzstil für das Aufteilen des Dokuments in Teile an, wenn [SplitCriteria.STYLE](../../com.aspose.words/splitcriteria/\#STYLE) verwendet wird.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der entsprechende java.lang.String-Wert. |

