---
title: "ParagraphAlignment"
linktitle: "ParagraphAlignment"
second_title: "Aspose.Words لـ Java"
description: "يحدد محاذاة النص في الفقرة في جافا."
type: docs
weight: 523
url: /ar/java/com.aspose.words/paragraphalignment/
---

**Inheritance:**
java.lang.Object
```
public class ParagraphAlignment
```

يحدد محاذاة النص في الفقرة.

 **Examples:** 

يوضح كيفية إنشاء مستند Aspose.Words يدوياً.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [ARABIC_HIGH_KASHIDA](#ARABIC-HIGH-KASHIDA) | العربية فقط. |
| [ARABIC_LOW_KASHIDA](#ARABIC-LOW-KASHIDA) | العربية فقط. |
| [ARABIC_MEDIUM_KASHIDA](#ARABIC-MEDIUM-KASHIDA) | العربية فقط. |
| [CENTER](#CENTER) | النص مُوسَّط أفقياً. |
| [DISTRIBUTED](#DISTRIBUTED) | النص موزع بالتساوي. |
| [JUSTIFY](#JUSTIFY) | النص مُحاذى إلى اليمين واليسار. |
| [LEFT](#LEFT) | النص محاذى إلى اليسار. |
| [MATH_ELEMENT_CENTER_AS_GROUP](#MATH-ELEMENT-CENTER-AS-GROUP) | العنصر الرياضي الوحيد في سطر، محاذى كـ 'مركّز كمجموعة'. |
| [RIGHT](#RIGHT) | النص محاذى إلى اليمين. |
| [THAI_DISTRIBUTED](#THAI-DISTRIBUTED) | تايلاندية فقط. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String paragraphAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int paragraphAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int paragraphAlignment)](#toString-int) |  |
### ARABIC_HIGH_KASHIDA {#ARABIC-HIGH-KASHIDA}
```
public static int ARABIC_HIGH_KASHIDA
```


العربية فقط. يتم تمديد طول الكاشدة للنص إلى أقصى طول ممكن.

### ARABIC_LOW_KASHIDA {#ARABIC-LOW-KASHIDA}
```
public static int ARABIC_LOW_KASHIDA
```


العربية فقط. يتم تمديد طول الكاشدة للنص إلى طول أطول قليلاً.

### ARABIC_MEDIUM_KASHIDA {#ARABIC-MEDIUM-KASHIDA}
```
public static int ARABIC_MEDIUM_KASHIDA
```


العربية فقط. يتم تمديد طول الكاشدة للنص إلى طول متوسط يحدده المستهلك.

### CENTER {#CENTER}
```
public static int CENTER
```


النص مُوسَّط أفقياً.

### DISTRIBUTED {#DISTRIBUTED}
```
public static int DISTRIBUTED
```


النص موزع بالتساوي.

### JUSTIFY {#JUSTIFY}
```
public static int JUSTIFY
```


النص مُحاذى إلى اليمين واليسار.

### LEFT {#LEFT}
```
public static int LEFT
```


النص محاذى إلى اليسار.

### MATH_ELEMENT_CENTER_AS_GROUP {#MATH-ELEMENT-CENTER-AS-GROUP}
```
public static int MATH_ELEMENT_CENTER_AS_GROUP
```


العنصر الرياضي الوحيد في سطر، محاذى كـ 'مركّز كمجموعة'.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


النص محاذى إلى اليمين.

### THAI_DISTRIBUTED {#THAI-DISTRIBUTED}
```
public static int THAI_DISTRIBUTED
```


تايلاندية فقط. النص مُضبط كمسطر مع تحسين للغة التايلاندية.

### length {#length}
```
public static int length
```


### fromName(String paragraphAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String paragraphAlignmentName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| paragraphAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int paragraphAlignment) {#getName-int}
```
public static String getName(int paragraphAlignment)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| paragraphAlignment | int |  |

**Returns:**
java.lang.String
