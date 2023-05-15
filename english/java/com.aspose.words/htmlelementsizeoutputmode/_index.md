---
title: HtmlElementSizeOutputMode
linktitle: HtmlElementSizeOutputMode
second_title: Aspose.Words for Java
description: Specifies how Aspose.Words exports element widths and heights to HTML MHTML and EPUB in Java.
type: docs
weight: 336
url: /java/com.aspose.words/htmlelementsizeoutputmode/
---

**Inheritance:**
java.lang.Object
```
public class HtmlElementSizeOutputMode
```

Specifies how Aspose.Words exports element widths and heights to HTML, MHTML and EPUB.

 **Examples:** 

Shows how to preserve negative indents in the output .html.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a table with a negative indent, which will push it to the left past the left page boundary.
 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, Cell 1");
 builder.insertCell();
 builder.write("Row 1, Cell 2");
 builder.endTable();
 table.setLeftIndent(-36);
 table.setPreferredWidth(PreferredWidth.fromPoints(144.0));

 builder.insertBreak(BreakType.PARAGRAPH_BREAK);

 // Insert a table with a positive indent, which will push the table to the right.
 table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, Cell 1");
 builder.insertCell();
 builder.write("Row 1, Cell 2");
 builder.endTable();
 table.setLeftIndent(36.0);
 table.setPreferredWidth(PreferredWidth.fromPoints(144.0));

 // When we save a document to HTML, Aspose.Words will only preserve negative indents
 // such as the one we have applied to the first table if we set the "AllowNegativeIndent" flag
 // in a SaveOptions object that we will pass to "true".
 HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.HTML);
 {
     options.setAllowNegativeIndent(allowNegativeIndent);
     options.setTableWidthOutputMode(HtmlElementSizeOutputMode.RELATIVE_ONLY);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.NegativeIndent.html", options);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.NegativeIndent.html"), StandardCharsets.UTF_8);

 if (allowNegativeIndent) {
     Assert.assertTrue(outDocContents.contains(
             " "));
     Assert.assertTrue(outDocContents.contains(
             " "));
 } else {
     Assert.assertTrue(outDocContents.contains(
             " "));
     Assert.assertTrue(outDocContents.contains(
             " "));
 }
 
```
## Fields

| Field | Description |
| --- | --- |
| [ALL](#ALL) | All element sizes, both in absolute and relative units, specified in the document are exported. |
| [NONE](#NONE) | Element sizes are not exported. |
| [RELATIVE_ONLY](#RELATIVE-ONLY) | Element sizes are exported only if they are specified in relative units in the document. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String htmlElementSizeOutputModeName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int htmlElementSizeOutputMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int htmlElementSizeOutputMode)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### ALL {#ALL}
```
public static int ALL
```


All element sizes, both in absolute and relative units, specified in the document are exported.

### NONE {#NONE}
```
public static int NONE
```


Element sizes are not exported. Visual agents will build layout automatically according to relationship between elements.

### RELATIVE_ONLY {#RELATIVE-ONLY}
```
public static int RELATIVE_ONLY
```


Element sizes are exported only if they are specified in relative units in the document. Fixed sizes are not exported in this mode. Visual agents will calculate missing sizes to make document layout more natural.

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
### fromName(String htmlElementSizeOutputModeName) {#fromName-java.lang.String}
```
public static int fromName(String htmlElementSizeOutputModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| htmlElementSizeOutputModeName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int htmlElementSizeOutputMode) {#getName-int}
```
public static String getName(int htmlElementSizeOutputMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| htmlElementSizeOutputMode | int |  |

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
### toString(int htmlElementSizeOutputMode) {#toString-int}
```
public static String toString(int htmlElementSizeOutputMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| htmlElementSizeOutputMode | int |  |

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

