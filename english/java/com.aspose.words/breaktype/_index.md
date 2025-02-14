---
title: BreakType
linktitle: BreakType
second_title: Aspose.Words for Java
description: Specifies type of a break inside a document in Java.
type: docs
weight: 49
url: /java/com.aspose.words/breaktype/
---

**Inheritance:**
java.lang.Object
```
public class BreakType
```

Specifies type of a break inside a document.

 **Examples:** 

Shows how to create headers and footers in a document using DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify that we want different headers and footers for first, even and odd pages.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(true);
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(true);

 // Create the headers, then add three pages to the document to display each header type.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.write("Header for the first page");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.write("Header for even pages");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Header for all other pages");

 builder.moveToSection(0);
 builder.writeln("Page1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page3");

 doc.save(getArtifactsDir() + "DocumentBuilder.HeadersAndFooters.docx");
 
```

Shows how to apply and revert page setup settings to sections in a document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```

Shows how to insert a Table of contents (TOC) into a document using heading styles as entries.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a table of contents for the first page of the document.
 // Configure the table to pick up paragraphs with headings of levels 1 to 3.
 // Also, set its entries to be hyperlinks that will take us
 // to the location of the heading when left-clicked in Microsoft Word.
 builder.insertTableOfContents("\\o \"1-3\" \\h \\z \\u");
 builder.insertBreak(BreakType.PAGE_BREAK);

 // Populate the table of contents by adding paragraphs with heading styles.
 // Each such heading with a level between 1 and 3 will create an entry in the table.
 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("Heading 1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 1.1");
 builder.writeln("Heading 1.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_1);
 builder.writeln("Heading 2");
 builder.writeln("Heading 3");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 3.1");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_3);
 builder.writeln("Heading 3.1.1");
 builder.writeln("Heading 3.1.2");
 builder.writeln("Heading 3.1.3");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_4);
 builder.writeln("Heading 3.1.3.1");
 builder.writeln("Heading 3.1.3.2");

 builder.getParagraphFormat().setStyleIdentifier(StyleIdentifier.HEADING_2);
 builder.writeln("Heading 3.2");
 builder.writeln("Heading 3.3");

 // A table of contents is a field of a type that needs to be updated to show an up-to-date result.
 doc.updateFields();
 doc.save(getArtifactsDir() + "DocumentBuilder.InsertToc.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [COLUMN_BREAK](#COLUMN-BREAK) | Explicit column break. |
| [LINE_BREAK](#LINE-BREAK) | Explicit line break. |
| [PAGE_BREAK](#PAGE-BREAK) | Explicit page break. |
| [PARAGRAPH_BREAK](#PARAGRAPH-BREAK) | Break between paragraphs. |
| [SECTION_BREAK_CONTINUOUS](#SECTION-BREAK-CONTINUOUS) | Specifies start of new section on the same page as the previous section. |
| [SECTION_BREAK_EVEN_PAGE](#SECTION-BREAK-EVEN-PAGE) | Specifies start of new section on a new even page. |
| [SECTION_BREAK_NEW_COLUMN](#SECTION-BREAK-NEW-COLUMN) | Specifies start of new section in the new column. |
| [SECTION_BREAK_NEW_PAGE](#SECTION-BREAK-NEW-PAGE) | Specifies start of new section on a new page. |
| [SECTION_BREAK_ODD_PAGE](#SECTION-BREAK-ODD-PAGE) | Specifies start of new section on a odd page. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String breakTypeName)](#fromName-java.lang.String) |  |
| [getName(int breakType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int breakType)](#toString-int) |  |
### COLUMN_BREAK {#COLUMN-BREAK}
```
public static int COLUMN_BREAK
```


Explicit column break.

### LINE_BREAK {#LINE-BREAK}
```
public static int LINE_BREAK
```


Explicit line break.

### PAGE_BREAK {#PAGE-BREAK}
```
public static int PAGE_BREAK
```


Explicit page break.

### PARAGRAPH_BREAK {#PARAGRAPH-BREAK}
```
public static int PARAGRAPH_BREAK
```


Break between paragraphs.

### SECTION_BREAK_CONTINUOUS {#SECTION-BREAK-CONTINUOUS}
```
public static int SECTION_BREAK_CONTINUOUS
```


Specifies start of new section on the same page as the previous section.

### SECTION_BREAK_EVEN_PAGE {#SECTION-BREAK-EVEN-PAGE}
```
public static int SECTION_BREAK_EVEN_PAGE
```


Specifies start of new section on a new even page.

### SECTION_BREAK_NEW_COLUMN {#SECTION-BREAK-NEW-COLUMN}
```
public static int SECTION_BREAK_NEW_COLUMN
```


Specifies start of new section in the new column.

### SECTION_BREAK_NEW_PAGE {#SECTION-BREAK-NEW-PAGE}
```
public static int SECTION_BREAK_NEW_PAGE
```


Specifies start of new section on a new page.

### SECTION_BREAK_ODD_PAGE {#SECTION-BREAK-ODD-PAGE}
```
public static int SECTION_BREAK_ODD_PAGE
```


Specifies start of new section on a odd page.

### length {#length}
```
public static int length
```


### fromName(String breakTypeName) {#fromName-java.lang.String}
```
public static int fromName(String breakTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| breakTypeName | java.lang.String |  |

**Returns:**
int
### getName(int breakType) {#getName-int}
```
public static String getName(int breakType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| breakType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int breakType) {#toString-int}
```
public static String toString(int breakType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| breakType | int |  |

**Returns:**
java.lang.String
