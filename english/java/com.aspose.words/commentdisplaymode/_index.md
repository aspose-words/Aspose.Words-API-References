---
title: CommentDisplayMode
linktitle: CommentDisplayMode
second_title: Aspose.Words for Java
description: Specifies the rendering mode for document comments in Java.
type: docs
weight: 107
url: /java/com.aspose.words/commentdisplaymode/
---

**Inheritance:**
java.lang.Object
```
public class CommentDisplayMode
```

Specifies the rendering mode for document comments.

 **Examples:** 

Shows how to show comments when saving a document to a rendered format.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.write("Hello world!");

 Comment comment = new Comment(doc, "John Doe", "J.D.", new Date());
 comment.setText("My comment.");
 builder.getCurrentParagraph().appendChild(comment);

 // ShowInAnnotations is only available in Pdf1.7 and Pdf1.5 formats.
 // In other formats, it will work similarly to Hide.
 doc.getLayoutOptions().setCommentDisplayMode(CommentDisplayMode.SHOW_IN_ANNOTATIONS);

 doc.save(getArtifactsDir() + "Document.ShowCommentsInAnnotations.pdf");

 // Note that it's required to rebuild the document page layout (via Document.UpdatePageLayout() method)
 // after changing the Document.LayoutOptions values.
 doc.getLayoutOptions().setCommentDisplayMode(CommentDisplayMode.SHOW_IN_BALLOONS);
 doc.updatePageLayout();

 doc.save(getArtifactsDir() + "Document.ShowCommentsInBalloons.pdf");
 
```
## Fields

| Field | Description |
| --- | --- |
| [HIDE](#HIDE) | No document comments are rendered. |
| [SHOW_IN_ANNOTATIONS](#SHOW-IN-ANNOTATIONS) | Renders document comments in annotations. |
| [SHOW_IN_BALLOONS](#SHOW-IN-BALLOONS) | Renders document comments in balloons in the margin. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String commentDisplayModeName)](#fromName-java.lang.String) |  |
| [getName(int commentDisplayMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int commentDisplayMode)](#toString-int) |  |
### HIDE {#HIDE}
```
public static int HIDE
```


No document comments are rendered.

### SHOW_IN_ANNOTATIONS {#SHOW-IN-ANNOTATIONS}
```
public static int SHOW_IN_ANNOTATIONS
```


Renders document comments in annotations. This is only available for Pdf format.

### SHOW_IN_BALLOONS {#SHOW-IN-BALLOONS}
```
public static int SHOW_IN_BALLOONS
```


Renders document comments in balloons in the margin. This is the default value.

### length {#length}
```
public static int length
```


### fromName(String commentDisplayModeName) {#fromName-java.lang.String}
```
public static int fromName(String commentDisplayModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| commentDisplayModeName | java.lang.String |  |

**Returns:**
int
### getName(int commentDisplayMode) {#getName-int}
```
public static String getName(int commentDisplayMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| commentDisplayMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int commentDisplayMode) {#toString-int}
```
public static String toString(int commentDisplayMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| commentDisplayMode | int |  |

**Returns:**
java.lang.String
