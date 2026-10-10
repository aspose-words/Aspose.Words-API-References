---
title: "SplitOptions"
linktitle: "SplitOptions"
second_title: "Aspose.Words pour Java"
description: "Spécifie les options de division du document en parties en Java."
type: docs
weight: 630
url: /fr/java/com.aspose.words/splitoptions/
---

**Inheritance:**
java.lang.Object
```
public class SplitOptions
```

Spécifie les options de découpage du document en parties.
## Méthodes

| Méthode | Description |
| --- | --- |
| [getSplitCriteria()](#getSplitCriteria) | Spécifie les critères de division du document en parties. |
| [getSplitStyle()](#getSplitStyle) | Spécifie le style de paragraphe pour diviser le document en parties lorsque [SplitCriteria.STYLE](../../com.aspose.words/splitcriteria/\#STYLE) est utilisé. |
| [setSplitCriteria(int value)](#setSplitCriteria-int) | Spécifie les critères de division du document en parties. |
| [setSplitStyle(String value)](#setSplitStyle-java.lang.String) | Spécifie le style de paragraphe pour diviser le document en parties lorsque [SplitCriteria.STYLE](../../com.aspose.words/splitcriteria/\#STYLE) est utilisé. |
### getSplitCriteria() {#getSplitCriteria}
```
public int getSplitCriteria()
```


Spécifie les critères de division du document en parties.

 **Examples:** 

Montre comment diviser le document par pages.

```

 String doc = getMyDir() + "Big document.docx";

 SplitOptions options = new SplitOptions();
 options.setSplitCriteria(SplitCriteria.PAGE);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.1.docx", options);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.2.docx", SaveFormat.DOCX, options);
 
```

**Returns:**
int - La valeur int correspondante. La valeur retournée est l'une des constantes [SplitCriteria](../../com.aspose.words/splitcriteria/).
### getSplitStyle() {#getSplitStyle}
```
public String getSplitStyle()
```


Spécifie le style de paragraphe pour diviser le document en parties lorsque [SplitCriteria.STYLE](../../com.aspose.words/splitcriteria/\#STYLE) est utilisé.

**Returns:**
java.lang.String - La valeur java.lang.String correspondante.
### setSplitCriteria(int value) {#setSplitCriteria-int}
```
public void setSplitCriteria(int value)
```


Spécifie les critères de division du document en parties.

 **Examples:** 

Montre comment diviser le document par pages.

```

 String doc = getMyDir() + "Big document.docx";

 SplitOptions options = new SplitOptions();
 options.setSplitCriteria(SplitCriteria.PAGE);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.1.docx", options);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.2.docx", SaveFormat.DOCX, options);
 
```

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | La valeur int correspondante. La valeur doit être l'une des constantes [SplitCriteria](../../com.aspose.words/splitcriteria/). |

### setSplitStyle(String value) {#setSplitStyle-java.lang.String}
```
public void setSplitStyle(String value)
```


Spécifie le style de paragraphe pour diviser le document en parties lorsque [SplitCriteria.STYLE](../../com.aspose.words/splitcriteria/\#STYLE) est utilisé.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | java.lang.String | La valeur java.lang.String correspondante. |

