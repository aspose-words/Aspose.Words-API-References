---
title: "HtmlFixedPageHorizontalAlignment"
linktitle: "HtmlFixedPageHorizontalAlignment"
second_title: "Aspose.Words para Java"
description: "Especifica la alineación horizontal para las páginas en el documento HTML de salida en Java."
type: docs
weight: 379
url: /es/java/com.aspose.words/htmlfixedpagehorizontalalignment/
---

**Inheritance:**
java.lang.Object
```
public class HtmlFixedPageHorizontalAlignment
```

Especifica la alineación horizontal para las páginas en el documento HTML de salida.

 **Examples:** 

Muestra cómo establecer la alineación horizontal de las páginas al guardar un documento en HTML.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();
 {
     htmlFixedSaveOptions.setPageHorizontalAlignment(pageHorizontalAlignment);
 }

 doc.save(getArtifactsDir() + "HtmlFixedSaveOptions.HorizontalAlignment.html", htmlFixedSaveOptions);

 String outDocContents = FileUtils.readFileToString(new File(getArtifactsDir() + "HtmlFixedSaveOptions.HorizontalAlignment/styles.css"), StandardCharsets.UTF_8);

 switch (pageHorizontalAlignment)
 {
     case HtmlFixedPageHorizontalAlignment.CENTER:
         Assert.assertTrue(Pattern.compile(
             "[.]awpage [{] position:relative; border:solid 1pt black; margin:10pt auto 10pt auto; overflow:hidden; [}]").matcher(outDocContents).find());
         break;
     case HtmlFixedPageHorizontalAlignment.LEFT:
         Assert.assertTrue(Pattern.compile(
             "[.]awpage [{] position:relative; border:solid 1pt black; margin:10pt auto 10pt 10pt; overflow:hidden; [}]").matcher(outDocContents).find());
         break;
     case HtmlFixedPageHorizontalAlignment.RIGHT:
         Assert.assertTrue(Pattern.compile(
             "[.]awpage [{] position:relative; border:solid 1pt black; margin:10pt 10pt 10pt auto; overflow:hidden; [}]").matcher(outDocContents).find());
         break;
 }
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [CENTER](#CENTER) | Centrar páginas. |
| [LEFT](#LEFT) | Alinear páginas a la izquierda. |
| [RIGHT](#RIGHT) | Alinear páginas a la derecha. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String htmlFixedPageHorizontalAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int htmlFixedPageHorizontalAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int htmlFixedPageHorizontalAlignment)](#toString-int) |  |
### CENTER {#CENTER}
```
public static int CENTER
```


Centrar páginas. Este es el valor predeterminado.

### LEFT {#LEFT}
```
public static int LEFT
```


Alinear páginas a la izquierda.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Alinear páginas a la derecha.

### length {#length}
```
public static int length
```


### fromName(String htmlFixedPageHorizontalAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String htmlFixedPageHorizontalAlignmentName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| htmlFixedPageHorizontalAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int htmlFixedPageHorizontalAlignment) {#getName-int}
```
public static String getName(int htmlFixedPageHorizontalAlignment)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| htmlFixedPageHorizontalAlignment | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int htmlFixedPageHorizontalAlignment) {#toString-int}
```
public static String toString(int htmlFixedPageHorizontalAlignment)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| htmlFixedPageHorizontalAlignment | int |  |

**Returns:**
java.lang.String
