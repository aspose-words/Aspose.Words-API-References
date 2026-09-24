---
title: "LayoutEntityType"
linktitle: "LayoutEntityType"
second_title: "Aspose.Words Java için"
description: "Java'daki düzen varlıklarının türleri."
type: docs
weight: 416
url: /tr/java/com.aspose.words/layoutentitytype/
---

**Inheritance:**
java.lang.Object
```
public class LayoutEntityType
```

Düzen varlıklarının türleri.

 **Examples:** 

Bir belgenin düzen varlıklarını dolaşma yollarını gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [CELL](#CELL) | Bir tablo hücresini temsil eder. |
| [COLUMN](#COLUMN) | Bir sayfadaki metin sütununu temsil eder. |
| [COMMENT](#COMMENT) | Yorum içeriği için yer tutucuyu temsil eder. |
| [ENDNOTE](#ENDNOTE) | Son not içeriği için yer tutucuyu temsil eder. |
| [FOOTNOTE](#FOOTNOTE) | Dipnot içeriği için yer tutucuyu temsil eder. |
| [HEADER_FOOTER](#HEADER-FOOTER) | Bir sayfadaki üstbilgi/altbilgi içeriği için yer tutucuyu temsil eder. |
| [LINE](#LINE) | Metin ve satır içi nesnelerden oluşan karakter satırını temsil eder. |
| [NONE](#NONE) | Varsayılan değer. |
| [NOTE](#NOTE) | Not içeriği için yer tutucuyu temsil eder. |
| [NOTE_SEPARATOR](#NOTE-SEPARATOR) | Dipnot/son not ayırıcıyı temsil eder. |
| [PAGE](#PAGE) | Bir belgenin sayfasını temsil eder. |
| [ROW](#ROW) | Bir tablo satırını temsil eder. |
| [SPAN](#SPAN) | Bir satırdaki bir veya daha fazla karakteri temsil eder. |
| [TEXT_BOX](#TEXT-BOX) | Bir şeklin içindeki metin alanını temsil eder. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
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


Bir tablo hücresini temsil eder. Hücre, [LINE](../../com.aspose.words/layoutentitytype/\#LINE) ve [ROW](../../com.aspose.words/layoutentitytype/\#ROW) alt varlıklara sahip olabilir.

### COLUMN {#COLUMN}
```
public static int COLUMN
```


Bir sayfadaki metin sütununu temsil eder. Sütun, [CELL](../../com.aspose.words/layoutentitytype/\#CELL) ile aynı alt varlıklara sahip olabilir, ayrıca [FOOTNOTE](../../com.aspose.words/layoutentitytype/\#FOOTNOTE), [ENDNOTE](../../com.aspose.words/layoutentitytype/\#ENDNOTE) ve [NOTE\_SEPARATOR](../../com.aspose.words/layoutentitytype/\#NOTE-SEPARATOR) varlıklarını da içerir.

### COMMENT {#COMMENT}
```
public static int COMMENT
```


Yorum içeriği için yer tutucuyu temsil eder. Yorum, [LINE](../../com.aspose.words/layoutentitytype/\#LINE) ve [ROW](../../com.aspose.words/layoutentitytype/\#ROW) alt varlıklara sahip olabilir.

### ENDNOTE {#ENDNOTE}
```
public static int ENDNOTE
```


Dipnot içeriği için yer tutucuyu temsil eder. Dipnot, [NOTE](../../com.aspose.words/layoutentitytype/\#NOTE) alt varlıklara sahip olabilir.

### FOOTNOTE {#FOOTNOTE}
```
public static int FOOTNOTE
```


Altnot içeriği için yer tutucuyu temsil eder. Altnot, [NOTE](../../com.aspose.words/layoutentitytype/\#NOTE) alt varlıklara sahip olabilir.

### HEADER_FOOTER {#HEADER-FOOTER}
```
public static int HEADER_FOOTER
```


Bir sayfadaki üstbilgi/altbilgi içeriği için yer tutucuyu temsil eder. HeaderFooter, [LINE](../../com.aspose.words/layoutentitytype/\#LINE) ve [ROW](../../com.aspose.words/layoutentitytype/\#ROW) alt varlıklara sahip olabilir.

### LINE {#LINE}
```
public static int LINE
```


Metin ve satır içi nesnelerden oluşan karakter satırını temsil eder. Line, [SPAN](../../com.aspose.words/layoutentitytype/\#SPAN) alt varlıklara sahip olabilir.

### NONE {#NONE}
```
public static int NONE
```


Varsayılan değer.

### NOTE {#NOTE}
```
public static int NOTE
```


Not içeriği için yer tutucuyu temsil eder. Note, [LINE](../../com.aspose.words/layoutentitytype/\#LINE) ve [ROW](../../com.aspose.words/layoutentitytype/\#ROW) alt varlıklara sahip olabilir.

### NOTE_SEPARATOR {#NOTE-SEPARATOR}
```
public static int NOTE_SEPARATOR
```


Altnot/dipnot ayırıcıyı temsil eder. NoteSeparator, [LINE](../../com.aspose.words/layoutentitytype/\#LINE) ve [ROW](../../com.aspose.words/layoutentitytype/\#ROW) alt varlıklara sahip olabilir.

### PAGE {#PAGE}
```
public static int PAGE
```


Bir belgenin sayfasını temsil eder. Page, [COLUMN](../../com.aspose.words/layoutentitytype/\#COLUMN), [HEADER\_FOOTER](../../com.aspose.words/layoutentitytype/\#HEADER-FOOTER) ve [COMMENT](../../com.aspose.words/layoutentitytype/\#COMMENT) alt varlıklara sahip olabilir.

### ROW {#ROW}
```
public static int ROW
```


Bir tablo satırını temsil eder. Row, [CELL](../../com.aspose.words/layoutentitytype/\#CELL) alt varlık olarak sahip olabilir.

### SPAN {#SPAN}
```
public static int SPAN
```


Bir satırda bir veya daha fazla karakteri temsil eder. Bu, alan başlangıç/bitiş işaretçileri, yer imleri ve yorumlar gibi özel karakterleri içerir. Span, alt varlıklara sahip olamaz.

### TEXT_BOX {#TEXT-BOX}
```
public static int TEXT_BOX
```


Bir şeklin içindeki metin alanını temsil eder. Textbox, [LINE](../../com.aspose.words/layoutentitytype/\#LINE) ve [ROW](../../com.aspose.words/layoutentitytype/\#ROW) alt varlıklara sahip olabilir.

### length {#length}
```
public static int length
```


### fromName(String layoutEntityTypeName) {#fromName-java.lang.String}
```
public static int fromName(String layoutEntityTypeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| layoutEntityTypeName | java.lang.String |  |

**Returns:**
int
### fromNames(Set layoutEntityTypeNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set layoutEntityTypeNames)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| layoutEntityTypeNames | java.util.Set |  |

**Returns:**
int
### getName(int layoutEntityType) {#getName-int}
```
public static String getName(int layoutEntityType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| layoutEntityType | int |  |

**Returns:**
java.lang.String
### getNames(int layoutEntityType) {#getNames-int}
```
public static Set getNames(int layoutEntityType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| layoutEntityType | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
