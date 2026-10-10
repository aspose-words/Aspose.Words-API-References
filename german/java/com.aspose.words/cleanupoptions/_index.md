---
title: "CleanupOptions"
linktitle: "CleanupOptions"
second_title: "Aspose.Words für Java"
description: "Ermöglicht das Festlegen von Optionen für die Dokumentenbereinigung in Java."
type: docs
weight: 103
url: /de/java/com.aspose.words/cleanupoptions/
---

**Inheritance:**
java.lang.Object
```
public class CleanupOptions
```

Ermöglicht die Angabe von Optionen für die Dokumentenreinigung.

Weitere Informationen finden Sie im Dokumentationsartikel [ Clean Up a Document ][Clean Up a Document].

 **Examples:** 

Zeigt, wie alle ungenutzten benutzerdefinierten Stile aus einem Dokument entfernt werden.

```

 Document doc = new Document();

 doc.getStyles().add(StyleType.LIST, "MyListStyle1");
 doc.getStyles().add(StyleType.LIST, "MyListStyle2");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle1");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle2");

 // Combined with the built-in styles, the document now has eight styles.
 // A custom style is marked as "used" while there is any text within the document
 // formatted in that style. This means that the 4 styles we added are currently unused.
 Assert.assertEquals(8, doc.getStyles().getCount());

 // Apply a custom character style, and then a custom list style. Doing so will mark them as "used".
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getFont().setStyle(doc.getStyles().get("MyParagraphStyle1"));
 builder.writeln("Hello world!");

 List docList = doc.getLists().add(doc.getStyles().get("MyListStyle1"));
 builder.getListFormat().setList(docList);
 builder.writeln("Item 1");
 builder.writeln("Item 2");

 // Now, there is one unused character style and one unused list style.
 // The Cleanup() method, when configured with a CleanupOptions object, can target unused styles and remove them.
 CleanupOptions cleanupOptions = new CleanupOptions();
 cleanupOptions.setUnusedLists(true);
 cleanupOptions.setUnusedStyles(true);
 cleanupOptions.setUnusedBuiltinStyles(true);

 doc.cleanup(cleanupOptions);

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Removing every node that a custom style is applied to marks it as "unused" again.
 // Rerun the Cleanup method to remove them.
 doc.getFirstSection().getBody().removeAllChildren();
 doc.cleanup(cleanupOptions);

 Assert.assertEquals(2, doc.getStyles().getCount());
 
```


