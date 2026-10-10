---
title: "TextBoxWrapMode"
linktitle: "TextBoxWrapMode"
second_title: "Aspose.Words Java için"
description: "Java'da bir şekil içinde metnin nasıl sarılacağını belirtir."
type: docs
weight: 669
url: /tr/java/com.aspose.words/textboxwrapmode/
---

**Inheritance:**
java.lang.Object
```
public class TextBoxWrapMode
```

Bir şekil içinde metnin nasıl sarıldığını belirtir.

 **Examples:** 

Bir metin kutusunun içeriği için sarma modunun nasıl ayarlanacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape textBoxShape = builder.insertShape(ShapeType.TEXT_BOX, 300.0, 300.0);
 TextBox textBox = textBoxShape.getTextBox();

 // Set the "TextBoxWrapMode" property to "TextBoxWrapMode.None" to increase the text box's width
 // to accommodate text, should it be large enough.
 // Set the "TextBoxWrapMode" property to "TextBoxWrapMode.Square" to
 // wrap all text inside the text box, preserving its dimensions.
 textBox.setTextBoxWrapMode(textBoxWrapMode);

 builder.moveTo(textBoxShape.getLastParagraph());
 builder.getFont().setSize(32.0);
 builder.write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 doc.save(getArtifactsDir() + "Shape.TextBoxContentsWrapMode.docx");
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [NONE](#NONE) | Metin bir şekil içinde sarılmaz. |
| [SQUARE](#SQUARE) | Metin bir şekil içinde sarılır. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String textBoxWrapModeName)](#fromName-java.lang.String) |  |
| [getName(int textBoxWrapMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int textBoxWrapMode)](#toString-int) |  |
### NONE {#NONE}
```
public static int NONE
```


Metin bir şekil içinde sarılmaz.

### SQUARE {#SQUARE}
```
public static int SQUARE
```


Metin bir şekil içinde sarılır.

### length {#length}
```
public static int length
```


### fromName(String textBoxWrapModeName) {#fromName-java.lang.String}
```
public static int fromName(String textBoxWrapModeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| textBoxWrapModeName | java.lang.String |  |

**Returns:**
int
### getName(int textBoxWrapMode) {#getName-int}
```
public static String getName(int textBoxWrapMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| textBoxWrapMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int textBoxWrapMode) {#toString-int}
```
public static String toString(int textBoxWrapMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| textBoxWrapMode | int |  |

**Returns:**
java.lang.String
