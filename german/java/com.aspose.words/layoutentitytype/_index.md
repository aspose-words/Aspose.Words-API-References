---
title: "LayoutEntityType"
linktitle: "LayoutEntityType"
second_title: "Aspose.Words für Java"
description: "Typen der Layout-Entitäten in Java."
type: docs
weight: 416
url: /de/java/com.aspose.words/layoutentitytype/
---

**Inheritance:**
java.lang.Object
```
public class LayoutEntityType
```

Typen der Layout‑Entitäten.

 **Examples:** 

Zeigt Möglichkeiten zum Durchlaufen der Layout-Entitäten eines Dokuments.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [CELL](#CELL) | Stellt eine Tabellenzelle dar. |
| [COLUMN](#COLUMN) | Stellt eine Textspalte auf einer Seite dar. |
| [COMMENT](#COMMENT) | Stellt einen Platzhalter für Kommentarinhalt dar. |
| [ENDNOTE](#ENDNOTE) | Stellt einen Platzhalter für Endnoteninhalt dar. |
| [FOOTNOTE](#FOOTNOTE) | Stellt einen Platzhalter für Fußnoteninhalt dar. |
| [HEADER_FOOTER](#HEADER-FOOTER) | Stellt einen Platzhalter für Kopf-/Fußzeileninhalt auf einer Seite dar. |
| [LINE](#LINE) | Stellt eine Zeile von Textzeichen und Inline-Objekten dar. |
| [NONE](#NONE) | Standardwert. |
| [NOTE](#NOTE) | Stellt einen Platzhalter für Notizinhalte dar. |
| [NOTE_SEPARATOR](#NOTE-SEPARATOR) | Stellt den Fußnoten-/Endnoten-Trenner dar. |
| [PAGE](#PAGE) | Stellt eine Seite eines Dokuments dar. |
| [ROW](#ROW) | Stellt eine Tabellenzeile dar. |
| [SPAN](#SPAN) | Stellt ein oder mehrere Zeichen in einer Zeile dar. |
| [TEXT_BOX](#TEXT-BOX) | Stellt einen Textbereich innerhalb einer Form dar. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
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


Stellt eine Tabellenzelle dar. Die Zelle kann die untergeordneten Entitäten [LINE](../../com.aspose.words/layoutentitytype/\#LINE) und [ROW](../../com.aspose.words/layoutentitytype/\#ROW) haben.

### COLUMN {#COLUMN}
```
public static int COLUMN
```


Stellt eine Textspalte auf einer Seite dar. Die Spalte kann dieselben untergeordneten Entitäten wie [CELL](../../com.aspose.words/layoutentitytype/\#CELL), zusätzlich die Entitäten [FOOTNOTE](../../com.aspose.words/layoutentitytype/\#FOOTNOTE), [ENDNOTE](../../com.aspose.words/layoutentitytype/\#ENDNOTE) und [NOTE\_SEPARATOR](../../com.aspose.words/layoutentitytype/\#NOTE-SEPARATOR) haben.

### COMMENT {#COMMENT}
```
public static int COMMENT
```


Stellt einen Platzhalter für Kommentarinhalt dar. Der Kommentar kann die untergeordneten Entitäten [LINE](../../com.aspose.words/layoutentitytype/\#LINE) und [ROW](../../com.aspose.words/layoutentitytype/\#ROW) haben.

### ENDNOTE {#ENDNOTE}
```
public static int ENDNOTE
```


Stellt einen Platzhalter für Endnoteninhalt dar. Die Endnote kann die untergeordnete Entität [NOTE](../../com.aspose.words/layoutentitytype/\#NOTE) haben.

### FOOTNOTE {#FOOTNOTE}
```
public static int FOOTNOTE
```


Stellt einen Platzhalter für Fußnoteninhalt dar. Die Fußnote kann die untergeordnete Entität [NOTE](../../com.aspose.words/layoutentitytype/\#NOTE) haben.

### HEADER_FOOTER {#HEADER-FOOTER}
```
public static int HEADER_FOOTER
```


Stellt einen Platzhalter für Kopf-/Fußzeileninhalt auf einer Seite dar. Die Kopf-/Fußzeile kann die untergeordneten Entitäten [LINE](../../com.aspose.words/layoutentitytype/\#LINE) und [ROW](../../com.aspose.words/layoutentitytype/\#ROW) haben.

### LINE {#LINE}
```
public static int LINE
```


Stellt eine Zeile von Textzeichen und Inline-Objekten dar. Die Zeile kann die untergeordnete Entität [SPAN](../../com.aspose.words/layoutentitytype/\#SPAN) haben.

### NONE {#NONE}
```
public static int NONE
```


Standardwert.

### NOTE {#NOTE}
```
public static int NOTE
```


Stellt einen Platzhalter für Notizinhalte dar. Die Notiz kann die untergeordneten Entitäten [LINE](../../com.aspose.words/layoutentitytype/\#LINE) und [ROW](../../com.aspose.words/layoutentitytype/\#ROW) haben.

### NOTE_SEPARATOR {#NOTE-SEPARATOR}
```
public static int NOTE_SEPARATOR
```


Stellt den Fußnoten-/Endnoten-Trenner dar. NoteSeparator kann [LINE](../../com.aspose.words/layoutentitytype/\#LINE) und [ROW](../../com.aspose.words/layoutentitytype/\#ROW) Kind-Entitäten haben.

### PAGE {#PAGE}
```
public static int PAGE
```


Stellt eine Seite eines Dokuments dar. Page kann [COLUMN](../../com.aspose.words/layoutentitytype/\#COLUMN), [HEADER\_FOOTER](../../com.aspose.words/layoutentitytype/\#HEADER-FOOTER) und [COMMENT](../../com.aspose.words/layoutentitytype/\#COMMENT) Kind-Entitäten haben.

### ROW {#ROW}
```
public static int ROW
```


Stellt eine Tabellenzeile dar. Row kann [CELL](../../com.aspose.words/layoutentitytype/\#CELL) als Kind-Entitäten haben.

### SPAN {#SPAN}
```
public static int SPAN
```


Stellt ein oder mehrere Zeichen in einer Zeile dar. Dies schließt Sonderzeichen wie Feld‑Start/End‑Markierungen, Lesezeichen und Kommentare ein. Span darf keine Kind-Entitäten haben.

### TEXT_BOX {#TEXT-BOX}
```
public static int TEXT_BOX
```


Stellt den Textbereich innerhalb einer Form dar. Textbox kann [LINE](../../com.aspose.words/layoutentitytype/\#LINE) und [ROW](../../com.aspose.words/layoutentitytype/\#ROW) Kind-Entitäten haben.

### length {#length}
```
public static int length
```


### fromName(String layoutEntityTypeName) {#fromName-java.lang.String}
```
public static int fromName(String layoutEntityTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| layoutEntityTypeName | java.lang.String |  |

**Returns:**
int
### fromNames(Set layoutEntityTypeNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set layoutEntityTypeNames)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| layoutEntityTypeNames | java.util.Set |  |

**Returns:**
int
### getName(int layoutEntityType) {#getName-int}
```
public static String getName(int layoutEntityType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| layoutEntityType | int |  |

**Returns:**
java.lang.String
### getNames(int layoutEntityType) {#getNames-int}
```
public static Set getNames(int layoutEntityType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| layoutEntityType | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
