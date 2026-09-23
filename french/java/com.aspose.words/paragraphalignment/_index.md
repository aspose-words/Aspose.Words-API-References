---
title: "ParagraphAlignment"
linktitle: "ParagraphAlignment"
second_title: "Aspose.Words pour Java"
description: "Spécifie l'alignement du texte dans un paragraphe en Java."
type: docs
weight: 523
url: /fr/java/com.aspose.words/paragraphalignment/
---

**Inheritance:**
java.lang.Object
```
public class ParagraphAlignment
```

Spécifie l'alignement du texte dans un paragraphe.

 **Examples:** 

Montre comment construire manuellement un document Aspose.Words.

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
## Champs

| Champ | Description |
| --- | --- |
| [ARABIC_HIGH_KASHIDA](#ARABIC-HIGH-KASHIDA) | Arabe uniquement. |
| [ARABIC_LOW_KASHIDA](#ARABIC-LOW-KASHIDA) | Arabe uniquement. |
| [ARABIC_MEDIUM_KASHIDA](#ARABIC-MEDIUM-KASHIDA) | Arabe uniquement. |
| [CENTER](#CENTER) | Le texte est centré horizontalement. |
| [DISTRIBUTED](#DISTRIBUTED) | Le texte est réparti uniformément. |
| [JUSTIFY](#JUSTIFY) | Le texte est aligné à la fois à gauche et à droite. |
| [LEFT](#LEFT) | Le texte est aligné à gauche. |
| [MATH_ELEMENT_CENTER_AS_GROUP](#MATH-ELEMENT-CENTER-AS-GROUP) | Le seul élément Math dans une ligne, aligné comme 'Centré en groupe'. |
| [RIGHT](#RIGHT) | Le texte est aligné à droite. |
| [THAI_DISTRIBUTED](#THAI-DISTRIBUTED) | Thaï uniquement. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String paragraphAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int paragraphAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int paragraphAlignment)](#toString-int) |  |
### ARABIC_HIGH_KASHIDA {#ARABIC-HIGH-KASHIDA}
```
public static int ARABIC_HIGH_KASHIDA
```


Arabe uniquement. La longueur du Kashida pour le texte est étendue à sa longueur maximale possible.

### ARABIC_LOW_KASHIDA {#ARABIC-LOW-KASHIDA}
```
public static int ARABIC_LOW_KASHIDA
```


Arabe uniquement. La longueur du Kashida pour le texte est étendue à une longueur légèrement plus longue.

### ARABIC_MEDIUM_KASHIDA {#ARABIC-MEDIUM-KASHIDA}
```
public static int ARABIC_MEDIUM_KASHIDA
```


Arabe uniquement. La longueur du Kashida pour le texte est étendue à une longueur moyenne déterminée par le consommateur.

### CENTER {#CENTER}
```
public static int CENTER
```


Le texte est centré horizontalement.

### DISTRIBUTED {#DISTRIBUTED}
```
public static int DISTRIBUTED
```


Le texte est réparti uniformément.

### JUSTIFY {#JUSTIFY}
```
public static int JUSTIFY
```


Le texte est aligné à la fois à gauche et à droite.

### LEFT {#LEFT}
```
public static int LEFT
```


Le texte est aligné à gauche.

### MATH_ELEMENT_CENTER_AS_GROUP {#MATH-ELEMENT-CENTER-AS-GROUP}
```
public static int MATH_ELEMENT_CENTER_AS_GROUP
```


Le seul élément Math dans une ligne, aligné comme 'Centré en groupe'.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Le texte est aligné à droite.

### THAI_DISTRIBUTED {#THAI-DISTRIBUTED}
```
public static int THAI_DISTRIBUTED
```


Thaï uniquement. Le texte est justifié avec une optimisation pour le thaï.

### length {#length}
```
public static int length
```


### fromName(String paragraphAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String paragraphAlignmentName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| paragraphAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int paragraphAlignment) {#getName-int}
```
public static String getName(int paragraphAlignment)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| paragraphAlignment | int |  |

**Returns:**
java.lang.String
