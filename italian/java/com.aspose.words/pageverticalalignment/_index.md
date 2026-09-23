---
title: "PageVerticalAlignment"
linktitle: "PageVerticalAlignment"
second_title: "Aspose.Words per Java"
description: "Specifica l'allineamento verticale del testo su ogni pagina in Java."
type: docs
weight: 520
url: /it/java/com.aspose.words/pageverticalalignment/
---

**Inheritance:**
java.lang.Object
```
public class PageVerticalAlignment
```

Specifica l'allineamento verticale del testo su ogni pagina.

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
| [BOTTOM](#BOTTOM) | Il testo è allineato nella parte inferiore della pagina. |
| [CENTER](#CENTER) | Il testo è allineato al centro della pagina. |
| [JUSTIFY](#JUSTIFY) | Il testo è distribuito per riempire la pagina. |
| [TOP](#TOP) | Il testo è allineato nella parte superiore della pagina. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String pageVerticalAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int pageVerticalAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pageVerticalAlignment)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Il testo è allineato nella parte inferiore della pagina.

### CENTER {#CENTER}
```
public static int CENTER
```


Il testo è allineato al centro della pagina.

### JUSTIFY {#JUSTIFY}
```
public static int JUSTIFY
```


Il testo è distribuito per riempire la pagina.

### TOP {#TOP}
```
public static int TOP
```


Il testo è allineato nella parte superiore della pagina.

### length {#length}
```
public static int length
```


### fromName(String pageVerticalAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String pageVerticalAlignmentName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pageVerticalAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int pageVerticalAlignment) {#getName-int}
```
public static String getName(int pageVerticalAlignment)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pageVerticalAlignment | int |  |

**Returns:**
java.lang.String
