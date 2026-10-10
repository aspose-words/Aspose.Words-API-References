---
title: "ParagraphAlignment"
linktitle: "ParagraphAlignment"
second_title: "Aspose.Words per Java"
description: "Specifica l'allineamento del testo in un paragrafo in Java."
type: docs
weight: 523
url: /it/java/com.aspose.words/paragraphalignment/
---

**Inheritance:**
java.lang.Object
```
public class ParagraphAlignment
```

Specifica l'allineamento del testo in un paragrafo.

 **Examples:** 

Mostra come costruire manualmente un documento Aspose.Words.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [ARABIC_HIGH_KASHIDA](#ARABIC-HIGH-KASHIDA) | Solo arabo. |
| [ARABIC_LOW_KASHIDA](#ARABIC-LOW-KASHIDA) | Solo arabo. |
| [ARABIC_MEDIUM_KASHIDA](#ARABIC-MEDIUM-KASHIDA) | Solo arabo. |
| [CENTER](#CENTER) | Il testo è centrato orizzontalmente. |
| [DISTRIBUTED](#DISTRIBUTED) | Il testo è distribuito uniformemente. |
| [JUSTIFY](#JUSTIFY) | Il testo è allineato sia a sinistra che a destra. |
| [LEFT](#LEFT) | Il testo è allineato a sinistra. |
| [MATH_ELEMENT_CENTER_AS_GROUP](#MATH-ELEMENT-CENTER-AS-GROUP) | L'unico elemento Math in una riga, allineato come 'Centered As Group'. |
| [RIGHT](#RIGHT) | Il testo è allineato a destra. |
| [THAI_DISTRIBUTED](#THAI-DISTRIBUTED) | Solo tailandese. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String paragraphAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int paragraphAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int paragraphAlignment)](#toString-int) |  |
### ARABIC_HIGH_KASHIDA {#ARABIC-HIGH-KASHIDA}
```
public static int ARABIC_HIGH_KASHIDA
```


Solo arabo. La lunghezza Kashida per il testo è estesa alla sua massima lunghezza possibile.

### ARABIC_LOW_KASHIDA {#ARABIC-LOW-KASHIDA}
```
public static int ARABIC_LOW_KASHIDA
```


Solo arabo. La lunghezza Kashida per il testo è estesa a una lunghezza leggermente più lunga.

### ARABIC_MEDIUM_KASHIDA {#ARABIC-MEDIUM-KASHIDA}
```
public static int ARABIC_MEDIUM_KASHIDA
```


Solo arabo. La lunghezza Kashida per il testo è estesa a una lunghezza media determinata dal consumatore.

### CENTER {#CENTER}
```
public static int CENTER
```


Il testo è centrato orizzontalmente.

### DISTRIBUTED {#DISTRIBUTED}
```
public static int DISTRIBUTED
```


Il testo è distribuito uniformemente.

### JUSTIFY {#JUSTIFY}
```
public static int JUSTIFY
```


Il testo è allineato sia a sinistra che a destra.

### LEFT {#LEFT}
```
public static int LEFT
```


Il testo è allineato a sinistra.

### MATH_ELEMENT_CENTER_AS_GROUP {#MATH-ELEMENT-CENTER-AS-GROUP}
```
public static int MATH_ELEMENT_CENTER_AS_GROUP
```


L'unico elemento Math in una riga, allineato come 'Centered As Group'.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Il testo è allineato a destra.

### THAI_DISTRIBUTED {#THAI-DISTRIBUTED}
```
public static int THAI_DISTRIBUTED
```


Solo tailandese. Il testo è giustificato con un'ottimizzazione per il tailandese.

### length {#length}
```
public static int length
```


### fromName(String paragraphAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String paragraphAlignmentName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| paragraphAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int paragraphAlignment) {#getName-int}
```
public static String getName(int paragraphAlignment)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| paragraphAlignment | int |  |

**Returns:**
java.lang.String
