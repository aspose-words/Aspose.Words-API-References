---
title: ExportListLabels
linktitle: ExportListLabels
second_title: Aspose.Words for Java
description: Specifies how list labels are exported to HTML MHTML and EPUB in Java.
type: docs
weight: 191
url: /java/com.aspose.words/exportlistlabels/
---

**Inheritance:**
java.lang.Object
```
public class ExportListLabels
```

Specifies how list labels are exported to HTML, MHTML and EPUB.

 **Examples:** 

Shows how to configure list exporting to HTML.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 List list = doc.getLists().add(ListTemplate.NUMBER_DEFAULT);
 builder.getListFormat().setList(list);

 builder.writeln("Default numbered list item 1.");
 builder.writeln("Default numbered list item 2.");
 builder.getListFormat().listIndent();
 builder.writeln("Default numbered list item 3.");
 builder.getListFormat().removeNumbers();

 list = doc.getLists().add(ListTemplate.OUTLINE_HEADINGS_LEGAL);
 builder.getListFormat().setList(list);

 builder.writeln("Outline legal heading list item 1.");
 builder.writeln("Outline legal heading list item 2.");
 builder.getListFormat().listIndent();
 builder.writeln("Outline legal heading list item 3.");
 builder.getListFormat().listIndent();
 builder.writeln("Outline legal heading list item 4.");
 builder.getListFormat().listIndent();
 builder.writeln("Outline legal heading list item 5.");
 builder.getListFormat().removeNumbers();

 // When saving the document to HTML, we can pass a SaveOptions object
 // to decide which HTML elements the document will use to represent lists.
 // Setting the "ExportListLabels" property to "ExportListLabels.AsInlineText"
 // will create lists by formatting spans.
 // Setting the "ExportListLabels" property to "ExportListLabels.Auto" will use the  tag
 // to build lists in cases when using the  and  tags may cause loss of formatting.
 // Setting the "ExportListLabels" property to "ExportListLabels.ByHtmlTags"
 // will use  and  tags to build all lists.
 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setExportListLabels(exportListLabels);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.List.html", options);
 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlSaveOptions.List.html"), StandardCharsets.UTF_8);

 switch (exportListLabels) {
     case ExportListLabels.AS_INLINE_TEXT:
         Assert.assertTrue(outDocContents.contains(
                 " " +
                         "" +
                         "a." +
                         "       " +
                         "" +
                         "Default numbered list item 3." +
                         ""));

         Assert.assertTrue(outDocContents.contains(
                 " " +
                         "" +
                         "2.1.1.1" +
                         "       " +
                         "" +
                         "Outline legal heading list item 5." +
                         ""));
         break;
     case ExportListLabels.AUTO:
         Assert.assertTrue(outDocContents.contains(
                 " " +
                         " " +
                         "Default numbered list item 3." +
                         "" +
                         ""));

         break;
     case ExportListLabels.BY_HTML_TAGS:
         Assert.assertTrue(outDocContents.contains(
                 " " +
                         " " +
                         "Default numbered list item 3." +
                         "" +
                         ""));

         break;
 }
 
```
## Fields

| Field | Description |
| --- | --- |
| [AS_INLINE_TEXT](#AS-INLINE-TEXT) | Outputs all list labels as inline text. |
| [AUTO](#AUTO) | Outputs list labels in auto mode. |
| [BY_HTML_TAGS](#BY-HTML-TAGS) | Outputs all list labels as HTML native elements. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String exportListLabelsName)](#fromName-java.lang.String) |  |
| [getName(int exportListLabels)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int exportListLabels)](#toString-int) |  |
### AS_INLINE_TEXT {#AS-INLINE-TEXT}
```
public static int AS_INLINE_TEXT
```


Outputs all list labels as inline text.

 **Remarks:** 

HTML

tag is used for any list label representation.

### AUTO {#AUTO}
```
public static int AUTO
```


Outputs list labels in auto mode. Uses HTML native elements when possible.

 **Remarks:** 

HTML

 *  tags are used for list label representation if it doesn't cause formatting loss, otherwise the HTML
    
    tag is used.

### BY_HTML_TAGS {#BY-HTML-TAGS}
```
public static int BY_HTML_TAGS
```


Outputs all list labels as HTML native elements.

 **Remarks:** 

HTML

 *  tags are used for list label representation. Some formatting loss is possible.

### length {#length}
```
public static int length
```


### fromName(String exportListLabelsName) {#fromName-java.lang.String}
```
public static int fromName(String exportListLabelsName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| exportListLabelsName | java.lang.String |  |

**Returns:**
int
### getName(int exportListLabels) {#getName-int}
```
public static String getName(int exportListLabels)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| exportListLabels | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int exportListLabels) {#toString-int}
```
public static String toString(int exportListLabels)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| exportListLabels | int |  |

**Returns:**
java.lang.String
