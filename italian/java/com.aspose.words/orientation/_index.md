---
title: "Orientamento"
linktitle: "Orientamento"
second_title: "Aspose.Words per Java"
description: "Specifica l'orientamento della pagina in Java."
type: docs
weight: 507
url: /it/java/com.aspose.words/orientation/
---

**Inheritance:**
java.lang.Object
```
public class Orientation
```

Specifica l'orientamento della pagina.

 **Examples:** 

Mostra come applicare e ripristinare le impostazioni di configurazione della pagina alle sezioni di un documento.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [LANDSCAPE](#LANDSCAPE) | Orientamento della pagina in orizzontale (largo e corto). |
| [PORTRAIT](#PORTRAIT) | Orientamento della pagina in verticale (stretto e alto). |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String orientationName)](#fromName-java.lang.String) |  |
| [getName(int orientation)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int orientation)](#toString-int) |  |
### LANDSCAPE {#LANDSCAPE}
```
public static int LANDSCAPE
```


Orientamento della pagina in orizzontale (largo e corto).

### PORTRAIT {#PORTRAIT}
```
public static int PORTRAIT
```


Orientamento della pagina in verticale (stretto e alto).

### length {#length}
```
public static int length
```


### fromName(String orientationName) {#fromName-java.lang.String}
```
public static int fromName(String orientationName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| orientationName | java.lang.String |  |

**Returns:**
int
### getName(int orientation) {#getName-int}
```
public static String getName(int orientation)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| orientation | int |  |

**Returns:**
java.lang.String
