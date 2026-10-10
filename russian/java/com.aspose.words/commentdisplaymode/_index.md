---
title: "CommentDisplayMode"
linktitle: "CommentDisplayMode"
second_title: "Aspose.Words для Java"
description: "Указывает режим отображения комментариев к документу в Java."
type: docs
weight: 110
url: /ru/java/com.aspose.words/commentdisplaymode/
---

**Inheritance:**
java.lang.Object
```
public class CommentDisplayMode
```

Указывает режим отображения комментариев документа.

 **Examples:** 

Показывает, как отображать комментарии при сохранении документа в отрисованный формат.

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
## Поля

| Поле | Описание |
| --- | --- |
| [HIDE](#HIDE) | Комментарии к документу не отображаются. |
| [SHOW_IN_ANNOTATIONS](#SHOW-IN-ANNOTATIONS) | Отображает комментарии к документу в виде аннотаций. |
| [SHOW_IN_BALLOONS](#SHOW-IN-BALLOONS) | Отображает комментарии к документу в виде баллонов на полях. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String commentDisplayModeName)](#fromName-java.lang.String) |  |
| [getName(int commentDisplayMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int commentDisplayMode)](#toString-int) |  |
### HIDE {#HIDE}
```
public static int HIDE
```


Комментарии к документу не отображаются.

### SHOW_IN_ANNOTATIONS {#SHOW-IN-ANNOTATIONS}
```
public static int SHOW_IN_ANNOTATIONS
```


Отображает комментарии к документу в виде аннотаций. Это доступно только для формата Pdf.

### SHOW_IN_BALLOONS {#SHOW-IN-BALLOONS}
```
public static int SHOW_IN_BALLOONS
```


Отображает комментарии к документу в виде баллонов на полях. Это значение по умолчанию.

### length {#length}
```
public static int length
```


### fromName(String commentDisplayModeName) {#fromName-java.lang.String}
```
public static int fromName(String commentDisplayModeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| commentDisplayModeName | java.lang.String |  |

**Returns:**
int
### getName(int commentDisplayMode) {#getName-int}
```
public static String getName(int commentDisplayMode)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| commentDisplayMode | int |  |

**Returns:**
java.lang.String
