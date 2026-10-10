---
title: "PageBorderDistanceFrom"
linktitle: "PageBorderDistanceFrom"
second_title: "Aspose.Words per Java"
description: "Specifica la posizione del bordo della pagina rispetto al margine della pagina in Java."
type: docs
weight: 511
url: /it/java/com.aspose.words/pageborderdistancefrom/
---

**Inheritance:**
java.lang.Object
```
public class PageBorderDistanceFrom
```

Specifica la posizione del bordo della pagina rispetto al margine della pagina.

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
| [PAGE_EDGE](#PAGE-EDGE) | La posizione del bordo è misurata dal bordo della pagina. |
| [TEXT](#TEXT) | La posizione del bordo è misurata dal margine della pagina. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String pageBorderDistanceFromName)](#fromName-java.lang.String) |  |
| [getName(int pageBorderDistanceFrom)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pageBorderDistanceFrom)](#toString-int) |  |
### PAGE_EDGE {#PAGE-EDGE}
```
public static int PAGE_EDGE
```


La posizione del bordo è misurata dal bordo della pagina.

### TEXT {#TEXT}
```
public static int TEXT
```


La posizione del bordo è misurata dal margine della pagina.

### length {#length}
```
public static int length
```


### fromName(String pageBorderDistanceFromName) {#fromName-java.lang.String}
```
public static int fromName(String pageBorderDistanceFromName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pageBorderDistanceFromName | java.lang.String |  |

**Returns:**
int
### getName(int pageBorderDistanceFrom) {#getName-int}
```
public static String getName(int pageBorderDistanceFrom)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pageBorderDistanceFrom | int |  |

**Returns:**
java.lang.String
