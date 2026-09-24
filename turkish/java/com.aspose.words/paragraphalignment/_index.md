---
title: "ParagraphAlignment"
linktitle: "ParagraphAlignment"
second_title: "Aspose.Words Java için"
description: "Java'da bir paragraftaki metin hizalamasını belirtir."
type: docs
weight: 523
url: /tr/java/com.aspose.words/paragraphalignment/
---

**Inheritance:**
java.lang.Object
```
public class ParagraphAlignment
```

Paragraftaki metin hizalamasını belirtir.

 **Examples:** 

Aspose.Words belgesini elle nasıl oluşturacağınızı gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [ARABIC_HIGH_KASHIDA](#ARABIC-HIGH-KASHIDA) | Yalnızca Arapça. |
| [ARABIC_LOW_KASHIDA](#ARABIC-LOW-KASHIDA) | Yalnızca Arapça. |
| [ARABIC_MEDIUM_KASHIDA](#ARABIC-MEDIUM-KASHIDA) | Yalnızca Arapça. |
| [CENTER](#CENTER) | Metin yatay olarak ortalanmıştır. |
| [DISTRIBUTED](#DISTRIBUTED) | Metin eşit olarak dağıtılmıştır. |
| [JUSTIFY](#JUSTIFY) | Metin hem sola hem de sağa hizalanmıştır. |
| [LEFT](#LEFT) | Metin sola hizalanmıştır. |
| [MATH_ELEMENT_CENTER_AS_GROUP](#MATH-ELEMENT-CENTER-AS-GROUP) | Bir satırdaki tek Matematik öğesi, 'Centered As Group' olarak hizalanmıştır. |
| [RIGHT](#RIGHT) | Metin sağa hizalanmıştır. |
| [THAI_DISTRIBUTED](#THAI-DISTRIBUTED) | Yalnızca Tayca. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String paragraphAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int paragraphAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int paragraphAlignment)](#toString-int) |  |
### ARABIC_HIGH_KASHIDA {#ARABIC-HIGH-KASHIDA}
```
public static int ARABIC_HIGH_KASHIDA
```


Yalnızca Arapça. Metin için Kashida uzunluğu en geniş olası uzunluğa genişletilir.

### ARABIC_LOW_KASHIDA {#ARABIC-LOW-KASHIDA}
```
public static int ARABIC_LOW_KASHIDA
```


Yalnızca Arapça. Metin için Kashida uzunluğu biraz daha uzun bir uzunluğa genişletilir.

### ARABIC_MEDIUM_KASHIDA {#ARABIC-MEDIUM-KASHIDA}
```
public static int ARABIC_MEDIUM_KASHIDA
```


Yalnızca Arapça. Metin için Kashida uzunluğu tüketici tarafından belirlenen orta bir uzunluğa genişletilir.

### CENTER {#CENTER}
```
public static int CENTER
```


Metin yatay olarak ortalanmıştır.

### DISTRIBUTED {#DISTRIBUTED}
```
public static int DISTRIBUTED
```


Metin eşit olarak dağıtılmıştır.

### JUSTIFY {#JUSTIFY}
```
public static int JUSTIFY
```


Metin hem sola hem de sağa hizalanmıştır.

### LEFT {#LEFT}
```
public static int LEFT
```


Metin sola hizalanmıştır.

### MATH_ELEMENT_CENTER_AS_GROUP {#MATH-ELEMENT-CENTER-AS-GROUP}
```
public static int MATH_ELEMENT_CENTER_AS_GROUP
```


Bir satırdaki tek Matematik öğesi, 'Centered As Group' olarak hizalanmıştır.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Metin sağa hizalanmıştır.

### THAI_DISTRIBUTED {#THAI-DISTRIBUTED}
```
public static int THAI_DISTRIBUTED
```


Yalnızca Tayca. Metin, Tayca için bir optimizasyonla iki yana yaslanır.

### length {#length}
```
public static int length
```


### fromName(String paragraphAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String paragraphAlignmentName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| paragraphAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int paragraphAlignment) {#getName-int}
```
public static String getName(int paragraphAlignment)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| paragraphAlignment | int |  |

**Returns:**
java.lang.String
