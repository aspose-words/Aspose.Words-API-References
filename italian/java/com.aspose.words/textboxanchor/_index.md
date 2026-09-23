---
title: "TextBoxAnchor"
linktitle: "TextBoxAnchor"
second_title: "Aspose.Words per Java"
description: "Specifica i valori utilizzati per l'allineamento verticale del testo della forma in Java."
type: docs
weight: 667
url: /it/java/com.aspose.words/textboxanchor/
---

**Inheritance:**
java.lang.Object
```
public class TextBoxAnchor
```

Specifica i valori usati per l'allineamento verticale del testo nella forma.

 **Examples:** 

Mostra come allineare verticalmente il contenuto di testo di una casella di testo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.TEXT_BOX, 200.0, 200.0);

 // Set the "VerticalAnchor" property to "TextBoxAnchor.Top" to
 // align the text in this text box with the top side of the shape.
 // Set the "VerticalAnchor" property to "TextBoxAnchor.Middle" to
 // align the text in this text box to the center of the shape.
 // Set the "VerticalAnchor" property to "TextBoxAnchor.Bottom" to
 // align the text in this text box to the bottom of the shape.
 shape.getTextBox().setVerticalAnchor(verticalAnchor);

 builder.moveTo(shape.getFirstParagraph());
 builder.write("Hello world!");

 // The vertical aligning of text inside text boxes is available from Microsoft Word 2007 onwards.
 doc.getCompatibilityOptions().optimizeFor(MsWordVersion.WORD_2007);
 doc.save(getArtifactsDir() + "Shape.VerticalAnchor.docx");
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [BOTTOM](#BOTTOM) | Il testo è allineato al fondo della casella di testo. |
| [BOTTOM_BASELINE](#BOTTOM-BASELINE) | Il testo è allineato alla linea di base inferiore della casella di testo. |
| [BOTTOM_CENTERED](#BOTTOM-CENTERED) | Il testo è allineato al centro inferiore della casella di testo. |
| [BOTTOM_CENTERED_BASELINE](#BOTTOM-CENTERED-BASELINE) | Il testo è allineato alla linea di base centrale inferiore della casella di testo. |
| [MIDDLE](#MIDDLE) | Il testo è allineato al centro della casella di testo. |
| [MIDDLE_CENTERED](#MIDDLE-CENTERED) | Il testo è allineato al centro medio della casella di testo. |
| [TOP](#TOP) | Il testo è allineato alla parte superiore della casella di testo. |
| [TOP_BASELINE](#TOP-BASELINE) | Il testo è allineato alla linea di base superiore della casella di testo. |
| [TOP_CENTERED](#TOP-CENTERED) | Il testo è allineato al centro superiore della casella di testo. |
| [TOP_CENTERED_BASELINE](#TOP-CENTERED-BASELINE) | Il testo è allineato alla linea di base centrale superiore della casella di testo. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String textBoxAnchorName)](#fromName-java.lang.String) |  |
| [getName(int textBoxAnchor)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textBoxAnchor)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Il testo è allineato al fondo della casella di testo.

### BOTTOM_BASELINE {#BOTTOM-BASELINE}
```
public static int BOTTOM_BASELINE
```


Il testo è allineato alla linea di base inferiore della casella di testo.

### BOTTOM_CENTERED {#BOTTOM-CENTERED}
```
public static int BOTTOM_CENTERED
```


Il testo è allineato al centro inferiore della casella di testo.

### BOTTOM_CENTERED_BASELINE {#BOTTOM-CENTERED-BASELINE}
```
public static int BOTTOM_CENTERED_BASELINE
```


Il testo è allineato alla linea di base centrale inferiore della casella di testo.

### MIDDLE {#MIDDLE}
```
public static int MIDDLE
```


Il testo è allineato al centro della casella di testo.

### MIDDLE_CENTERED {#MIDDLE-CENTERED}
```
public static int MIDDLE_CENTERED
```


Il testo è allineato al centro medio della casella di testo.

### TOP {#TOP}
```
public static int TOP
```


Il testo è allineato alla parte superiore della casella di testo.

### TOP_BASELINE {#TOP-BASELINE}
```
public static int TOP_BASELINE
```


Il testo è allineato alla linea di base superiore della casella di testo.

### TOP_CENTERED {#TOP-CENTERED}
```
public static int TOP_CENTERED
```


Il testo è allineato al centro superiore della casella di testo.

### TOP_CENTERED_BASELINE {#TOP-CENTERED-BASELINE}
```
public static int TOP_CENTERED_BASELINE
```


Il testo è allineato alla linea di base centrale superiore della casella di testo.

### length {#length}
```
public static int length
```


### fromName(String textBoxAnchorName) {#fromName-java.lang.String}
```
public static int fromName(String textBoxAnchorName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| textBoxAnchorName | java.lang.String |  |

**Returns:**
int
### getName(int textBoxAnchor) {#getName-int}
```
public static String getName(int textBoxAnchor)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| textBoxAnchor | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int textBoxAnchor) {#toString-int}
```
public static String toString(int textBoxAnchor)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| textBoxAnchor | int |  |

**Returns:**
java.lang.String
