---
title: "HtmlFixedPageHorizontalAlignment"
linktitle: "HtmlFixedPageHorizontalAlignment"
second_title: "Aspose.Words pour Java"
description: "Spécifie l’alignement horizontal des pages dans le document HTML de sortie en Java."
type: docs
weight: 379
url: /fr/java/com.aspose.words/htmlfixedpagehorizontalalignment/
---

**Inheritance:**
java.lang.Object
```
public class HtmlFixedPageHorizontalAlignment
```

Spécifie l’alignement horizontal des pages dans le document HTML de sortie.

 **Examples:** 

Montre comment définir l'alignement horizontal des pages lors de l'enregistrement d'un document au format HTML.

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
## Champs

| Champ | Description |
| --- | --- |
| [CENTER](#CENTER) | Centrer les pages. |
| [LEFT](#LEFT) | Aligner les pages à gauche. |
| [RIGHT](#RIGHT) | Aligner les pages à droite. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String htmlFixedPageHorizontalAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int htmlFixedPageHorizontalAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int htmlFixedPageHorizontalAlignment)](#toString-int) |  |
### CENTER {#CENTER}
```
public static int CENTER
```


Centrer les pages. C'est la valeur par défaut.

### LEFT {#LEFT}
```
public static int LEFT
```


Aligner les pages à gauche.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Aligner les pages à droite.

### length {#length}
```
public static int length
```


### fromName(String htmlFixedPageHorizontalAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String htmlFixedPageHorizontalAlignmentName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| htmlFixedPageHorizontalAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int htmlFixedPageHorizontalAlignment) {#getName-int}
```
public static String getName(int htmlFixedPageHorizontalAlignment)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| htmlFixedPageHorizontalAlignment | int |  |

**Returns:**
java.lang.String
