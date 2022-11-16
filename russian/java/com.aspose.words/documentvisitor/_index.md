---
title: DocumentVisitor
second_title: Справочник по API Aspose.Words для Java
description: Базовый класс для пользовательских посетителей документов.
type: docs
weight: 132
url: /ru/java/com.aspose.words/documentvisitor/
---

**Наследование:**
java.lang.Object
```
public abstract class DocumentVisitor
```

Базовый класс для пользовательских посетителей документов.

 Чтобы узнать больше, посетите**Aspose.Words Document Object Model (DOM)** документальная статья.

 С**DocumentVisitor** вы можете определять и выполнять пользовательские операции, требующие перечисления по дереву документов.

 Например, Aspose.Words использует**DocumentVisitor** внутри для экономии**Document** в различных форматах и для других операций, таких как поиск полей или закладок над фрагментом документа.

Использовать**DocumentVisitor**:

1.   Создайте класс, производный от**DocumentVisitor**.
2.  Переопределите и предоставьте реализации для некоторых или всех методов VisitXXX для выполнения некоторых пользовательских операций.
3.   Вызов[Node.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/node\#accept-com.aspose.words.DocumentVisitor-) на**Node** с которого вы хотите начать перечисление.

**DocumentVisitor** предоставляет реализации по умолчанию для всех методов VisitXXX, чтобы упростить создание новых посетителей документа, поскольку необходимо переопределить только методы, необходимые для конкретного посетителя. Нет необходимости переопределять все методы посетителя.

Дополнительные сведения см. в шаблоне проектирования «Посетитель».
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [visitAbsolutePositionTab(AbsolutePositionTab tab)](#visitAbsolutePositionTab-com.aspose.words.AbsolutePositionTab-) |  Вызывается, когда[AbsolutePositionTab](../../com.aspose.words/absolutepositiontab) узел встречается в документе. |
| [visitBodyEnd(Body body)](#visitBodyEnd-com.aspose.words.Body-) | Вызывается, когда закончился перечисление основной текстовой истории в разделе. |
| [visitBodyStart(Body body)](#visitBodyStart-com.aspose.words.Body-) | Вызывается, когда начался перебор основной текстовой истории в разделе. |
| [visitBookmarkEnd(BookmarkEnd bookmarkEnd)](#visitBookmarkEnd-com.aspose.words.BookmarkEnd-) | Вызывается, когда в документе встречается конец закладки. |
| [visitBookmarkStart(BookmarkStart bookmarkStart)](#visitBookmarkStart-com.aspose.words.BookmarkStart-) | Вызывается, когда в документе встречается начало закладки. |
| [visitBuildingBlockEnd(BuildingBlock block)](#visitBuildingBlockEnd-com.aspose.words.BuildingBlock-) | Вызывается после окончания перечисления стандартного блока. |
| [visitBuildingBlockStart(BuildingBlock block)](#visitBuildingBlockStart-com.aspose.words.BuildingBlock-) | Вызывается, когда начинается перечисление стандартного блока. |
| [visitCellEnd(Cell cell)](#visitCellEnd-com.aspose.words.Cell-) | Вызывается, когда закончилось перечисление ячейки таблицы. |
| [visitCellStart(Cell cell)](#visitCellStart-com.aspose.words.Cell-) | Вызывается, когда начинается перечисление ячейки таблицы. |
| [visitCommentEnd(Comment comment)](#visitCommentEnd-com.aspose.words.Comment-) | Вызывается, когда закончилось перечисление текста комментария. |
| [visitCommentRangeEnd(CommentRangeEnd commentRangeEnd)](#visitCommentRangeEnd-com.aspose.words.CommentRangeEnd-) | Вызывается, когда встречается конец закомментированного диапазона текста. |
| [visitCommentRangeStart(CommentRangeStart commentRangeStart)](#visitCommentRangeStart-com.aspose.words.CommentRangeStart-) | Вызывается, когда встречается начало закомментированного диапазона текста. |
| [visitCommentStart(Comment comment)](#visitCommentStart-com.aspose.words.Comment-) | Вызывается, когда начинается перечисление текста комментария. |
| [visitDocumentEnd(Document doc)](#visitDocumentEnd-com.aspose.words.Document-) | Вызывается после завершения перечисления документа. |
| [visitDocumentStart(Document doc)](#visitDocumentStart-com.aspose.words.Document-) | Вызывается, когда начинается перечисление документа. |
| [visitEditableRangeEnd(EditableRangeEnd editableRangeEnd)](#visitEditableRangeEnd-com.aspose.words.EditableRangeEnd-) | Вызывается, когда в документе встречается конец редактируемого диапазона. |
| [visitEditableRangeStart(EditableRangeStart editableRangeStart)](#visitEditableRangeStart-com.aspose.words.EditableRangeStart-) | Вызывается, когда в документе встречается начало редактируемого диапазона. |
| [visitFieldEnd(FieldEnd fieldEnd)](#visitFieldEnd-com.aspose.words.FieldEnd-) | Вызывается, когда поле заканчивается в документе. |
| [visitFieldSeparator(FieldSeparator fieldSeparator)](#visitFieldSeparator-com.aspose.words.FieldSeparator-) | Вызывается, когда в документе встречается разделитель полей. |
| [visitFieldStart(FieldStart fieldStart)](#visitFieldStart-com.aspose.words.FieldStart-) | Вызывается, когда в документе начинается поле. |
| [visitFootnoteEnd(Footnote footnote)](#visitFootnoteEnd-com.aspose.words.Footnote-) | Вызывается, когда закончилось перечисление текста сноски или концевой сноски. |
| [visitFootnoteStart(Footnote footnote)](#visitFootnoteStart-com.aspose.words.Footnote-) | Вызывается, когда начинается перечисление текста сноски или концевой сноски. |
| [visitFormField(FormField formField)](#visitFormField-com.aspose.words.FormField-) | Вызывается, когда в документе встречается поле формы. |
| [visitGlossaryDocumentEnd(GlossaryDocument glossary)](#visitGlossaryDocumentEnd-com.aspose.words.GlossaryDocument-) | Вызывается, когда закончилось перечисление документа глоссария. |
| [visitGlossaryDocumentStart(GlossaryDocument glossary)](#visitGlossaryDocumentStart-com.aspose.words.GlossaryDocument-) | Вызывается, когда начинается перечисление документа глоссария. |
| [visitGroupShapeEnd(GroupShape groupShape)](#visitGroupShapeEnd-com.aspose.words.GroupShape-) | Вызывается, когда закончилось перечисление формы группы. |
| [visitGroupShapeStart(GroupShape groupShape)](#visitGroupShapeStart-com.aspose.words.GroupShape-) | Вызывается, когда начинается перечисление формы группы. |
| [visitHeaderFooterEnd(HeaderFooter headerFooter)](#visitHeaderFooterEnd-com.aspose.words.HeaderFooter-) | Вызывается, когда закончилось перечисление верхнего или нижнего колонтитула в разделе. |
| [visitHeaderFooterStart(HeaderFooter headerFooter)](#visitHeaderFooterStart-com.aspose.words.HeaderFooter-) | Вызывается, когда начинается перечисление верхнего или нижнего колонтитула в разделе. |
| [visitOfficeMathEnd(OfficeMath officeMath)](#visitOfficeMathEnd-com.aspose.words.OfficeMath-) | Вызывается после завершения перечисления объекта Office Math. |
| [visitOfficeMathStart(OfficeMath officeMath)](#visitOfficeMathStart-com.aspose.words.OfficeMath-) | Вызывается при запуске перечисления объекта Office Math. |
| [visitParagraphEnd(Paragraph paragraph)](#visitParagraphEnd-com.aspose.words.Paragraph-) | Вызывается, когда закончилось перечисление абзаца. |
| [visitParagraphStart(Paragraph paragraph)](#visitParagraphStart-com.aspose.words.Paragraph-) | Вызывается, когда начинается перечисление абзаца. |
| [visitRowEnd(Row row)](#visitRowEnd-com.aspose.words.Row-) | Вызывается, когда закончилось перечисление строки таблицы. |
| [visitRowStart(Row row)](#visitRowStart-com.aspose.words.Row-) | Вызывается, когда начинается перечисление строки таблицы. |
| [visitRun(Run run)](#visitRun-com.aspose.words.Run-) | Вызывается при обнаружении фрагмента текста в . |
| [visitSectionEnd(Section section)](#visitSectionEnd-com.aspose.words.Section-) | Вызывается, когда закончилось перечисление секции. |
| [visitSectionStart(Section section)](#visitSectionStart-com.aspose.words.Section-) | Вызывается, когда началось перечисление раздела. |
| [visitShapeEnd(Shape shape)](#visitShapeEnd-com.aspose.words.Shape-) | Вызывается, когда перечисление формы закончилось. |
| [visitShapeStart(Shape shape)](#visitShapeStart-com.aspose.words.Shape-) | Вызывается, когда начинается перечисление фигуры. |
| [visitSmartTagEnd(SmartTag smartTag)](#visitSmartTagEnd-com.aspose.words.SmartTag-) | Вызывается, когда закончилось перечисление смарт-тега. |
| [visitSmartTagStart(SmartTag smartTag)](#visitSmartTagStart-com.aspose.words.SmartTag-) | Вызывается, когда начинается перечисление смарт-тега. |
| [visitSpecialChar(SpecialChar specialChar)](#visitSpecialChar-com.aspose.words.SpecialChar-) |  Вызывается, когда[SpecialChar](../../com.aspose.words/specialchar) узел встречается в документе. |
| [visitStructuredDocumentTagEnd(StructuredDocumentTag sdt)](#visitStructuredDocumentTagEnd-com.aspose.words.StructuredDocumentTag-) | Вызывается, когда закончилось перечисление тега структурированного документа. |
| [visitStructuredDocumentTagRangeEnd(StructuredDocumentTagRangeEnd sdtRangeEnd)](#visitStructuredDocumentTagRangeEnd-com.aspose.words.StructuredDocumentTagRangeEnd-) |  |
| [visitStructuredDocumentTagRangeStart(StructuredDocumentTagRangeStart sdtRangeStart)](#visitStructuredDocumentTagRangeStart-com.aspose.words.StructuredDocumentTagRangeStart-) |  |
| [visitStructuredDocumentTagStart(StructuredDocumentTag sdt)](#visitStructuredDocumentTagStart-com.aspose.words.StructuredDocumentTag-) | Вызывается, когда начинается перечисление тега структурированного документа. |
| [visitSubDocument(SubDocument subDocument)](#visitSubDocument-com.aspose.words.SubDocument-) | Вызывается при обнаружении вложенного документа. |
| [visitTableEnd(Table table)](#visitTableEnd-com.aspose.words.Table-) | Вызывается, когда закончилось перечисление таблицы. |
| [visitTableStart(Table table)](#visitTableStart-com.aspose.words.Table-) | Вызывается, когда начинается перечисление таблицы. |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
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
### visitAbsolutePositionTab(AbsolutePositionTab tab) {#visitAbsolutePositionTab-com.aspose.words.AbsolutePositionTab-}
```
public int visitAbsolutePositionTab(AbsolutePositionTab tab)
```


 Вызывается, когда[AbsolutePositionTab](../../com.aspose.words/absolutepositiontab) узел встречается в документе.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| tab | [AbsolutePositionTab](../../com.aspose.words/absolutepositiontab) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitBodyEnd(Body body) {#visitBodyEnd-com.aspose.words.Body-}
```
public int visitBodyEnd(Body body)
```


Вызывается, когда закончился перечисление основной текстовой истории в разделе.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| body | [Body](../../com.aspose.words/body) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitBodyStart(Body body) {#visitBodyStart-com.aspose.words.Body-}
```
public int visitBodyStart(Body body)
```


Вызывается, когда начался перебор основной текстовой истории в разделе.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| body | [Body](../../com.aspose.words/body) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitBookmarkEnd(BookmarkEnd bookmarkEnd) {#visitBookmarkEnd-com.aspose.words.BookmarkEnd-}
```
public int visitBookmarkEnd(BookmarkEnd bookmarkEnd)
```


Вызывается, когда в документе встречается конец закладки.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| bookmarkEnd | [BookmarkEnd](../../com.aspose.words/bookmarkend) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitBookmarkStart(BookmarkStart bookmarkStart) {#visitBookmarkStart-com.aspose.words.BookmarkStart-}
```
public int visitBookmarkStart(BookmarkStart bookmarkStart)
```


Вызывается, когда в документе встречается начало закладки.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| bookmarkStart | [BookmarkStart](../../com.aspose.words/bookmarkstart) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitBuildingBlockEnd(BuildingBlock block) {#visitBuildingBlockEnd-com.aspose.words.BuildingBlock-}
```
public int visitBuildingBlockEnd(BuildingBlock block)
```


Вызывается после окончания перечисления стандартного блока.

Примечание. Узел стандартного блока и его дочерние элементы не посещаются, когда вы выполняете посетителя над узлом.[Document](../../com.aspose.words/document) . Если вы хотите выполнить посетителя над строительным блоком, вам нужно выполнить посетителя над[GlossaryDocument](../../com.aspose.words/glossarydocument) или позвоните по телефону[BuildingBlock.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/buildingblock\#accept-com.aspose.words.DocumentVisitor-).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| block | [BuildingBlock](../../com.aspose.words/buildingblock) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitBuildingBlockStart(BuildingBlock block) {#visitBuildingBlockStart-com.aspose.words.BuildingBlock-}
```
public int visitBuildingBlockStart(BuildingBlock block)
```


Вызывается, когда начинается перечисление стандартного блока.

Примечание. Узел стандартного блока и его дочерние элементы не посещаются, когда вы выполняете посетителя над узлом.[Document](../../com.aspose.words/document) . Если вы хотите выполнить посетителя над строительным блоком, вам нужно выполнить посетителя над[GlossaryDocument](../../com.aspose.words/glossarydocument) или позвоните по телефону[BuildingBlock.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/buildingblock\#accept-com.aspose.words.DocumentVisitor-).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| block | [BuildingBlock](../../com.aspose.words/buildingblock) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitCellEnd(Cell cell) {#visitCellEnd-com.aspose.words.Cell-}
```
public int visitCellEnd(Cell cell)
```


Вызывается, когда закончилось перечисление ячейки таблицы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| cell | [Cell](../../com.aspose.words/cell) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitCellStart(Cell cell) {#visitCellStart-com.aspose.words.Cell-}
```
public int visitCellStart(Cell cell)
```


Вызывается, когда начинается перечисление ячейки таблицы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| cell | [Cell](../../com.aspose.words/cell) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitCommentEnd(Comment comment) {#visitCommentEnd-com.aspose.words.Comment-}
```
public int visitCommentEnd(Comment comment)
```


Вызывается, когда закончилось перечисление текста комментария.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| comment | [Comment](../../com.aspose.words/comment) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitCommentRangeEnd(CommentRangeEnd commentRangeEnd) {#visitCommentRangeEnd-com.aspose.words.CommentRangeEnd-}
```
public int visitCommentRangeEnd(CommentRangeEnd commentRangeEnd)
```


Вызывается, когда встречается конец закомментированного диапазона текста.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| commentRangeEnd | [CommentRangeEnd](../../com.aspose.words/commentrangeend) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitCommentRangeStart(CommentRangeStart commentRangeStart) {#visitCommentRangeStart-com.aspose.words.CommentRangeStart-}
```
public int visitCommentRangeStart(CommentRangeStart commentRangeStart)
```


Вызывается, когда встречается начало закомментированного диапазона текста.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| commentRangeStart | [CommentRangeStart](../../com.aspose.words/commentrangestart) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitCommentStart(Comment comment) {#visitCommentStart-com.aspose.words.Comment-}
```
public int visitCommentStart(Comment comment)
```


Вызывается, когда начинается перечисление текста комментария.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| comment | [Comment](../../com.aspose.words/comment) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitDocumentEnd(Document doc) {#visitDocumentEnd-com.aspose.words.Document-}
```
public int visitDocumentEnd(Document doc)
```


Вызывается после завершения перечисления документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitDocumentStart(Document doc) {#visitDocumentStart-com.aspose.words.Document-}
```
public int visitDocumentStart(Document doc)
```


Вызывается, когда начинается перечисление документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitEditableRangeEnd(EditableRangeEnd editableRangeEnd) {#visitEditableRangeEnd-com.aspose.words.EditableRangeEnd-}
```
public int visitEditableRangeEnd(EditableRangeEnd editableRangeEnd)
```


Вызывается, когда в документе встречается конец редактируемого диапазона.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| editableRangeEnd | [EditableRangeEnd](../../com.aspose.words/editablerangeend) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitEditableRangeStart(EditableRangeStart editableRangeStart) {#visitEditableRangeStart-com.aspose.words.EditableRangeStart-}
```
public int visitEditableRangeStart(EditableRangeStart editableRangeStart)
```


Вызывается, когда в документе встречается начало редактируемого диапазона.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| editableRangeStart | [EditableRangeStart](../../com.aspose.words/editablerangestart) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitFieldEnd(FieldEnd fieldEnd) {#visitFieldEnd-com.aspose.words.FieldEnd-}
```
public int visitFieldEnd(FieldEnd fieldEnd)
```


Вызывается, когда поле заканчивается в документе.

 Для получения дополнительной информации см.[visitFieldStart(com.aspose.words.FieldStart)](../../com.aspose.words/documentvisitor\#visitFieldStart-com.aspose.words.FieldStart-)

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldEnd | [FieldEnd](../../com.aspose.words/fieldend) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitFieldSeparator(FieldSeparator fieldSeparator) {#visitFieldSeparator-com.aspose.words.FieldSeparator-}
```
public int visitFieldSeparator(FieldSeparator fieldSeparator)
```


Вызывается, когда в документе встречается разделитель полей.

Разделитель полей отделяет код поля от значения поля в документе. Обратите внимание, что некоторые поля имеют только код поля и не имеют разделителя полей и значения поля.

 Для получения дополнительной информации см.[visitFieldStart(com.aspose.words.FieldStart)](../../com.aspose.words/documentvisitor\#visitFieldStart-com.aspose.words.FieldStart-)

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldSeparator | [FieldSeparator](../../com.aspose.words/fieldseparator) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitFieldStart(FieldStart fieldStart) {#visitFieldStart-com.aspose.words.FieldStart-}
```
public int visitFieldStart(FieldStart fieldStart)
```


Вызывается, когда в документе начинается поле.

Поле в документе Word состоит из кода поля и значения поля.

Например, поле, отображающее номер страницы, можно представить следующим образом:

[Начало поля] СТРАНИЦА[Разделитель полей]98[FieldEnd]

Разделитель полей отделяет код поля от значения поля в документе. Обратите внимание, что некоторые поля имеют только код поля и не имеют разделителя полей и значения поля.

Поля могут быть вложенными.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldStart | [FieldStart](../../com.aspose.words/fieldstart) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitFootnoteEnd(Footnote footnote) {#visitFootnoteEnd-com.aspose.words.Footnote-}
```
public int visitFootnoteEnd(Footnote footnote)
```


Вызывается, когда закончилось перечисление текста сноски или концевой сноски.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| footnote | [Footnote](../../com.aspose.words/footnote) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitFootnoteStart(Footnote footnote) {#visitFootnoteStart-com.aspose.words.Footnote-}
```
public int visitFootnoteStart(Footnote footnote)
```


Вызывается, когда начинается перечисление текста сноски или концевой сноски.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| footnote | [Footnote](../../com.aspose.words/footnote) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitFormField(FormField formField) {#visitFormField-com.aspose.words.FormField-}
```
public int visitFormField(FormField formField)
```


Вызывается, когда в документе встречается поле формы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| formField | [FormField](../../com.aspose.words/formfield) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitGlossaryDocumentEnd(GlossaryDocument glossary) {#visitGlossaryDocumentEnd-com.aspose.words.GlossaryDocument-}
```
public int visitGlossaryDocumentEnd(GlossaryDocument glossary)
```


Вызывается, когда закончилось перечисление документа глоссария.

 Примечание. Узел документа глоссария и его дочерние элементы не посещаются, когда вы выполняете посетителя над[Document](../../com.aspose.words/document) . Если вы хотите выполнить посетителя над документом глоссария, вам нужно вызвать[GlossaryDocument.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/glossarydocument\#accept-com.aspose.words.DocumentVisitor-).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| glossary | [GlossaryDocument](../../com.aspose.words/glossarydocument) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitGlossaryDocumentStart(GlossaryDocument glossary) {#visitGlossaryDocumentStart-com.aspose.words.GlossaryDocument-}
```
public int visitGlossaryDocumentStart(GlossaryDocument glossary)
```


Вызывается, когда начинается перечисление документа глоссария.

 Примечание. Узел документа глоссария и его дочерние элементы не посещаются, когда вы выполняете посетителя над[Document](../../com.aspose.words/document) . Если вы хотите выполнить посетителя над документом глоссария, вам нужно вызвать[GlossaryDocument.accept(com.aspose.words.DocumentVisitor)](../../com.aspose.words/glossarydocument\#accept-com.aspose.words.DocumentVisitor-).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| glossary | [GlossaryDocument](../../com.aspose.words/glossarydocument) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitGroupShapeEnd(GroupShape groupShape) {#visitGroupShapeEnd-com.aspose.words.GroupShape-}
```
public int visitGroupShapeEnd(GroupShape groupShape)
```


Вызывается, когда закончилось перечисление формы группы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| groupShape | [GroupShape](../../com.aspose.words/groupshape) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitGroupShapeStart(GroupShape groupShape) {#visitGroupShapeStart-com.aspose.words.GroupShape-}
```
public int visitGroupShapeStart(GroupShape groupShape)
```


Вызывается, когда начинается перечисление формы группы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| groupShape | [GroupShape](../../com.aspose.words/groupshape) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitHeaderFooterEnd(HeaderFooter headerFooter) {#visitHeaderFooterEnd-com.aspose.words.HeaderFooter-}
```
public int visitHeaderFooterEnd(HeaderFooter headerFooter)
```


Вызывается, когда закончилось перечисление верхнего или нижнего колонтитула в разделе.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| headerFooter | [HeaderFooter](../../com.aspose.words/headerfooter) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitHeaderFooterStart(HeaderFooter headerFooter) {#visitHeaderFooterStart-com.aspose.words.HeaderFooter-}
```
public int visitHeaderFooterStart(HeaderFooter headerFooter)
```


Вызывается, когда начинается перечисление верхнего или нижнего колонтитула в разделе.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| headerFooter | [HeaderFooter](../../com.aspose.words/headerfooter) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitOfficeMathEnd(OfficeMath officeMath) {#visitOfficeMathEnd-com.aspose.words.OfficeMath-}
```
public int visitOfficeMathEnd(OfficeMath officeMath)
```


Вызывается после завершения перечисления объекта Office Math.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| officeMath | [OfficeMath](../../com.aspose.words/officemath) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitOfficeMathStart(OfficeMath officeMath) {#visitOfficeMathStart-com.aspose.words.OfficeMath-}
```
public int visitOfficeMathStart(OfficeMath officeMath)
```


Вызывается при запуске перечисления объекта Office Math.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| officeMath | [OfficeMath](../../com.aspose.words/officemath) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitParagraphEnd(Paragraph paragraph) {#visitParagraphEnd-com.aspose.words.Paragraph-}
```
public int visitParagraphEnd(Paragraph paragraph)
```


Вызывается, когда закончилось перечисление абзаца.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| paragraph | [Paragraph](../../com.aspose.words/paragraph) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitParagraphStart(Paragraph paragraph) {#visitParagraphStart-com.aspose.words.Paragraph-}
```
public int visitParagraphStart(Paragraph paragraph)
```


Вызывается, когда начинается перечисление абзаца.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| paragraph | [Paragraph](../../com.aspose.words/paragraph) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitRowEnd(Row row) {#visitRowEnd-com.aspose.words.Row-}
```
public int visitRowEnd(Row row)
```


Вызывается, когда закончилось перечисление строки таблицы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| row | [Row](../../com.aspose.words/row) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitRowStart(Row row) {#visitRowStart-com.aspose.words.Row-}
```
public int visitRowStart(Row row)
```


Вызывается, когда начинается перечисление строки таблицы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| row | [Row](../../com.aspose.words/row) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitRun(Run run) {#visitRun-com.aspose.words.Run-}
```
public int visitRun(Run run)
```


Вызывается при обнаружении фрагмента текста в .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| run | [Run](../../com.aspose.words/run) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitSectionEnd(Section section) {#visitSectionEnd-com.aspose.words.Section-}
```
public int visitSectionEnd(Section section)
```


Вызывается, когда закончилось перечисление секции.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| section | [Section](../../com.aspose.words/section) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitSectionStart(Section section) {#visitSectionStart-com.aspose.words.Section-}
```
public int visitSectionStart(Section section)
```


Вызывается, когда началось перечисление раздела.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| section | [Section](../../com.aspose.words/section) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitShapeEnd(Shape shape) {#visitShapeEnd-com.aspose.words.Shape-}
```
public int visitShapeEnd(Shape shape)
```


Вызывается, когда перечисление формы закончилось.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| shape | [Shape](../../com.aspose.words/shape) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitShapeStart(Shape shape) {#visitShapeStart-com.aspose.words.Shape-}
```
public int visitShapeStart(Shape shape)
```


Вызывается, когда начинается перечисление фигуры.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| shape | [Shape](../../com.aspose.words/shape) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitSmartTagEnd(SmartTag smartTag) {#visitSmartTagEnd-com.aspose.words.SmartTag-}
```
public int visitSmartTagEnd(SmartTag smartTag)
```


Вызывается, когда закончилось перечисление смарт-тега.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| smartTag | [SmartTag](../../com.aspose.words/smarttag) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitSmartTagStart(SmartTag smartTag) {#visitSmartTagStart-com.aspose.words.SmartTag-}
```
public int visitSmartTagStart(SmartTag smartTag)
```


Вызывается, когда начинается перечисление смарт-тега.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| smartTag | [SmartTag](../../com.aspose.words/smarttag) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitSpecialChar(SpecialChar specialChar) {#visitSpecialChar-com.aspose.words.SpecialChar-}
```
public int visitSpecialChar(SpecialChar specialChar)
```


 Вызывается, когда[SpecialChar](../../com.aspose.words/specialchar) узел встречается в документе.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| specialChar | [SpecialChar](../../com.aspose.words/specialchar) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы. Этот метод не вызывается для общих управляющих символов (см.[ControlChar](../../com.aspose.words/controlchar)), которые могут присутствовать в документе.
### visitStructuredDocumentTagEnd(StructuredDocumentTag sdt) {#visitStructuredDocumentTagEnd-com.aspose.words.StructuredDocumentTag-}
```
public int visitStructuredDocumentTagEnd(StructuredDocumentTag sdt)
```


Вызывается, когда закончилось перечисление тега структурированного документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| sdt | [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitStructuredDocumentTagRangeEnd(StructuredDocumentTagRangeEnd sdtRangeEnd) {#visitStructuredDocumentTagRangeEnd-com.aspose.words.StructuredDocumentTagRangeEnd-}
```
public int visitStructuredDocumentTagRangeEnd(StructuredDocumentTagRangeEnd sdtRangeEnd)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| sdtRangeEnd | [StructuredDocumentTagRangeEnd](../../com.aspose.words/structureddocumenttagrangeend) |  |

**Возвращает:**
инт
### visitStructuredDocumentTagRangeStart(StructuredDocumentTagRangeStart sdtRangeStart) {#visitStructuredDocumentTagRangeStart-com.aspose.words.StructuredDocumentTagRangeStart-}
```
public int visitStructuredDocumentTagRangeStart(StructuredDocumentTagRangeStart sdtRangeStart)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| sdtRangeStart | [StructuredDocumentTagRangeStart](../../com.aspose.words/structureddocumenttagrangestart) |  |

**Возвращает:**
инт
### visitStructuredDocumentTagStart(StructuredDocumentTag sdt) {#visitStructuredDocumentTagStart-com.aspose.words.StructuredDocumentTag-}
```
public int visitStructuredDocumentTagStart(StructuredDocumentTag sdt)
```


Вызывается, когда начинается перечисление тега структурированного документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| sdt | [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitSubDocument(SubDocument subDocument) {#visitSubDocument-com.aspose.words.SubDocument-}
```
public int visitSubDocument(SubDocument subDocument)
```


Вызывается при обнаружении вложенного документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| subDocument | [SubDocument](../../com.aspose.words/subdocument) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitTableEnd(Table table) {#visitTableEnd-com.aspose.words.Table-}
```
public int visitTableEnd(Table table)
```


Вызывается, когда закончилось перечисление таблицы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| table | [Table](../../com.aspose.words/table) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
### visitTableStart(Table table) {#visitTableStart-com.aspose.words.Table-}
```
public int visitTableStart(Table table)
```


Вызывается, когда начинается перечисление таблицы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| table | [Table](../../com.aspose.words/table) | Объект, который посещается. |

**Возвращает:**
 интервал - А[VisitorAction](../../com.aspose.words/visitoraction) значение, указывающее, как продолжить перечисление. Возвращаемое значение является одним из[VisitorAction](../../com.aspose.words/visitoraction) константы.
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
