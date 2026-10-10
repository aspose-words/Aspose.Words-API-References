---
title: "SdtAppearance"
linktitle: "SdtAppearance"
second_title: "Aspose.Words para Java"
description: "Especifica la apariencia de una etiqueta de documento estructurado en Java."
type: docs
weight: 599
url: /es/java/com.aspose.words/sdtappearance/
---

**Inheritance:**
java.lang.Object
```
public class SdtAppearance
```

Especifica la apariencia de una etiqueta de documento estructurado.

 **Examples:** 

Muestra cómo mostrar la etiqueta alrededor del contenido.

```

 Document doc = new Document(getMyDir() + "Multi-section structured document tags.docx");
 StructuredDocumentTagRangeStart tag = (StructuredDocumentTagRangeStart) doc.getChild(NodeType.STRUCTURED_DOCUMENT_TAG_RANGE_START, 0, true);

 if (tag.getAppearance() == SdtAppearance.HIDDEN)
     tag.setAppearance(SdtAppearance.TAGS);
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [BOUNDING_BOX](#BOUNDING-BOX) | Representa una etiqueta de documento estructurado que se muestra como un rectángulo sombreado o un cuadro delimitador. |
| [DEFAULT](#DEFAULT) | Por defecto es [BOUNDING\_BOX](../../com.aspose.words/sdtappearance/\#BOUNDING-BOX). |
| [HIDDEN](#HIDDEN) | Representa una etiqueta de documento estructurado que no se muestra. |
| [TAGS](#TAGS) | Representa una etiqueta de documento estructurado que se muestra como marcadores de inicio y fin. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String sdtAppearanceName)](#fromName-java.lang.String) |  |
| [getName(int sdtAppearance)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sdtAppearance)](#toString-int) |  |
### BOUNDING_BOX {#BOUNDING-BOX}
```
public static int BOUNDING_BOX
```


Representa una etiqueta de documento estructurado que se muestra como un rectángulo sombreado o un cuadro delimitador.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Por defecto es [BOUNDING\_BOX](../../com.aspose.words/sdtappearance/\#BOUNDING-BOX).

### HIDDEN {#HIDDEN}
```
public static int HIDDEN
```


Representa una etiqueta de documento estructurado que no se muestra.

### TAGS {#TAGS}
```
public static int TAGS
```


Representa una etiqueta de documento estructurado que se muestra como marcadores de inicio y fin.

### length {#length}
```
public static int length
```


### fromName(String sdtAppearanceName) {#fromName-java.lang.String}
```
public static int fromName(String sdtAppearanceName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| sdtAppearanceName | java.lang.String |  |

**Returns:**
int
### getName(int sdtAppearance) {#getName-int}
```
public static String getName(int sdtAppearance)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| sdtAppearance | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int sdtAppearance) {#toString-int}
```
public static String toString(int sdtAppearance)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| sdtAppearance | int |  |

**Returns:**
java.lang.String
