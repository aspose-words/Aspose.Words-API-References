---
title: "PageVerticalAlignment"
linktitle: "PageVerticalAlignment"
second_title: "Aspose.Words pour Java"
description: "Spécifie la justification verticale du texte sur chaque page en Java."
type: docs
weight: 520
url: /fr/java/com.aspose.words/pageverticalalignment/
---

**Inheritance:**
java.lang.Object
```
public class PageVerticalAlignment
```

Spécifie la justification verticale du texte sur chaque page.

 **Examples:** 

Montre comment appliquer et rétablir les paramètres de mise en page aux sections d'un document.

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
## Champs

| Champ | Description |
| --- | --- |
| [BOTTOM](#BOTTOM) | Le texte est aligné en bas de la page. |
| [CENTER](#CENTER) | Le texte est aligné au milieu de la page. |
| [JUSTIFY](#JUSTIFY) | Le texte est réparti pour remplir la page. |
| [TOP](#TOP) | Le texte est aligné en haut de la page. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String pageVerticalAlignmentName)](#fromName-java.lang.String) |  |
| [getName(int pageVerticalAlignment)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pageVerticalAlignment)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Le texte est aligné en bas de la page.

### CENTER {#CENTER}
```
public static int CENTER
```


Le texte est aligné au milieu de la page.

### JUSTIFY {#JUSTIFY}
```
public static int JUSTIFY
```


Le texte est réparti pour remplir la page.

### TOP {#TOP}
```
public static int TOP
```


Le texte est aligné en haut de la page.

### length {#length}
```
public static int length
```


### fromName(String pageVerticalAlignmentName) {#fromName-java.lang.String}
```
public static int fromName(String pageVerticalAlignmentName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| pageVerticalAlignmentName | java.lang.String |  |

**Returns:**
int
### getName(int pageVerticalAlignment) {#getName-int}
```
public static String getName(int pageVerticalAlignment)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| pageVerticalAlignment | int |  |

**Returns:**
java.lang.String
