---
title: "PageBorderAppliesTo"
linktitle: "PageBorderAppliesTo"
second_title: "Aspose.Words per Java"
description: "Specifica su quali pagine il bordo della pagina viene stampato in Java."
type: docs
weight: 510
url: /it/java/com.aspose.words/pageborderappliesto/
---

**Inheritance:**
java.lang.Object
```
public class PageBorderAppliesTo
```

Specifica su quali pagine il bordo della pagina viene stampato.

 **Examples:** 

Mostra come creare un bordo a banda blu larga nella parte superiore della prima pagina.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [ALL_PAGES](#ALL-PAGES) | Il bordo della pagina è mostrato su tutte le pagine della sezione. |
| [FIRST_PAGE](#FIRST-PAGE) | Il bordo della pagina è mostrato solo sulla prima pagina della sezione. |
| [OTHER_PAGES](#OTHER-PAGES) | Il bordo della pagina è mostrato su tutte le pagine tranne la prima pagina della sezione. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String pageBorderAppliesToName)](#fromName-java.lang.String) |  |
| [getName(int pageBorderAppliesTo)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pageBorderAppliesTo)](#toString-int) |  |
### ALL_PAGES {#ALL-PAGES}
```
public static int ALL_PAGES
```


Il bordo della pagina è mostrato su tutte le pagine della sezione.

### FIRST_PAGE {#FIRST-PAGE}
```
public static int FIRST_PAGE
```


Il bordo della pagina è mostrato solo sulla prima pagina della sezione.

### OTHER_PAGES {#OTHER-PAGES}
```
public static int OTHER_PAGES
```


Il bordo della pagina è mostrato su tutte le pagine tranne la prima pagina della sezione.

### length {#length}
```
public static int length
```


### fromName(String pageBorderAppliesToName) {#fromName-java.lang.String}
```
public static int fromName(String pageBorderAppliesToName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pageBorderAppliesToName | java.lang.String |  |

**Returns:**
int
### getName(int pageBorderAppliesTo) {#getName-int}
```
public static String getName(int pageBorderAppliesTo)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pageBorderAppliesTo | int |  |

**Returns:**
java.lang.String