[Clean Up a Document]: https://docs.aspose.com/words/java/clean-up-a-document/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getDuplicateStyle()](#getDuplicateStyle) | Liest/Setzt ein Flag, das angibt, ob doppelte Formatvorlagen aus dem Dokument entfernt werden sollen. |
| [getUnusedBuiltinStyles()](#getUnusedBuiltinStyles) | Gibt an, dass nicht verwendete [Style.getBuiltIn()](../../com.aspose.words/style/\\#getBuiltIn)-Stile aus dem Dokument entfernt werden sollen. |
| [getUnusedLists()](#getUnusedLists) | Gibt an, ob nicht verwendete Listen und Listendefinitionen aus dem Dokument entfernt werden sollen. |
| [getUnusedStyles()](#getUnusedStyles) | Gibt an, ob nicht verwendete Formatvorlagen aus dem Dokument entfernt werden sollen. |
| [setDuplicateStyle(boolean value)](#setDuplicateStyle-boolean) | Liest/Setzt ein Flag, das angibt, ob doppelte Formatvorlagen aus dem Dokument entfernt werden sollen. |
| [setUnusedBuiltinStyles(boolean value)](#setUnusedBuiltinStyles-boolean) | Gibt an, dass nicht verwendete [Style.getBuiltIn()](../../com.aspose.words/style/\\#getBuiltIn)-Stile aus dem Dokument entfernt werden sollen. |
| [setUnusedLists(boolean value)](#setUnusedLists-boolean) | Gibt an, ob nicht verwendete Listen und Listendefinitionen aus dem Dokument entfernt werden sollen. |
| [setUnusedStyles(boolean value)](#setUnusedStyles-boolean) | Gibt an, ob nicht verwendete Formatvorlagen aus dem Dokument entfernt werden sollen. |
### getDuplicateStyle() {#getDuplicateStyle}
```
public boolean getDuplicateStyle()
```


Liest/Setzt ein Flag, das angibt, ob doppelte Formatvorlagen aus dem Dokument entfernt werden sollen. Standardwert ist false.

 **Examples:** 

Zeigt, wie du doppelte Formatvorlagen aus dem Dokument entfernst.

```

 Document doc = new Document();

 // Add two styles to the document with identical properties,
 // but different names. The second style is considered a duplicate of the first.
 Style myStyle = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle1");
 myStyle.getFont().setSize(14.0);
 myStyle.getFont().setName("Courier New");
 myStyle.getFont().setColor(Color.BLUE);

 Style duplicateStyle = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle2");
 duplicateStyle.getFont().setSize(14.0);
 duplicateStyle.getFont().setName("Courier New");
 duplicateStyle.getFont().setColor(Color.BLUE);

 Assert.assertEquals(6, doc.getStyles().getCount());

 // Apply both styles to different paragraphs within the document.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getParagraphFormat().setStyleName(myStyle.getName());
 builder.writeln("Hello world!");

 builder.getParagraphFormat().setStyleName(duplicateStyle.getName());
 builder.writeln("Hello again!");

 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 Assert.assertEquals(myStyle, paragraphs.get(0).getParagraphFormat().getStyle());
 Assert.assertEquals(duplicateStyle, paragraphs.get(1).getParagraphFormat().getStyle());

 // Configure a CleanOptions object, then call the Cleanup method to substitute all duplicate styles
 // with the original and remove the duplicates from the document.
 CleanupOptions cleanupOptions = new CleanupOptions();
 cleanupOptions.setDuplicateStyle(true);

 doc.cleanup(cleanupOptions);

 Assert.assertEquals(5, doc.getStyles().getCount());
 Assert.assertEquals(myStyle, paragraphs.get(0).getParagraphFormat().getStyle());
 Assert.assertEquals(myStyle, paragraphs.get(1).getParagraphFormat().getStyle());
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getUnusedBuiltinStyles() {#getUnusedBuiltinStyles}
```
public boolean getUnusedBuiltinStyles()
```


Gibt an, dass nicht verwendete [Style.getBuiltIn()](../../com.aspose.words/style/\\#getBuiltIn)-Stile aus dem Dokument entfernt werden sollen.

 **Examples:** 

Zeigt, wie alle ungenutzten benutzerdefinierten Stile aus einem Dokument entfernt werden.

```

 Document doc = new Document();

 doc.getStyles().add(StyleType.LIST, "MyListStyle1");
 doc.getStyles().add(StyleType.LIST, "MyListStyle2");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle1");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle2");

 // Combined with the built-in styles, the document now has eight styles.
 // A custom style is marked as "used" while there is any text within the document
 // formatted in that style. This means that the 4 styles we added are currently unused.
 Assert.assertEquals(8, doc.getStyles().getCount());

 // Apply a custom character style, and then a custom list style. Doing so will mark them as "used".
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getFont().setStyle(doc.getStyles().get("MyParagraphStyle1"));
 builder.writeln("Hello world!");

 List docList = doc.getLists().add(doc.getStyles().get("MyListStyle1"));
 builder.getListFormat().setList(docList);
 builder.writeln("Item 1");
 builder.writeln("Item 2");

 // Now, there is one unused character style and one unused list style.
 // The Cleanup() method, when configured with a CleanupOptions object, can target unused styles and remove them.
 CleanupOptions cleanupOptions = new CleanupOptions();
 cleanupOptions.setUnusedLists(true);
 cleanupOptions.setUnusedStyles(true);
 cleanupOptions.setUnusedBuiltinStyles(true);

 doc.cleanup(cleanupOptions);

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Removing every node that a custom style is applied to marks it as "unused" again.
 // Rerun the Cleanup method to remove them.
 doc.getFirstSection().getBody().removeAllChildren();
 doc.cleanup(cleanupOptions);

 Assert.assertEquals(2, doc.getStyles().getCount());
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getUnusedLists() {#getUnusedLists}
```
public boolean getUnusedLists()
```


Gibt an, ob nicht verwendete Listen und Listendefinitionen aus dem Dokument entfernt werden sollen. Standardwert ist true.

 **Examples:** 

Zeigt, wie alle ungenutzten benutzerdefinierten Stile aus einem Dokument entfernt werden.

```

 Document doc = new Document();

 doc.getStyles().add(StyleType.LIST, "MyListStyle1");
 doc.getStyles().add(StyleType.LIST, "MyListStyle2");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle1");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle2");

 // Combined with the built-in styles, the document now has eight styles.
 // A custom style is marked as "used" while there is any text within the document
 // formatted in that style. This means that the 4 styles we added are currently unused.
 Assert.assertEquals(8, doc.getStyles().getCount());

 // Apply a custom character style, and then a custom list style. Doing so will mark them as "used".
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getFont().setStyle(doc.getStyles().get("MyParagraphStyle1"));
 builder.writeln("Hello world!");

 List docList = doc.getLists().add(doc.getStyles().get("MyListStyle1"));
 builder.getListFormat().setList(docList);
 builder.writeln("Item 1");
 builder.writeln("Item 2");

 // Now, there is one unused character style and one unused list style.
 // The Cleanup() method, when configured with a CleanupOptions object, can target unused styles and remove them.
 CleanupOptions cleanupOptions = new CleanupOptions();
 cleanupOptions.setUnusedLists(true);
 cleanupOptions.setUnusedStyles(true);
 cleanupOptions.setUnusedBuiltinStyles(true);

 doc.cleanup(cleanupOptions);

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Removing every node that a custom style is applied to marks it as "unused" again.
 // Rerun the Cleanup method to remove them.
 doc.getFirstSection().getBody().removeAllChildren();
 doc.cleanup(cleanupOptions);

 Assert.assertEquals(2, doc.getStyles().getCount());
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### getUnusedStyles() {#getUnusedStyles}
```
public boolean getUnusedStyles()
```


Gibt an, ob nicht verwendete Formatvorlagen aus dem Dokument entfernt werden sollen. Standardwert ist true.

 **Examples:** 

Zeigt, wie alle ungenutzten benutzerdefinierten Stile aus einem Dokument entfernt werden.

```

 Document doc = new Document();

 doc.getStyles().add(StyleType.LIST, "MyListStyle1");
 doc.getStyles().add(StyleType.LIST, "MyListStyle2");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle1");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle2");

 // Combined with the built-in styles, the document now has eight styles.
 // A custom style is marked as "used" while there is any text within the document
 // formatted in that style. This means that the 4 styles we added are currently unused.
 Assert.assertEquals(8, doc.getStyles().getCount());

 // Apply a custom character style, and then a custom list style. Doing so will mark them as "used".
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getFont().setStyle(doc.getStyles().get("MyParagraphStyle1"));
 builder.writeln("Hello world!");

 List docList = doc.getLists().add(doc.getStyles().get("MyListStyle1"));
 builder.getListFormat().setList(docList);
 builder.writeln("Item 1");
 builder.writeln("Item 2");

 // Now, there is one unused character style and one unused list style.
 // The Cleanup() method, when configured with a CleanupOptions object, can target unused styles and remove them.
 CleanupOptions cleanupOptions = new CleanupOptions();
 cleanupOptions.setUnusedLists(true);
 cleanupOptions.setUnusedStyles(true);
 cleanupOptions.setUnusedBuiltinStyles(true);

 doc.cleanup(cleanupOptions);

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Removing every node that a custom style is applied to marks it as "unused" again.
 // Rerun the Cleanup method to remove them.
 doc.getFirstSection().getBody().removeAllChildren();
 doc.cleanup(cleanupOptions);

 Assert.assertEquals(2, doc.getStyles().getCount());
 
```

**Returns:**
boolean - Der entsprechende  boolean  Wert.
### setDuplicateStyle(boolean value) {#setDuplicateStyle-boolean}
```
public void setDuplicateStyle(boolean value)
```


Liest/Setzt ein Flag, das angibt, ob doppelte Formatvorlagen aus dem Dokument entfernt werden sollen. Standardwert ist false.

 **Examples:** 

Zeigt, wie du doppelte Formatvorlagen aus dem Dokument entfernst.

```

 Document doc = new Document();

 // Add two styles to the document with identical properties,
 // but different names. The second style is considered a duplicate of the first.
 Style myStyle = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle1");
 myStyle.getFont().setSize(14.0);
 myStyle.getFont().setName("Courier New");
 myStyle.getFont().setColor(Color.BLUE);

 Style duplicateStyle = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle2");
 duplicateStyle.getFont().setSize(14.0);
 duplicateStyle.getFont().setName("Courier New");
 duplicateStyle.getFont().setColor(Color.BLUE);

 Assert.assertEquals(6, doc.getStyles().getCount());

 // Apply both styles to different paragraphs within the document.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getParagraphFormat().setStyleName(myStyle.getName());
 builder.writeln("Hello world!");

 builder.getParagraphFormat().setStyleName(duplicateStyle.getName());
 builder.writeln("Hello again!");

 ParagraphCollection paragraphs = doc.getFirstSection().getBody().getParagraphs();

 Assert.assertEquals(myStyle, paragraphs.get(0).getParagraphFormat().getStyle());
 Assert.assertEquals(duplicateStyle, paragraphs.get(1).getParagraphFormat().getStyle());

 // Configure a CleanOptions object, then call the Cleanup method to substitute all duplicate styles
 // with the original and remove the duplicates from the document.
 CleanupOptions cleanupOptions = new CleanupOptions();
 cleanupOptions.setDuplicateStyle(true);

 doc.cleanup(cleanupOptions);

 Assert.assertEquals(5, doc.getStyles().getCount());
 Assert.assertEquals(myStyle, paragraphs.get(0).getParagraphFormat().getStyle());
 Assert.assertEquals(myStyle, paragraphs.get(1).getParagraphFormat().getStyle());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setUnusedBuiltinStyles(boolean value) {#setUnusedBuiltinStyles-boolean}
```
public void setUnusedBuiltinStyles(boolean value)
```


Gibt an, dass nicht verwendete [Style.getBuiltIn()](../../com.aspose.words/style/\\#getBuiltIn)-Stile aus dem Dokument entfernt werden sollen.

 **Examples:** 

Zeigt, wie alle ungenutzten benutzerdefinierten Stile aus einem Dokument entfernt werden.

```

 Document doc = new Document();

 doc.getStyles().add(StyleType.LIST, "MyListStyle1");
 doc.getStyles().add(StyleType.LIST, "MyListStyle2");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle1");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle2");

 // Combined with the built-in styles, the document now has eight styles.
 // A custom style is marked as "used" while there is any text within the document
 // formatted in that style. This means that the 4 styles we added are currently unused.
 Assert.assertEquals(8, doc.getStyles().getCount());

 // Apply a custom character style, and then a custom list style. Doing so will mark them as "used".
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getFont().setStyle(doc.getStyles().get("MyParagraphStyle1"));
 builder.writeln("Hello world!");

 List docList = doc.getLists().add(doc.getStyles().get("MyListStyle1"));
 builder.getListFormat().setList(docList);
 builder.writeln("Item 1");
 builder.writeln("Item 2");

 // Now, there is one unused character style and one unused list style.
 // The Cleanup() method, when configured with a CleanupOptions object, can target unused styles and remove them.
 CleanupOptions cleanupOptions = new CleanupOptions();
 cleanupOptions.setUnusedLists(true);
 cleanupOptions.setUnusedStyles(true);
 cleanupOptions.setUnusedBuiltinStyles(true);

 doc.cleanup(cleanupOptions);

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Removing every node that a custom style is applied to marks it as "unused" again.
 // Rerun the Cleanup method to remove them.
 doc.getFirstSection().getBody().removeAllChildren();
 doc.cleanup(cleanupOptions);

 Assert.assertEquals(2, doc.getStyles().getCount());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setUnusedLists(boolean value) {#setUnusedLists-boolean}
```
public void setUnusedLists(boolean value)
```


Gibt an, ob nicht verwendete Listen und Listendefinitionen aus dem Dokument entfernt werden sollen. Standardwert ist true.

 **Examples:** 

Zeigt, wie alle ungenutzten benutzerdefinierten Stile aus einem Dokument entfernt werden.

```

 Document doc = new Document();

 doc.getStyles().add(StyleType.LIST, "MyListStyle1");
 doc.getStyles().add(StyleType.LIST, "MyListStyle2");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle1");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle2");

 // Combined with the built-in styles, the document now has eight styles.
 // A custom style is marked as "used" while there is any text within the document
 // formatted in that style. This means that the 4 styles we added are currently unused.
 Assert.assertEquals(8, doc.getStyles().getCount());

 // Apply a custom character style, and then a custom list style. Doing so will mark them as "used".
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getFont().setStyle(doc.getStyles().get("MyParagraphStyle1"));
 builder.writeln("Hello world!");

 List docList = doc.getLists().add(doc.getStyles().get("MyListStyle1"));
 builder.getListFormat().setList(docList);
 builder.writeln("Item 1");
 builder.writeln("Item 2");

 // Now, there is one unused character style and one unused list style.
 // The Cleanup() method, when configured with a CleanupOptions object, can target unused styles and remove them.
 CleanupOptions cleanupOptions = new CleanupOptions();
 cleanupOptions.setUnusedLists(true);
 cleanupOptions.setUnusedStyles(true);
 cleanupOptions.setUnusedBuiltinStyles(true);

 doc.cleanup(cleanupOptions);

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Removing every node that a custom style is applied to marks it as "unused" again.
 // Rerun the Cleanup method to remove them.
 doc.getFirstSection().getBody().removeAllChildren();
 doc.cleanup(cleanupOptions);

 Assert.assertEquals(2, doc.getStyles().getCount());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setUnusedStyles(boolean value) {#setUnusedStyles-boolean}
```
public void setUnusedStyles(boolean value)
```


Gibt an, ob nicht verwendete Formatvorlagen aus dem Dokument entfernt werden sollen. Standardwert ist true.

 **Examples:** 

Zeigt, wie alle ungenutzten benutzerdefinierten Stile aus einem Dokument entfernt werden.

```

 Document doc = new Document();

 doc.getStyles().add(StyleType.LIST, "MyListStyle1");
 doc.getStyles().add(StyleType.LIST, "MyListStyle2");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle1");
 doc.getStyles().add(StyleType.CHARACTER, "MyParagraphStyle2");

 // Combined with the built-in styles, the document now has eight styles.
 // A custom style is marked as "used" while there is any text within the document
 // formatted in that style. This means that the 4 styles we added are currently unused.
 Assert.assertEquals(8, doc.getStyles().getCount());

 // Apply a custom character style, and then a custom list style. Doing so will mark them as "used".
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.getFont().setStyle(doc.getStyles().get("MyParagraphStyle1"));
 builder.writeln("Hello world!");

 List docList = doc.getLists().add(doc.getStyles().get("MyListStyle1"));
 builder.getListFormat().setList(docList);
 builder.writeln("Item 1");
 builder.writeln("Item 2");

 // Now, there is one unused character style and one unused list style.
 // The Cleanup() method, when configured with a CleanupOptions object, can target unused styles and remove them.
 CleanupOptions cleanupOptions = new CleanupOptions();
 cleanupOptions.setUnusedLists(true);
 cleanupOptions.setUnusedStyles(true);
 cleanupOptions.setUnusedBuiltinStyles(true);

 doc.cleanup(cleanupOptions);

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Removing every node that a custom style is applied to marks it as "unused" again.
 // Rerun the Cleanup method to remove them.
 doc.getFirstSection().getBody().removeAllChildren();
 doc.cleanup(cleanupOptions);

 Assert.assertEquals(2, doc.getStyles().getCount());
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

