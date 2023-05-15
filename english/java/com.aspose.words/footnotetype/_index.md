---
title: FootnoteType
linktitle: FootnoteType
second_title: Aspose.Words for Java
description: Specifies whether this is a footnote or an endnote in Java.
type: docs
weight: 307
url: /java/com.aspose.words/footnotetype/
---

**Inheritance:**
java.lang.Object
```
public class FootnoteType
```

Specifies whether this is a footnote or an endnote.

 **Remarks:** 

Both footnotes and endnotes are represented by objects by the [FOOTNOTE](../../com.aspose.words/footnotetype/\#FOOTNOTE) class. Use [Footnote.getFootnoteType()](../../com.aspose.words/footnote/\#getFootnoteType) to distinguish between footnotes and endnotes.

 **Examples:** 

Shows how to reference text with a footnote and an endnote.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert some text and mark it with a footnote with the IsAuto property set to "true" by default,
 // so the marker seen in the body text will be auto-numbered at "1",
 // and the footnote will appear at the bottom of the page.
 builder.write("This text will be referenced by a footnote.");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote comment regarding referenced text.");

 // Insert more text and mark it with an endnote with a custom reference mark,
 // which will be used in place of the number "2" and set "IsAuto" to false.
 builder.write("This text will be referenced by an endnote.");
 builder.insertFootnote(FootnoteType.ENDNOTE, "Endnote comment regarding referenced text.", "CustomMark");

 // Footnotes always appear at the bottom of their referenced text,
 // so this page break will not affect the footnote.
 // On the other hand, endnotes are always at the end of the document
 // so that this page break will push the endnote down to the next page.
 builder.insertBreak(BreakType.PAGE_BREAK);

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertFootnote.docx");
 
```

Shows how to insert and customize footnotes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add text, and reference it with a footnote. This footnote will place a small superscript reference
 // mark after the text that it references and create an entry below the main body text at the bottom of the page.
 // This entry will contain the footnote's reference mark and the reference text,
 // which we will pass to the document builder's "InsertFootnote" method.
 builder.write("Main body text.");
 Footnote footnote = builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote text.");

 // If this property is set to "true", then our footnote's reference mark
 // will be its index among all the section's footnotes.
 // This is the first footnote, so the reference mark will be "1".
 Assert.assertTrue(footnote.isAuto());

 // We can move the document builder inside the footnote to edit its reference text.
 builder.moveTo(footnote.getFirstParagraph());
 builder.write(" More text added by a DocumentBuilder.");
 builder.moveToDocumentEnd();

 Assert.assertEquals(footnote.getParagraphs().get(0).toString(SaveFormat.TEXT).trim(), "Footnote text. More text added by a DocumentBuilder.");

 builder.write(" More main body text.");
 footnote = builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote text.");

 // We can set a custom reference mark which the footnote will use instead of its index number.
 footnote.setReferenceMark("RefMark");

 Assert.assertFalse(footnote.isAuto());

 // A bookmark with the "IsAuto" flag set to true will still show its real index
 // even if previous bookmarks display custom reference marks, so this bookmark's reference mark will be a "3".
 builder.write(" More main body text.");
 footnote = builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote text.");

 Assert.assertTrue(footnote.isAuto());

 doc.save(getArtifactsDir() + "InlineStory.AddFootnote.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [ENDNOTE](#ENDNOTE) | The object is an endnote. |
| [FOOTNOTE](#FOOTNOTE) | The object is a footnote. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String footnoteTypeName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int footnoteType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int footnoteType)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### ENDNOTE {#ENDNOTE}
```
public static int ENDNOTE
```


The object is an endnote.

### FOOTNOTE {#FOOTNOTE}
```
public static int FOOTNOTE
```


The object is a footnote.

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
### fromName(String footnoteTypeName) {#fromName-java.lang.String}
```
public static int fromName(String footnoteTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| footnoteTypeName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int footnoteType) {#getName-int}
```
public static String getName(int footnoteType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| footnoteType | int |  |

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
### toString(int footnoteType) {#toString-int}
```
public static String toString(int footnoteType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| footnoteType | int |  |

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

