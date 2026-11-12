---
title: "NodeType"
linktitle: "NodeType"
second_title: "Aspose.Words для Java"
description: "Указывает тип узла документа Word в Java."
type: docs
weight: 483
url: /ru/java/com.aspose.words/nodetype/
---

**Inheritance:**
java.lang.Object
```
public class NodeType
```

Указывает тип узла документа Word.

 **Examples:** 

Показывает, как пройтись по коллекции дочерних узлов составного узла.

```

 Document doc = new Document();

 // Add two runs and one shape as child nodes to the first paragraph of this document.
 Paragraph paragraph = (Paragraph) doc.getChild(NodeType.PARAGRAPH, 0, true);
 paragraph.appendChild(new Run(doc, "Hello world! "));

 Shape shape = new Shape(doc, ShapeType.RECTANGLE);
 shape.setWidth(200.0);
 shape.setHeight(200.0);
 // Note that the 'CustomNodeId' is not saved to an output file and exists only during the node lifetime.
 shape.setCustomNodeId(100);
 shape.setWrapType(WrapType.INLINE);
 paragraph.appendChild(shape);

 paragraph.appendChild(new Run(doc, "Hello again!"));

 // Iterate through the paragraph's collection of immediate children,
 // and print any runs or shapes that we find within.
 NodeCollection children = paragraph.getChildNodes(NodeType.ANY, false);

 Assert.assertEquals(3, paragraph.getChildNodes(NodeType.ANY, false).getCount());

 for (Node child : (Iterable) children)
     switch (child.getNodeType()) {
         case NodeType.RUN:
             System.out.println("Run contents:");
             System.out.println(MessageFormat.format("\t\"{0}\"", child.getText().trim()));
             break;
         case NodeType.SHAPE:
             Shape childShape = (Shape)child;
             System.out.println("Shape:");
             System.out.println(MessageFormat.format("\t{0}, {1}x{2}", childShape.getShapeType(), childShape.getWidth(), childShape.getHeight()));
             break;
     }
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [ANY](#ANY) | Указывает все типы узлов. |
| [BODY](#BODY) | Объект [Body](../../com.aspose.words/body/), содержащий основной текст раздела (основная текстовая история). |
| [BOOKMARK_END](#BOOKMARK-END) | Конец маркера закладки. |
| [BOOKMARK_START](#BOOKMARK-START) | Начало маркера закладки. |
| [BUILDING_BLOCK](#BUILDING-BLOCK) | Строительный блок в документе глоссария (например, |
| [CELL](#CELL) | Ячейка строки таблицы. |
| [COMMENT](#COMMENT) | Комментарий в документе Word. |
| [COMMENT_RANGE_END](#COMMENT-RANGE-END) | Маркерный узел, представляющий конец комментируемого диапазона. |
| [COMMENT_RANGE_START](#COMMENT-RANGE-START) | Маркерный узел, представляющий начало комментируемого диапазона. |
| [DOCUMENT](#DOCUMENT) | Объект [Document](../../com.aspose.words/document/), который, будучи корнем дерева документа, предоставляет доступ ко всему документу Word. |
| [EDITABLE_RANGE_END](#EDITABLE-RANGE-END) | Конец редактируемого диапазона. |
| [EDITABLE_RANGE_START](#EDITABLE-RANGE-START) | Начало редактируемого диапазона. |
| [FIELD_END](#FIELD-END) | Специальный символ, обозначающий конец поля Word. |
| [FIELD_SEPARATOR](#FIELD-SEPARATOR) | Специальный символ, разделяющий код поля и результат поля. |
| [FIELD_START](#FIELD-START) | Специальный символ, обозначающий начало поля Word. |
| [FOOTNOTE](#FOOTNOTE) | Сноска или концевая сноска в документе Word. |
| [FORM_FIELD](#FORM-FIELD) | Поле формы. |
| [GLOSSARY_DOCUMENT](#GLOSSARY-DOCUMENT) | Документ глоссария внутри основного документа. |
| [GROUP_SHAPE](#GROUP-SHAPE) | Группа фигур, изображений, OLE‑объектов или других групповых фигур. |
| [HEADER_FOOTER](#HEADER-FOOTER) | Объект [HeaderFooter](../../com.aspose.words/headerfooter/) , содержащий текст конкретного верхнего или нижнего колонтитула внутри раздела. |
| [MOVE_FROM_RANGE_END](#MOVE-FROM-RANGE-END) | Конец диапазона MoveFrom. |
| [MOVE_FROM_RANGE_START](#MOVE-FROM-RANGE-START) | Начало диапазона MoveFrom. |
| [MOVE_TO_RANGE_END](#MOVE-TO-RANGE-END) | Конец диапазона MoveTo. |
| [MOVE_TO_RANGE_START](#MOVE-TO-RANGE-START) | Начало диапазона MoveTo. |
| [NULL](#NULL) | Зарезервировано для внутреннего использования Aspose.Words. |
| [OFFICE_MATH](#OFFICE-MATH) | Объект Office Math. |
| [PARAGRAPH](#PARAGRAPH) | Абзац текста. |
| [ROW](#ROW) | Строка таблицы. |
| [RUN](#RUN) | Фрагмент текста. |
| [SECTION](#SECTION) | Объект [Section](../../com.aspose.words/section/) , соответствующий одному разделу в документе Word. |
| [SHAPE](#SHAPE) | Графический объект, такой как фигура OfficeArt, изображение или OLE‑объект. |
| [SMART_TAG](#SMART-TAG) | Умный тег вокруг одной или нескольких встроенных структур (фрагментов, изображений, полей и т.д.) в абзаце |
| [SPECIAL_CHAR](#SPECIAL-CHAR) | Специальный символ, который не относится к более конкретным типам специальных символов. |
| [STRUCTURED_DOCUMENT_TAG](#STRUCTURED-DOCUMENT-TAG) | Позволяет определить специфичную для клиента информацию и способы её представления. |
| [STRUCTURED_DOCUMENT_TAG_RANGE_END](#STRUCTURED-DOCUMENT-TAG-RANGE-END) | Конец тега структурированного документа **ranged**, который принимает контент из нескольких разделов. |
| [STRUCTURED_DOCUMENT_TAG_RANGE_START](#STRUCTURED-DOCUMENT-TAG-RANGE-START) | Начало тега структурированного документа **ranged**, который принимает контент из нескольких разделов. |
| [SUB_DOCUMENT](#SUB-DOCUMENT) | Узел поддокумента, являющийся ссылкой на другой документ. |
| [SYSTEM](#SYSTEM) | Зарезервировано для внутреннего использования Aspose.Words. |
| [TABLE](#TABLE) | Объект [Table](../../com.aspose.words/table/) , представляющий таблицу в документе Word. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String nodeTypeName)](#fromName-java.lang.String) |  |
| [getName(int nodeType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int nodeType)](#toString-int) |  |
### ANY {#ANY}
```
public static int ANY
```


Указывает все типы узлов. Позволяет выбрать всех дочерних элементов.

### BODY {#BODY}
```
public static int BODY
```


Объект [Body](../../com.aspose.words/body/), содержащий основной текст раздела (основная текстовая история).

Узел [Body](../../com.aspose.words/body/) может содержать узлы [Paragraph](../../com.aspose.words/paragraph/) и [Table](../../com.aspose.words/table/).

### BOOKMARK_END {#BOOKMARK-END}
```
public static int BOOKMARK_END
```


Конец маркера закладки.

### BOOKMARK_START {#BOOKMARK-START}
```
public static int BOOKMARK_START
```


Начало маркера закладки.

### BUILDING_BLOCK {#BUILDING-BLOCK}
```
public static int BUILDING_BLOCK
```


Строительный блок внутри глоссарного документа (например, запись глоссарного документа).

### CELL {#CELL}
```
public static int CELL
```


Ячейка строки таблицы.

Узел [Cell](../../com.aspose.words/cell/) может содержать узлы [Paragraph](../../com.aspose.words/paragraph/) и [Table](../../com.aspose.words/table/).

### COMMENT {#COMMENT}
```
public static int COMMENT
```


Комментарий в документе Word.

Узел [Comment](../../com.aspose.words/comment/) может содержать узлы [Paragraph](../../com.aspose.words/paragraph/) и [Table](../../com.aspose.words/table/).

### COMMENT_RANGE_END {#COMMENT-RANGE-END}
```
public static int COMMENT_RANGE_END
```


Маркерный узел, представляющий конец комментируемого диапазона.

### COMMENT_RANGE_START {#COMMENT-RANGE-START}
```
public static int COMMENT_RANGE_START
```


Маркерный узел, представляющий начало комментируемого диапазона.

### DOCUMENT {#DOCUMENT}
```
public static int DOCUMENT
```


Объект [Document](../../com.aspose.words/document/), который, будучи корнем дерева документа, предоставляет доступ ко всему документу Word.

Узел [Document](../../com.aspose.words/document/) может содержать узлы [Section](../../com.aspose.words/section/).

### EDITABLE_RANGE_END {#EDITABLE-RANGE-END}
```
public static int EDITABLE_RANGE_END
```


Конец редактируемого диапазона.

### EDITABLE_RANGE_START {#EDITABLE-RANGE-START}
```
public static int EDITABLE_RANGE_START
```


Начало редактируемого диапазона.

### FIELD_END {#FIELD-END}
```
public static int FIELD_END
```


Специальный символ, обозначающий конец поля Word.

### FIELD_SEPARATOR {#FIELD-SEPARATOR}
```
public static int FIELD_SEPARATOR
```


Специальный символ, разделяющий код поля и результат поля.

### FIELD_START {#FIELD-START}
```
public static int FIELD_START
```


Специальный символ, обозначающий начало поля Word.

### FOOTNOTE {#FOOTNOTE}
```
public static int FOOTNOTE
```


Сноска или концевая сноска в документе Word.

Узел [Footnote](../../com.aspose.words/footnote/) может содержать узлы [Paragraph](../../com.aspose.words/paragraph/) и [Table](../../com.aspose.words/table/).

### FORM_FIELD {#FORM-FIELD}
```
public static int FORM_FIELD
```


Поле формы.

### GLOSSARY_DOCUMENT {#GLOSSARY-DOCUMENT}
```
public static int GLOSSARY_DOCUMENT
```


Документ глоссария внутри основного документа.

### GROUP_SHAPE {#GROUP-SHAPE}
```
public static int GROUP_SHAPE
```


Группа фигур, изображений, OLE‑объектов или других групповых фигур.

Узел [GroupShape](../../com.aspose.words/groupshape/) может содержать другие узлы [Shape](../../com.aspose.words/shape/) и [GroupShape](../../com.aspose.words/groupshape/).

### HEADER_FOOTER {#HEADER-FOOTER}
```
public static int HEADER_FOOTER
```


Объект [HeaderFooter](../../com.aspose.words/headerfooter/) , содержащий текст конкретного верхнего или нижнего колонтитула внутри раздела.

Узел [HeaderFooter](../../com.aspose.words/headerfooter/) может содержать узлы [Paragraph](../../com.aspose.words/paragraph/) и [Table](../../com.aspose.words/table/).

### MOVE_FROM_RANGE_END {#MOVE-FROM-RANGE-END}
```
public static int MOVE_FROM_RANGE_END
```


Конец диапазона MoveFrom.

### MOVE_FROM_RANGE_START {#MOVE-FROM-RANGE-START}
```
public static int MOVE_FROM_RANGE_START
```


Начало диапазона MoveFrom.

### MOVE_TO_RANGE_END {#MOVE-TO-RANGE-END}
```
public static int MOVE_TO_RANGE_END
```


Конец диапазона MoveTo.

### MOVE_TO_RANGE_START {#MOVE-TO-RANGE-START}
```
public static int MOVE_TO_RANGE_START
```


Начало диапазона MoveTo.

### NULL {#NULL}
```
public static int NULL
```


Зарезервировано для внутреннего использования Aspose.Words.

### OFFICE_MATH {#OFFICE-MATH}
```
public static int OFFICE_MATH
```


Объект Office Math. Может быть уравнением, функцией, матрицей или одним из других математических объектов. Может представлять собой коллекцию математических объектов и также может содержать некоторые нематематические объекты, такие как фрагменты текста.

### PARAGRAPH {#PARAGRAPH}
```
public static int PARAGRAPH
```


Абзац текста.

Узел [Paragraph](../../com.aspose.words/paragraph/) является контейнером для встроенных элементов уровня inline: [Run](../../com.aspose.words/run/), [FieldStart](../../com.aspose.words/fieldstart/), [FieldSeparator](../../com.aspose.words/fieldseparator/), [FieldEnd](../../com.aspose.words/fieldend/), [FormField](../../com.aspose.words/formfield/), [Shape](../../com.aspose.words/shape/), [GroupShape](../../com.aspose.words/groupshape/), [Footnote](../../com.aspose.words/footnote/), [Comment](../../com.aspose.words/comment/), [SpecialChar](../../com.aspose.words/specialchar/), а также [BookmarkStart](../../com.aspose.words/bookmarkstart/) и [BookmarkEnd](../../com.aspose.words/bookmarkend/).

### ROW {#ROW}
```
public static int ROW
```


Строка таблицы.

Узел [Row](../../com.aspose.words/row/) может содержать узлы [Cell](../../com.aspose.words/cell/).

### RUN {#RUN}
```
public static int RUN
```


Фрагмент текста.

### SECTION {#SECTION}
```
public static int SECTION
```


Объект [Section](../../com.aspose.words/section/) , соответствующий одному разделу в документе Word.

Узел [Section](../../com.aspose.words/section/) может содержать узлы [Body](../../com.aspose.words/body/) и [HeaderFooter](../../com.aspose.words/headerfooter/).

### SHAPE {#SHAPE}
```
public static int SHAPE
```


Графический объект, такой как фигура OfficeArt, изображение или OLE‑объект.

Узел [Shape](../../com.aspose.words/shape/) может содержать узлы [Paragraph](../../com.aspose.words/paragraph/) и [Table](../../com.aspose.words/table/).

### SMART_TAG {#SMART-TAG}
```
public static int SMART_TAG
```


Умный тег вокруг одной или нескольких встроенных структур (фрагментов, изображений, полей и т.д.) в абзаце

### SPECIAL_CHAR {#SPECIAL-CHAR}
```
public static int SPECIAL_CHAR
```


Специальный символ, который не относится к более конкретным типам специальных символов.

### STRUCTURED_DOCUMENT_TAG {#STRUCTURED-DOCUMENT-TAG}
```
public static int STRUCTURED_DOCUMENT_TAG
```


Позволяет определить специфичную для клиента информацию и способы её представления.

### STRUCTURED_DOCUMENT_TAG_RANGE_END {#STRUCTURED-DOCUMENT-TAG-RANGE-END}
```
public static int STRUCTURED_DOCUMENT_TAG_RANGE_END
```


Конец тега структурированного документа **ranged**, который принимает контент из нескольких разделов.

### STRUCTURED_DOCUMENT_TAG_RANGE_START {#STRUCTURED-DOCUMENT-TAG-RANGE-START}
```
public static int STRUCTURED_DOCUMENT_TAG_RANGE_START
```


Начало тега структурированного документа **ranged**, который принимает контент из нескольких разделов.

### SUB_DOCUMENT {#SUB-DOCUMENT}
```
public static int SUB_DOCUMENT
```


Узел поддокумента, являющийся ссылкой на другой документ.

### SYSTEM {#SYSTEM}
```
public static int SYSTEM
```


Зарезервировано для внутреннего использования Aspose.Words.

### TABLE {#TABLE}
```
public static int TABLE
```


Объект [Table](../../com.aspose.words/table/) , представляющий таблицу в документе Word.

Узел [Table](../../com.aspose.words/table/) может содержать узлы [Row](../../com.aspose.words/row/).

### length {#length}
```
public static int length
```


### fromName(String nodeTypeName) {#fromName-java.lang.String}
```
public static int fromName(String nodeTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| nodeTypeName | java.lang.String |  |

**Returns:**
int
### getName(int nodeType) {#getName-int}
```
public static String getName(int nodeType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| nodeType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int nodeType) {#toString-int}
```
public static String toString(int nodeType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| nodeType | int |  |

**Returns:**
java.lang.String
