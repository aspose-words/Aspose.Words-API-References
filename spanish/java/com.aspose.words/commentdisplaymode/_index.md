---
title: "CommentDisplayMode"
linktitle: "CommentDisplayMode"
second_title: "Aspose.Words para Java"
description: "Especifica el modo de renderizado de los comentarios del documento en Java."
type: docs
weight: 110
url: /es/java/com.aspose.words/commentdisplaymode/
---

**Inheritance:**
java.lang.Object
```
public class CommentDisplayMode
```

Especifica el modo de renderizado para los comentarios del documento.

 **Examples:** 

Muestra cómo mostrar los comentarios al guardar un documento en un formato renderizado.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [HIDE](#HIDE) | No se renderizan los comentarios del documento. |
| [SHOW_IN_ANNOTATIONS](#SHOW-IN-ANNOTATIONS) | Renderiza los comentarios del documento en anotaciones. |
| [SHOW_IN_BALLOONS](#SHOW-IN-BALLOONS) | Renderiza los comentarios del documento en globos en el margen. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String commentDisplayModeName)](#fromName-java.lang.String) |  |
| [getName(int commentDisplayMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int commentDisplayMode)](#toString-int) |  |
### HIDE {#HIDE}
```
public static int HIDE
```


No se renderizan los comentarios del documento.

### SHOW_IN_ANNOTATIONS {#SHOW-IN-ANNOTATIONS}
```
public static int SHOW_IN_ANNOTATIONS
```


Renderiza los comentarios del documento en anotaciones. Esto solo está disponible para el formato Pdf.

### SHOW_IN_BALLOONS {#SHOW-IN-BALLOONS}
```
public static int SHOW_IN_BALLOONS
```


Renderiza los comentarios del documento en globos en el margen. Este es el valor predeterminado.

### length {#length}
```
public static int length
```


### fromName(String commentDisplayModeName) {#fromName-java.lang.String}
```
public static int fromName(String commentDisplayModeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| commentDisplayModeName | java.lang.String |  |

**Returns:**
int
### getName(int commentDisplayMode) {#getName-int}
```
public static String getName(int commentDisplayMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| commentDisplayMode | int |  |

**Returns:**
java.lang.String
