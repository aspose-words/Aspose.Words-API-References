---
title: "PageBorderAppliesTo"
linktitle: "PageBorderAppliesTo"
second_title: "Aspose.Words für Java"
description: "Gibt an, auf welchen Seiten der Seitenrand in Java gedruckt wird."
type: docs
weight: 510
url: /de/java/com.aspose.words/pageborderappliesto/
---

**Inheritance:**
java.lang.Object
```
public class PageBorderAppliesTo
```

Gibt an, auf welchen Seiten der Seitenrand gedruckt wird.

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
| [ALL_PAGES](#ALL-PAGES) | Der Seitenrand wird auf allen Seiten des Abschnitts angezeigt. |
| [FIRST_PAGE](#FIRST-PAGE) | Der Seitenrand wird nur auf der ersten Seite des Abschnitts angezeigt. |
| [OTHER_PAGES](#OTHER-PAGES) | Der Seitenrand wird auf allen Seiten außer der ersten Seite des Abschnitts angezeigt. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String pageBorderAppliesToName)](#fromName-java.lang.String) |  |
| [getName(int pageBorderAppliesTo)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pageBorderAppliesTo)](#toString-int) |  |
### ALL_PAGES {#ALL-PAGES}
```
public static int ALL_PAGES
```


Der Seitenrand wird auf allen Seiten des Abschnitts angezeigt.

### FIRST_PAGE {#FIRST-PAGE}
```
public static int FIRST_PAGE
```


Der Seitenrand wird nur auf der ersten Seite des Abschnitts angezeigt.

### OTHER_PAGES {#OTHER-PAGES}
```
public static int OTHER_PAGES
```


Der Seitenrand wird auf allen Seiten außer der ersten Seite des Abschnitts angezeigt.

### length {#length}
```
public static int length
```


### fromName(String pageBorderAppliesToName) {#fromName-java.lang.String}
```
public static int fromName(String pageBorderAppliesToName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pageBorderAppliesToName | java.lang.String |  |

**Returns:**
int
### getName(int pageBorderAppliesTo) {#getName-int}
```
public static String getName(int pageBorderAppliesTo)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pageBorderAppliesTo | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pageBorderAppliesTo) {#toString-int}
```
public static String toString(int pageBorderAppliesTo)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pageBorderAppliesTo | int |  |

**Returns:**
java.lang.String
