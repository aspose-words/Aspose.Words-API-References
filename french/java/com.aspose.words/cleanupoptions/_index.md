---
title: "CleanupOptions"
linktitle: "CleanupOptions"
second_title: "Aspose.Words pour Java"
description: "Permet de spécifier des options pour le nettoyage de documents en Java."
type: docs
weight: 103
url: /fr/java/com.aspose.words/cleanupoptions/
---

**Inheritance:**
java.lang.Object
```
public class CleanupOptions
```

Permet de spécifier des options pour le nettoyage de documents.

Pour en savoir plus, consultez l'article de documentation [ Clean Up a Document ][Clean Up a Document].

 **Examples:** 

Montre comment supprimer tous les styles personnalisés inutilisés d'un document.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [getDuplicateStyle()](#getDuplicateStyle) | Obtient/definit un indicateur indiquant si les styles en double doivent être supprimés du document. |
| [getUnusedBuiltinStyles()](#getUnusedBuiltinStyles) | Spécifie que les styles inutilisés [Style.getBuiltIn()](../../com.aspose.words/style/#getBuiltIn) doivent être supprimés du document. |
| [getUnusedLists()](#getUnusedLists) | Spécifie si les listes et définitions de listes inutilisées doivent être supprimées du document. |
| [getUnusedStyles()](#getUnusedStyles) | Spécifie si les styles inutilisés doivent être supprimés du document. |
| [setDuplicateStyle(boolean value)](#setDuplicateStyle-boolean) | Obtient/definit un indicateur indiquant si les styles en double doivent être supprimés du document. |
| [setUnusedBuiltinStyles(boolean value)](#setUnusedBuiltinStyles-boolean) | Spécifie que les styles inutilisés [Style.getBuiltIn()](../../com.aspose.words/style/#getBuiltIn) doivent être supprimés du document. |
| [setUnusedLists(boolean value)](#setUnusedLists-boolean) | Spécifie si les listes et définitions de listes inutilisées doivent être supprimées du document. |
| [setUnusedStyles(boolean value)](#setUnusedStyles-boolean) | Spécifie si les styles inutilisés doivent être supprimés du document. |
### getDuplicateStyle() {#getDuplicateStyle}
```
public boolean getDuplicateStyle()
```


Obtient/definit un indicateur indiquant si les styles en double doivent être supprimés du document. La valeur par défaut est false.

 **Examples:** 

Montre comment supprimer les styles dupliqués du document.

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
boolean - La valeur  boolean  correspondante.
### getUnusedBuiltinStyles() {#getUnusedBuiltinStyles}
```
public boolean getUnusedBuiltinStyles()
```


Spécifie que les styles inutilisés [Style.getBuiltIn()](../../com.aspose.words/style/#getBuiltIn) doivent être supprimés du document.

 **Examples:** 

Montre comment supprimer tous les styles personnalisés inutilisés d'un document.

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
boolean - La valeur  boolean  correspondante.
### getUnusedLists() {#getUnusedLists}
```
public boolean getUnusedLists()
```


Spécifie si les listes inutilisées et leurs définitions doivent être supprimées du document. La valeur par défaut est true.

 **Examples:** 

Montre comment supprimer tous les styles personnalisés inutilisés d'un document.

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
boolean - La valeur  boolean  correspondante.
### getUnusedStyles() {#getUnusedStyles}
```
public boolean getUnusedStyles()
```


Spécifie si les styles inutilisés doivent être supprimés du document. La valeur par défaut est true.

 **Examples:** 

Montre comment supprimer tous les styles personnalisés inutilisés d'un document.

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
boolean - La valeur  boolean  correspondante.
### setDuplicateStyle(boolean value) {#setDuplicateStyle-boolean}
```
public void setDuplicateStyle(boolean value)
```


Obtient/definit un indicateur indiquant si les styles en double doivent être supprimés du document. La valeur par défaut est false.

 **Examples:** 

Montre comment supprimer les styles dupliqués du document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setUnusedBuiltinStyles(boolean value) {#setUnusedBuiltinStyles-boolean}
```
public void setUnusedBuiltinStyles(boolean value)
```


Spécifie que les styles inutilisés [Style.getBuiltIn()](../../com.aspose.words/style/#getBuiltIn) doivent être supprimés du document.

 **Examples:** 

Montre comment supprimer tous les styles personnalisés inutilisés d'un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setUnusedLists(boolean value) {#setUnusedLists-boolean}
```
public void setUnusedLists(boolean value)
```


Spécifie si les listes inutilisées et leurs définitions doivent être supprimées du document. La valeur par défaut est true.

 **Examples:** 

Montre comment supprimer tous les styles personnalisés inutilisés d'un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

### setUnusedStyles(boolean value) {#setUnusedStyles-boolean}
```
public void setUnusedStyles(boolean value)
```


Spécifie si les styles inutilisés doivent être supprimés du document. La valeur par défaut est true.

 **Examples:** 

Montre comment supprimer tous les styles personnalisés inutilisés d'un document.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| valeur | boolean | La valeur  boolean  correspondante. |

