---
title: "Style"
linktitle: "Style"
second_title: "Aspose.Words für Java"
description: "Stellt einen einzelnen integrierten oder benutzerdefinierten Stil in Java dar."
type: docs
weight: 641
url: /de/java/com.aspose.words/style/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class Style implements Cloneable
```

Stellt einen einzelnen integrierten oder benutzerdefinierten Stil dar.

Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [ Working with Styles and Themes ][Working with Styles and Themes].

 **Examples:** 

Zeigt, wie man einen benutzerdefinierten Stil erstellt und anwendet.

```

 Document doc = new Document();

 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 style.getFont().setName("Times New Roman");
 style.getFont().setSize(16.0);
 style.getFont().setColor(Color.magenta);
 // Automatically redefine style.
 style.setAutomaticallyUpdate(true);

 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply one of the styles from the document to the paragraph that the document builder is creating.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle"));
 builder.writeln("Hello world!");

 Style firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 Assert.assertEquals(style, firstParagraphStyle);

 // Remove our custom style from the document's styles collection.
 doc.getStyles().get("MyStyle").remove();

 firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 // Any text that used a removed style reverts to the default formatting.
 Assert.assertFalse(IterableUtils.matchesAny(doc.getStyles(), s -> s.getName() == "MyStyle"));
 Assert.assertEquals("Times New Roman", firstParagraphStyle.getFont().getName());
 Assert.assertEquals(12.0d, firstParagraphStyle.getFont().getSize());
 Assert.assertEquals(0, firstParagraphStyle.getFont().getColor().getRGB());
 
```

Zeigt, wie man einen Absatzstil mit Listformatierung erstellt und verwendet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a custom paragraph style.
 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle1");
 style.getFont().setSize(24.0);
 style.getFont().setName("Verdana");
 style.getParagraphFormat().setSpaceAfter(12.0);

 // Create a list and make sure the paragraphs that use this style will use this list.
 style.getListFormat().setList(doc.getLists().add(ListTemplate.BULLET_DEFAULT));
 style.getListFormat().setListLevelNumber(0);

 // Apply the paragraph style to the document builder's current paragraph, and then add some text.
 builder.getParagraphFormat().setStyle(style);
 builder.writeln("Hello World: MyStyle1, bulleted list.");

 // Change the document builder's style to one that has no list formatting and write another paragraph.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));
 builder.writeln("Hello World: Normal.");

 builder.getDocument().save(getArtifactsDir() + "Styles.ParagraphStyleBulletedList.docx");
 
```


