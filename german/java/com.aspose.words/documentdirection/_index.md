---
title: "DocumentDirection"
linktitle: "DocumentDirection"
second_title: "Aspose.Words für Java"
description: "Ermöglicht die Angabe der Fließrichtung des Textes in einem Dokument in Java."
type: docs
weight: 165
url: /de/java/com.aspose.words/documentdirection/
---

**Inheritance:**
java.lang.Object
```
public class DocumentDirection
```

Ermöglicht das Festlegen der Fließrichtung des Textes in einem Dokument.

 **Examples:** 

Zeigt, wie die Textflussrichtung eines Klartextdokuments erkannt wird.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [AUTO](#AUTO) | Richtung automatisch erkennen. |
| [LEFT_TO_RIGHT](#LEFT-TO-RIGHT) | Links‑nach‑rechts‑Richtung. |
| [RIGHT_TO_LEFT](#RIGHT-TO-LEFT) | Rechts‑nach‑links‑Richtung. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String documentDirectionName)](#fromName-java.lang.String) |  |
| [getName(int documentDirection)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int documentDirection)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Richtung automatisch erkennen.

 **Remarks:** 

Wenn diese Option ausgewählt ist und der Text Zeichen aus RTL‑Schriften enthält, wird die Dokumentenrichtung automatisch auf RTL gesetzt.

### LEFT_TO_RIGHT {#LEFT-TO-RIGHT}
```
public static int LEFT_TO_RIGHT
```


Links‑nach‑rechts‑Richtung.

### RIGHT_TO_LEFT {#RIGHT-TO-LEFT}
```
public static int RIGHT_TO_LEFT
```


Rechts‑nach‑links‑Richtung.

### length {#length}
```
public static int length
```


### fromName(String documentDirectionName) {#fromName-java.lang.String}
```
public static int fromName(String documentDirectionName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| documentDirectionName | java.lang.String |  |

**Returns:**
int
### getName(int documentDirection) {#getName-int}
```
public static String getName(int documentDirection)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| documentDirection | int |  |

**Returns:**
java.lang.String
