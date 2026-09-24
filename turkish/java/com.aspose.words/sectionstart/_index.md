---
title: "SectionStart"
linktitle: "SectionStart"
second_title: "Aspose.Words Java için"
description: "Java'da bölümün başındaki kesme türü."
type: docs
weight: 608
url: /tr/java/com.aspose.words/sectionstart/
---

**Inheritance:**
java.lang.Object
```
public class SectionStart
```

Bölümün başındaki kesme türü.

 **Examples:** 

Yeni bir bölümün önceki bölüme nasıl ayrıldığını belirtmenin nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("This text is in section 1.");

 // Section break types determine how a new section separates itself from the previous section.
 // Below are five types of section breaks.
 // 1 -  Starts the next section on a new page:
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.writeln("This text is in section 2.");

 Assert.assertEquals(SectionStart.NEW_PAGE, doc.getSections().get(1).getPageSetup().getSectionStart());

 // 2 -  Starts the next section on the current page:
 builder.insertBreak(BreakType.SECTION_BREAK_CONTINUOUS);
 builder.writeln("This text is in section 3.");

 Assert.assertEquals(SectionStart.CONTINUOUS, doc.getSections().get(2).getPageSetup().getSectionStart());

 // 3 -  Starts the next section on a new even page:
 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);
 builder.writeln("This text is in section 4.");

 Assert.assertEquals(SectionStart.EVEN_PAGE, doc.getSections().get(3).getPageSetup().getSectionStart());

 // 4 -  Starts the next section on a new odd page:
 builder.insertBreak(BreakType.SECTION_BREAK_ODD_PAGE);
 builder.writeln("This text is in section 5.");

 Assert.assertEquals(SectionStart.ODD_PAGE, doc.getSections().get(4).getPageSetup().getSectionStart());

 // 5 -  Starts the next section on a new column:
 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setCount(2);

 builder.insertBreak(BreakType.SECTION_BREAK_NEW_COLUMN);
 builder.writeln("This text is in section 6.");

 Assert.assertEquals(SectionStart.NEW_COLUMN, doc.getSections().get(5).getPageSetup().getSectionStart());

 doc.save(getArtifactsDir() + "PageSetup.SetSectionStart.docx");
 
```

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
| [CONTINUOUS](#CONTINUOUS) | Yeni bölüm, önceki bölümle aynı sayfada başlar. |
| [EVEN_PAGE](#EVEN-PAGE) | Bölüm yeni çift sayfada başlar. |
| [NEW_COLUMN](#NEW-COLUMN) | Bölüm yeni bir sütundan başlar. |
| [NEW_PAGE](#NEW-PAGE) | Bölüm yeni bir sayfadan başlar. |
| [ODD_PAGE](#ODD-PAGE) | Bölüm yeni tek sayfada başlar. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String sectionStartName)](#fromName-java.lang.String) |  |
| [getName(int sectionStart)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sectionStart)](#toString-int) |  |
### CONTINUOUS {#CONTINUOUS}
```
public static int CONTINUOUS
```


Yeni bölüm, önceki bölümle aynı sayfada başlar.

### EVEN_PAGE {#EVEN-PAGE}
```
public static int EVEN_PAGE
```


Bölüm yeni çift sayfada başlar.

### NEW_COLUMN {#NEW-COLUMN}
```
public static int NEW_COLUMN
```


Bölüm yeni bir sütundan başlar.

### NEW_PAGE {#NEW-PAGE}
```
public static int NEW_PAGE
```


Bölüm yeni bir sayfadan başlar.

### ODD_PAGE {#ODD-PAGE}
```
public static int ODD_PAGE
```


Bölüm yeni tek sayfada başlar.

### length {#length}
```
public static int length
```


### fromName(String sectionStartName) {#fromName-java.lang.String}
```
public static int fromName(String sectionStartName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sectionStartName | java.lang.String |  |

**Returns:**
int
### getName(int sectionStart) {#getName-int}
```
public static String getName(int sectionStart)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sectionStart | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int sectionStart) {#toString-int}
```
public static String toString(int sectionStart)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sectionStart | int |  |

**Returns:**
java.lang.String
