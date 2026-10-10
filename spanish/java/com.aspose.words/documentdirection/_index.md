---
title: "DocumentDirection"
linktitle: "DocumentDirection"
second_title: "Aspose.Words para Java"
description: "Permite especificar la dirección en la que fluye el texto en un documento en Java."
type: docs
weight: 165
url: /es/java/com.aspose.words/documentdirection/
---

**Inheritance:**
java.lang.Object
```
public class DocumentDirection
```

Permite especificar la dirección del flujo de texto en un documento.

 **Examples:** 

Muestra cómo detectar la dirección del texto en un documento de texto plano.

```

 // Create a "TxtLoadOptions" object, which we can pass to a document's constructor
 // to modify how we load a plaintext document.
 TxtLoadOptions loadOptions = new TxtLoadOptions();

 // Set the "DocumentDirection" property to "DocumentDirection.Auto" automatically detects
 // the direction of every paragraph of text that Aspose.Words loads from plaintext.
 // Each paragraph's "Bidi" property will store its direction.
 loadOptions.setDocumentDirection(DocumentDirection.AUTO);

 // Detect Hebrew text as right-to-left.
 Document doc = new Document(getMyDir() + "Hebrew text.txt", loadOptions);

 Assert.assertTrue(doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBidi());

 // Detect English text as right-to-left.
 doc = new Document(getMyDir() + "English text.txt", loadOptions);

 Assert.assertFalse(doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getBidi());
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [AUTO](#AUTO) | Dirección de detección automática. |
| [LEFT_TO_RIGHT](#LEFT-TO-RIGHT) | Dirección de izquierda a derecha. |
| [RIGHT_TO_LEFT](#RIGHT-TO-LEFT) | Dirección de derecha a izquierda. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String documentDirectionName)](#fromName-java.lang.String) |  |
| [getName(int documentDirection)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int documentDirection)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Dirección de detección automática.

 **Remarks:** 

Cuando se selecciona esta opción y el texto contiene caracteres pertenecientes a scripts RTL, la dirección del documento se establecerá automáticamente a RTL.

### LEFT_TO_RIGHT {#LEFT-TO-RIGHT}
```
public static int LEFT_TO_RIGHT
```


Dirección de izquierda a derecha.

### RIGHT_TO_LEFT {#RIGHT-TO-LEFT}
```
public static int RIGHT_TO_LEFT
```


Dirección de derecha a izquierda.

### length {#length}
```
public static int length
```


### fromName(String documentDirectionName) {#fromName-java.lang.String}
```
public static int fromName(String documentDirectionName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| documentDirectionName | java.lang.String |  |

**Returns:**
int
### getName(int documentDirection) {#getName-int}
```
public static String getName(int documentDirection)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| documentDirection | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int documentDirection) {#toString-int}
```
public static String toString(int documentDirection)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| documentDirection | int |  |

**Returns:**
java.lang.String
