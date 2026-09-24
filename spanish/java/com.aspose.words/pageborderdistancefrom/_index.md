---
title: "PageBorderDistanceFrom"
linktitle: "PageBorderDistanceFrom"
second_title: "Aspose.Words para Java"
description: "Especifica la posición del borde de la página en relación con el margen de la página en Java."
type: docs
weight: 511
url: /es/java/com.aspose.words/pageborderdistancefrom/
---

**Inheritance:**
java.lang.Object
```
public class PageBorderDistanceFrom
```

Especifica la posición del borde de la página respecto al margen de la página.

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
| [PAGE_EDGE](#PAGE-EDGE) | La posición del borde se mide desde el borde de la página. |
| [TEXT](#TEXT) | La posición del borde se mide desde el margen de la página. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String pageBorderDistanceFromName)](#fromName-java.lang.String) |  |
| [getName(int pageBorderDistanceFrom)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pageBorderDistanceFrom)](#toString-int) |  |
### PAGE_EDGE {#PAGE-EDGE}
```
public static int PAGE_EDGE
```


La posición del borde se mide desde el borde de la página.

### TEXT {#TEXT}
```
public static int TEXT
```


La posición del borde se mide desde el margen de la página.

### length {#length}
```
public static int length
```


### fromName(String pageBorderDistanceFromName) {#fromName-java.lang.String}
```
public static int fromName(String pageBorderDistanceFromName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pageBorderDistanceFromName | java.lang.String |  |

**Returns:**
int
### getName(int pageBorderDistanceFrom) {#getName-int}
```
public static String getName(int pageBorderDistanceFrom)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pageBorderDistanceFrom | int |  |

**Returns:**
java.lang.String
