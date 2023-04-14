---
title: LineNumberRestartMode
linktitle: LineNumberRestartMode
second_title: Aspose.Words for Java API Reference
description: Determines when automatic line numbering restarts in Java.
type: docs
weight: 369
url: /java/com.aspose.words/linenumberrestartmode/
---

**Inheritance:**
java.lang.Object
```
public class LineNumberRestartMode
```

Determines when automatic line numbering restarts.

 **Examples:** 

Shows how to enable line numbering for a section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can use the section's PageSetup object to display numbers to the left of the section's text lines.
 // This is the same behavior as a List object,
 // but it covers the entire section and does not modify the text in any way.
 // Our section will restart the numbering on each new page from 1 and display the number,
 // if it is a multiple of 3, at 50pt to the left of the line.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setLineStartingNumber(1);
 pageSetup.setLineNumberCountBy(3);
 pageSetup.setLineNumberRestartMode(LineNumberRestartMode.RESTART_PAGE);
 pageSetup.setLineNumberDistanceFromText(50.0d);

 for (int i = 1; i <= 25; i++)
     builder.writeln(MessageFormat.format("Line {0}.", i));

 // The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
 // This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
 // The section's line counter will also ignore this line, treat the next line as the 15th,
 // and continue the count from that point onward.
 doc.getFirstSection().getBody().getParagraphs().get(14).getParagraphFormat().setSuppressLineNumbers(true);

 doc.save(getArtifactsDir() + "PageSetup.LineNumbers.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [CONTINUOUS](#CONTINUOUS) | Line numbering continuous from the previous section. |
| [RESTART_PAGE](#RESTART-PAGE) | Line numbering restarts at the start of every page. |
| [RESTART_SECTION](#RESTART-SECTION) | Line numbering restarts at the section start. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String lineNumberRestartModeName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int lineNumberRestartMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int lineNumberRestartMode)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### CONTINUOUS {#CONTINUOUS}
```
public static int CONTINUOUS
```


Line numbering continuous from the previous section.

### RESTART_PAGE {#RESTART-PAGE}
```
public static int RESTART_PAGE
```


Line numbering restarts at the start of every page.

### RESTART_SECTION {#RESTART-SECTION}
```
public static int RESTART_SECTION
```


Line numbering restarts at the section start.

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
### fromName(String lineNumberRestartModeName) {#fromName-java.lang.String}
```
public static int fromName(String lineNumberRestartModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| lineNumberRestartModeName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int lineNumberRestartMode) {#getName-int}
```
public static String getName(int lineNumberRestartMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| lineNumberRestartMode | int |  |

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
### toString(int lineNumberRestartMode) {#toString-int}
```
public static String toString(int lineNumberRestartMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| lineNumberRestartMode | int |  |

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

