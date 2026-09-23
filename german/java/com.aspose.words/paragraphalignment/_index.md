---
title: "ParagraphAlignment"
linktitle: "ParagraphAlignment"
second_title: "Aspose.Words für Java"
description: "Gibt die Textausrichtung in einem Absatz in Java an."
type: docs
weight: 523
url: /de/java/com.aspose.words/paragraphalignment/
---

**Inheritance:**
java.lang.Object
```
public class ParagraphAlignment
```

Gibt die Textausrichtung in einem Absatz an.

 **Examples:** 

Zeigt, wie man ein Aspose.Words-Dokument von Hand erstellt.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [ARABIC_HIGH_KASHIDA](#ARABIC-HIGH-KASHIDA) | Nur Arabisch. |
| [ARABIC_LOW_KASHIDA](#ARABIC-LOW-KASHIDA) | Nur Arabisch. |
| [ARABIC_MEDIUM_KASHIDA](#ARABIC-MEDIUM-KASHIDA) | Nur Arabisch. |
| [CENTER](#CENTER) | Der Text ist horizontal zentriert. |
| [DISTRIBUTED](#DISTRIBUTED) | Der Text ist gleichmäßig verteilt. |
| [JUSTIFY](#JUSTIFY) | Der Text ist links und rechts ausgerichtet. |
| [LEFT](#LEFT) | Der Text ist linksbündig ausgerichtet. |
| [MATH_ELEMENT_CENTER_AS_GROUP](#MATH-ELEMENT-CENTER-AS-GROUP) | Das einzige Math-Element in einer Zeile, ausgerichtet als 'Centered As Group'. |
| [RIGHT](#RIGHT) | Der Text ist rechtsbündig ausgerichtet. |
| [THAI_DISTRIBUTED](#THAI-DISTRIBUTED) | Nur Thailändisch. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String paragraphAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int paragraphAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int paragraphAlignment)](#toString-int) |  |
### ARABIC_HIGH_KASHIDA {#ARABIC-HIGH-KASHIDA}
```
public static int ARABIC_HIGH_KASHIDA
```


Nur Arabisch. Die Kashida-Länge für den Text wird auf die größtmögliche Länge erweitert.

### ARABIC_LOW_KASHIDA {#ARABIC-LOW-KASHIDA}
```
public static int ARABIC_LOW_KASHIDA
```


Nur Arabisch. Die Kashida-Länge für den Text wird auf eine leicht längere Länge erweitert.

### ARABIC_MEDIUM_KASHIDA {#ARABIC-MEDIUM-KASHIDA}
```
public static int ARABIC_MEDIUM_KASHIDA
```


Nur Arabisch. Die Kashida-Länge für den Text wird auf eine mittlere Länge erweitert, die vom Verbraucher bestimmt wird.

### CENTER {#CENTER}
```
public static int CENTER
```


Der Text ist horizontal zentriert.

### DISTRIBUTED {#DISTRIBUTED}
```
public static int DISTRIBUTED
```


Der Text ist gleichmäßig verteilt.

### JUSTIFY {#JUSTIFY}
```
public static int JUSTIFY
```


Der Text ist links und rechts ausgerichtet.

### LEFT {#LEFT}
```
public static int LEFT
```


Der Text ist linksbündig ausgerichtet.

### MATH_ELEMENT_CENTER_AS_GROUP {#MATH-ELEMENT-CENTER-AS-GROUP}
```
public static int MATH_ELEMENT_CENTER_AS_GROUP
```


Das einzige Math-Element in einer Zeile, ausgerichtet als 'Centered As Group'.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Der Text ist rechtsbündig ausgerichtet.

### THAI_DISTRIBUTED {#THAI-DISTRIBUTED}
```
public static int THAI_DISTRIBUTED
```


Nur Thailändisch. Der Text ist mit einer Optimierung für Thailändisch im Blocksatz.

### length {#length}
```
public static int length
```


### fromName(String paragraphAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String paragraphAlignmentName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| paragraphAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int paragraphAlignment) {#getName-int}
```
public static String getName(int paragraphAlignment)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| paragraphAlignment | int |  |

**Returns:**
java.lang.String
