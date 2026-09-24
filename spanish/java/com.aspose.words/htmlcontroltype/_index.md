---
title: "HtmlControlType"
linktitle: "HtmlControlType"
second_title: "Aspose.Words para Java"
description: "Tipo de nodos de documento que representan los elementos  y  importados desde HTML en Java."
type: docs
weight: 377
url: /es/java/com.aspose.words/htmlcontroltype/
---

**Inheritance:**
java.lang.Object
```
public class HtmlControlType
```

Tipo de nodos de documento que representan los elementos  y  importados desde HTML. Ejemplos: Muestra cómo establecer el tipo preferido de nodos de documento que representarán los elementos importados  y  .   final String html = "\\r\\n\\r\\n\\r\\n" + "item1\\r\\n\\r\\n\\r\\n\\r\\n"; HtmlLoadOptions htmlLoadOptions = new HtmlLoadOptions(); htmlLoadOptions.setPreferredControlType(HtmlControlType.STRUCTURED\_DOCUMENT\_TAG); Document doc = new Document(new ByteArrayInputStream(html.getBytes(StandardCharsets.UTF\_8)), htmlLoadOptions); NodeCollection nodes = doc.getChildNodes(NodeType.STRUCTURED\_DOCUMENT\_TAG, true); StructuredDocumentTag tag = (StructuredDocumentTag) nodes.get(0);
## Campos

| Campo | Descripción |
| --- | --- |
| [FORM_FIELD](#FORM-FIELD) | Un campo de formulario. |
| [STRUCTURED_DOCUMENT_TAG](#STRUCTURED-DOCUMENT-TAG) | Una etiqueta de documento estructurado |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String htmlControlTypeName)](#fromName-java.lang.String) |  |
| [getName(int htmlControlType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int htmlControlType)](#toString-int) |  |
### FORM_FIELD {#FORM-FIELD}
```
public static int FORM_FIELD
```


Un campo de formulario.

### STRUCTURED_DOCUMENT_TAG {#STRUCTURED-DOCUMENT-TAG}
```
public static int STRUCTURED_DOCUMENT_TAG
```


Una etiqueta de documento estructurado

### length {#length}
```
public static int length
```


### fromName(String htmlControlTypeName) {#fromName-java.lang.String}
```
public static int fromName(String htmlControlTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| htmlControlTypeName | java.lang.String |  |

**Returns:**
int
### getName(int htmlControlType) {#getName-int}
```
public static String getName(int htmlControlType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| htmlControlType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int htmlControlType) {#toString-int}
```
public static String toString(int htmlControlType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| htmlControlType | int |  |

**Returns:**
java.lang.String
