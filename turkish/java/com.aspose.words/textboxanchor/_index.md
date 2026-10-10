---
title: "TextBoxAnchor"
linktitle: "TextBoxAnchor"
second_title: "Aspose.Words Java için"
description: "Java'da şekil metni dikey hizalama için kullanılan değerleri belirtir."
type: docs
weight: 667
url: /tr/java/com.aspose.words/textboxanchor/
---

**Inheritance:**
java.lang.Object
```
public class TextBoxAnchor
```

Şekil metni dikey hizalama için kullanılan değerleri belirtir.

 **Examples:** 

Bir metin kutusunun metin içeriğini dikey olarak nasıl hizalayacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.TEXT_BOX, 200.0, 200.0);

 // Set the "VerticalAnchor" property to "TextBoxAnchor.Top" to
 // align the text in this text box with the top side of the shape.
 // Set the "VerticalAnchor" property to "TextBoxAnchor.Middle" to
 // align the text in this text box to the center of the shape.
 // Set the "VerticalAnchor" property to "TextBoxAnchor.Bottom" to
 // align the text in this text box to the bottom of the shape.
 shape.getTextBox().setVerticalAnchor(verticalAnchor);

 builder.moveTo(shape.getFirstParagraph());
 builder.write("Hello world!");

 // The vertical aligning of text inside text boxes is available from Microsoft Word 2007 onwards.
 doc.getCompatibilityOptions().optimizeFor(MsWordVersion.WORD_2007);
 doc.save(getArtifactsDir() + "Shape.VerticalAnchor.docx");
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [BOTTOM](#BOTTOM) | Metin, metin kutusunun altına hizalanır. |
| [BOTTOM_BASELINE](#BOTTOM-BASELINE) | Metin, metin kutusunun alt temel çizgisine hizalanır. |
| [BOTTOM_CENTERED](#BOTTOM-CENTERED) | Metin, metin kutusunun alt ortasına hizalanır. |
| [BOTTOM_CENTERED_BASELINE](#BOTTOM-CENTERED-BASELINE) | Metin, metin kutusunun alt ortadaki temel çizgisine hizalanır. |
| [MIDDLE](#MIDDLE) | Metin, metin kutusunun ortasına hizalanır. |
| [MIDDLE_CENTERED](#MIDDLE-CENTERED) | Metin, metin kutusunun ortasında ortalanmış şekilde hizalanır. |
| [TOP](#TOP) | Metin, metin kutusunun üstüne hizalanır. |
| [TOP_BASELINE](#TOP-BASELINE) | Metin, metin kutusunun üst temel çizgisine hizalanır. |
| [TOP_CENTERED](#TOP-CENTERED) | Metin, metin kutusunun üst ortasına hizalanır. |
| [TOP_CENTERED_BASELINE](#TOP-CENTERED-BASELINE) | Metin, metin kutusunun üst ortadaki temel çizgisine hizalanır. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String textBoxAnchorName)](#fromName-java.lang.String) |  |
| [getName(int textBoxAnchor)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textBoxAnchor)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Metin, metin kutusunun altına hizalanır.

### BOTTOM_BASELINE {#BOTTOM-BASELINE}
```
public static int BOTTOM_BASELINE
```


Metin, metin kutusunun alt temel çizgisine hizalanır.

### BOTTOM_CENTERED {#BOTTOM-CENTERED}
```
public static int BOTTOM_CENTERED
```


Metin, metin kutusunun alt ortasına hizalanır.

### BOTTOM_CENTERED_BASELINE {#BOTTOM-CENTERED-BASELINE}
```
public static int BOTTOM_CENTERED_BASELINE
```


Metin, metin kutusunun alt ortadaki temel çizgisine hizalanır.

### MIDDLE {#MIDDLE}
```
public static int MIDDLE
```


Metin, metin kutusunun ortasına hizalanır.

### MIDDLE_CENTERED {#MIDDLE-CENTERED}
```
public static int MIDDLE_CENTERED
```


Metin, metin kutusunun ortasında ortalanmış şekilde hizalanır.

### TOP {#TOP}
```
public static int TOP
```


Metin, metin kutusunun üstüne hizalanır.

### TOP_BASELINE {#TOP-BASELINE}
```
public static int TOP_BASELINE
```


Metin, metin kutusunun üst temel çizgisine hizalanır.

### TOP_CENTERED {#TOP-CENTERED}
```
public static int TOP_CENTERED
```


Metin, metin kutusunun üst ortasına hizalanır.

### TOP_CENTERED_BASELINE {#TOP-CENTERED-BASELINE}
```
public static int TOP_CENTERED_BASELINE
```


Metin, metin kutusunun üst ortadaki temel çizgisine hizalanır.

### length {#length}
```
public static int length
```


### fromName(String textBoxAnchorName) {#fromName-java.lang.String}
```
public static int fromName(String textBoxAnchorName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| textBoxAnchorName | java.lang.String |  |

**Returns:**
int
### getName(int textBoxAnchor) {#getName-int}
```
public static String getName(int textBoxAnchor)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| textBoxAnchor | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int textBoxAnchor) {#toString-int}
```
public static String toString(int textBoxAnchor)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| textBoxAnchor | int |  |

**Returns:**
java.lang.String
