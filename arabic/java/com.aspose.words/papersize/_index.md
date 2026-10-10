---
title: "PaperSize"
linktitle: "PaperSize"
second_title: "Aspose.Words لـ Java"
description: "يحدد حجم الورق في Java."
type: docs
weight: 521
url: /ar/java/com.aspose.words/papersize/
---

**Inheritance:**
java.lang.Object
```
public class PaperSize
```

يحدد حجم الورق.

 **Examples:** 

يوضح كيفية ضبط حجم الورق، الاتجاه، الهوامش، إلى جانب إعدادات أخرى لقسم.

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

يظهر كيفية تعيين أحجام الصفحات.

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
| [A3](#A3) | 297 x 420 مم. |
| [A4](#A4) | 210 x 297 مم. |
| [A5](#A5) | 148 x 210 مم. |
| [B4](#B4) | 250 x 353 مم. |
| [B5](#B5) | 176 x 250 مم. |
| [CUSTOM](#CUSTOM) | حجم ورق مخصص. |
| [ENVELOPE_DL](#ENVELOPE-DL) | 110 x 220 مم. |
| [EXECUTIVE](#EXECUTIVE) | 7.25 x 10.5 بوصة. |
| [FOLIO](#FOLIO) | 8.5 x 13 بوصة. |
| [JIS_B_4](#JIS-B-4) | 257 x 364 مم. |
| [JIS_B_5](#JIS-B-5) | 182 x 257 مم. |
| [LEDGER](#LEDGER) | 17 x 11 بوصة. |
| [LEGAL](#LEGAL) | 8.5 x 14 بوصة. |
| [LETTER](#LETTER) | 8.5 x 11 بوصة. |
| [NUMBER_10_ENVELOPE](#NUMBER-10-ENVELOPE) | 4.125 x 9.5 بوصة. |
| [PAPER_10_X_14](#PAPER-10-X-14) | 10 x 14 بوصة. |
| [PAPER_11_X_17](#PAPER-11-X-17) | 11 x 17 بوصة. |
| [QUARTO](#QUARTO) | 8.47 x 10.83 بوصة. |
| [STATEMENT](#STATEMENT) | 8.5 x 5.5 بوصة. |
| [TABLOID](#TABLOID) | 11 x 17 بوصة. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String paperSizeName)](#fromName-java.lang.String) |  |
| [getName(int paperSize)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int paperSize)](#toString-int) |  |
### A3 {#A3}
```
public static int A3
```


297 x 420 مم.

### A4 {#A4}
```
public static int A4
```


210 x 297 مم.

### A5 {#A5}
```
public static int A5
```


148 x 210 مم.

### B4 {#B4}
```
public static int B4
```


250 x 353 مم.

### B5 {#B5}
```
public static int B5
```


176 x 250 مم.

### CUSTOM {#CUSTOM}
```
public static int CUSTOM
```


حجم ورق مخصص.

### ENVELOPE_DL {#ENVELOPE-DL}
```
public static int ENVELOPE_DL
```


110 x 220 مم.

### EXECUTIVE {#EXECUTIVE}
```
public static int EXECUTIVE
```


7.25 x 10.5 بوصة.

### FOLIO {#FOLIO}
```
public static int FOLIO
```


8.5 x 13 بوصة.

### JIS_B_4 {#JIS-B-4}
```
public static int JIS_B_4
```


257 x 364 مم.

### JIS_B_5 {#JIS-B-5}
```
public static int JIS_B_5
```


182 x 257 مم.

### LEDGER {#LEDGER}
```
public static int LEDGER
```


17 x 11 بوصة.

### LEGAL {#LEGAL}
```
public static int LEGAL
```


8.5 x 14 بوصة.

### LETTER {#LETTER}
```
public static int LETTER
```


8.5 x 11 بوصة.

### NUMBER_10_ENVELOPE {#NUMBER-10-ENVELOPE}
```
public static int NUMBER_10_ENVELOPE
```


4.125 x 9.5 بوصة.

### PAPER_10_X_14 {#PAPER-10-X-14}
```
public static int PAPER_10_X_14
```


10 x 14 بوصة.

### PAPER_11_X_17 {#PAPER-11-X-17}
```
public static int PAPER_11_X_17
```


11 x 17 بوصة.

### QUARTO {#QUARTO}
```
public static int QUARTO
```


8.47 x 10.83 بوصة.

### STATEMENT {#STATEMENT}
```
public static int STATEMENT
```


8.5 x 5.5 بوصة.

### TABLOID {#TABLOID}
```
public static int TABLOID
```


11 x 17 بوصة.

### length {#length}
```
public static int length
```


### fromName(String paperSizeName) {#fromName-java.lang.String}
```
public static int fromName(String paperSizeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| paperSizeName | java.lang.String |  |

**Returns:**
int
### getName(int paperSize) {#getName-int}
```
public static String getName(int paperSize)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| paperSize | int |  |

**Returns:**
java.lang.String
