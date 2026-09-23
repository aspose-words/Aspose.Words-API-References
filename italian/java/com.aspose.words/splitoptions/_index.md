---
title: "SplitOptions"
linktitle: "SplitOptions"
second_title: "Aspose.Words per Java"
description: "Specifica le opzioni su come il documento viene suddiviso in parti in Java."
type: docs
weight: 630
url: /it/java/com.aspose.words/splitoptions/
---

**Inheritance:**
java.lang.Object
```
public class SplitOptions
```

Specifica le opzioni su come il documento viene suddiviso in parti.
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getSplitCriteria()](#getSplitCriteria) | Specifica i criteri per suddividere il documento in parti. |
| [getSplitStyle()](#getSplitStyle) | Specifica lo stile del paragrafo per suddividere il documento in parti quando viene utilizzato [SplitCriteria.STYLE](../../com.aspose.words/splitcriteria/#STYLE). |
| [setSplitCriteria(int value)](#setSplitCriteria-int) | Specifica i criteri per suddividere il documento in parti. |
| [setSplitStyle(String value)](#setSplitStyle-java.lang.String) | Specifica lo stile del paragrafo per suddividere il documento in parti quando viene utilizzato [SplitCriteria.STYLE](../../com.aspose.words/splitcriteria/#STYLE). |
### getSplitCriteria() {#getSplitCriteria}
```
public int getSplitCriteria()
```


Specifica i criteri per suddividere il documento in parti.

 **Examples:** 

Mostra come suddividere il documento per pagine.

```

 String doc = getMyDir() + "Big document.docx";

 SplitOptions options = new SplitOptions();
 options.setSplitCriteria(SplitCriteria.PAGE);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.1.docx", options);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.2.docx", SaveFormat.DOCX, options);
 
```

**Returns:**
int - Il valore intero corrispondente. Il valore restituito è una delle costanti [SplitCriteria](../../com.aspose.words/splitcriteria/).
### getSplitStyle() {#getSplitStyle}
```
public String getSplitStyle()
```


Specifica lo stile del paragrafo per suddividere il documento in parti quando viene utilizzato [SplitCriteria.STYLE](../../com.aspose.words/splitcriteria/#STYLE).

**Returns:**
java.lang.String - Il valore java.lang.String corrispondente.
### setSplitCriteria(int value) {#setSplitCriteria-int}
```
public void setSplitCriteria(int value)
```


Specifica i criteri per suddividere il documento in parti.

 **Examples:** 

Mostra come suddividere il documento per pagine.

```

 String doc = getMyDir() + "Big document.docx";

 SplitOptions options = new SplitOptions();
 options.setSplitCriteria(SplitCriteria.PAGE);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.1.docx", options);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.2.docx", SaveFormat.DOCX, options);
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| value | int | Il valore intero corrispondente. Il valore deve essere una delle costanti [SplitCriteria](../../com.aspose.words/splitcriteria/). |

### setSplitStyle(String value) {#setSplitStyle-java.lang.String}
```
public void setSplitStyle(String value)
```


Specifica lo stile del paragrafo per suddividere il documento in parti quando viene utilizzato [SplitCriteria.STYLE](../../com.aspose.words/splitcriteria/#STYLE).

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | java.lang.String | Il valore java.lang.String corrispondente. |

