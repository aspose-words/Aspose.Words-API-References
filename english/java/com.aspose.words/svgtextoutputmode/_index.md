---
title: SvgTextOutputMode
linktitle: SvgTextOutputMode
second_title: Aspose.Words for Java
description: Allows to specify how text inside a document should be rendered when saving in SVG format in Java.
type: docs
weight: 647
url: /java/com.aspose.words/svgtextoutputmode/
---

**Inheritance:**
java.lang.Object
```
public class SvgTextOutputMode
```

Allows to specify how text inside a document should be rendered when saving in SVG format.

 **Examples:** 

Shows how to mimic the properties of images when converting a .docx document to .svg.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 // Configure the SvgSaveOptions object to save with no page borders or selectable text.
 SvgSaveOptions options = new SvgSaveOptions();
 {
     options.setFitToViewPort(true);
     options.setShowPageBorder(false);
     options.setTextOutputMode(SvgTextOutputMode.USE_PLACED_GLYPHS);
 }

 doc.save(getArtifactsDir() + "SvgSaveOptions.SaveLikeImage.svg", options);
 
```
## Fields

| Field | Description |
| --- | --- |
| [USE_PLACED_GLYPHS](#USE-PLACED-GLYPHS) | Text is rendered using curves. |
| [USE_SVG_FONTS](#USE-SVG-FONTS) | SVG fonts are used to render text. |
| [USE_TARGET_MACHINE_FONTS](#USE-TARGET-MACHINE-FONTS) | Fonts installed on the target machine are used to render text. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String svgTextOutputModeName)](#fromName-java.lang.String) |  |
| [getName(int svgTextOutputMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int svgTextOutputMode)](#toString-int) |  |
### USE_PLACED_GLYPHS {#USE-PLACED-GLYPHS}
```
public static int USE_PLACED_GLYPHS
```


Text is rendered using curves. Note, text selection will not work if you use this option.

### USE_SVG_FONTS {#USE-SVG-FONTS}
```
public static int USE_SVG_FONTS
```


SVG fonts are used to render text. Note, not all browsers support SVG fonts.

### USE_TARGET_MACHINE_FONTS {#USE-TARGET-MACHINE-FONTS}
```
public static int USE_TARGET_MACHINE_FONTS
```


Fonts installed on the target machine are used to render text. Note, if some of fonts used in the document are not available on the target machine, document can look differently.

### length {#length}
```
public static int length
```


### fromName(String svgTextOutputModeName) {#fromName-java.lang.String}
```
public static int fromName(String svgTextOutputModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| svgTextOutputModeName | java.lang.String |  |

**Returns:**
int
### getName(int svgTextOutputMode) {#getName-int}
```
public static String getName(int svgTextOutputMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| svgTextOutputMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int svgTextOutputMode) {#toString-int}
```
public static String toString(int svgTextOutputMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| svgTextOutputMode | int |  |

**Returns:**
java.lang.String
