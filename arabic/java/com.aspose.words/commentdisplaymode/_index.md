---
title: "CommentDisplayMode"
linktitle: "CommentDisplayMode"
second_title: "Aspose.Words لـ Java"
description: "يحدد وضع العرض لتعليقات المستند في Java."
type: docs
weight: 110
url: /ar/java/com.aspose.words/commentdisplaymode/
---

**Inheritance:**
java.lang.Object
```
public class CommentDisplayMode
```

يحدد وضع العرض لتعليقات المستند.

 **Examples:** 

يوضح كيفية إظهار التعليقات عند حفظ المستند إلى تنسيق مُعرض.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [HIDE](#HIDE) | لا يتم عرض أي تعليقات على المستند. |
| [SHOW_IN_ANNOTATIONS](#SHOW-IN-ANNOTATIONS) | يعرض تعليقات المستند كتعليقات توضيحية. |
| [SHOW_IN_BALLOONS](#SHOW-IN-BALLOONS) | يعرض تعليقات المستند في فقاعات بالهوامش. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String commentDisplayModeName)](#fromName-java.lang.String) |  |
| [getName(int commentDisplayMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int commentDisplayMode)](#toString-int) |  |
### HIDE {#HIDE}
```
public static int HIDE
```


لا يتم عرض أي تعليقات على المستند.

### SHOW_IN_ANNOTATIONS {#SHOW-IN-ANNOTATIONS}
```
public static int SHOW_IN_ANNOTATIONS
```


يعرض تعليقات المستند كتعليقات توضيحية. هذا متاح فقط لتنسيق Pdf.

### SHOW_IN_BALLOONS {#SHOW-IN-BALLOONS}
```
public static int SHOW_IN_BALLOONS
```


يعرض تعليقات المستند في فقاعات بالهوامش. هذه هي القيمة الافتراضية.

### length {#length}
```
public static int length
```


### fromName(String commentDisplayModeName) {#fromName-java.lang.String}
```
public static int fromName(String commentDisplayModeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| commentDisplayModeName | java.lang.String |  |

**Returns:**
int
### getName(int commentDisplayMode) {#getName-int}
```
public static String getName(int commentDisplayMode)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| commentDisplayMode | int |  |

**Returns:**
java.lang.String
