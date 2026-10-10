---
title: "PageBorderDistanceFrom"
linktitle: "PageBorderDistanceFrom"
second_title: "Aspose.Words für Java"
description: "Gibt die Positionierung des Seitenrands relativ zum Seitenrand in Java an."
type: docs
weight: 511
url: /de/java/com.aspose.words/pageborderdistancefrom/
---

**Inheritance:**
java.lang.Object
```
public class PageBorderDistanceFrom
```

Gibt die Position des Seitenrands relativ zum Seitenrand an.

 **Examples:** 

Zeigt, wie man einen breiten blauen Bandrahmen oben auf der ersten Seite erstellt.

```

 Document doc = new Document();

 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setBorderAlwaysInFront(false);
 pageSetup.setBorderDistanceFrom(PageBorderDistanceFrom.PAGE_EDGE);
 pageSetup.setBorderAppliesTo(PageBorderAppliesTo.FIRST_PAGE);

 Border border = pageSetup.getBorders().getByBorderType(BorderType.TOP);
 border.setLineStyle(LineStyle.SINGLE);
 border.setLineWidth(30.0);
 border.setColor(Color.BLUE);
 border.setDistanceFromText(0.0);

 doc.save(getArtifactsDir() + "PageSetup.PageBorderProperties.docx");
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [PAGE_EDGE](#PAGE-EDGE) | Die Randposition wird von der Seitenkante aus gemessen. |
| [TEXT](#TEXT) | Die Randposition wird vom Seitenrand aus gemessen. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String pageBorderDistanceFromName)](#fromName-java.lang.String) |  |
| [getName(int pageBorderDistanceFrom)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pageBorderDistanceFrom)](#toString-int) |  |
### PAGE_EDGE {#PAGE-EDGE}
```
public static int PAGE_EDGE
```


Die Randposition wird von der Seitenkante aus gemessen.

### TEXT {#TEXT}
```
public static int TEXT
```


Die Randposition wird vom Seitenrand aus gemessen.

### length {#length}
```
public static int length
```


### fromName(String pageBorderDistanceFromName) {#fromName-java.lang.String}
```
public static int fromName(String pageBorderDistanceFromName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pageBorderDistanceFromName | java.lang.String |  |

**Returns:**
int
### getName(int pageBorderDistanceFrom) {#getName-int}
```
public static String getName(int pageBorderDistanceFrom)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pageBorderDistanceFrom | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pageBorderDistanceFrom) {#toString-int}
```
public static String toString(int pageBorderDistanceFrom)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pageBorderDistanceFrom | int |  |

**Returns:**
java.lang.String
