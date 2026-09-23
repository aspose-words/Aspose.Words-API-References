---
title: "LayoutEntityType"
linktitle: "LayoutEntityType"
second_title: "Aspose.Words для Java"
description: "Типы элементов макета в Java."
type: docs
weight: 416
url: /ru/java/com.aspose.words/layoutentitytype/
---

**Inheritance:**
java.lang.Object
```
public class LayoutEntityType
```

Типы сущностей компоновки.

 **Examples:** 

Показывает способы обхода элементов макета документа.

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
## Поля

| Поле | Описание |
| --- | --- |
| [CELL](#CELL) | Представляет ячейку таблицы. |
| [COLUMN](#COLUMN) | Представляет колонку текста на странице. |
| [COMMENT](#COMMENT) | Представляет заполнитель для содержимого комментария. |
| [ENDNOTE](#ENDNOTE) | Представляет заполнитель для содержимого сноски. |
| [FOOTNOTE](#FOOTNOTE) | Представляет заполнитель для содержимого сноски. |
| [HEADER_FOOTER](#HEADER-FOOTER) | Представляет заполнитель для содержимого верхнего/нижнего колонтитула на странице. |
| [LINE](#LINE) | Представляет строку символов текста и встроенных объектов. |
| [NONE](#NONE) | Значение по умолчанию. |
| [NOTE](#NOTE) | Представляет заполнитель для содержимого заметки. |
| [NOTE_SEPARATOR](#NOTE-SEPARATOR) | Представляет разделитель сносок/конечных сносок. |
| [PAGE](#PAGE) | Представляет страницу документа. |
| [ROW](#ROW) | Представляет строку таблицы. |
| [SPAN](#SPAN) | Представляет один или несколько символов в строке. |
| [TEXT_BOX](#TEXT-BOX) | Представляет текстовую область внутри фигуры. |
| [length](#length) |  |
## Методы

| Метод | Описание |
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


Представляет ячейку таблицы. Ячейка может иметь дочерние сущности [LINE](../../com.aspose.words/layoutentitytype/\#LINE) и [ROW](../../com.aspose.words/layoutentitytype/\#ROW).

### COLUMN {#COLUMN}
```
public static int COLUMN
```


Представляет колонку текста на странице. Колонка может иметь те же дочерние сущности, что и [CELL](../../com.aspose.words/layoutentitytype/\#CELL), плюс сущности [FOOTNOTE](../../com.aspose.words/layoutentitytype/\#FOOTNOTE), [ENDNOTE](../../com.aspose.words/layoutentitytype/\#ENDNOTE) и [NOTE\_SEPARATOR](../../com.aspose.words/layoutentitytype/\#NOTE-SEPARATOR).

### COMMENT {#COMMENT}
```
public static int COMMENT
```


Представляет заполнитель для содержимого комментария. Комментарий может иметь дочерние сущности [LINE](../../com.aspose.words/layoutentitytype/\#LINE) и [ROW](../../com.aspose.words/layoutentitytype/\#ROW).

### ENDNOTE {#ENDNOTE}
```
public static int ENDNOTE
```


Представляет заполнитель для содержимого сноски. Сноска может иметь дочерние сущности [NOTE](../../com.aspose.words/layoutentitytype/\#NOTE).

### FOOTNOTE {#FOOTNOTE}
```
public static int FOOTNOTE
```


Представляет заполнитель для содержимого сноски. Сноска может иметь дочерние сущности [NOTE](../../com.aspose.words/layoutentitytype/\#NOTE).

### HEADER_FOOTER {#HEADER-FOOTER}
```
public static int HEADER_FOOTER
```


Представляет заполнитель для содержимого верхнего/нижнего колонтитула на странице. HeaderFooter может иметь дочерние сущности [LINE](../../com.aspose.words/layoutentitytype/\#LINE) и [ROW](../../com.aspose.words/layoutentitytype/\#ROW).

### LINE {#LINE}
```
public static int LINE
```


Представляет строку символов текста и встроенных объектов. Line может иметь дочерние сущности [SPAN](../../com.aspose.words/layoutentitytype/\#SPAN).

### NONE {#NONE}
```
public static int NONE
```


Значение по умолчанию.

### NOTE {#NOTE}
```
public static int NOTE
```


Представляет заполнитель для содержимого заметки. Note может иметь дочерние сущности [LINE](../../com.aspose.words/layoutentitytype/\#LINE) и [ROW](../../com.aspose.words/layoutentitytype/\#ROW).

### NOTE_SEPARATOR {#NOTE-SEPARATOR}
```
public static int NOTE_SEPARATOR
```


Представляет разделитель сносок/конечных сносок. NoteSeparator может иметь дочерние сущности [LINE](../../com.aspose.words/layoutentitytype/\#LINE) и [ROW](../../com.aspose.words/layoutentitytype/\#ROW).

### PAGE {#PAGE}
```
public static int PAGE
```


Представляет страницу документа. Page может иметь дочерние сущности [COLUMN](../../com.aspose.words/layoutentitytype/\#COLUMN), [HEADER\_FOOTER](../../com.aspose.words/layoutentitytype/\#HEADER-FOOTER) и [COMMENT](../../com.aspose.words/layoutentitytype/\#COMMENT).

### ROW {#ROW}
```
public static int ROW
```


Представляет строку таблицы. Row может иметь дочерние сущности [CELL](../../com.aspose.words/layoutentitytype/\#CELL).

### SPAN {#SPAN}
```
public static int SPAN
```


Представляет один или несколько символов в строке. Это включает специальные символы, такие как маркеры начала/конца поля, закладки и комментарии. Span не может иметь дочерних сущностей.

### TEXT_BOX {#TEXT-BOX}
```
public static int TEXT_BOX
```


Представляет текстовую область внутри фигуры. Textbox может иметь дочерние сущности [LINE](../../com.aspose.words/layoutentitytype/\#LINE) и [ROW](../../com.aspose.words/layoutentitytype/\#ROW).

### length {#length}
```
public static int length
```


### fromName(String layoutEntityTypeName) {#fromName-java.lang.String}
```
public static int fromName(String layoutEntityTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| layoutEntityTypeName | java.lang.String |  |

**Returns:**
int
### fromNames(Set layoutEntityTypeNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set layoutEntityTypeNames)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| layoutEntityTypeNames | java.util.Set |  |

**Returns:**
int
### getName(int layoutEntityType) {#getName-int}
```
public static String getName(int layoutEntityType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| layoutEntityType | int |  |

**Returns:**
java.lang.String
### getNames(int layoutEntityType) {#getNames-int}
```
public static Set getNames(int layoutEntityType)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| layoutEntityType | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
