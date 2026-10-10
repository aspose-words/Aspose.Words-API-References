---
title: "ParagraphAlignment"
linktitle: "ParagraphAlignment"
second_title: "Aspose.Words para Java"
description: "Especifica la alineación del texto en un párrafo en Java."
type: docs
weight: 523
url: /es/java/com.aspose.words/paragraphalignment/
---

**Inheritance:**
java.lang.Object
```
public class ParagraphAlignment
```

Especifica la alineación del texto en un párrafo.

 **Examples:** 

Muestra cómo construir un documento Aspose.Words manualmente.

```

 Document doc = new Document();

 // A blank document contains one section, one body and one paragraph.
 // Call the "RemoveAllChildren" method to remove all those nodes,
 // and end up with a document node with no children.
 doc.removeAllChildren();

 // This document now has no composite child nodes that we can add content to.
 // If we wish to edit it, we will need to repopulate its node collection.
 // First, create a new section, and then append it as a child to the root document node.
 Section section = new Section(doc);
 doc.appendChild(section);

 // Set some page setup properties for the section.
 section.getPageSetup().setSectionStart(SectionStart.NEW_PAGE);
 section.getPageSetup().setPaperSize(PaperSize.LETTER);

 // A section needs a body, which will contain and display all its contents
 // on the page between the section's header and footer.
 Body body = new Body(doc);
 section.appendChild(body);

 // Create a paragraph, set some formatting properties, and then append it as a child to the body.
 Paragraph para = new Paragraph(doc);

 para.getParagraphFormat().setStyleName("Heading 1");
 para.getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 body.appendChild(para);

 // Finally, add some content to do the document. Create a run,
 // set its appearance and contents, and then append it as a child to the paragraph.
 Run run = new Run(doc);
 run.setText("Hello World!");
 run.getFont().setColor(Color.RED);
 para.appendChild(run);

 Assert.assertEquals("Hello World!", doc.getText().trim());

 doc.save(getArtifactsDir() + "Section.CreateManually.docx");
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [ARABIC_HIGH_KASHIDA](#ARABIC-HIGH-KASHIDA) | Solo árabe. |
| [ARABIC_LOW_KASHIDA](#ARABIC-LOW-KASHIDA) | Solo árabe. |
| [ARABIC_MEDIUM_KASHIDA](#ARABIC-MEDIUM-KASHIDA) | Solo árabe. |
| [CENTER](#CENTER) | El texto está centrado horizontalmente. |
| [DISTRIBUTED](#DISTRIBUTED) | El texto está distribuido uniformemente. |
| [JUSTIFY](#JUSTIFY) | El texto está alineado tanto a la izquierda como a la derecha. |
| [LEFT](#LEFT) | El texto está alineado a la izquierda. |
| [MATH_ELEMENT_CENTER_AS_GROUP](#MATH-ELEMENT-CENTER-AS-GROUP) | El único elemento Math en una línea, alineado como 'Centered As Group'. |
| [RIGHT](#RIGHT) | El texto está alineado a la derecha. |
| [THAI_DISTRIBUTED](#THAI-DISTRIBUTED) | Solo tailandés. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String paragraphAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int paragraphAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int paragraphAlignment)](#toString-int) |  |
### ARABIC_HIGH_KASHIDA {#ARABIC-HIGH-KASHIDA}
```
public static int ARABIC_HIGH_KASHIDA
```


Solo árabe. La longitud de Kashida para el texto se extiende a su longitud máxima posible.

### ARABIC_LOW_KASHIDA {#ARABIC-LOW-KASHIDA}
```
public static int ARABIC_LOW_KASHIDA
```


Solo árabe. La longitud de Kashida para el texto se extiende a una longitud ligeramente mayor.

### ARABIC_MEDIUM_KASHIDA {#ARABIC-MEDIUM-KASHIDA}
```
public static int ARABIC_MEDIUM_KASHIDA
```


Solo árabe. La longitud de Kashida para el texto se extiende a una longitud media determinada por el consumidor.

### CENTER {#CENTER}
```
public static int CENTER
```


El texto está centrado horizontalmente.

### DISTRIBUTED {#DISTRIBUTED}
```
public static int DISTRIBUTED
```


El texto está distribuido uniformemente.

### JUSTIFY {#JUSTIFY}
```
public static int JUSTIFY
```


El texto está alineado tanto a la izquierda como a la derecha.

### LEFT {#LEFT}
```
public static int LEFT
```


El texto está alineado a la izquierda.

### MATH_ELEMENT_CENTER_AS_GROUP {#MATH-ELEMENT-CENTER-AS-GROUP}
```
public static int MATH_ELEMENT_CENTER_AS_GROUP
```


El único elemento Math en una línea, alineado como 'Centered As Group'.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


El texto está alineado a la derecha.

### THAI_DISTRIBUTED {#THAI-DISTRIBUTED}
```
public static int THAI_DISTRIBUTED
```


Solo tailandés. El texto está justificado con una optimización para tailandés.

### length {#length}
```
public static int length
```


### fromName(String paragraphAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String paragraphAlignmentName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| paragraphAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int paragraphAlignment) {#getName-int}
```
public static String getName(int paragraphAlignment)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| paragraphAlignment | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int paragraphAlignment) {#toString-int}
```
public static String toString(int paragraphAlignment)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| paragraphAlignment | int |  |

**Returns:**
java.lang.String
