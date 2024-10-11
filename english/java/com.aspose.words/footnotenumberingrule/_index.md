---
title: FootnoteNumberingRule
linktitle: FootnoteNumberingRule
second_title: Aspose.Words for Java
description: Determines when automatic footnote or endnote numbering restarts in Java.
type: docs
weight: 326
url: /java/com.aspose.words/footnotenumberingrule/
---

**Inheritance:**
java.lang.Object
```
public class FootnoteNumberingRule
```

Determines when automatic footnote or endnote numbering restarts.

 **Examples:** 

Shows how to restart footnote/endnote numbering at certain places in the document.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Footnotes and endnotes are a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting a footnote/endnote adds a small superscript reference symbol
 // at the main body text where we insert the footnote/endnote.
 // Each footnote/endnote also creates an entry, which consists of a symbol that matches the reference
 // symbol in the main body text. The reference text that we pass to the document builder's "InsertEndnote" method.
 // Footnote entries, by default, show up at the bottom of each page that contains
 // their reference symbols, and endnotes show up at the end of the document.
 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 2.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 3.");
 builder.write("Text 4. ");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote 4.");

 builder.insertBreak(BreakType.PAGE_BREAK);

 builder.write("Text 1. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 1.");
 builder.write("Text 2. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 2.");
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);
 builder.write("Text 3. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 3.");
 builder.write("Text 4. ");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote 4.");

 // By default, the reference symbol for each footnote and endnote is its index
 // among all the document's footnotes/endnotes. Each document maintains separate counts
 // for footnotes and endnotes and does not restart these counts at any point.
 Assert.assertEquals(doc.getFootnoteOptions().getRestartRule(), FootnoteNumberingRule.DEFAULT);
 Assert.assertEquals(FootnoteNumberingRule.DEFAULT, FootnoteNumberingRule.CONTINUOUS);

 // We can use the "RestartRule" property to get the document to restart
 // the footnote/endnote counts at a new page or section.
 doc.getFootnoteOptions().setRestartRule(FootnoteNumberingRule.RESTART_PAGE);
 doc.getEndnoteOptions().setRestartRule(FootnoteNumberingRule.RESTART_SECTION);

 doc.save(getArtifactsDir() + "InlineStory.NumberingRule.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [CONTINUOUS](#CONTINUOUS) | Numbering continuous throughout the document. |
| [DEFAULT](#DEFAULT) | Equals [CONTINUOUS](../../com.aspose.words/footnotenumberingrule/\#CONTINUOUS). |
| [RESTART_PAGE](#RESTART-PAGE) | Numbering restarts at each page. |
| [RESTART_SECTION](#RESTART-SECTION) | Numbering restarts at each section. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String footnoteNumberingRuleName)](#fromName-java.lang.String) |  |
| [getName(int footnoteNumberingRule)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int footnoteNumberingRule)](#toString-int) |  |
### CONTINUOUS {#CONTINUOUS}
```
public static int CONTINUOUS
```


Numbering continuous throughout the document.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Equals [CONTINUOUS](../../com.aspose.words/footnotenumberingrule/\#CONTINUOUS).

### RESTART_PAGE {#RESTART-PAGE}
```
public static int RESTART_PAGE
```


Numbering restarts at each page. Valid for footnotes only.

### RESTART_SECTION {#RESTART-SECTION}
```
public static int RESTART_SECTION
```


Numbering restarts at each section.

### length {#length}
```
public static int length
```


### fromName(String footnoteNumberingRuleName) {#fromName-java.lang.String}
```
public static int fromName(String footnoteNumberingRuleName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| footnoteNumberingRuleName | java.lang.String |  |

**Returns:**
int
### getName(int footnoteNumberingRule) {#getName-int}
```
public static String getName(int footnoteNumberingRule)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| footnoteNumberingRule | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int footnoteNumberingRule) {#toString-int}
```
public static String toString(int footnoteNumberingRule)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| footnoteNumberingRule | int |  |

**Returns:**
java.lang.String
