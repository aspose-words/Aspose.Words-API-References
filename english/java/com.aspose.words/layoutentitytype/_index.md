---
title: LayoutEntityType
linktitle: LayoutEntityType
second_title: Aspose.Words for Java
description: Types of the layout entities in Java.
type: docs
weight: 406
url: /java/com.aspose.words/layoutentitytype/
---

**Inheritance:**
java.lang.Object
```
public class LayoutEntityType
```

Types of the layout entities.

 **Examples:** 

Shows ways of traversing a document's layout entities.

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
## Fields

| Field | Description |
| --- | --- |
| [CELL](#CELL) | Represents a table cell. |
| [COLUMN](#COLUMN) | Represents a column of text on a page. |
| [COMMENT](#COMMENT) | Represents placeholder for comment content. |
| [ENDNOTE](#ENDNOTE) | Represents placeholder for endnote content. |
| [FOOTNOTE](#FOOTNOTE) | Represents placeholder for footnote content. |
| [HEADER_FOOTER](#HEADER-FOOTER) | Represents placeholder for header/footer content on a page. |
| [LINE](#LINE) | Represents line of characters of text and inline objects. |
| [NONE](#NONE) | Default value. |
| [NOTE](#NOTE) | Represents placeholder for note content. |
| [NOTE_SEPARATOR](#NOTE-SEPARATOR) | Represents footnote/endnote separator. |
| [PAGE](#PAGE) | Represents page of a document. |
| [ROW](#ROW) | Represents a table row. |
| [SPAN](#SPAN) | Represents one or more characters in a line. |
| [TEXT_BOX](#TEXT-BOX) | Represents text area inside of a shape. |
| [length](#length) |  |
## Methods

| Method | Description |
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


Represents a table cell. Cell may have [LINE](../../com.aspose.words/layoutentitytype/\#LINE) and [ROW](../../com.aspose.words/layoutentitytype/\#ROW) child entities.

### COLUMN {#COLUMN}
```
public static int COLUMN
```


Represents a column of text on a page. Column may have the same child entities as [CELL](../../com.aspose.words/layoutentitytype/\#CELL), plus [FOOTNOTE](../../com.aspose.words/layoutentitytype/\#FOOTNOTE), [ENDNOTE](../../com.aspose.words/layoutentitytype/\#ENDNOTE) and [NOTE\_SEPARATOR](../../com.aspose.words/layoutentitytype/\#NOTE-SEPARATOR) entities.

### COMMENT {#COMMENT}
```
public static int COMMENT
```


Represents placeholder for comment content. Comment may have [LINE](../../com.aspose.words/layoutentitytype/\#LINE) and [ROW](../../com.aspose.words/layoutentitytype/\#ROW) child entities.

### ENDNOTE {#ENDNOTE}
```
public static int ENDNOTE
```


Represents placeholder for endnote content. Endnote may have [NOTE](../../com.aspose.words/layoutentitytype/\#NOTE) child entities.

### FOOTNOTE {#FOOTNOTE}
```
public static int FOOTNOTE
```


Represents placeholder for footnote content. Footnote may have [NOTE](../../com.aspose.words/layoutentitytype/\#NOTE) child entities.

### HEADER_FOOTER {#HEADER-FOOTER}
```
public static int HEADER_FOOTER
```


Represents placeholder for header/footer content on a page. HeaderFooter may have [LINE](../../com.aspose.words/layoutentitytype/\#LINE) and [ROW](../../com.aspose.words/layoutentitytype/\#ROW) child entities.

### LINE {#LINE}
```
public static int LINE
```


Represents line of characters of text and inline objects. Line may have [SPAN](../../com.aspose.words/layoutentitytype/\#SPAN) child entities.

### NONE {#NONE}
```
public static int NONE
```


Default value.

### NOTE {#NOTE}
```
public static int NOTE
```


Represents placeholder for note content. Note may have [LINE](../../com.aspose.words/layoutentitytype/\#LINE) and [ROW](../../com.aspose.words/layoutentitytype/\#ROW) child entities.

### NOTE_SEPARATOR {#NOTE-SEPARATOR}
```
public static int NOTE_SEPARATOR
```


Represents footnote/endnote separator. NoteSeparator may have [LINE](../../com.aspose.words/layoutentitytype/\#LINE) and [ROW](../../com.aspose.words/layoutentitytype/\#ROW) child entities.

### PAGE {#PAGE}
```
public static int PAGE
```


Represents page of a document. Page may have [COLUMN](../../com.aspose.words/layoutentitytype/\#COLUMN), [HEADER\_FOOTER](../../com.aspose.words/layoutentitytype/\#HEADER-FOOTER) and [COMMENT](../../com.aspose.words/layoutentitytype/\#COMMENT) child entities.

### ROW {#ROW}
```
public static int ROW
```


Represents a table row. Row may have [CELL](../../com.aspose.words/layoutentitytype/\#CELL) as child entities.

### SPAN {#SPAN}
```
public static int SPAN
```


Represents one or more characters in a line. This include special characters like field start/end markers, bookmarks and comments. Span may not have child entities.

### TEXT_BOX {#TEXT-BOX}
```
public static int TEXT_BOX
```


Represents text area inside of a shape. Textbox may have [LINE](../../com.aspose.words/layoutentitytype/\#LINE) and [ROW](../../com.aspose.words/layoutentitytype/\#ROW) child entities.

### length {#length}
```
public static int length
```


### fromName(String layoutEntityTypeName) {#fromName-java.lang.String}
```
public static int fromName(String layoutEntityTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| layoutEntityTypeName | java.lang.String |  |

**Returns:**
int
### fromNames(Set layoutEntityTypeNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set layoutEntityTypeNames)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| layoutEntityTypeNames | java.util.Set |  |

**Returns:**
int
### getName(int layoutEntityType) {#getName-int}
```
public static String getName(int layoutEntityType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| layoutEntityType | int |  |

**Returns:**
java.lang.String
### getNames(int layoutEntityType) {#getNames-int}
```
public static Set getNames(int layoutEntityType)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| layoutEntityType | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
