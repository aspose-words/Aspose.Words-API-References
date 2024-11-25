---
title: PaperSize
linktitle: PaperSize
second_title: Aspose.Words for Java
description: Specifies paper size in Java.
type: docs
weight: 496
url: /java/com.aspose.words/papersize/
---

**Inheritance:**
java.lang.Object
```
public class PaperSize
```

Specifies paper size.

 **Examples:** 

Shows how to adjust paper size, orientation, margins, along with other settings for a section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

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

Shows how to set page sizes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can change the current page's size to a pre-defined size
 // by using the "PaperSize" property of this section's PageSetup object.
 builder.getPageSetup().setPaperSize(PaperSize.TABLOID);

 Assert.assertEquals(792.0d, builder.getPageSetup().getPageWidth());
 Assert.assertEquals(1224.0d, builder.getPageSetup().getPageHeight());

 builder.writeln(MessageFormat.format("This page is {0}x{1}.", builder.getPageSetup().getPageWidth(), builder.getPageSetup().getPageHeight()));

 // Each section has its own PageSetup object. When we use a document builder to make a new section,
 // that section's PageSetup object inherits all the previous section's PageSetup object's values.
 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);

 Assert.assertEquals(PaperSize.TABLOID, builder.getPageSetup().getPaperSize());

 builder.getPageSetup().setPaperSize(PaperSize.A5);
 builder.writeln(MessageFormat.format("This page is {0}x{1}.", builder.getPageSetup().getPageWidth(), builder.getPageSetup().getPageHeight()));

 Assert.assertEquals(419.55d, builder.getPageSetup().getPageWidth());
 Assert.assertEquals(595.30d, builder.getPageSetup().getPageHeight());

 builder.insertBreak(BreakType.SECTION_BREAK_EVEN_PAGE);

 // Set a custom size for this section's pages.
 builder.getPageSetup().setPageWidth(620.0);
 builder.getPageSetup().setPageHeight(480.0);

 Assert.assertEquals(PaperSize.CUSTOM, builder.getPageSetup().getPaperSize());

 builder.writeln(MessageFormat.format("This page is {0}x{1}.", builder.getPageSetup().getPageWidth(), builder.getPageSetup().getPageHeight()));

 doc.save(getArtifactsDir() + "PageSetup.PaperSizes.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [A3](#A3) | 297 x 420 mm. |
| [A4](#A4) | 210 x 297 mm. |
| [A5](#A5) | 148 x 210 mm. |
| [B4](#B4) | 250 x 353 mm. |
| [B5](#B5) | 176 x 250 mm. |
| [CUSTOM](#CUSTOM) | Custom paper size. |
| [ENVELOPE_DL](#ENVELOPE-DL) | 110 x 220 mm. |
| [EXECUTIVE](#EXECUTIVE) | 7.25 x 10.5 inches. |
| [FOLIO](#FOLIO) | 8.5 x 13 inches. |
| [LEDGER](#LEDGER) | 17 x 11 inches. |
| [LEGAL](#LEGAL) | 8.5 x 14 inches. |
| [LETTER](#LETTER) | 8.5 x 11 inches. |
| [NUMBER_10_ENVELOPE](#NUMBER-10-ENVELOPE) | 4.125 x 9.5 inches. |
| [PAPER_10_X_14](#PAPER-10-X-14) | 10 x 14 inches. |
| [PAPER_11_X_17](#PAPER-11-X-17) | 11 x 17 inches. |
| [QUARTO](#QUARTO) | 8.47 x 10.83 inches. |
| [STATEMENT](#STATEMENT) | 8.5 x 5.5 inches. |
| [TABLOID](#TABLOID) | 11 x 17 inches. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String paperSizeName)](#fromName-java.lang.String) |  |
| [getName(int paperSize)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int paperSize)](#toString-int) |  |
### A3 {#A3}
```
public static int A3
```


297 x 420 mm.

### A4 {#A4}
```
public static int A4
```


210 x 297 mm.

### A5 {#A5}
```
public static int A5
```


148 x 210 mm.

### B4 {#B4}
```
public static int B4
```


250 x 353 mm.

### B5 {#B5}
```
public static int B5
```


176 x 250 mm.

### CUSTOM {#CUSTOM}
```
public static int CUSTOM
```


Custom paper size.

### ENVELOPE_DL {#ENVELOPE-DL}
```
public static int ENVELOPE_DL
```


110 x 220 mm.

### EXECUTIVE {#EXECUTIVE}
```
public static int EXECUTIVE
```


7.25 x 10.5 inches.

### FOLIO {#FOLIO}
```
public static int FOLIO
```


8.5 x 13 inches.

### LEDGER {#LEDGER}
```
public static int LEDGER
```


17 x 11 inches.

### LEGAL {#LEGAL}
```
public static int LEGAL
```


8.5 x 14 inches.

### LETTER {#LETTER}
```
public static int LETTER
```


8.5 x 11 inches.

### NUMBER_10_ENVELOPE {#NUMBER-10-ENVELOPE}
```
public static int NUMBER_10_ENVELOPE
```


4.125 x 9.5 inches.

### PAPER_10_X_14 {#PAPER-10-X-14}
```
public static int PAPER_10_X_14
```


10 x 14 inches.

### PAPER_11_X_17 {#PAPER-11-X-17}
```
public static int PAPER_11_X_17
```


11 x 17 inches.

### QUARTO {#QUARTO}
```
public static int QUARTO
```


8.47 x 10.83 inches.

### STATEMENT {#STATEMENT}
```
public static int STATEMENT
```


8.5 x 5.5 inches.

### TABLOID {#TABLOID}
```
public static int TABLOID
```


11 x 17 inches.

### length {#length}
```
public static int length
```


### fromName(String paperSizeName) {#fromName-java.lang.String}
```
public static int fromName(String paperSizeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| paperSizeName | java.lang.String |  |

**Returns:**
int
### getName(int paperSize) {#getName-int}
```
public static String getName(int paperSize)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| paperSize | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int paperSize) {#toString-int}
```
public static String toString(int paperSize)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| paperSize | int |  |

**Returns:**
java.lang.String