[Working with Styles and Themes]: https://docs.aspose.com/words/java/working-with-styles-and-themes/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [clearParaAttrs()](#clearParaAttrs) |  |
| [clearRunAttrs()](#clearRunAttrs) |  |
| [equals(Style style)](#equals-com.aspose.words.Style) | Vergleicht mit dem angegebenen Stil. |
| [fetchInheritedParaAttr(int key)](#fetchInheritedParaAttr-int) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int) |  |
| [fetchParaAttr(int key)](#fetchParaAttr-int) |  |
| [getAliases()](#getAliases) | Liefert alle Aliasnamen dieses Stils. |
| [getAutomaticallyUpdate()](#getAutomaticallyUpdate) | Gibt an, ob dieser Stil basierend auf dem entsprechenden Wert automatisch neu definiert wird. |
| [getBaseStyleName()](#getBaseStyleName) | Liest/setzt den Namen des Stils, auf dem dieser Stil basiert. |
| [getBuiltIn()](#getBuiltIn) | Wahr, wenn dieser Stil einer der integrierten Stile in MS Word ist. |
| [getDirectParaAttr(int key)](#getDirectParaAttr-int) |  |
| [getDirectParaAttr(int key, int revisionsView)](#getDirectParaAttr-int-int) |  |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int) |  |
| [getDirectRunAttr(int key, int revisionsView)](#getDirectRunAttr-int-int) |  |
| [getDocument()](#getDocument) | Ruft das zugehörige Dokument ab. |
| [getFont()](#getFont) | Liefert die Zeichenformatierung des Stils. |
| [getLinkedStyleName()](#getLinkedStyleName) | Liest/setzt den Namen des mit diesem verknüpften [Style](../../com.aspose.words/style/). |
| [getList()](#getList) | Liefert die Liste, die die Formatierung dieses Listenstils definiert. |
| [getListFormat()](#getListFormat) | Bietet Zugriff auf die Listformatierungseigenschaften eines Absatzstils. |
| [getLocked()](#getLocked) | Gibt an, ob dieser Stil gesperrt ist. |
| [getName()](#getName) | Liefert den Namen des Stils. |
| [getNextParagraphStyleName()](#getNextParagraphStyleName) | Liest/setzt den Namen des Stils, der automatisch auf einen neuen Absatz angewendet wird, der nach einem mit dem angegebenen Stil formatierten Absatz eingefügt wird. |
| [getParagraphFormat()](#getParagraphFormat) | Liefert die Absatzformatierung des Stils. |
| [getPriority()](#getPriority) | Liest/setzt den ganzzahligen Wert, der die Priorität für die Sortierung der Stile im Styles task pane darstellt. |
| [getSemiHidden()](#getSemiHidden) | Liest/setzt, ob der Stil in der Styles-Galerie und im Styles task pane ausgeblendet wird. |
| [getStyleIdentifier()](#getStyleIdentifier) | Liefert den sprachunabhängigen Stil-Identifikator für einen integrierten Stil. |
| [getStyles()](#getStyles) | Liefert die Sammlung von Stilen, zu denen dieser Stil gehört. |
| [getType()](#getType) | Ermittelt den Stiltyp (Absatz oder Zeichen). |
| [getUnhideWhenUsed()](#getUnhideWhenUsed) | Liest/legt fest, ob der im aktuellen Dokument verwendete Stil aus der Styles-Galerie und dem Styles-Aufgabenbereich wieder eingeblendet wird. |
| [isHeading()](#isHeading) | Wahr, wenn der Stil einer der integrierten Überschriftsstile ist. |
| [isQuickStyle()](#isQuickStyle) | Gibt an, ob dieser Stil in der Schnellformatvorlagen-Galerie in der MS‑Word‑Benutzeroberfläche angezeigt wird. |
| [isQuickStyle(boolean value)](#isQuickStyle-boolean) | Gibt an, ob dieser Stil in der Schnellformatvorlagen-Galerie in der MS‑Word‑Benutzeroberfläche angezeigt wird. |
| [remove()](#remove) | Entfernt den angegebenen Stil aus dem Dokument. |
| [removeParaAttr(int key)](#removeParaAttr-int) |  |
| [removeRunAttr(int key)](#removeRunAttr-int) |  |
| [setAutomaticallyUpdate(boolean value)](#setAutomaticallyUpdate-boolean) | Gibt an, ob dieser Stil basierend auf dem entsprechenden Wert automatisch neu definiert wird. |
| [setBaseStyleName(String value)](#setBaseStyleName-java.lang.String) | Liest/setzt den Namen des Stils, auf dem dieser Stil basiert. |
| [setLinkedStyleName(String value)](#setLinkedStyleName-java.lang.String) | Liest/setzt den Namen des mit diesem verknüpften [Style](../../com.aspose.words/style/). |
| [setLocked(boolean value)](#setLocked-boolean) | Gibt an, ob dieser Stil gesperrt ist. |
| [setName(String value)](#setName-java.lang.String) | Legt den Namen des Stils fest. |
| [setNextParagraphStyleName(String value)](#setNextParagraphStyleName-java.lang.String) | Liest/setzt den Namen des Stils, der automatisch auf einen neuen Absatz angewendet wird, der nach einem mit dem angegebenen Stil formatierten Absatz eingefügt wird. |
| [setParaAttr(int key, Object value)](#setParaAttr-int-java.lang.Object) |  |
| [setPriority(int value)](#setPriority-int) | Liest/setzt den ganzzahligen Wert, der die Priorität für die Sortierung der Stile im Styles task pane darstellt. |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object) |  |
| [setSemiHidden(boolean value)](#setSemiHidden-boolean) | Liest/setzt, ob der Stil in der Styles-Galerie und im Styles task pane ausgeblendet wird. |
| [setUnhideWhenUsed(boolean value)](#setUnhideWhenUsed-boolean) | Liest/legt fest, ob der im aktuellen Dokument verwendete Stil aus der Styles-Galerie und dem Styles-Aufgabenbereich wieder eingeblendet wird. |
### clearParaAttrs() {#clearParaAttrs}
```
public void clearParaAttrs()
```




### clearRunAttrs() {#clearRunAttrs}
```
public void clearRunAttrs()
```




### equals(Style style) {#equals-com.aspose.words.Style}
```
public boolean equals(Style style)
```


Vergleicht mit dem angegebenen Stil. Stile werden nur für integrierte Stile verglichen. Standardwerte von Stilen sind im Vergleich nicht enthalten. Basisstil, verknüpfter Stil und nächster Absatzstil werden rekursiv verglichen.

 **Examples:** 

Zeigt, wie Stil‑Aliase verwendet werden.

```

 Document doc = new Document(getMyDir() + "Style with alias.docx");

 // This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
 // If a style's name has multiple values separated by commas, each clause is a separate alias.
 Style style = doc.getStyles().get("MyStyle");
 Assert.assertEquals(new String[]{"MyStyle Alias 1", "MyStyle Alias 2"}, style.getAliases());
 Assert.assertEquals("Title", style.getBaseStyleName());
 Assert.assertEquals("MyStyle Char", style.getLinkedStyleName());

 // We can reference a style using its alias, as well as its name.
 Assert.assertEquals(doc.getStyles().get("MyStyle Alias 1"), doc.getStyles().get("MyStyle Alias 2"));

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 1"));
 builder.writeln("Hello world!");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 2"));
 builder.write("Hello again!");

 Assert.assertEquals(doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle(),
         doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| style | [Style](../../com.aspose.words/style/) |  |

**Returns:**
boolean
### fetchInheritedParaAttr(int key) {#fetchInheritedParaAttr-int}
```
public Object fetchInheritedParaAttr(int key)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedRunAttr(int key) {#fetchInheritedRunAttr-int}
```
public Object fetchInheritedRunAttr(int key)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchParaAttr(int key) {#fetchParaAttr-int}
```
public Object fetchParaAttr(int key)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getAliases() {#getAliases}
```
public String[] getAliases()
```


Ermittelt alle Aliase dieses Stils. Wenn der Stil keine Aliase hat, wird ein leeres String‑Array zurückgegeben.

 **Examples:** 

Zeigt, wie Stil‑Aliase verwendet werden.

```

 Document doc = new Document(getMyDir() + "Style with alias.docx");

 // This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
 // If a style's name has multiple values separated by commas, each clause is a separate alias.
 Style style = doc.getStyles().get("MyStyle");
 Assert.assertEquals(new String[]{"MyStyle Alias 1", "MyStyle Alias 2"}, style.getAliases());
 Assert.assertEquals("Title", style.getBaseStyleName());
 Assert.assertEquals("MyStyle Char", style.getLinkedStyleName());

 // We can reference a style using its alias, as well as its name.
 Assert.assertEquals(doc.getStyles().get("MyStyle Alias 1"), doc.getStyles().get("MyStyle Alias 2"));

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 1"));
 builder.writeln("Hello world!");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 2"));
 builder.write("Hello again!");

 Assert.assertEquals(doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle(),
         doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle());
 
```

**Returns:**
java.lang.String[] – Alle Aliase dieses Stils.
### getAutomaticallyUpdate() {#getAutomaticallyUpdate}
```
public boolean getAutomaticallyUpdate()
```


Gibt an, ob dieser Stil basierend auf dem entsprechenden Wert automatisch neu definiert wird.

 **Remarks:** 

Wenn der Eigenschaftswert auf true gesetzt ist, definiert MS Word den aktuellen Stil automatisch neu, sobald die entsprechende Absatzformatierung geändert wurde.

Die Eigenschaft AutomaticallyUpdate gilt nur für Absatzstile.

Der Standardwert ist  false .

 **Examples:** 

Zeigt, wie man einen benutzerdefinierten Stil erstellt und anwendet.

```

 Document doc = new Document();

 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 style.getFont().setName("Times New Roman");
 style.getFont().setSize(16.0);
 style.getFont().setColor(Color.magenta);
 // Automatically redefine style.
 style.setAutomaticallyUpdate(true);

 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply one of the styles from the document to the paragraph that the document builder is creating.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle"));
 builder.writeln("Hello world!");

 Style firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 Assert.assertEquals(style, firstParagraphStyle);

 // Remove our custom style from the document's styles collection.
 doc.getStyles().get("MyStyle").remove();

 firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 // Any text that used a removed style reverts to the default formatting.
 Assert.assertFalse(IterableUtils.matchesAny(doc.getStyles(), s -> s.getName() == "MyStyle"));
 Assert.assertEquals("Times New Roman", firstParagraphStyle.getFont().getName());
 Assert.assertEquals(12.0d, firstParagraphStyle.getFont().getSize());
 Assert.assertEquals(0, firstParagraphStyle.getFont().getColor().getRGB());
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getBaseStyleName() {#getBaseStyleName}
```
public String getBaseStyleName()
```


Liest/setzt den Namen des Stils, auf dem dieser Stil basiert.

 **Remarks:** 

Dies ist ein leerer String, wenn der Stil nicht auf einem anderen Stil basiert, und er kann auf einen leeren String gesetzt werden.

 **Examples:** 

Zeigt, wie Stil‑Aliase verwendet werden.

```

 Document doc = new Document(getMyDir() + "Style with alias.docx");

 // This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
 // If a style's name has multiple values separated by commas, each clause is a separate alias.
 Style style = doc.getStyles().get("MyStyle");
 Assert.assertEquals(new String[]{"MyStyle Alias 1", "MyStyle Alias 2"}, style.getAliases());
 Assert.assertEquals("Title", style.getBaseStyleName());
 Assert.assertEquals("MyStyle Char", style.getLinkedStyleName());

 // We can reference a style using its alias, as well as its name.
 Assert.assertEquals(doc.getStyles().get("MyStyle Alias 1"), doc.getStyles().get("MyStyle Alias 2"));

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 1"));
 builder.writeln("Hello world!");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 2"));
 builder.write("Hello again!");

 Assert.assertEquals(doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle(),
         doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle());
 
```

**Returns:**
java.lang.String - Der entsprechende java.lang.String-Wert.
### getBuiltIn() {#getBuiltIn}
```
public boolean getBuiltIn()
```


Wahr, wenn dieser Stil einer der integrierten Stile in MS Word ist.

 **Examples:** 

Zeigt, wie benutzerdefinierte Stile von integrierten Stilen unterschieden werden.

```

 Document doc = new Document();

 // When we create a document using Microsoft Word, or programmatically using Aspose.Words,
 // the document will come with a collection of styles to apply to its text to modify its appearance.
 // We can access these built-in styles via the document's "Styles" collection.
 // These styles will all have the "BuiltIn" flag set to "true".
 Style style = doc.getStyles().get("Emphasis");

 Assert.assertTrue(style.getBuiltIn());

 // Create a custom style and add it to the collection.
 // Custom styles such as this will have the "BuiltIn" flag set to "false".
 style = doc.getStyles().add(StyleType.CHARACTER, "MyStyle");
 style.getFont().setColor(Color.RED);
 style.getFont().setName("Courier New");

 Assert.assertFalse(style.getBuiltIn());
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getDirectParaAttr(int key) {#getDirectParaAttr-int}
```
public Object getDirectParaAttr(int key)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectParaAttr(int key, int revisionsView) {#getDirectParaAttr-int-int}
```
public Object getDirectParaAttr(int key, int revisionsView)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key) {#getDirectRunAttr-int}
```
public Object getDirectRunAttr(int key)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key, int revisionsView) {#getDirectRunAttr-int-int}
```
public Object getDirectRunAttr(int key, int revisionsView)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
### getDocument() {#getDocument}
```
public DocumentBase getDocument()
```


Ruft das zugehörige Dokument ab.

 **Examples:** 

Zeigt, wie auf die Stilsammlung eines Dokuments zugegriffen wird.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase/) - The owner document.
### getFont() {#getFont}
```
public Font getFont()
```


Liefert die Zeichenformatierung des Stils.

 **Remarks:** 

Bei Listenstilen gibt diese Eigenschaft null zurück.

 **Examples:** 

Zeigt, wie man einen benutzerdefinierten Stil erstellt und anwendet.

```

 Document doc = new Document();

 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 style.getFont().setName("Times New Roman");
 style.getFont().setSize(16.0);
 style.getFont().setColor(Color.magenta);
 // Automatically redefine style.
 style.setAutomaticallyUpdate(true);

 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply one of the styles from the document to the paragraph that the document builder is creating.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle"));
 builder.writeln("Hello world!");

 Style firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 Assert.assertEquals(style, firstParagraphStyle);

 // Remove our custom style from the document's styles collection.
 doc.getStyles().get("MyStyle").remove();

 firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 // Any text that used a removed style reverts to the default formatting.
 Assert.assertFalse(IterableUtils.matchesAny(doc.getStyles(), s -> s.getName() == "MyStyle"));
 Assert.assertEquals("Times New Roman", firstParagraphStyle.getFont().getName());
 Assert.assertEquals(12.0d, firstParagraphStyle.getFont().getSize());
 Assert.assertEquals(0, firstParagraphStyle.getFont().getColor().getRGB());
 
```

Zeigt, wie man einen Absatzstil mit Listformatierung erstellt und verwendet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a custom paragraph style.
 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle1");
 style.getFont().setSize(24.0);
 style.getFont().setName("Verdana");
 style.getParagraphFormat().setSpaceAfter(12.0);

 // Create a list and make sure the paragraphs that use this style will use this list.
 style.getListFormat().setList(doc.getLists().add(ListTemplate.BULLET_DEFAULT));
 style.getListFormat().setListLevelNumber(0);

 // Apply the paragraph style to the document builder's current paragraph, and then add some text.
 builder.getParagraphFormat().setStyle(style);
 builder.writeln("Hello World: MyStyle1, bulleted list.");

 // Change the document builder's style to one that has no list formatting and write another paragraph.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));
 builder.writeln("Hello World: Normal.");

 builder.getDocument().save(getArtifactsDir() + "Styles.ParagraphStyleBulletedList.docx");
 
```

**Returns:**
[Font](../../com.aspose.words/font/) - The character formatting of the style.
### getLinkedStyleName() {#getLinkedStyleName}
```
public String getLinkedStyleName()
```


Liest/legt den Namen des mit diesem verknüpften [Style](../../com.aspose.words/style/) fest. Gibt einen leeren String zurück, wenn keine Stile verknüpft sind.

 **Remarks:** 

Es ist nur erlaubt, den Absatzstil mit dem Zeichenstil zu verknüpfen und umgekehrt.

Das Festlegen von LinkedStyleName für den aktuellen Stil führt automatisch dazu, dass LinkedStyleName für den verknüpften Stil gesetzt wird.

Das Zuweisen eines leeren Strings entspricht dem Aufheben der Verknüpfung des zuvor verknüpften Stils.

 **Examples:** 

Zeigt, wie Stil‑Aliase verwendet werden.

```

 Document doc = new Document(getMyDir() + "Style with alias.docx");

 // This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
 // If a style's name has multiple values separated by commas, each clause is a separate alias.
 Style style = doc.getStyles().get("MyStyle");
 Assert.assertEquals(new String[]{"MyStyle Alias 1", "MyStyle Alias 2"}, style.getAliases());
 Assert.assertEquals("Title", style.getBaseStyleName());
 Assert.assertEquals("MyStyle Char", style.getLinkedStyleName());

 // We can reference a style using its alias, as well as its name.
 Assert.assertEquals(doc.getStyles().get("MyStyle Alias 1"), doc.getStyles().get("MyStyle Alias 2"));

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 1"));
 builder.writeln("Hello world!");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 2"));
 builder.write("Hello again!");

 Assert.assertEquals(doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle(),
         doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle());
 
```

Zeigt, wie Stile untereinander verknüpft werden.

```

 Document doc = new Document();

 Style styleHeading1 = doc.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1);

 Style styleHeading1Char = doc.getStyles().add(StyleType.CHARACTER, "Heading 1 Char");
 styleHeading1Char.getFont().setName("Verdana");
 styleHeading1Char.getFont().setBold(true);
 styleHeading1Char.getFont().getBorder().setLineStyle(LineStyle.DOT);
 styleHeading1Char.getFont().getBorder().setLineWidth(15.0);

 styleHeading1.setLinkedStyleName("Heading 1 Char");

 Assert.assertEquals("Heading 1 Char", styleHeading1.getLinkedStyleName());
 Assert.assertEquals("Heading 1", styleHeading1Char.getLinkedStyleName());
 
```

**Returns:**
java.lang.String - Der entsprechende java.lang.String-Wert.
### getList() {#getList}
```
public List getList()
```


Liefert die Liste, die die Formatierung dieses Listenstils definiert.

 **Remarks:** 

Diese Eigenschaft ist nur für Listenstile gültig. Für andere Stiltypen gibt diese Eigenschaft null zurück.

 **Examples:** 

Zeigt, wie man einen Liststil erstellt und in einem Dokument verwendet.

```

 Document doc = new Document();

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // We can contain an entire List object within a style.
 Style listStyle = doc.getStyles().add(StyleType.LIST, "MyListStyle");

 List list1 = listStyle.getList();

 Assert.assertTrue(list1.isListStyleDefinition());
 Assert.assertFalse(list1.isListStyleReference());
 Assert.assertTrue(list1.isMultiLevel());
 Assert.assertEquals(listStyle, list1.getStyle());

 // Change the appearance of all list levels in our list.
 for (ListLevel level : list1.getListLevels()) {
     level.getFont().setName("Verdana");
     level.getFont().setColor(Color.BLUE);
     level.getFont().setBold(true);
 }

 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Using list style first time:");

 // Create another list from a list within a style.
 List list2 = doc.getLists().add(listStyle);

 Assert.assertFalse(list2.isListStyleDefinition());
 Assert.assertTrue(list2.isListStyleReference());
 Assert.assertEquals(listStyle, list2.getStyle());

 // Add some list items that our list will format.
 builder.getListFormat().setList(list2);
 builder.writeln("Item 1");
 builder.writeln("Item 2");
 builder.getListFormat().removeNumbers();

 builder.writeln("Using list style second time:");

 // Create and apply another list based on the list style.
 List list3 = doc.getLists().add(listStyle);
 builder.getListFormat().setList(list3);
 builder.writeln("Item 1");
 builder.writeln("Item 2");
 builder.getListFormat().removeNumbers();

 builder.getDocument().save(getArtifactsDir() + "Lists.CreateAndUseListStyle.docx");
 
```

**Returns:**
[List](../../com.aspose.words/list/) - The list that defines formatting of this list style.
### getListFormat() {#getListFormat}
```
public ListFormat getListFormat()
```


Bietet Zugriff auf die Listformatierungseigenschaften eines Absatzstils.

 **Remarks:** 

Diese Eigenschaft ist nur für Absatzstile gültig. Für andere Stiltypen gibt diese Eigenschaft null zurück.

 **Examples:** 

Zeigt, wie man einen Absatzstil mit Listformatierung erstellt und verwendet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a custom paragraph style.
 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle1");
 style.getFont().setSize(24.0);
 style.getFont().setName("Verdana");
 style.getParagraphFormat().setSpaceAfter(12.0);

 // Create a list and make sure the paragraphs that use this style will use this list.
 style.getListFormat().setList(doc.getLists().add(ListTemplate.BULLET_DEFAULT));
 style.getListFormat().setListLevelNumber(0);

 // Apply the paragraph style to the document builder's current paragraph, and then add some text.
 builder.getParagraphFormat().setStyle(style);
 builder.writeln("Hello World: MyStyle1, bulleted list.");

 // Change the document builder's style to one that has no list formatting and write another paragraph.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));
 builder.writeln("Hello World: Normal.");

 builder.getDocument().save(getArtifactsDir() + "Styles.ParagraphStyleBulletedList.docx");
 
```

**Returns:**
[ListFormat](../../com.aspose.words/listformat/) - The corresponding [ListFormat](../../com.aspose.words/listformat/) value.
### getLocked() {#getLocked}
```
public boolean getLocked()
```


Gibt an, ob dieser Stil gesperrt ist.

 **Examples:** 

Zeigt, wie ein Stil gesperrt wird.

```

 Document doc = new Document();

 Style styleHeading1 = doc.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1);
 if (!styleHeading1.getLocked())
     styleHeading1.setLocked(true);

 doc.save(getArtifactsDir() + "Styles.LockStyle.docx");
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getName() {#getName}
```
public String getName()
```


Liefert den Namen des Stils.

 **Remarks:** 

Darf nicht leer sein.

Wenn bereits ein Stil mit diesem Namen in der Sammlung existiert, wird dieser Stil ihn überschreiben. Alle betroffenen Knoten verweisen auf den neuen Stil.

 **Examples:** 

Zeigt, wie auf die Stilsammlung eines Dokuments zugegriffen wird.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
java.lang.String - Der Name des Stils.
### getNextParagraphStyleName() {#getNextParagraphStyleName}
```
public String getNextParagraphStyleName()
```


Liest/setzt den Namen des Stils, der automatisch auf einen neuen Absatz angewendet wird, der nach einem mit dem angegebenen Stil formatierten Absatz eingefügt wird.

 **Remarks:** 

Diese Eigenschaft wird von Aspose.Words nicht verwendet. Der nächste Absatzstil wird nur automatisch angewendet, wenn Sie das Dokument in MS Word bearbeiten.

 **Examples:** 

Zeigt, wie auf die Stilsammlung eines Dokuments zugegriffen wird.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
java.lang.String - Der entsprechende java.lang.String-Wert.
### getParagraphFormat() {#getParagraphFormat}
```
public ParagraphFormat getParagraphFormat()
```


Liefert die Absatzformatierung des Stils.

 **Remarks:** 

Für Zeichen- und Listenvorlagen gibt diese Eigenschaft null zurück.

 **Examples:** 

Zeigt, wie man einen Absatzstil mit Listformatierung erstellt und verwendet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a custom paragraph style.
 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle1");
 style.getFont().setSize(24.0);
 style.getFont().setName("Verdana");
 style.getParagraphFormat().setSpaceAfter(12.0);

 // Create a list and make sure the paragraphs that use this style will use this list.
 style.getListFormat().setList(doc.getLists().add(ListTemplate.BULLET_DEFAULT));
 style.getListFormat().setListLevelNumber(0);

 // Apply the paragraph style to the document builder's current paragraph, and then add some text.
 builder.getParagraphFormat().setStyle(style);
 builder.writeln("Hello World: MyStyle1, bulleted list.");

 // Change the document builder's style to one that has no list formatting and write another paragraph.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));
 builder.writeln("Hello World: Normal.");

 builder.getDocument().save(getArtifactsDir() + "Styles.ParagraphStyleBulletedList.docx");
 
```

**Returns:**
[ParagraphFormat](../../com.aspose.words/paragraphformat/) - The paragraph formatting of the style.
### getPriority() {#getPriority}
```
public int getPriority()
```


Liest/setzt den ganzzahligen Wert, der die Priorität für die Sortierung der Stile im Styles task pane darstellt.

 **Examples:** 

Zeigt, wie man einen Stil priorisiert und ausblendet.

```

 Document doc = new Document();
 Style styleTitle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.SUBTITLE);

 if (styleTitle.getPriority() == 9)
     styleTitle.setPriority(10);

 if (!styleTitle.getUnhideWhenUsed())
     styleTitle.setUnhideWhenUsed(true);

 if (styleTitle.getSemiHidden())
     styleTitle.setSemiHidden(true);

 doc.save(getArtifactsDir() + "Styles.StylePriority.docx");
 
```

**Returns:**
int - Der entsprechende int-Wert.
### getSemiHidden() {#getSemiHidden}
```
public boolean getSemiHidden()
```


Liest/setzt, ob der Stil in der Styles-Galerie und im Styles task pane ausgeblendet wird.

 **Examples:** 

Zeigt, wie man einen Stil priorisiert und ausblendet.

```

 Document doc = new Document();
 Style styleTitle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.SUBTITLE);

 if (styleTitle.getPriority() == 9)
     styleTitle.setPriority(10);

 if (!styleTitle.getUnhideWhenUsed())
     styleTitle.setUnhideWhenUsed(true);

 if (styleTitle.getSemiHidden())
     styleTitle.setSemiHidden(true);

 doc.save(getArtifactsDir() + "Styles.StylePriority.docx");
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getStyleIdentifier() {#getStyleIdentifier}
```
public int getStyleIdentifier()
```


Liefert den sprachunabhängigen Stil-Identifikator für einen integrierten Stil.

 **Remarks:** 

Für benutzerdefinierte (eigene) Stile gibt diese Eigenschaft [StyleIdentifier.USER](../../com.aspose.words/styleidentifier/\#USER) zurück.

 **Examples:** 

Zeigt, wie man die Position des rechten Tabstopps in TOC‑bezogenen Absätzen ändert.

```

 Document doc = new Document(getMyDir() + "Table of contents.docx");

 // Iterate through all paragraphs with TOC result-based styles; this is any style between TOC and TOC9.
 for (Paragraph para : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     if (para.getParagraphFormat().getStyle().getStyleIdentifier() >= StyleIdentifier.TOC_1
             && para.getParagraphFormat().getStyle().getStyleIdentifier() <= StyleIdentifier.TOC_9) {
         // Get the first tab used in this paragraph, this should be the tab used to align the page numbers.
         TabStop tab = para.getParagraphFormat().getTabStops().get(0);

         // Replace the first default tab, stop with a custom tab stop.
         para.getParagraphFormat().getTabStops().removeByPosition(tab.getPosition());
         para.getParagraphFormat().getTabStops().add(tab.getPosition() - 50.0, tab.getAlignment(), tab.getLeader());
     }
 }

 doc.save(getArtifactsDir() + "Styles.ChangeTocsTabStops.docx");
 
```

**Returns:**
int - Der lokalisierungsunabhängige Stilbezeichner für einen integrierten Stil. Der zurückgegebene Wert ist einer der Konstanten von [StyleIdentifier](../../com.aspose.words/styleidentifier/).
### getStyles() {#getStyles}
```
public StyleCollection getStyles()
```


Liefert die Sammlung von Stilen, zu denen dieser Stil gehört.

 **Examples:** 

Zeigt, wie auf die Stilsammlung eines Dokuments zugegriffen wird.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
[StyleCollection](../../com.aspose.words/stylecollection/) - The collection of styles this style belongs to.
### getType() {#getType}
```
public int getType()
```


Ermittelt den Stiltyp (Absatz oder Zeichen).

 **Examples:** 

Zeigt, wie auf die Stilsammlung eines Dokuments zugegriffen wird.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
int - Der Stiltyp (Absatz oder Zeichen). Der zurückgegebene Wert ist einer der Konstanten von [StyleType](../../com.aspose.words/styletype/).
### getUnhideWhenUsed() {#getUnhideWhenUsed}
```
public boolean getUnhideWhenUsed()
```


Liest/legt fest, ob der im aktuellen Dokument verwendete Stil aus der Stilegalerie und dem Stile‑Task‑Paneel wieder eingeblendet wird. Wahr, wenn der verwendete Stil in der Stilegalerie angezeigt werden soll.

 **Examples:** 

Zeigt, wie man einen Stil priorisiert und ausblendet.

```

 Document doc = new Document();
 Style styleTitle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.SUBTITLE);

 if (styleTitle.getPriority() == 9)
     styleTitle.setPriority(10);

 if (!styleTitle.getUnhideWhenUsed())
     styleTitle.setUnhideWhenUsed(true);

 if (styleTitle.getSemiHidden())
     styleTitle.setSemiHidden(true);

 doc.save(getArtifactsDir() + "Styles.StylePriority.docx");
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### isHeading() {#isHeading}
```
public boolean isHeading()
```


Wahr, wenn der Stil einer der integrierten Überschriftsstile ist.

 **Examples:** 

Zeigt, wie auf die Stilsammlung eines Dokuments zugegriffen wird.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### isQuickStyle() {#isQuickStyle}
```
public boolean isQuickStyle()
```


Gibt an, ob dieser Stil in der Schnellformatvorlagen-Galerie in der MS‑Word‑Benutzeroberfläche angezeigt wird.

 **Examples:** 

Zeigt, wie auf die Stilsammlung eines Dokuments zugegriffen wird.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### isQuickStyle(boolean value) {#isQuickStyle-boolean}
```
public void isQuickStyle(boolean value)
```


Gibt an, ob dieser Stil in der Schnellformatvorlagen-Galerie in der MS‑Word‑Benutzeroberfläche angezeigt wird.

 **Examples:** 

Zeigt, wie auf die Stilsammlung eines Dokuments zugegriffen wird.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### remove() {#remove}
```
public void remove()
```


Entfernt den angegebenen Stil aus dem Dokument.

 **Remarks:** 

Das Entfernen von Stilen hat folgende Auswirkungen auf das Dokumentmodell:

 *  All references to the style are removed from corresponding paragraphs, runs and tables.
 *  If base style is removed its formatting is moved to child styles.
 *  If style to be deleted has a linked style, then both of these are deleted.

 **Examples:** 

Zeigt, wie man einen benutzerdefinierten Stil erstellt und anwendet.

```

 Document doc = new Document();

 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 style.getFont().setName("Times New Roman");
 style.getFont().setSize(16.0);
 style.getFont().setColor(Color.magenta);
 // Automatically redefine style.
 style.setAutomaticallyUpdate(true);

 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply one of the styles from the document to the paragraph that the document builder is creating.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle"));
 builder.writeln("Hello world!");

 Style firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 Assert.assertEquals(style, firstParagraphStyle);

 // Remove our custom style from the document's styles collection.
 doc.getStyles().get("MyStyle").remove();

 firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 // Any text that used a removed style reverts to the default formatting.
 Assert.assertFalse(IterableUtils.matchesAny(doc.getStyles(), s -> s.getName() == "MyStyle"));
 Assert.assertEquals("Times New Roman", firstParagraphStyle.getFont().getName());
 Assert.assertEquals(12.0d, firstParagraphStyle.getFont().getSize());
 Assert.assertEquals(0, firstParagraphStyle.getFont().getColor().getRGB());
 
```

### removeParaAttr(int key) {#removeParaAttr-int}
```
public void removeParaAttr(int key)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |

### removeRunAttr(int key) {#removeRunAttr-int}
```
public void removeRunAttr(int key)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |

### setAutomaticallyUpdate(boolean value) {#setAutomaticallyUpdate-boolean}
```
public void setAutomaticallyUpdate(boolean value)
```


Gibt an, ob dieser Stil basierend auf dem entsprechenden Wert automatisch neu definiert wird.

 **Remarks:** 

Wenn der Eigenschaftswert auf true gesetzt ist, definiert MS Word den aktuellen Stil automatisch neu, sobald die entsprechende Absatzformatierung geändert wurde.

Die Eigenschaft AutomaticallyUpdate gilt nur für Absatzstile.

Der Standardwert ist  false .

 **Examples:** 

Zeigt, wie man einen benutzerdefinierten Stil erstellt und anwendet.

```

 Document doc = new Document();

 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 style.getFont().setName("Times New Roman");
 style.getFont().setSize(16.0);
 style.getFont().setColor(Color.magenta);
 // Automatically redefine style.
 style.setAutomaticallyUpdate(true);

 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply one of the styles from the document to the paragraph that the document builder is creating.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle"));
 builder.writeln("Hello world!");

 Style firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 Assert.assertEquals(style, firstParagraphStyle);

 // Remove our custom style from the document's styles collection.
 doc.getStyles().get("MyStyle").remove();

 firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 // Any text that used a removed style reverts to the default formatting.
 Assert.assertFalse(IterableUtils.matchesAny(doc.getStyles(), s -> s.getName() == "MyStyle"));
 Assert.assertEquals("Times New Roman", firstParagraphStyle.getFont().getName());
 Assert.assertEquals(12.0d, firstParagraphStyle.getFont().getSize());
 Assert.assertEquals(0, firstParagraphStyle.getFont().getColor().getRGB());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setBaseStyleName(String value) {#setBaseStyleName-java.lang.String}
```
public void setBaseStyleName(String value)
```


Liest/setzt den Namen des Stils, auf dem dieser Stil basiert.

 **Remarks:** 

Dies ist ein leerer String, wenn der Stil nicht auf einem anderen Stil basiert, und er kann auf einen leeren String gesetzt werden.

 **Examples:** 

Zeigt, wie Stil‑Aliase verwendet werden.

```

 Document doc = new Document(getMyDir() + "Style with alias.docx");

 // This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
 // If a style's name has multiple values separated by commas, each clause is a separate alias.
 Style style = doc.getStyles().get("MyStyle");
 Assert.assertEquals(new String[]{"MyStyle Alias 1", "MyStyle Alias 2"}, style.getAliases());
 Assert.assertEquals("Title", style.getBaseStyleName());
 Assert.assertEquals("MyStyle Char", style.getLinkedStyleName());

 // We can reference a style using its alias, as well as its name.
 Assert.assertEquals(doc.getStyles().get("MyStyle Alias 1"), doc.getStyles().get("MyStyle Alias 2"));

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 1"));
 builder.writeln("Hello world!");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 2"));
 builder.write("Hello again!");

 Assert.assertEquals(doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle(),
         doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der entsprechende java.lang.String-Wert. |

### setLinkedStyleName(String value) {#setLinkedStyleName-java.lang.String}
```
public void setLinkedStyleName(String value)
```


Liest/legt den Namen des mit diesem verknüpften [Style](../../com.aspose.words/style/) fest. Gibt einen leeren String zurück, wenn keine Stile verknüpft sind.

 **Remarks:** 

Es ist nur erlaubt, den Absatzstil mit dem Zeichenstil zu verknüpfen und umgekehrt.

Das Festlegen von LinkedStyleName für den aktuellen Stil führt automatisch dazu, dass LinkedStyleName für den verknüpften Stil gesetzt wird.

Das Zuweisen eines leeren Strings entspricht dem Aufheben der Verknüpfung des zuvor verknüpften Stils.

 **Examples:** 

Zeigt, wie Stil‑Aliase verwendet werden.

```

 Document doc = new Document(getMyDir() + "Style with alias.docx");

 // This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
 // If a style's name has multiple values separated by commas, each clause is a separate alias.
 Style style = doc.getStyles().get("MyStyle");
 Assert.assertEquals(new String[]{"MyStyle Alias 1", "MyStyle Alias 2"}, style.getAliases());
 Assert.assertEquals("Title", style.getBaseStyleName());
 Assert.assertEquals("MyStyle Char", style.getLinkedStyleName());

 // We can reference a style using its alias, as well as its name.
 Assert.assertEquals(doc.getStyles().get("MyStyle Alias 1"), doc.getStyles().get("MyStyle Alias 2"));

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 1"));
 builder.writeln("Hello world!");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 2"));
 builder.write("Hello again!");

 Assert.assertEquals(doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle(),
         doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle());
 
```

Zeigt, wie Stile untereinander verknüpft werden.

```

 Document doc = new Document();

 Style styleHeading1 = doc.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1);

 Style styleHeading1Char = doc.getStyles().add(StyleType.CHARACTER, "Heading 1 Char");
 styleHeading1Char.getFont().setName("Verdana");
 styleHeading1Char.getFont().setBold(true);
 styleHeading1Char.getFont().getBorder().setLineStyle(LineStyle.DOT);
 styleHeading1Char.getFont().getBorder().setLineWidth(15.0);

 styleHeading1.setLinkedStyleName("Heading 1 Char");

 Assert.assertEquals("Heading 1 Char", styleHeading1.getLinkedStyleName());
 Assert.assertEquals("Heading 1", styleHeading1Char.getLinkedStyleName());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der entsprechende java.lang.String-Wert. |

### setLocked(boolean value) {#setLocked-boolean}
```
public void setLocked(boolean value)
```


Gibt an, ob dieser Stil gesperrt ist.

 **Examples:** 

Zeigt, wie ein Stil gesperrt wird.

```

 Document doc = new Document();

 Style styleHeading1 = doc.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1);
 if (!styleHeading1.getLocked())
     styleHeading1.setLocked(true);

 doc.save(getArtifactsDir() + "Styles.LockStyle.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Legt den Namen des Stils fest.

 **Remarks:** 

Darf nicht leer sein.

Wenn bereits ein Stil mit diesem Namen in der Sammlung existiert, wird dieser Stil ihn überschreiben. Alle betroffenen Knoten verweisen auf den neuen Stil.

 **Examples:** 

Zeigt, wie auf die Stilsammlung eines Dokuments zugegriffen wird.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der Name des Stils. |

### setNextParagraphStyleName(String value) {#setNextParagraphStyleName-java.lang.String}
```
public void setNextParagraphStyleName(String value)
```


Liest/setzt den Namen des Stils, der automatisch auf einen neuen Absatz angewendet wird, der nach einem mit dem angegebenen Stil formatierten Absatz eingefügt wird.

 **Remarks:** 

Diese Eigenschaft wird von Aspose.Words nicht verwendet. Der nächste Absatzstil wird nur automatisch angewendet, wenn Sie das Dokument in MS Word bearbeiten.

 **Examples:** 

Zeigt, wie auf die Stilsammlung eines Dokuments zugegriffen wird.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der entsprechende java.lang.String-Wert. |

### setParaAttr(int key, Object value) {#setParaAttr-int-java.lang.Object}
```
public void setParaAttr(int key, Object value)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |
| Wert | java.lang.Object |  |

### setPriority(int value) {#setPriority-int}
```
public void setPriority(int value)
```


Liest/setzt den ganzzahligen Wert, der die Priorität für die Sortierung der Stile im Styles task pane darstellt.

 **Examples:** 

Zeigt, wie man einen Stil priorisiert und ausblendet.

```

 Document doc = new Document();
 Style styleTitle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.SUBTITLE);

 if (styleTitle.getPriority() == 9)
     styleTitle.setPriority(10);

 if (!styleTitle.getUnhideWhenUsed())
     styleTitle.setUnhideWhenUsed(true);

 if (styleTitle.getSemiHidden())
     styleTitle.setSemiHidden(true);

 doc.save(getArtifactsDir() + "Styles.StylePriority.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Der entsprechende  int  Wert. |

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object}
```
public void setRunAttr(int key, Object value)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| key | int |  |
| Wert | java.lang.Object |  |

### setSemiHidden(boolean value) {#setSemiHidden-boolean}
```
public void setSemiHidden(boolean value)
```


Liest/setzt, ob der Stil in der Styles-Galerie und im Styles task pane ausgeblendet wird.

 **Examples:** 

Zeigt, wie man einen Stil priorisiert und ausblendet.

```

 Document doc = new Document();
 Style styleTitle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.SUBTITLE);

 if (styleTitle.getPriority() == 9)
     styleTitle.setPriority(10);

 if (!styleTitle.getUnhideWhenUsed())
     styleTitle.setUnhideWhenUsed(true);

 if (styleTitle.getSemiHidden())
     styleTitle.setSemiHidden(true);

 doc.save(getArtifactsDir() + "Styles.StylePriority.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setUnhideWhenUsed(boolean value) {#setUnhideWhenUsed-boolean}
```
public void setUnhideWhenUsed(boolean value)
```


Liest/legt fest, ob der im aktuellen Dokument verwendete Stil aus der Stilegalerie und dem Stile‑Task‑Paneel wieder eingeblendet wird. Wahr, wenn der verwendete Stil in der Stilegalerie angezeigt werden soll.

 **Examples:** 

Zeigt, wie man einen Stil priorisiert und ausblendet.

```

 Document doc = new Document();
 Style styleTitle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.SUBTITLE);

 if (styleTitle.getPriority() == 9)
     styleTitle.setPriority(10);

 if (!styleTitle.getUnhideWhenUsed())
     styleTitle.setUnhideWhenUsed(true);

 if (styleTitle.getSemiHidden())
     styleTitle.setSemiHidden(true);

 doc.save(getArtifactsDir() + "Styles.StylePriority.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

