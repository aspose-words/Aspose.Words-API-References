---
title: "PageBorderAppliesTo"
linktitle: "PageBorderAppliesTo"
second_title: "Aspose.Words para Java"
description: "Especifica en qué páginas se imprime el borde de página en Java."
type: docs
weight: 510
url: /es/java/com.aspose.words/pageborderappliesto/
---

**Inheritance:**
java.lang.Object
```
public class PageBorderAppliesTo
```

Especifica en qué páginas se imprime el borde de la página.

 **Examples:** 

Muestra cómo crear un borde de banda azul ancha en la parte superior de la primera página.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [ALL_PAGES](#ALL-PAGES) | El borde de página se muestra en todas las páginas de la sección. |
| [FIRST_PAGE](#FIRST-PAGE) | El borde de página se muestra solo en la primera página de la sección. |
| [OTHER_PAGES](#OTHER-PAGES) | El borde de página se muestra en todas las páginas excepto en la primera página de la sección. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String pageBorderAppliesToName)](#fromName-java.lang.String) |  |
| [getName(int pageBorderAppliesTo)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pageBorderAppliesTo)](#toString-int) |  |
### ALL_PAGES {#ALL-PAGES}
```
public static int ALL_PAGES
```


El borde de página se muestra en todas las páginas de la sección.

### FIRST_PAGE {#FIRST-PAGE}
```
public static int FIRST_PAGE
```


El borde de página se muestra solo en la primera página de la sección.

### OTHER_PAGES {#OTHER-PAGES}
```
public static int OTHER_PAGES
```


El borde de página se muestra en todas las páginas excepto en la primera página de la sección.

### length {#length}
```
public static int length
```


### fromName(String pageBorderAppliesToName) {#fromName-java.lang.String}
```
public static int fromName(String pageBorderAppliesToName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pageBorderAppliesToName | java.lang.String |  |

**Returns:**
int
### getName(int pageBorderAppliesTo) {#getName-int}
```
public static String getName(int pageBorderAppliesTo)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pageBorderAppliesTo | int |  |

**Returns:**
java.lang.String
