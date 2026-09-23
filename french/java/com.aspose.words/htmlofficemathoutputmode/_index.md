---
title: "HtmlOfficeMathOutputMode"
linktitle: "HtmlOfficeMathOutputMode"
second_title: "Aspose.Words pour Java"
description: "Spécifie comment Aspose.Words exporte OfficeMath vers HTML, MHTML et EPUB en Java."
type: docs
weight: 384
url: /fr/java/com.aspose.words/htmlofficemathoutputmode/
---

**Inheritance:**
java.lang.Object
```
public class HtmlOfficeMathOutputMode
```

Spécifie comment Aspose.Words exporte OfficeMath vers HTML, MHTML et EPUB.

 **Examples:** 

Montre comment spécifier l'exportation des objets Microsoft OfficeMath vers HTML.

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
## Champs

| Champ | Description |
| --- | --- |
|  | [IMAGE](#IMAGE) | OfficeMath est converti en HTML sous forme d'image spécifiée par la balise ![Image 1][]. |


[Image 1]:  |
| [MATH_ML](#MATH-ML) | OfficeMath est converti en HTML en utilisant MathML. |
| [TEXT](#TEXT) | OfficeMath est converti en HTML sous forme de séquence de runs spécifiée par  tags. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String htmlOfficeMathOutputModeName)](#fromName-java.lang.String) |  |
| [getName(int htmlOfficeMathOutputMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int htmlOfficeMathOutputMode)](#toString-int) |  |
### IMAGE {#IMAGE}
```
public static int IMAGE
```


OfficeMath est converti en HTML sous forme d'image spécifiée par la balise ![Image 1][].


[Image 1]: 

### MATH_ML {#MATH-ML}
```
public static int MATH_ML
```


OfficeMath est converti en HTML en utilisant MathML.

### TEXT {#TEXT}
```
public static int TEXT
```


OfficeMath est converti en HTML sous forme de séquence de runs spécifiée par  tags.

### length {#length}
```
public static int length
```


### fromName(String htmlOfficeMathOutputModeName) {#fromName-java.lang.String}
```
public static int fromName(String htmlOfficeMathOutputModeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| htmlOfficeMathOutputModeName | java.lang.String |  |

**Returns:**
int
### getName(int htmlOfficeMathOutputMode) {#getName-int}
```
public static String getName(int htmlOfficeMathOutputMode)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| htmlOfficeMathOutputMode | int |  |

**Returns:**
java.lang.String
