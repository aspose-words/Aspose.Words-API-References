---
title: "HtmlOfficeMathOutputMode"
linktitle: "HtmlOfficeMathOutputMode"
second_title: "Aspose.Words para Java"
description: "Especifica cómo Aspose.Words exporta OfficeMath a HTML, MHTML y EPUB en Java."
type: docs
weight: 384
url: /es/java/com.aspose.words/htmlofficemathoutputmode/
---

**Inheritance:**
java.lang.Object
```
public class HtmlOfficeMathOutputMode
```

Especifica cómo Aspose.Words exporta OfficeMath a HTML, MHTML y EPUB.

 **Examples:** 

Muestra cómo especificar la exportación de objetos Microsoft OfficeMath a HTML.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 // When we save the document to HTML, we can pass a SaveOptions object
 // to determine how the saving operation handles OfficeMath objects.
 // Setting the "OfficeMathOutputMode" property to "HtmlOfficeMathOutputMode.Image"
 // will render each OfficeMath object into an image.
 // Setting the "OfficeMathOutputMode" property to "HtmlOfficeMathOutputMode.MathML"
 // will convert each OfficeMath object into MathML.
 // Setting the "OfficeMathOutputMode" property to "HtmlOfficeMathOutputMode.Text"
 // will represent each OfficeMath formula using plain HTML text.
 HtmlSaveOptions options = new HtmlSaveOptions();
 {
     options.setOfficeMathOutputMode(htmlOfficeMathOutputMode);
 }

 doc.save(getArtifactsDir() + "HtmlSaveOptions.OfficeMathOutputMode.html", options);
 
```
## Campos

| Campo | Descripción |
| --- | --- |
|  | [IMAGE](#IMAGE) | OfficeMath se convierte a HTML como una imagen especificada por la etiqueta ![Image 1][] . |


[Image 1]:  |
| [MATH_ML](#MATH-ML) | OfficeMath se convierte a HTML usando MathML. |
| [TEXT](#TEXT) | OfficeMath se convierte a HTML como una secuencia de ejecuciones especificada por etiquetas . |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String htmlOfficeMathOutputModeName)](#fromName-java.lang.String) |  |
| [getName(int htmlOfficeMathOutputMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int htmlOfficeMathOutputMode)](#toString-int) |  |
### IMAGE {#IMAGE}
```
public static int IMAGE
```


OfficeMath se convierte a HTML como una imagen especificada por la etiqueta ![Image 1][] .


[Image 1]: 

### MATH_ML {#MATH-ML}
```
public static int MATH_ML
```


OfficeMath se convierte a HTML usando MathML.

### TEXT {#TEXT}
```
public static int TEXT
```


OfficeMath se convierte a HTML como una secuencia de ejecuciones especificada por etiquetas .

### length {#length}
```
public static int length
```


### fromName(String htmlOfficeMathOutputModeName) {#fromName-java.lang.String}
```
public static int fromName(String htmlOfficeMathOutputModeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| htmlOfficeMathOutputModeName | java.lang.String |  |

**Returns:**
int
### getName(int htmlOfficeMathOutputMode) {#getName-int}
```
public static String getName(int htmlOfficeMathOutputMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| htmlOfficeMathOutputMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int htmlOfficeMathOutputMode) {#toString-int}
```
public static String toString(int htmlOfficeMathOutputMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| htmlOfficeMathOutputMode | int |  |

**Returns:**
java.lang.String
