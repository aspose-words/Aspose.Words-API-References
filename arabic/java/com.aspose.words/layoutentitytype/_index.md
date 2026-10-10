---
title: "LayoutEntityType"
linktitle: "LayoutEntityType"
second_title: "Aspose.Words لـ Java"
description: "أنواع كيانات التخطيط في Java."
type: docs
weight: 416
url: /ar/java/com.aspose.words/layoutentitytype/
---

**Inheritance:**
java.lang.Object
```
public class LayoutEntityType
```

أنواع كيانات التخطيط.

 **Examples:** 

يعرض طرق استعراض كيانات تخطيط المستند.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [CELL](#CELL) | يمثل خلية جدول. |
| [COLUMN](#COLUMN) | يمثل عمودًا من النص على صفحة. |
| [COMMENT](#COMMENT) | يمثل عنصرًا نائبًا لمحتوى التعليق. |
| [ENDNOTE](#ENDNOTE) | يمثل عنصرًا نائبًا لمحتوى الحاشية الختامية. |
| [FOOTNOTE](#FOOTNOTE) | يمثل عنصرًا نائبًا لمحتوى الحاشية السفلية. |
| [HEADER_FOOTER](#HEADER-FOOTER) | يمثل عنصرًا نائبًا لمحتوى الرأس/التذييل على صفحة. |
| [LINE](#LINE) | يمثل سطرًا من أحرف النص والكائنات المضمنة. |
| [NONE](#NONE) | القيمة الافتراضية. |
| [NOTE](#NOTE) | يمثل عنصرًا نائبًا لمحتوى الملاحظة. |
| [NOTE_SEPARATOR](#NOTE-SEPARATOR) | يمثل فاصل الحاشية السفلية/الحاشية الختامية. |
| [PAGE](#PAGE) | يمثل صفحة من مستند. |
| [ROW](#ROW) | يمثل صفًا في الجدول. |
| [SPAN](#SPAN) | يمثل حرفًا واحدًا أو أكثر في سطر. |
| [TEXT_BOX](#TEXT-BOX) | يمثل منطقة نص داخل شكل. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
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


يمثل خلية جدول. قد تحتوي الخلية على كيانات فرعية [LINE](../../com.aspose.words/layoutentitytype/\#LINE) و [ROW](../../com.aspose.words/layoutentitytype/\#ROW).

### COLUMN {#COLUMN}
```
public static int COLUMN
```


يمثل عمودًا من النص على صفحة. قد يحتوي العمود على نفس الكيانات الفرعية مثل [CELL](../../com.aspose.words/layoutentitytype/\#CELL)، بالإضافة إلى كيانات [FOOTNOTE](../../com.aspose.words/layoutentitytype/\#FOOTNOTE)، [ENDNOTE](../../com.aspose.words/layoutentitytype/\#ENDNOTE) و [NOTE\_SEPARATOR](../../com.aspose.words/layoutentitytype/\#NOTE-SEPARATOR).

### COMMENT {#COMMENT}
```
public static int COMMENT
```


يمثل عنصر نائب لمحتوى التعليق. قد يحتوي التعليق على كيانات فرعية [LINE](../../com.aspose.words/layoutentitytype/\#LINE) و [ROW](../../com.aspose.words/layoutentitytype/\#ROW).

### ENDNOTE {#ENDNOTE}
```
public static int ENDNOTE
```


يمثل عنصر نائب لمحتوى الحاشية الختامية. قد تحتوي الحاشية الختامية على كيانات فرعية [NOTE](../../com.aspose.words/layoutentitytype/\#NOTE).

### FOOTNOTE {#FOOTNOTE}
```
public static int FOOTNOTE
```


يمثل عنصر نائب لمحتوى الحاشية السفلية. قد تحتوي الحاشية السفلية على كيانات فرعية [NOTE](../../com.aspose.words/layoutentitytype/\#NOTE).

### HEADER_FOOTER {#HEADER-FOOTER}
```
public static int HEADER_FOOTER
```


يمثل عنصر نائب لمحتوى الترويسة/التذييل في صفحة. قد يحتوي HeaderFooter على كيانات فرعية [LINE](../../com.aspose.words/layoutentitytype/\#LINE) و [ROW](../../com.aspose.words/layoutentitytype/\#ROW).

### LINE {#LINE}
```
public static int LINE
```


يمثل سطرًا من أحرف النص والكائنات المضمنة. قد يحتوي السطر على كيانات فرعية [SPAN](../../com.aspose.words/layoutentitytype/\#SPAN).

### NONE {#NONE}
```
public static int NONE
```


القيمة الافتراضية.

### NOTE {#NOTE}
```
public static int NOTE
```


يمثل عنصر نائب لمحتوى الملاحظة. قد تحتوي الملاحظة على كيانات فرعية [LINE](../../com.aspose.words/layoutentitytype/\#LINE) و [ROW](../../com.aspose.words/layoutentitytype/\#ROW).

### NOTE_SEPARATOR {#NOTE-SEPARATOR}
```
public static int NOTE_SEPARATOR
```


يمثل فاصل الحاشية السفلية/الحاشية الختامية. قد يحتوي NoteSeparator على كيانات فرعية [LINE](../../com.aspose.words/layoutentitytype/\#LINE) و [ROW](../../com.aspose.words/layoutentitytype/\#ROW).

### PAGE {#PAGE}
```
public static int PAGE
```


يمثل صفحة من مستند. قد تحتوي الصفحة على كيانات فرعية [COLUMN](../../com.aspose.words/layoutentitytype/\#COLUMN), [HEADER\_FOOTER](../../com.aspose.words/layoutentitytype/\#HEADER-FOOTER) و [COMMENT](../../com.aspose.words/layoutentitytype/\#COMMENT).

### ROW {#ROW}
```
public static int ROW
```


يمثل صفًا في جدول. قد يحتوي الصف على [CELL](../../com.aspose.words/layoutentitytype/\#CELL) ككيانات فرعية.

### SPAN {#SPAN}
```
public static int SPAN
```


يمثل حرفًا أو أكثر في سطر. يتضمن ذلك أحرفًا خاصة مثل علامات بدء/إنهاء الحقل، والإشارات المرجعية، والتعليقات. قد لا يحتوي Span على كيانات فرعية.

### TEXT_BOX {#TEXT-BOX}
```
public static int TEXT_BOX
```


يمثل مساحة نص داخل شكل. قد يحتوي Textbox على كيانات فرعية [LINE](../../com.aspose.words/layoutentitytype/\#LINE) و [ROW](../../com.aspose.words/layoutentitytype/\#ROW).

### length {#length}
```
public static int length
```


### fromName(String layoutEntityTypeName) {#fromName-java.lang.String}
```
public static int fromName(String layoutEntityTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| layoutEntityTypeName | java.lang.String |  |

**Returns:**
int
### fromNames(Set layoutEntityTypeNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set layoutEntityTypeNames)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| layoutEntityTypeNames | java.util.Set |  |

**Returns:**
int
### getName(int layoutEntityType) {#getName-int}
```
public static String getName(int layoutEntityType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| layoutEntityType | int |  |

**Returns:**
java.lang.String
### getNames(int layoutEntityType) {#getNames-int}
```
public static Set getNames(int layoutEntityType)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| layoutEntityType | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
