---
title: "SplitOptions"
linktitle: "SplitOptions"
second_title: "Aspose.Words para Java"
description: "Especifica opciones sobre cómo se divide el documento en partes en Java."
type: docs
weight: 630
url: /es/java/com.aspose.words/splitoptions/
---

**Inheritance:**
java.lang.Object
```
public class SplitOptions
```

Especifica opciones de cómo se divide el documento en partes.
## Métodos

| Método | Descripción |
| --- | --- |
| [getSplitCriteria()](#getSplitCriteria) | Especifica los criterios para dividir el documento en partes. |
| [getSplitStyle()](#getSplitStyle) | Especifica el estilo de párrafo para dividir el documento en partes cuando se usa [SplitCriteria.STYLE](../../com.aspose.words/splitcriteria/\#STYLE). |
| [setSplitCriteria(int value)](#setSplitCriteria-int) | Especifica los criterios para dividir el documento en partes. |
| [setSplitStyle(String value)](#setSplitStyle-java.lang.String) | Especifica el estilo de párrafo para dividir el documento en partes cuando se usa [SplitCriteria.STYLE](../../com.aspose.words/splitcriteria/\#STYLE). |
### getSplitCriteria() {#getSplitCriteria}
```
public int getSplitCriteria()
```


Especifica los criterios para dividir el documento en partes.

 **Examples:** 

Muestra cómo dividir el documento por páginas.

```

 String doc = getMyDir() + "Big document.docx";

 SplitOptions options = new SplitOptions();
 options.setSplitCriteria(SplitCriteria.PAGE);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.1.docx", options);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.2.docx", SaveFormat.DOCX, options);
 
```

**Returns:**
int - El valor entero correspondiente. El valor devuelto es una de las constantes de [SplitCriteria](../../com.aspose.words/splitcriteria/).
### getSplitStyle() {#getSplitStyle}
```
public String getSplitStyle()
```


Especifica el estilo de párrafo para dividir el documento en partes cuando se usa [SplitCriteria.STYLE](../../com.aspose.words/splitcriteria/\#STYLE).

**Returns:**
java.lang.String - El valor java.lang.String correspondiente.
### setSplitCriteria(int value) {#setSplitCriteria-int}
```
public void setSplitCriteria(int value)
```


Especifica los criterios para dividir el documento en partes.

 **Examples:** 

Muestra cómo dividir el documento por páginas.

```

 String doc = getMyDir() + "Big document.docx";

 SplitOptions options = new SplitOptions();
 options.setSplitCriteria(SplitCriteria.PAGE);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.1.docx", options);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.2.docx", SaveFormat.DOCX, options);
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | El valor entero correspondiente. El valor debe ser una de las constantes de [SplitCriteria](../../com.aspose.words/splitcriteria/). |

### setSplitStyle(String value) {#setSplitStyle-java.lang.String}
```
public void setSplitStyle(String value)
```


Especifica el estilo de párrafo para dividir el documento en partes cuando se usa [SplitCriteria.STYLE](../../com.aspose.words/splitcriteria/\#STYLE).

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | java.lang.String | El valor java.lang.String correspondiente. |

