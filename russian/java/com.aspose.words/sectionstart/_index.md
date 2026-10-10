---
title: "SectionStart"
linktitle: "SectionStart"
second_title: "Aspose.Words для Java"
description: "Тип разрыва в начале раздела в Java."
type: docs
weight: 608
url: /ru/java/com.aspose.words/sectionstart/
---

**Inheritance:**
java.lang.Object
```
public class SectionStart
```

Тип разрыва в начале раздела.

 **Examples:** 

Показывает, как указать, как новый раздел отделяется от предыдущего.

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
| [CONTINUOUS](#CONTINUOUS) | Новый раздел начинается на той же странице, что и предыдущий раздел. |
| [EVEN_PAGE](#EVEN-PAGE) | Раздел начинается на новой чётной странице. |
| [NEW_COLUMN](#NEW-COLUMN) | Раздел начинается с новой колонки. |
| [NEW_PAGE](#NEW-PAGE) | Раздел начинается с новой страницы. |
| [ODD_PAGE](#ODD-PAGE) | Раздел начинается на новой нечётной странице. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String sectionStartName)](#fromName-java.lang.String) |  |
| [getName(int sectionStart)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int sectionStart)](#toString-int) |  |
### CONTINUOUS {#CONTINUOUS}
```
public static int CONTINUOUS
```


Новый раздел начинается на той же странице, что и предыдущий раздел.

### EVEN_PAGE {#EVEN-PAGE}
```
public static int EVEN_PAGE
```


Раздел начинается на новой чётной странице.

### NEW_COLUMN {#NEW-COLUMN}
```
public static int NEW_COLUMN
```


Раздел начинается с новой колонки.

### NEW_PAGE {#NEW-PAGE}
```
public static int NEW_PAGE
```


Раздел начинается с новой страницы.

### ODD_PAGE {#ODD-PAGE}
```
public static int ODD_PAGE
```


Раздел начинается на новой нечётной странице.

### length {#length}
```
public static int length
```


### fromName(String sectionStartName) {#fromName-java.lang.String}
```
public static int fromName(String sectionStartName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| sectionStartName | java.lang.String |  |

**Returns:**
int
### getName(int sectionStart) {#getName-int}
```
public static String getName(int sectionStart)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| sectionStart | int |  |

**Returns:**
java.lang.String
