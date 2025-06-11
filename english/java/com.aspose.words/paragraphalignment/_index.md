---
title: ParagraphAlignment
linktitle: ParagraphAlignment
second_title: Aspose.Words for Java
description: Specifies text alignment in a paragraph in Java.
type: docs
weight: 516
url: /java/com.aspose.words/paragraphalignment/
---

**Inheritance:**
java.lang.Object
```
public class ParagraphAlignment
```

Specifies text alignment in a paragraph.

 **Examples:** 

Shows how to construct an Aspose.Words document by hand.

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
## Fields

| Field | Description |
| --- | --- |
| [ARABIC_HIGH_KASHIDA](#ARABIC-HIGH-KASHIDA) | Arabic only. |
| [ARABIC_LOW_KASHIDA](#ARABIC-LOW-KASHIDA) | Arabic only. |
| [ARABIC_MEDIUM_KASHIDA](#ARABIC-MEDIUM-KASHIDA) | Arabic only. |
| [CENTER](#CENTER) | Text is centered horizontally. |
| [DISTRIBUTED](#DISTRIBUTED) | Text is evenly distributed. |
| [JUSTIFY](#JUSTIFY) | Text is aligned to both left and right. |
| [LEFT](#LEFT) | Text is aligned to the left. |
| [MATH_ELEMENT_CENTER_AS_GROUP](#MATH-ELEMENT-CENTER-AS-GROUP) | The only Math element in a line, aligned as 'Centered As Group'. |
| [RIGHT](#RIGHT) | Text is aligned to the right. |
| [THAI_DISTRIBUTED](#THAI-DISTRIBUTED) | Thai only. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String paragraphAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int paragraphAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int paragraphAlignment)](#toString-int) |  |
### ARABIC_HIGH_KASHIDA {#ARABIC-HIGH-KASHIDA}
```
public static int ARABIC_HIGH_KASHIDA
```


Arabic only. Kashida length for text is extended to its widest possible length.

### ARABIC_LOW_KASHIDA {#ARABIC-LOW-KASHIDA}
```
public static int ARABIC_LOW_KASHIDA
```


Arabic only. Kashida length for text is extended to a slightly longer length.

### ARABIC_MEDIUM_KASHIDA {#ARABIC-MEDIUM-KASHIDA}
```
public static int ARABIC_MEDIUM_KASHIDA
```


Arabic only. Kashida length for text is extended to a medium length determined by the consumer.

### CENTER {#CENTER}
```
public static int CENTER
```


Text is centered horizontally.

### DISTRIBUTED {#DISTRIBUTED}
```
public static int DISTRIBUTED
```


Text is evenly distributed.

### JUSTIFY {#JUSTIFY}
```
public static int JUSTIFY
```


Text is aligned to both left and right.

### LEFT {#LEFT}
```
public static int LEFT
```


Text is aligned to the left.

### MATH_ELEMENT_CENTER_AS_GROUP {#MATH-ELEMENT-CENTER-AS-GROUP}
```
public static int MATH_ELEMENT_CENTER_AS_GROUP
```


The only Math element in a line, aligned as 'Centered As Group'.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Text is aligned to the right.

### THAI_DISTRIBUTED {#THAI-DISTRIBUTED}
```
public static int THAI_DISTRIBUTED
```


Thai only. Text is justified with an optimization for Thai.

### length {#length}
```
public static int length
```


### fromName(String paragraphAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String paragraphAlignmentName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| paragraphAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int paragraphAlignment) {#getName-int}
```
public static String getName(int paragraphAlignment)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| paragraphAlignment | int |  |

**Returns:**
java.lang.String
