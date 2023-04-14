---
title: FootnoteNumberingRule
linktitle: FootnoteNumberingRule
second_title: Aspose.Words for Java API Reference
description: Determines when automatic footnote or endnote numbering restarts in Java.
type: docs
weight: 295
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
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String footnoteNumberingRuleName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int footnoteNumberingRule)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int footnoteNumberingRule)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
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


### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
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
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
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
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
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
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

