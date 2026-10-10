---
title: "HtmlFixedPageHorizontalAlignment"
linktitle: "HtmlFixedPageHorizontalAlignment"
second_title: "Aspose.Words für Java"
description: "Gibt die horizontale Ausrichtung für Seiten im ausgegebenen HTML-Dokument in Java an."
type: docs
weight: 379
url: /de/java/com.aspose.words/htmlfixedpagehorizontalalignment/
---

**Inheritance:**
java.lang.Object
```
public class HtmlFixedPageHorizontalAlignment
```

Gibt die horizontale Ausrichtung für Seiten im ausgegebenen HTML-Dokument an.

 **Examples:** 

Zeigt, wie die horizontale Ausrichtung von Seiten beim Speichern eines Dokuments als HTML festgelegt wird.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [CENTER](#CENTER) | Seiten zentrieren. |
| [LEFT](#LEFT) | Seiten linksbündig ausrichten. |
| [RIGHT](#RIGHT) | Seiten rechtsbündig ausrichten. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String htmlFixedPageHorizontalAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int htmlFixedPageHorizontalAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int htmlFixedPageHorizontalAlignment)](#toString-int) |  |
### CENTER {#CENTER}
```
public static int CENTER
```


Seiten zentrieren. Dies ist der Standardwert.

### LEFT {#LEFT}
```
public static int LEFT
```


Seiten linksbündig ausrichten.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Seiten rechtsbündig ausrichten.

### length {#length}
```
public static int length
```


### fromName(String htmlFixedPageHorizontalAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String htmlFixedPageHorizontalAlignmentName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| htmlFixedPageHorizontalAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int htmlFixedPageHorizontalAlignment) {#getName-int}
```
public static String getName(int htmlFixedPageHorizontalAlignment)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| htmlFixedPageHorizontalAlignment | int |  |

**Returns:**
java.lang.String
