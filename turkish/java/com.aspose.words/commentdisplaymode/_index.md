---
title: "CommentDisplayMode"
linktitle: "CommentDisplayMode"
second_title: "Aspose.Words Java için"
description: "Java'da belge yorumları için işleme modunu belirtir."
type: docs
weight: 110
url: /tr/java/com.aspose.words/commentdisplaymode/
---

**Inheritance:**
java.lang.Object
```
public class CommentDisplayMode
```

Belge yorumları için işleme modunu belirtir.

 **Examples:** 

Bir belgeyi işlenmiş bir formata kaydederken yorumların nasıl gösterileceğini gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [HIDE](#HIDE) | Belge yorumları işlenmez. |
| [SHOW_IN_ANNOTATIONS](#SHOW-IN-ANNOTATIONS) | Belge yorumlarını açıklamalarda işler. |
| [SHOW_IN_BALLOONS](#SHOW-IN-BALLOONS) | Belge yorumlarını kenardaki balonlarda işler. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String commentDisplayModeName)](#fromName-java.lang.String) |  |
| [getName(int commentDisplayMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int commentDisplayMode)](#toString-int) |  |
### HIDE {#HIDE}
```
public static int HIDE
```


Belge yorumları işlenmez.

### SHOW_IN_ANNOTATIONS {#SHOW-IN-ANNOTATIONS}
```
public static int SHOW_IN_ANNOTATIONS
```


Belge yorumlarını açıklamalarda işler. Bu yalnızca Pdf formatı için kullanılabilir.

### SHOW_IN_BALLOONS {#SHOW-IN-BALLOONS}
```
public static int SHOW_IN_BALLOONS
```


Belge yorumlarını kenardaki balonlarda işler. Bu varsayılan değerdir.

### length {#length}
```
public static int length
```


### fromName(String commentDisplayModeName) {#fromName-java.lang.String}
```
public static int fromName(String commentDisplayModeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| commentDisplayModeName | java.lang.String |  |

**Returns:**
int
### getName(int commentDisplayMode) {#getName-int}
```
public static String getName(int commentDisplayMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| commentDisplayMode | int |  |

**Returns:**
java.lang.String
