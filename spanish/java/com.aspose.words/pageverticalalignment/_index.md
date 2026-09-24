---
title: "PageVerticalAlignment"
linktitle: "PageVerticalAlignment"
second_title: "Aspose.Words para Java"
description: "Especifica la justificación vertical del texto en cada página en Java."
type: docs
weight: 520
url: /es/java/com.aspose.words/pageverticalalignment/
---

**Inheritance:**
java.lang.Object
```
public class PageVerticalAlignment
```

Especifica la justificación vertical del texto en cada página.

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
| [BOTTOM](#BOTTOM) | El texto está alineado en la parte inferior de la página. |
| [CENTER](#CENTER) | El texto está alineado en el centro de la página. |
| [JUSTIFY](#JUSTIFY) | El texto se extiende para llenar la página. |
| [TOP](#TOP) | El texto está alineado en la parte superior de la página. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String pageVerticalAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int pageVerticalAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pageVerticalAlignment)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


El texto está alineado en la parte inferior de la página.

### CENTER {#CENTER}
```
public static int CENTER
```


El texto está alineado en el centro de la página.

### JUSTIFY {#JUSTIFY}
```
public static int JUSTIFY
```


El texto se extiende para llenar la página.

### TOP {#TOP}
```
public static int TOP
```


El texto está alineado en la parte superior de la página.

### length {#length}
```
public static int length
```


### fromName(String pageVerticalAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String pageVerticalAlignmentName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pageVerticalAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int pageVerticalAlignment) {#getName-int}
```
public static String getName(int pageVerticalAlignment)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pageVerticalAlignment | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pageVerticalAlignment) {#toString-int}
```
public static String toString(int pageVerticalAlignment)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pageVerticalAlignment | int |  |

**Returns:**
java.lang.String
