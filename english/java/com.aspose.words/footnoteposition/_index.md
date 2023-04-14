---
title: FootnotePosition
linktitle: FootnotePosition
second_title: Aspose.Words for Java API Reference
description: Defines the footnote position in Java.
type: docs
weight: 297
url: /java/com.aspose.words/footnoteposition/
---

**Inheritance:**
java.lang.Object
```
public class FootnotePosition
```

Defines the footnote position.

 **Examples:** 

Shows how to select a different place where the document collects and displays its footnotes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A footnote is a way to attach a reference or a side comment to text
 // that does not interfere with the main body text's flow.
 // Inserting a footnote adds a small superscript reference symbol
 // at the main body text where we insert the footnote.
 // Each footnote also creates an entry at the bottom of the page, consisting of a symbol
 // that matches the reference symbol in the main body text.
 // The reference text that we pass to the document builder's "InsertFootnote" method.
 builder.write("Hello world!");
 builder.insertFootnote(FootnoteType.FOOTNOTE, "Footnote contents.");

 // We can use the "Position" property to determine where the document will place all its footnotes.
 // If we set the value of the "Position" property to "FootnotePosition.BottomOfPage",
 // every footnote will show up at the bottom of the page that contains its reference mark. This is the default value.
 // If we set the value of the "Position" property to "FootnotePosition.BeneathText",
 // every footnote will show up at the end of the page's text that contains its reference mark.
 doc.getFootnoteOptions().setPosition(footnotePosition);

 doc.save(getArtifactsDir() + "InlineStory.PositionFootnote.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [BENEATH_TEXT](#BENEATH-TEXT) | Footnotes are output beneath text on each page. |
| [BOTTOM_OF_PAGE](#BOTTOM-OF-PAGE) | Footnotes are output at the bottom of each page. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String footnotePositionName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int footnotePosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int footnotePosition)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### BENEATH_TEXT {#BENEATH-TEXT}
```
public static int BENEATH_TEXT
```


Footnotes are output beneath text on each page.

### BOTTOM_OF_PAGE {#BOTTOM-OF-PAGE}
```
public static int BOTTOM_OF_PAGE
```


Footnotes are output at the bottom of each page.

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
### fromName(String footnotePositionName) {#fromName-java.lang.String}
```
public static int fromName(String footnotePositionName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| footnotePositionName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int footnotePosition) {#getName-int}
```
public static String getName(int footnotePosition)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| footnotePosition | int |  |

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
### toString(int footnotePosition) {#toString-int}
```
public static String toString(int footnotePosition)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| footnotePosition | int |  |

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

