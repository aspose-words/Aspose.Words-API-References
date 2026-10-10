---
title: "PageBorderAppliesTo"
linktitle: "PageBorderAppliesTo"
second_title: "Aspose.Words pour Java"
description: "Spécifie sur quelles pages la bordure de page est imprimée en Java."
type: docs
weight: 510
url: /fr/java/com.aspose.words/pageborderappliesto/
---

**Inheritance:**
java.lang.Object
```
public class PageBorderAppliesTo
```

Spécifie sur quelles pages la bordure de page est imprimée.

 **Examples:** 

Montre comment créer une bordure à bande bleue large en haut de la première page.

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
## Champs

| Champ | Description |
| --- | --- |
| [ALL_PAGES](#ALL-PAGES) | La bordure de page est affichée sur toutes les pages de la section. |
| [FIRST_PAGE](#FIRST-PAGE) | La bordure de page est affichée uniquement sur la première page de la section. |
| [OTHER_PAGES](#OTHER-PAGES) | La bordure de page est affichée sur toutes les pages sauf la première page de la section. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String pageBorderAppliesToName)](#fromName-java.lang.String) |  |
| [getName(int pageBorderAppliesTo)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pageBorderAppliesTo)](#toString-int) |  |
### ALL_PAGES {#ALL-PAGES}
```
public static int ALL_PAGES
```


La bordure de page est affichée sur toutes les pages de la section.

### FIRST_PAGE {#FIRST-PAGE}
```
public static int FIRST_PAGE
```


La bordure de page est affichée uniquement sur la première page de la section.

### OTHER_PAGES {#OTHER-PAGES}
```
public static int OTHER_PAGES
```


La bordure de page est affichée sur toutes les pages sauf la première page de la section.

### length {#length}
```
public static int length
```


### fromName(String pageBorderAppliesToName) {#fromName-java.lang.String}
```
public static int fromName(String pageBorderAppliesToName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| pageBorderAppliesToName | java.lang.String |  |

**Returns:**
int
### getName(int pageBorderAppliesTo) {#getName-int}
```
public static String getName(int pageBorderAppliesTo)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| pageBorderAppliesTo | int |  |

**Returns:**
java.lang.String
