---
title: "ParagraphAlignment"
linktitle: "ParagraphAlignment"
second_title: "Aspose.Words для Java"
description: "Указывает выравнивание текста в абзаце в Java."
type: docs
weight: 523
url: /ru/java/com.aspose.words/paragraphalignment/
---

**Inheritance:**
java.lang.Object
```
public class ParagraphAlignment
```

Указывает выравнивание текста в абзаце.

 **Examples:** 

Показывает, как вручную создать документ Aspose.Words.

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
## Поля

| Поле | Описание |
| --- | --- |
| [ARABIC_HIGH_KASHIDA](#ARABIC-HIGH-KASHIDA) | Только арабский. |
| [ARABIC_LOW_KASHIDA](#ARABIC-LOW-KASHIDA) | Только арабский. |
| [ARABIC_MEDIUM_KASHIDA](#ARABIC-MEDIUM-KASHIDA) | Только арабский. |
| [CENTER](#CENTER) | Текст выровнен по центру по горизонтали. |
| [DISTRIBUTED](#DISTRIBUTED) | Текст распределён равномерно. |
| [JUSTIFY](#JUSTIFY) | Текст выровнен по левому и правому краю. |
| [LEFT](#LEFT) | Текст выровнен по левому краю. |
| [MATH_ELEMENT_CENTER_AS_GROUP](#MATH-ELEMENT-CENTER-AS-GROUP) | Единственный элемент Math в строке, выровнен как 'Centered As Group'. |
| [RIGHT](#RIGHT) | Текст выровнен по правому краю. |
| [THAI_DISTRIBUTED](#THAI-DISTRIBUTED) | Только тайский. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String paragraphAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int paragraphAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int paragraphAlignment)](#toString-int) |  |
### ARABIC_HIGH_KASHIDA {#ARABIC-HIGH-KASHIDA}
```
public static int ARABIC_HIGH_KASHIDA
```


Только арабский. Длина кашиды для текста расширена до максимально возможной длины.

### ARABIC_LOW_KASHIDA {#ARABIC-LOW-KASHIDA}
```
public static int ARABIC_LOW_KASHIDA
```


Только арабский. Длина кашиды для текста расширена до слегка большей длины.

### ARABIC_MEDIUM_KASHIDA {#ARABIC-MEDIUM-KASHIDA}
```
public static int ARABIC_MEDIUM_KASHIDA
```


Только арабский. Длина кашиды для текста расширена до средней длины, определяемой потребителем.

### CENTER {#CENTER}
```
public static int CENTER
```


Текст выровнен по центру по горизонтали.

### DISTRIBUTED {#DISTRIBUTED}
```
public static int DISTRIBUTED
```


Текст распределён равномерно.

### JUSTIFY {#JUSTIFY}
```
public static int JUSTIFY
```


Текст выровнен по левому и правому краю.

### LEFT {#LEFT}
```
public static int LEFT
```


Текст выровнен по левому краю.

### MATH_ELEMENT_CENTER_AS_GROUP {#MATH-ELEMENT-CENTER-AS-GROUP}
```
public static int MATH_ELEMENT_CENTER_AS_GROUP
```


Единственный элемент Math в строке, выровнен как 'Centered As Group'.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Текст выровнен по правому краю.

### THAI_DISTRIBUTED {#THAI-DISTRIBUTED}
```
public static int THAI_DISTRIBUTED
```


Только тайский. Текст выровнен по ширине с оптимизацией для тайского.

### length {#length}
```
public static int length
```


### fromName(String paragraphAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String paragraphAlignmentName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| paragraphAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int paragraphAlignment) {#getName-int}
```
public static String getName(int paragraphAlignment)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| paragraphAlignment | int |  |

**Returns:**
java.lang.String
