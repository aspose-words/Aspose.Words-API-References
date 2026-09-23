---
title: "LayoutEntityType"
linktitle: "LayoutEntityType"
second_title: "Aspose.Words pour Java"
description: "Types des entités de mise en page en Java."
type: docs
weight: 416
url: /fr/java/com.aspose.words/layoutentitytype/
---

**Inheritance:**
java.lang.Object
```
public class LayoutEntityType
```

Types des entités de mise en page.

 **Examples:** 

Présente les méthodes de traversée des entités de mise en page d'un document.

```

 public void layoutEnumerator() throws Exception {
     // Open a document that contains a variety of layout entities.
     // Layout entities are pages, cells, rows, lines, and other objects included in the LayoutEntityType enum.
     // Each layout entity has a rectangular space that it occupies in the document body.
     Document doc = new Document(getMyDir() + "Layout entities.docx");

     // Create an enumerator that can traverse these entities like a tree.
     LayoutEnumerator layoutEnumerator = new LayoutEnumerator(doc);

     Assert.assertEquals(doc, layoutEnumerator.getDocument());

     layoutEnumerator.moveParent(LayoutEntityType.PAGE);

     Assert.assertEquals(LayoutEntityType.PAGE, layoutEnumerator.getType());
     Assert.assertThrows(IllegalStateException.class, () -> System.out.println(layoutEnumerator.getText()));

     // We can call this method to make sure that the enumerator will be at the first layout entity.
     layoutEnumerator.reset();

     // There are two orders that determine how the layout enumerator continues traversing layout entities
     // when it encounters entities that span across multiple pages.
     // 1 -  In visual order:
     // When moving through an entity's children that span multiple pages,
     // page layout takes precedence, and we move to other child elements on this page and avoid the ones on the next.
     System.out.println("Traversing from first to last, elements between pages separated:");
     traverseLayoutForward(layoutEnumerator, 1);

     // Our enumerator is now at the end of the collection. We can traverse the layout entities backwards to go back to the beginning.
     System.out.println("Traversing from last to first, elements between pages separated:");
     traverseLayoutBackward(layoutEnumerator, 1);

     // 2 -  In logical order:
     // When moving through an entity's children that span multiple pages,
     // the enumerator will move between pages to traverse all the child entities.
     System.out.println("Traversing from first to last, elements between pages mixed:");
     traverseLayoutForwardLogical(layoutEnumerator, 1);

     System.out.println("Traversing from last to first, elements between pages mixed:");
     traverseLayoutBackwardLogical(layoutEnumerator, 1);
 }

 /// 
 /// Enumerate through layoutEnumerator's layout entity collection front-to-back,
 /// in a depth-first manner, and in the "Visual" order.
 /// 
 private static void traverseLayoutForward(LayoutEnumerator layoutEnumerator, int depth) throws Exception {
     do {
         printCurrentEntity(layoutEnumerator, depth);

         if (layoutEnumerator.moveFirstChild()) {
             traverseLayoutForward(layoutEnumerator, depth + 1);
             layoutEnumerator.moveParent();
         }
     } while (layoutEnumerator.moveNext());
 }

 /// 
 /// Enumerate through layoutEnumerator's layout entity collection back-to-front,
 /// in a depth-first manner, and in the "Visual" order.
 /// 
 private static void traverseLayoutBackward(LayoutEnumerator layoutEnumerator, int depth) throws Exception {
     do {
         printCurrentEntity(layoutEnumerator, depth);

         if (layoutEnumerator.moveLastChild()) {
             traverseLayoutBackward(layoutEnumerator, depth + 1);
             layoutEnumerator.moveParent();
         }
     } while (layoutEnumerator.movePrevious());
 }

 /// 
 /// Enumerate through layoutEnumerator's layout entity collection front-to-back,
 /// in a depth-first manner, and in the "Logical" order.
 /// 
 private static void traverseLayoutForwardLogical(LayoutEnumerator layoutEnumerator, int depth) throws Exception {
     do {
         printCurrentEntity(layoutEnumerator, depth);

         if (layoutEnumerator.moveFirstChild()) {
             traverseLayoutForwardLogical(layoutEnumerator, depth + 1);
             layoutEnumerator.moveParent();
         }
     } while (layoutEnumerator.moveNextLogical());
 }

 /// 
 /// Enumerate through layoutEnumerator's layout entity collection back-to-front,
 /// in a depth-first manner, and in the "Logical" order.
 /// 
 private static void traverseLayoutBackwardLogical(LayoutEnumerator layoutEnumerator, int depth) throws Exception {
     do {
         printCurrentEntity(layoutEnumerator, depth);

         if (layoutEnumerator.moveLastChild()) {
             traverseLayoutBackwardLogical(layoutEnumerator, depth + 1);
             layoutEnumerator.moveParent();
         }
     } while (layoutEnumerator.movePreviousLogical());
 }

 /// 
 /// Print information about layoutEnumerator's current entity to the console, while indenting the text with tab characters
 /// based on its depth relative to the root node that we provided in the constructor LayoutEnumerator instance.
 /// The rectangle that we process at the end represents the area and location that the entity takes up in the document.
 /// 
 private static void printCurrentEntity(LayoutEnumerator layoutEnumerator, int indent) throws Exception {
     String tabs = StringUtils.repeat("\t", indent);

     System.out.println(layoutEnumerator.getKind().equals("")
             ? MessageFormat.format("{0}-> Entity type: {1}", tabs, layoutEnumerator.getType())
             : MessageFormat.format("{0}-> Entity type & kind: {1}, {2}", tabs, layoutEnumerator.getType(), layoutEnumerator.getKind()));

     // Only spans can contain text.
     if (layoutEnumerator.getType() == LayoutEntityType.SPAN)
         System.out.println("{tabs}   Span contents: \"{layoutEnumerator.Text}\"");

     Rectangle2D.Float leRect = layoutEnumerator.getRectangle();
     System.out.println(MessageFormat.format("{0}   Rectangle dimensions {1}x{2}, X={3} Y={4}", tabs, leRect.getWidth(), leRect.getHeight(), leRect.getX(), leRect.getY()));
     System.out.println(MessageFormat.format("{0}   Page {1}", tabs, layoutEnumerator.getPageIndex()));
 }
 
```
## Champs

