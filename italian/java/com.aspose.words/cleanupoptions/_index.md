---
title: "CleanupOptions"
linktitle: "CleanupOptions"
second_title: "Aspose.Words per Java"
description: "Consente di specificare le opzioni per la pulizia del documento in Java."
type: docs
weight: 103
url: /it/java/com.aspose.words/cleanupoptions/
---

**Inheritance:**
java.lang.Object
```
public class CleanupOptions
```

Consente di specificare opzioni per la pulizia del documento.

Per saperne di più, visita l'articolo di documentazione [ Clean Up a Document ][Clean Up a Document].

 **Examples:** 

Mostra come rimuovere tutti gli stili personalizzati non utilizzati da un documento.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getDuplicateStyle()](#getDuplicateStyle) | Ottiene/Imposta un flag che indica se gli stili duplicati devono essere rimossi dal documento. |
| [getUnusedBuiltinStyles()](#getUnusedBuiltinStyles) | Specifica che gli stili non utilizzati [Style.getBuiltIn()](../../com.aspose.words/style/#getBuiltIn) devono essere rimossi dal documento. |
| [getUnusedLists()](#getUnusedLists) | Specifica se gli elenchi e le definizioni di elenco non utilizzati devono essere rimossi dal documento. |
| [getUnusedStyles()](#getUnusedStyles) | Specifica se gli stili non utilizzati devono essere rimossi dal documento. |
| [setDuplicateStyle(boolean value)](#setDuplicateStyle-boolean) | Ottiene/Imposta un flag che indica se gli stili duplicati devono essere rimossi dal documento. |
| [setUnusedBuiltinStyles(boolean value)](#setUnusedBuiltinStyles-boolean) | Specifica che gli stili non utilizzati [Style.getBuiltIn()](../../com.aspose.words/style/#getBuiltIn) devono essere rimossi dal documento. |
| [setUnusedLists(boolean value)](#setUnusedLists-boolean) | Specifica se gli elenchi e le definizioni di elenco non utilizzati devono essere rimossi dal documento. |
| [setUnusedStyles(boolean value)](#setUnusedStyles-boolean) | Specifica se gli stili non utilizzati devono essere rimossi dal documento. |
### getDuplicateStyle() {#getDuplicateStyle}
```
public boolean getDuplicateStyle()
```


Ottiene/imposta un flag che indica se gli stili duplicati devono essere rimossi dal documento. Il valore predefinito è false.

 **Examples:** 

Mostra come rimuovere gli stili duplicati dal documento.

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
boolean - Il valore booleano corrispondente.
### getUnusedBuiltinStyles() {#getUnusedBuiltinStyles}
```
public boolean getUnusedBuiltinStyles()
```


Specifica che gli stili non utilizzati [Style.getBuiltIn()](../../com.aspose.words/style/#getBuiltIn) devono essere rimossi dal documento.

 **Examples:** 

Mostra come rimuovere tutti gli stili personalizzati non utilizzati da un documento.

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
boolean - Il valore booleano corrispondente.
### getUnusedLists() {#getUnusedLists}
```
public boolean getUnusedLists()
```


Specifica se le liste inutilizzate e le definizioni di elenco devono essere rimosse dal documento. Il valore predefinito è true.

 **Examples:** 

Mostra come rimuovere tutti gli stili personalizzati non utilizzati da un documento.

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
boolean - Il valore booleano corrispondente.
### getUnusedStyles() {#getUnusedStyles}
```
public boolean getUnusedStyles()
```


Specifica se gli stili inutilizzati devono essere rimossi dal documento. Il valore predefinito è true.

 **Examples:** 

Mostra come rimuovere tutti gli stili personalizzati non utilizzati da un documento.

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
boolean - Il valore booleano corrispondente.
### setDuplicateStyle(boolean value) {#setDuplicateStyle-boolean}
```
public void setDuplicateStyle(boolean value)
```


Ottiene/imposta un flag che indica se gli stili duplicati devono essere rimossi dal documento. Il valore predefinito è false.

 **Examples:** 

Mostra come rimuovere gli stili duplicati dal documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setUnusedBuiltinStyles(boolean value) {#setUnusedBuiltinStyles-boolean}
```
public void setUnusedBuiltinStyles(boolean value)
```


Specifica che gli stili non utilizzati [Style.getBuiltIn()](../../com.aspose.words/style/#getBuiltIn) devono essere rimossi dal documento.

 **Examples:** 

Mostra come rimuovere tutti gli stili personalizzati non utilizzati da un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setUnusedLists(boolean value) {#setUnusedLists-boolean}
```
public void setUnusedLists(boolean value)
```


Specifica se le liste inutilizzate e le definizioni di elenco devono essere rimosse dal documento. Il valore predefinito è true.

 **Examples:** 

Mostra come rimuovere tutti gli stili personalizzati non utilizzati da un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

### setUnusedStyles(boolean value) {#setUnusedStyles-boolean}
```
public void setUnusedStyles(boolean value)
```


Specifica se gli stili inutilizzati devono essere rimossi dal documento. Il valore predefinito è true.

 **Examples:** 

Mostra come rimuovere tutti gli stili personalizzati non utilizzati da un documento.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | boolean | Il valore booleano corrispondente. |

