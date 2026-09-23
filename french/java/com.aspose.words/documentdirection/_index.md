---
title: "DocumentDirection"
linktitle: "DocumentDirection"
second_title: "Aspose.Words pour Java"
description: "Permet de spécifier la direction du flux du texte dans un document en Java."
type: docs
weight: 165
url: /fr/java/com.aspose.words/documentdirection/
---

**Inheritance:**
java.lang.Object
```
public class DocumentDirection
```

Permet de spécifier la direction du flux de texte dans un document.

 **Examples:** 

Montre comment détecter la direction du texte d'un document en texte brut.

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
## Champs

| Champ | Description |
| --- | --- |
| [AUTO](#AUTO) | Détection automatique de la direction. |
| [LEFT_TO_RIGHT](#LEFT-TO-RIGHT) | Direction de gauche à droite. |
| [RIGHT_TO_LEFT](#RIGHT-TO-LEFT) | Direction de droite à gauche. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String documentDirectionName)](#fromName-java.lang.String) |  |
| [getName(int documentDirection)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int documentDirection)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Détection automatique de la direction.

 **Remarks:** 

Lorsque cette option est sélectionnée et que le texte contient des caractères appartenant aux scripts RTL, la direction du document sera automatiquement définie sur RTL.

### LEFT_TO_RIGHT {#LEFT-TO-RIGHT}
```
public static int LEFT_TO_RIGHT
```


Direction de gauche à droite.

### RIGHT_TO_LEFT {#RIGHT-TO-LEFT}
```
public static int RIGHT_TO_LEFT
```


Direction de droite à gauche.

### length {#length}
```
public static int length
```


### fromName(String documentDirectionName) {#fromName-java.lang.String}
```
public static int fromName(String documentDirectionName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| documentDirectionName | java.lang.String |  |

**Returns:**
int
### getName(int documentDirection) {#getName-int}
```
public static String getName(int documentDirection)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| documentDirection | int |  |

**Returns:**
java.lang.String