| Champ | Description |
| --- | --- |
| [CELL](#CELL) | Représente une cellule de tableau. |
| [COLUMN](#COLUMN) | Représente une colonne de texte sur une page. |
| [COMMENT](#COMMENT) | Représente un espace réservé au contenu du commentaire. |
| [ENDNOTE](#ENDNOTE) | Représente un espace réservé au contenu de la note de fin. |
| [FOOTNOTE](#FOOTNOTE) | Représente un espace réservé au contenu de la note de bas de page. |
| [HEADER_FOOTER](#HEADER-FOOTER) | Représente un espace réservé au contenu d'en-tête/pied de page sur une page. |
| [LINE](#LINE) | Représente une ligne de caractères de texte et d'objets en ligne. |
| [NONE](#NONE) | Valeur par défaut. |
| [NOTE](#NOTE) | Représente un espace réservé au contenu de la note. |
| [NOTE_SEPARATOR](#NOTE-SEPARATOR) | Représente le séparateur de note de bas de page/note de fin. |
| [PAGE](#PAGE) | Représente une page d'un document. |
| [ROW](#ROW) | Représente une ligne de tableau. |
| [SPAN](#SPAN) | Représente un ou plusieurs caractères dans une ligne. |
| [TEXT_BOX](#TEXT-BOX) | Représente la zone de texte à l'intérieur d'une forme. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String layoutEntityTypeName)](#fromName-java.lang.String) |  |
| [fromNames(Set layoutEntityTypeNames)](#fromNames-java.util.Set) |  |
| [getName(int layoutEntityType)](#getName-int) |  |
| [getNames(int layoutEntityType)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int layoutEntityType)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### CELL {#CELL}
```
public static int CELL
```


Représente une cellule de tableau. La cellule peut contenir les entités enfants [LINE](../../com.aspose.words/layoutentitytype/\#LINE) et [ROW](../../com.aspose.words/layoutentitytype/\#ROW).

### COLUMN {#COLUMN}
```
public static int COLUMN
```


Représente une colonne de texte sur une page. La colonne peut contenir les mêmes entités enfants que [CELL](../../com.aspose.words/layoutentitytype/\#CELL), ainsi que les entités [FOOTNOTE](../../com.aspose.words/layoutentitytype/\#FOOTNOTE), [ENDNOTE](../../com.aspose.words/layoutentitytype/\#ENDNOTE) et [NOTE\_SEPARATOR](../../com.aspose.words/layoutentitytype/\#NOTE-SEPARATOR).

### COMMENT {#COMMENT}
```
public static int COMMENT
```


Représente un espace réservé pour le contenu du commentaire. Le commentaire peut avoir les entités enfants [LINE](../../com.aspose.words/layoutentitytype/\#LINE) et [ROW](../../com.aspose.words/layoutentitytype/\#ROW) entités enfants.

### ENDNOTE {#ENDNOTE}
```
public static int ENDNOTE
```


Représente un espace réservé pour le contenu de la note de fin. La note de fin peut avoir l'entité enfant [NOTE](../../com.aspose.words/layoutentitytype/\#NOTE).

### FOOTNOTE {#FOOTNOTE}
```
public static int FOOTNOTE
```


Représente un espace réservé pour le contenu de la note de bas de page. La note de bas de page peut avoir l'entité enfant [NOTE](../../com.aspose.words/layoutentitytype/\#NOTE).

### HEADER_FOOTER {#HEADER-FOOTER}
```
public static int HEADER_FOOTER
```


Représente un espace réservé pour le contenu d'en‑tête/pied de page sur une page. HeaderFooter peut avoir les entités enfants [LINE](../../com.aspose.words/layoutentitytype/\#LINE) et [ROW](../../com.aspose.words/layoutentitytype/\#ROW) entités enfants.

### LINE {#LINE}
```
public static int LINE
```


Représente une ligne de caractères de texte et d'objets en ligne. Line peut avoir l'entité enfant [SPAN](../../com.aspose.words/layoutentitytype/\#SPAN).

### NONE {#NONE}
```
public static int NONE
```


Valeur par défaut.

### NOTE {#NOTE}
```
public static int NOTE
```


Représente un espace réservé pour le contenu de la note. Note peut avoir les entités enfants [LINE](../../com.aspose.words/layoutentitytype/\#LINE) et [ROW](../../com.aspose.words/layoutentitytype/\#ROW) entités enfants.

### NOTE_SEPARATOR {#NOTE-SEPARATOR}
```
public static int NOTE_SEPARATOR
```


Représente le séparateur de note de bas de page/note de fin. NoteSeparator peut avoir les entités enfants [LINE](../../com.aspose.words/layoutentitytype/\#LINE) et [ROW](../../com.aspose.words/layoutentitytype/\#ROW) entités enfants.

### PAGE {#PAGE}
```
public static int PAGE
```


Représente une page d'un document. Page peut avoir les entités enfants [COLUMN](../../com.aspose.words/layoutentitytype/\#COLUMN), [HEADER\_FOOTER](../../com.aspose.words/layoutentitytype/\#HEADER-FOOTER) et [COMMENT](../../com.aspose.words/layoutentitytype/\#COMMENT) entités enfants.

### ROW {#ROW}
```
public static int ROW
```


Représente une ligne de tableau. Row peut avoir [CELL](../../com.aspose.words/layoutentitytype/\#CELL) comme entités enfants.

### SPAN {#SPAN}
```
public static int SPAN
```


Représente un ou plusieurs caractères dans une ligne. Cela inclut les caractères spéciaux tels que les marqueurs de début/fin de champ, les signets et les commentaires. Span ne peut pas avoir d'entités enfants.

### TEXT_BOX {#TEXT-BOX}
```
public static int TEXT_BOX
```


Représente une zone de texte à l'intérieur d'une forme. Textbox peut avoir les entités enfants [LINE](../../com.aspose.words/layoutentitytype/\#LINE) et [ROW](../../com.aspose.words/layoutentitytype/\#ROW) entités enfants.

### length {#length}
```
public static int length
```


### fromName(String layoutEntityTypeName) {#fromName-java.lang.String}
```
public static int fromName(String layoutEntityTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| layoutEntityTypeName | java.lang.String |  |

**Returns:**
int
### fromNames(Set layoutEntityTypeNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set layoutEntityTypeNames)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| layoutEntityTypeNames | java.util.Set |  |

**Returns:**
int
### getName(int layoutEntityType) {#getName-int}
```
public static String getName(int layoutEntityType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| layoutEntityType | int |  |

**Returns:**
java.lang.String
### getNames(int layoutEntityType) {#getNames-int}
```
public static Set getNames(int layoutEntityType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| layoutEntityType | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int layoutEntityType) {#toString-int}
```
public static String toString(int layoutEntityType)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| layoutEntityType | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
