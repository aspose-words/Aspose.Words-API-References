---
title: "DocumentDirection"
linktitle: "DocumentDirection"
second_title: "Aspose.Words per Java"
description: "Consente di specificare la direzione di flusso del testo in un documento in Java."
type: docs
weight: 165
url: /it/java/com.aspose.words/documentdirection/
---

**Inheritance:**
java.lang.Object
```
public class DocumentDirection
```

Consente di specificare la direzione di flusso del testo in un documento.

 **Examples:** 

Mostra come rilevare la direzione del testo di un documento di testo semplice.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [AUTO](#AUTO) | Rileva automaticamente la direzione. |
| [LEFT_TO_RIGHT](#LEFT-TO-RIGHT) | Direzione da sinistra a destra. |
| [RIGHT_TO_LEFT](#RIGHT-TO-LEFT) | Direzione da destra a sinistra. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String documentDirectionName)](#fromName-java.lang.String) |  |
| [getName(int documentDirection)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int documentDirection)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Rileva automaticamente la direzione.

 **Remarks:** 

Quando questa opzione è selezionata e il testo contiene caratteri appartenenti a script RTL, la direzione del documento verrà impostata automaticamente su RTL.

### LEFT_TO_RIGHT {#LEFT-TO-RIGHT}
```
public static int LEFT_TO_RIGHT
```


Direzione da sinistra a destra.

### RIGHT_TO_LEFT {#RIGHT-TO-LEFT}
```
public static int RIGHT_TO_LEFT
```


Direzione da destra a sinistra.

### length {#length}
```
public static int length
```


### fromName(String documentDirectionName) {#fromName-java.lang.String}
```
public static int fromName(String documentDirectionName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| documentDirectionName | java.lang.String |  |

**Returns:**
int
### getName(int documentDirection) {#getName-int}
```
public static String getName(int documentDirection)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| documentDirection | int |  |

**Returns:**
java.lang.String
