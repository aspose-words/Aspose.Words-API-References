---
title: NodeType
second_title: Справочник по API Aspose.Words для Java
description: Указывает тип узла документа Word.
type: docs
weight: 408
url: /ru/java/com.aspose.words/nodetype/
---

**Наследование:**
java.lang.Object
```
public class NodeType
```

Указывает тип узла документа Word.
## Поля

| Поле | Описание |
| --- | --- |
| [ANY](#ANY) | Указывает все типы узлов. |
| [BODY](#BODY) |  А[Body](../../com.aspose.words/body) объект, содержащий основной текст раздела (основной текстовый рассказ). |
| [BOOKMARK_END](#BOOKMARK-END) | Конец маркера закладки. |
| [BOOKMARK_START](#BOOKMARK-START) | Начало маркера закладки. |
| [BUILDING_BLOCK](#BUILDING-BLOCK) | Строительный блок в документе глоссария (например, |
| [CELL](#CELL) | Ячейка строки таблицы. |
| [COMMENT](#COMMENT) | Комментарий в документе Word. |
| [COMMENT_RANGE_END](#COMMENT-RANGE-END) | Узел-маркер, представляющий конец закомментированного диапазона. |
| [COMMENT_RANGE_START](#COMMENT-RANGE-START) | Узел-маркер, представляющий начало комментируемого диапазона. |
| [DOCUMENT](#DOCUMENT) |  А[Document](../../com.aspose.words/document) объект, который как корень дерева документов обеспечивает доступ ко всему документу Word. |
| [EDITABLE_RANGE_END](#EDITABLE-RANGE-END) | Конец редактируемого диапазона. |
| [EDITABLE_RANGE_START](#EDITABLE-RANGE-START) | Начало редактируемого диапазона. |
| [FIELD_END](#FIELD-END) | Специальный символ, обозначающий конец поля Word. |
| [FIELD_SEPARATOR](#FIELD-SEPARATOR) | Специальный символ, отделяющий код поля от результата поля. |
| [FIELD_START](#FIELD-START) | Специальный символ, обозначающий начало поля Word. |
| [FOOTNOTE](#FOOTNOTE) | Сноска или концевая сноска в документе Word. |
| [FORM_FIELD](#FORM-FIELD) | Поле формы. |
| [GLOSSARY_DOCUMENT](#GLOSSARY-DOCUMENT) | Глоссарий в основном документе. |
| [GROUP_SHAPE](#GROUP-SHAPE) | Группа фигур, изображений, объектов OLE или других фигур группы. |
| [HEADER_FOOTER](#HEADER-FOOTER) |  А[HeaderFooter](../../com.aspose.words/headerfooter) объект, содержащий текст определенного верхнего или нижнего колонтитула внутри раздела. |
| [MOVE_FROM_RANGE_END](#MOVE-FROM-RANGE-END) | Конец диапазона MoveFrom. |
| [MOVE_FROM_RANGE_START](#MOVE-FROM-RANGE-START) | Начало диапазона MoveFrom. |
| [MOVE_TO_RANGE_END](#MOVE-TO-RANGE-END) | Конец диапазона MoveTo. |
| [MOVE_TO_RANGE_START](#MOVE-TO-RANGE-START) | Начало диапазона MoveTo. |
| [NULL](#NULL) | Зарезервировано для внутреннего использования Aspose.Words. |
| [OFFICE_MATH](#OFFICE-MATH) | Объект Office Math. |
| [PARAGRAPH](#PARAGRAPH) | Абзац текста. |
| [ROW](#ROW) | Ряд таблицы. |
| [RUN](#RUN) | Прогон текста. |
| [SECTION](#SECTION) |  А[Section](../../com.aspose.words/section) объект, соответствующий одному разделу в документе Word. |
| [SHAPE](#SHAPE) | Объект рисования, например фигура OfficeArt, изображение или объект OLE. |
| [SMART_TAG](#SMART-TAG) | Смарт-тег вокруг одной или нескольких встроенных структур (прогонов, изображений, полей и т. д.) внутри абзаца. |
| [SPECIAL_CHAR](#SPECIAL-CHAR) | Специальный символ, который не относится к более конкретным типам специальных символов. |
| [STRUCTURED_DOCUMENT_TAG](#STRUCTURED-DOCUMENT-TAG) | Позволяет определить специфичную для заказчика информацию и средства ее представления. |
| [STRUCTURED_DOCUMENT_TAG_RANGE_END](#STRUCTURED-DOCUMENT-TAG-RANGE-END) |  Конец**ranged** тег структурированного документа, который принимает содержимое из нескольких разделов. |
| [STRUCTURED_DOCUMENT_TAG_RANGE_START](#STRUCTURED-DOCUMENT-TAG-RANGE-START) |  Начало**ranged** тег структурированного документа, который принимает содержимое из нескольких разделов. |
| [SUB_DOCUMENT](#SUB-DOCUMENT) | Узел вложенного документа, который является ссылкой на другой документ. |
| [SYSTEM](#SYSTEM) | Зарезервировано для внутреннего использования Aspose.Words. |
| [TABLE](#TABLE) |  А[Table](../../com.aspose.words/table) объект, представляющий таблицу в документе Word. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String nodeTypeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int nodeType)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int nodeType)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### ANY {#ANY}
```
public static int ANY
```


Указывает все типы узлов. Позволяет выбрать всех детей.

### BODY {#BODY}
```
public static int BODY
```


 А[Body](../../com.aspose.words/body) объект, содержащий основной текст раздела (основной текстовый рассказ).

 А[Body](../../com.aspose.words/body) узел может иметь[Paragraph](../../com.aspose.words/paragraph) а также[Table](../../com.aspose.words/table) узлы.

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


Строительный блок в документе глоссария (например, запись в документе глоссария).

### CELL {#CELL}
```
public static int CELL
```


Ячейка строки таблицы.

 А[Cell](../../com.aspose.words/cell) узел может иметь[Paragraph](../../com.aspose.words/paragraph) а также[Table](../../com.aspose.words/table) узлы.

### COMMENT {#COMMENT}
```
public static int COMMENT
```


Комментарий в документе Word.

 А[Comment](../../com.aspose.words/comment) узел может иметь[Paragraph](../../com.aspose.words/paragraph) а также[Table](../../com.aspose.words/table) узлы.

### COMMENT_RANGE_END {#COMMENT-RANGE-END}
```
public static int COMMENT_RANGE_END
```


Узел-маркер, представляющий конец закомментированного диапазона.

### COMMENT_RANGE_START {#COMMENT-RANGE-START}
```
public static int COMMENT_RANGE_START
```


Узел-маркер, представляющий начало комментируемого диапазона.

### DOCUMENT {#DOCUMENT}
```
public static int DOCUMENT
```


 А[Document](../../com.aspose.words/document) объект, который как корень дерева документов обеспечивает доступ ко всему документу Word.

 А[Document](../../com.aspose.words/document) узел может иметь[Section](../../com.aspose.words/section) узлы.

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


Специальный символ, отделяющий код поля от результата поля.

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

 А[Footnote](../../com.aspose.words/footnote) узел может иметь[Paragraph](../../com.aspose.words/paragraph) а также[Table](../../com.aspose.words/table) узлы.

### FORM_FIELD {#FORM-FIELD}
```
public static int FORM_FIELD
```


Поле формы.

### GLOSSARY_DOCUMENT {#GLOSSARY-DOCUMENT}
```
public static int GLOSSARY_DOCUMENT
```


Глоссарий в основном документе.

### GROUP_SHAPE {#GROUP-SHAPE}
```
public static int GROUP_SHAPE
```


Группа фигур, изображений, объектов OLE или других фигур группы.

 А[GroupShape](../../com.aspose.words/groupshape) узел может содержать другие[Shape](../../com.aspose.words/shape) а также[GroupShape](../../com.aspose.words/groupshape) узлы.

### HEADER_FOOTER {#HEADER-FOOTER}
```
public static int HEADER_FOOTER
```


 А[HeaderFooter](../../com.aspose.words/headerfooter) объект, содержащий текст определенного верхнего или нижнего колонтитула внутри раздела.

 А[HeaderFooter](../../com.aspose.words/headerfooter) узел может иметь[Paragraph](../../com.aspose.words/paragraph) а также[Table](../../com.aspose.words/table) узлы.

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


Объект Office Math. Может быть уравнением, функцией, матрицей или одним из других математических объектов. Может быть коллекцией математических объектов, а также может содержать некоторые нематематические объекты, например фрагменты текста.

### PARAGRAPH {#PARAGRAPH}
```
public static int PARAGRAPH
```


Абзац текста.

 А[Paragraph](../../com.aspose.words/paragraph) узел — это контейнер для встроенных элементов уровня[Run](../../com.aspose.words/run), [FieldStart](../../com.aspose.words/fieldstart), [FieldSeparator](../../com.aspose.words/fieldseparator), [FieldEnd](../../com.aspose.words/fieldend), [FormField](../../com.aspose.words/formfield), [Shape](../../com.aspose.words/shape), [GroupShape](../../com.aspose.words/groupshape), [Footnote](../../com.aspose.words/footnote), [Comment](../../com.aspose.words/comment), [SpecialChar](../../com.aspose.words/specialchar) , так же как[BookmarkStart](../../com.aspose.words/bookmarkstart) а также[BookmarkEnd](../../com.aspose.words/bookmarkend).

### ROW {#ROW}
```
public static int ROW
```


Ряд таблицы.

 А[Row](../../com.aspose.words/row) узел может иметь[Cell](../../com.aspose.words/cell) узлы.

### RUN {#RUN}
```
public static int RUN
```


Прогон текста.

### SECTION {#SECTION}
```
public static int SECTION
```


 А[Section](../../com.aspose.words/section) объект, соответствующий одному разделу в документе Word.

 А[Section](../../com.aspose.words/section) узел может иметь**Body** а также**HeaderFooter** узлы.

### SHAPE {#SHAPE}
```
public static int SHAPE
```


Объект рисования, например фигура OfficeArt, изображение или объект OLE.

 А[Shape](../../com.aspose.words/shape) узел может содержать[Paragraph](../../com.aspose.words/paragraph) а также[Table](../../com.aspose.words/table) узлы.

### SMART_TAG {#SMART-TAG}
```
public static int SMART_TAG
```


Смарт-тег вокруг одной или нескольких встроенных структур (прогонов, изображений, полей и т. д.) внутри абзаца.

### SPECIAL_CHAR {#SPECIAL-CHAR}
```
public static int SPECIAL_CHAR
```


Специальный символ, который не относится к более конкретным типам специальных символов.

### STRUCTURED_DOCUMENT_TAG {#STRUCTURED-DOCUMENT-TAG}
```
public static int STRUCTURED_DOCUMENT_TAG
```


Позволяет определить специфичную для заказчика информацию и средства ее представления.

### STRUCTURED_DOCUMENT_TAG_RANGE_END {#STRUCTURED-DOCUMENT-TAG-RANGE-END}
```
public static int STRUCTURED_DOCUMENT_TAG_RANGE_END
```


 Конец**ranged** тег структурированного документа, который принимает содержимое из нескольких разделов.

### STRUCTURED_DOCUMENT_TAG_RANGE_START {#STRUCTURED-DOCUMENT-TAG-RANGE-START}
```
public static int STRUCTURED_DOCUMENT_TAG_RANGE_START
```


 Начало**ranged** тег структурированного документа, который принимает содержимое из нескольких разделов.

### SUB_DOCUMENT {#SUB-DOCUMENT}
```
public static int SUB_DOCUMENT
```


Узел вложенного документа, который является ссылкой на другой документ.

### SYSTEM {#SYSTEM}
```
public static int SYSTEM
```


Зарезервировано для внутреннего использования Aspose.Words.

### TABLE {#TABLE}
```
public static int TABLE
```


 А[Table](../../com.aspose.words/table) объект, представляющий таблицу в документе Word.

 А[Table](../../com.aspose.words/table) узел может иметь[Row](../../com.aspose.words/row) узлы.

### length {#length}
```
public static int length
```


### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Возвращает:**
логический
### fromName(String nodeTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String nodeTypeName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| nodeTypeName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int nodeType) {#getName-int-}
```
public static String getName(int nodeType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| nodeType | int |  |

**Возвращает:**
java.lang.String
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Возвращает:**
инт[]
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### toString() {#toString--}
```
public String toString()
```




**Возвращает:**
java.lang.String
### toString(int nodeType) {#toString-int-}
```
public static String toString(int nodeType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| nodeType | int |  |

**Возвращает:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
