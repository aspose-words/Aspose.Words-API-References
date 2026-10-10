---
title: "Orientación"
linktitle: "Orientación"
second_title: "Aspose.Words para Java"
description: "Especifica la orientación de página en Java."
type: docs
weight: 507
url: /es/java/com.aspose.words/orientation/
---

**Inheritance:**
java.lang.Object
```
public class Orientation
```

Especifica la orientación de la página.

 **Examples:** 

Muestra cómo aplicar y revertir la configuración de página a secciones en un documento.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Modify the page setup properties for the builder's current section and add text.
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setVerticalAlignment(PageVerticalAlignment.CENTER);
 builder.writeln("This is the first section, which landscape oriented with vertically centered text.");

 // If we start a new section using a document builder,
 // it will inherit the builder's current page setup properties.
 builder.insertBreak(BreakType.SECTION_BREAK_NEW_PAGE);

 Assert.assertEquals(Orientation.LANDSCAPE, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.CENTER, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 // We can revert its page setup properties to their default values using the "ClearFormatting" method.
 builder.getPageSetup().clearFormatting();

 Assert.assertEquals(Orientation.PORTRAIT, doc.getSections().get(1).getPageSetup().getOrientation());
 Assert.assertEquals(PageVerticalAlignment.TOP, doc.getSections().get(1).getPageSetup().getVerticalAlignment());

 builder.writeln("This is the second section, which is in default Letter paper size, portrait orientation and top alignment.");

 doc.save(getArtifactsDir() + "PageSetup.ClearFormatting.docx");
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [LANDSCAPE](#LANDSCAPE) | Orientación de página horizontal (ancha y corta). |
| [PORTRAIT](#PORTRAIT) | Orientación de página vertical (estrecha y alta). |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String orientationName)](#fromName-java.lang.String) |  |
| [getName(int orientation)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int orientation)](#toString-int) |  |
### LANDSCAPE {#LANDSCAPE}
```
public static int LANDSCAPE
```


Orientación de página horizontal (ancha y corta).

### PORTRAIT {#PORTRAIT}
```
public static int PORTRAIT
```


Orientación de página vertical (estrecha y alta).

### length {#length}
```
public static int length
```


### fromName(String orientationName) {#fromName-java.lang.String}
```
public static int fromName(String orientationName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| orientationName | java.lang.String |  |

**Returns:**
int
### getName(int orientation) {#getName-int}
```
public static String getName(int orientation)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| orientation | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int orientation) {#toString-int}
```
public static String toString(int orientation)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| orientation | int |  |

**Returns:**
java.lang.String
