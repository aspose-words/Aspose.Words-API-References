---
title: DocumentBuilder
second_title: Справочник по API Aspose.Words для Java
description: Предоставляет методы для вставки текстовых изображений и другого содержимого, определения шрифта, абзаца и форматирования раздела.
type: docs
weight: 122
url: /ru/java/com.aspose.words/documentbuilder/
---

**Наследование:**
java.lang.Object
```
public class DocumentBuilder
```

Предоставляет методы для вставки текста, изображений и другого содержимого, указания шрифта, форматирования абзаца и раздела.

 Чтобы узнать больше, посетите**Document Builder Overview** документальная статья.

**DocumentBuilder** делает процесс создания**Document** Полегче.**Document** представляет собой составной объект, состоящий из дерева узлов, и хотя вставка узлов содержимого непосредственно в дерево возможна, для этого требуется хорошее понимание структуры дерева.**DocumentBuilder** является «фасадом» сложной структуры**Document**и позволяет быстро и легко вставлять содержимое и форматирование.

 Создать**DocumentBuilder** и связать его с[getDocument()](../../com.aspose.words/documentbuilder\#getDocument--) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder\#setDocument-com.aspose.words.Document-).

**DocumentBuilder** имеет внутренний курсор, куда будет вставляться текст при вызове[write(java.lang.String)](../../com.aspose.words/documentbuilder\#write-java.lang.String-), [writeln(java.lang.String)](../../com.aspose.words/documentbuilder\#writeln-java.lang.String-), **M:Aspose.Words.DocumentBuilder.InsertBreak(Aspose.Words.BreakType)** и другие методы. Вы можете перемещаться по**DocumentBuilder** переместить курсор в другое место в документе с помощью различных методов MoveToXXX.

 Использовать[getFont()](../../com.aspose.words/documentbuilder\#getFont--) свойство, чтобы указать форматирование символов, которое будет применяться ко всему тексту, вставляемому с текущей позиции в документе и далее.

 Использовать[getParagraphFormat()](../../com.aspose.words/documentbuilder\#getParagraphFormat--) свойство, чтобы указать форматирование абзаца для текущего и всех абзацев, которые будут вставлены.

 Использовать[getPageSetup()](../../com.aspose.words/documentbuilder\#getPageSetup--) свойство, чтобы указать свойства страницы и раздела для текущего раздела и всех разделов, которые будут вставлены.

 Использовать[getCellFormat()](../../com.aspose.words/documentbuilder\#getCellFormat--) а также[getRowFormat()](../../com.aspose.words/documentbuilder\#getRowFormat--) properties, чтобы указать свойства форматирования для ячеек и строк таблицы. Пользователь[insertCell()](../../com.aspose.words/documentbuilder\#insertCell--) а также[endRow()](../../com.aspose.words/documentbuilder\#endRow--) методы построения таблицы.

 Обратите внимание, что**Font**, **ParagraphFormat** а также**PageSetup** свойства обновляются всякий раз, когда вы переходите к другому месту в документе, чтобы отразить свойства форматирования, доступные в новом месте.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [DocumentBuilder()](#DocumentBuilder--) | Инициализирует новый экземпляр этого класса. |
| [DocumentBuilder(Document doc)](#DocumentBuilder-com.aspose.words.Document-) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [clearCellAttrs()](#clearCellAttrs--) |  |
| [clearRowAttrs()](#clearRowAttrs--) |  |
| [clearRunAttrs()](#clearRunAttrs--) |  |
| [deleteRow(int tableIndex, int rowIndex)](#deleteRow-int-int-) | Удаляет строку из таблицы. |
| [endBookmark(String bookmarkName)](#endBookmark-java.lang.String-) | Отмечает текущую позицию в документе как конец закладки. |
| [endColumnBookmark(String bookmarkName)](#endColumnBookmark-java.lang.String-) | Отмечает текущую позицию в документе как конец закладки столбца. |
| [endEditableRange()](#endEditableRange--) | Помечает текущую позицию в документе как редактируемый конец диапазона. |
| [endEditableRange(EditableRangeStart start)](#endEditableRange-com.aspose.words.EditableRangeStart-) | Помечает текущую позицию в документе как редактируемый конец диапазона. |
| [endRow()](#endRow--) | Завершает строку таблицы в документе. |
| [endTable()](#endTable--) | Завершает таблицу в документе. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchCellAttr(int key)](#fetchCellAttr-int-) |  |
| [fetchInheritedCellAttr(int key)](#fetchInheritedCellAttr-int-) |  |
| [fetchInheritedRowAttr(int key)](#fetchInheritedRowAttr-int-) |  |
| [fetchInheritedRunAttr(int fontAttr)](#fetchInheritedRunAttr-int-) |  |
| [fetchRowAttr(int key)](#fetchRowAttr-int-) |  |
| [getBold()](#getBold--) | Истинно, если шрифт отформатирован как полужирный. |
| [getCellFormat()](#getCellFormat--) | Возвращает объект, представляющий текущие свойства форматирования ячейки таблицы. |
| [getClass()](#getClass--) |  |
| [getCurrentNode()](#getCurrentNode--) | Получает узел, выбранный в данный момент в этом DocumentBuilder. |
| [getCurrentParagraph()](#getCurrentParagraph--) | Получает абзац, выбранный в данный момент в этом DocumentBuilder. |
| [getCurrentSection()](#getCurrentSection--) | Получает раздел, выбранный в данный момент в этом DocumentBuilder. |
| [getCurrentStory()](#getCurrentStory--) | Получает историю, выбранную в настоящий момент в этом DocumentBuilder. |
| [getCurrentStructuredDocumentTag()](#getCurrentStructuredDocumentTag--) | Получает тег структурированного документа, выбранный в данный момент в этом DocumentBuilder. |
| [getDirectCellAttr(int key)](#getDirectCellAttr-int-) |  |
| [getDirectRowAttr(int key)](#getDirectRowAttr-int-) |  |
| [getDirectRunAttr(int fontAttr)](#getDirectRunAttr-int-) |  |
| [getDocument()](#getDocument--) |  Получает[getDocument()](../../com.aspose.words/documentbuilder\#getDocument--) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder\#setDocument-com.aspose.words.Document-) объект, к которому этот объект прикреплен. |
| [getFont()](#getFont--) | Возвращает объект, представляющий текущие свойства форматирования шрифта. |
| [getItalic()](#getItalic--) | Истинно, если шрифт отформатирован как курсив. |
| [getListFormat()](#getListFormat--) | Возвращает объект, представляющий текущие свойства форматирования списка. |
| [getPageSetup()](#getPageSetup--) | Возвращает объект, представляющий текущую настройку страницы и свойства раздела. |
| [getParagraphFormat()](#getParagraphFormat--) | Возвращает объект, представляющий текущие свойства форматирования абзаца. |
| [getRowFormat()](#getRowFormat--) | Возвращает объект, представляющий текущие свойства форматирования строки таблицы. |
| [getUnderline()](#getUnderline--) | Получает/устанавливает тип подчеркивания для текущего шрифта. |
| [hashCode()](#hashCode--) |  |
| [insertBreak(int breakType)](#insertBreak-int-) |  |
| [insertCell()](#insertCell--) | Вставляет ячейку таблицы в документ. |
| [insertChart(int chartType, double width, double height)](#insertChart-int-double-double-) |  |
| [insertChart(int chartType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertChart-int-int-double-int-double-double-double-int-) |  |
| [insertCheckBox(String name, boolean defaultValue, boolean checkedValue, int size)](#insertCheckBox-java.lang.String-boolean-boolean-int-) | Вставляет поле формы флажка в текущую позицию. |
| [insertCheckBox(String name, boolean checkedValue, int size)](#insertCheckBox-java.lang.String-boolean-int-) | Вставляет поле формы флажка в текущую позицию. |
| [insertComboBox(String name, String[] items, int selectedIndex)](#insertComboBox-java.lang.String-java.lang.String---int-) | Вставляет поле формы со списком в текущую позицию. |
| [insertDocument(Document srcDoc, int importFormatMode)](#insertDocument-com.aspose.words.Document-int-) |  |
| [insertDocument(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions)](#insertDocument-com.aspose.words.Document-int-com.aspose.words.ImportFormatOptions-) |  |
| [insertField(int fieldType, boolean updateField)](#insertField-int-boolean-) |  |
| [insertField(String fieldCode)](#insertField-java.lang.String-) | Вставляет поле Word в документ. |
| [insertField(String fieldCode, String fieldValue)](#insertField-java.lang.String-java.lang.String-) | Вставляет поле Word в документ без обновления результата поля. |
| [insertFootnote(int footnoteType, String footnoteText)](#insertFootnote-int-java.lang.String-) |  |
| [insertFootnote(int footnoteType, String footnoteText, String referenceMark)](#insertFootnote-int-java.lang.String-java.lang.String-) |  |
| [insertHorizontalRule()](#insertHorizontalRule--) | Вставляет в документ фигуру горизонтальной линейки. |
| [insertHtml(String html)](#insertHtml-java.lang.String-) | Вставляет строку HTML в документ. |
| [insertHtml(String html, boolean useBuilderFormatting)](#insertHtml-java.lang.String-boolean-) | Вставляет строку HTML в документ. |
| [insertHtml(String html, int options)](#insertHtml-java.lang.String-int-) |  |
| [insertHyperlink(String displayText, String urlOrBookmark, boolean isBookmark)](#insertHyperlink-java.lang.String-java.lang.String-boolean-) | Вставляет гиперссылку в документ. |
| [insertImage(byte[] imageBytes)](#insertImage-byte---) | Вставляет изображение из массива байтов в документ. |
| [insertImage(byte[] imageBytes, double width, double height)](#insertImage-byte---double-double-) | Вставляет встроенное изображение из массива байтов в документ и масштабирует его до указанного размера. |
| [insertImage(byte[] imageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertImage-byte---int-double-int-double-double-double-int-) |  |
| [insertImage(BufferedImage image)](#insertImage-java.awt.image.BufferedImage-) | Вставляет изображение в документ. |
| [insertImage(BufferedImage image, double width, double height)](#insertImage-java.awt.image.BufferedImage-double-double-) | Вставляет встроенное изображение из объекта в документ и масштабирует его до указанного размера. |
| [insertImage(BufferedImage image, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertImage-java.awt.image.BufferedImage-int-double-int-double-double-double-int-) |  |
| [insertImage(InputStream stream)](#insertImage-java.io.InputStream-) |  |
| [insertImage(InputStream stream, double width, double height)](#insertImage-java.io.InputStream-double-double-) |  |
| [insertImage(InputStream stream, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertImage-java.io.InputStream-int-double-int-double-double-double-int-) |  |
| [insertImage(String fileName)](#insertImage-java.lang.String-) | Вставляет изображение из файла или URL-адреса в документ. |
| [insertImage(String fileName, double width, double height)](#insertImage-java.lang.String-double-double-) | Вставляет встроенное изображение из файла или URL-адреса в документ и масштабирует его до указанного размера. |
| [insertImage(String fileName, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertImage-java.lang.String-int-double-int-double-double-double-int-) |  |
| [insertNode(Node node)](#insertNode-com.aspose.words.Node-) | Вставляет узел перед курсором. |
| [insertOleObject(InputStream stream, String progId, boolean asIcon, InputStream presentation)](#insertOleObject-java.io.InputStream-java.lang.String-boolean-java.io.InputStream-) |  |
| [insertOleObject(String fileName, boolean isLinked, boolean asIcon, InputStream presentation)](#insertOleObject-java.lang.String-boolean-boolean-java.io.InputStream-) |  |
| [insertOleObject(String fileName, String progId, boolean isLinked, boolean asIcon, InputStream presentation)](#insertOleObject-java.lang.String-java.lang.String-boolean-boolean-java.io.InputStream-) |  |
| [insertOleObjectAsIcon(InputStream stream, String progId, String iconFile, String iconCaption)](#insertOleObjectAsIcon-java.io.InputStream-java.lang.String-java.lang.String-java.lang.String-) |  |
| [insertOleObjectAsIcon(String fileName, boolean isLinked, String iconFile, String iconCaption)](#insertOleObjectAsIcon-java.lang.String-boolean-java.lang.String-java.lang.String-) | Вставляет встроенный или связанный объект OLE в виде значка в документ. |
| [insertOleObjectAsIcon(String fileName, String progId, boolean isLinked, String iconFile, String iconCaption)](#insertOleObjectAsIcon-java.lang.String-java.lang.String-boolean-java.lang.String-java.lang.String-) | Вставляет встроенный или связанный объект OLE в виде значка в документ. |
| [insertOnlineVideo(String videoUrl, double width, double height)](#insertOnlineVideo-java.lang.String-double-double-) | Вставляет объект онлайн-видео в документ и масштабирует его до указанного размера. |
| [insertOnlineVideo(String videoUrl, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertOnlineVideo-java.lang.String-int-double-int-double-double-double-int-) |  |
| [insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, double width, double height)](#insertOnlineVideo-java.lang.String-java.lang.String-byte---double-double-) | Вставляет объект онлайн-видео в документ и масштабирует его до указанного размера. |
| [insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertOnlineVideo-java.lang.String-java.lang.String-byte---int-double-int-double-double-double-int-) |  |
| [insertParagraph()](#insertParagraph--) | Вставляет разрыв абзаца в документ. |
| [insertShape(int shapeType, double width, double height)](#insertShape-int-double-double-) |  |
| [insertShape(int shapeType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)](#insertShape-int-int-double-int-double-double-double-int-) |  |
| [insertSignatureLine(SignatureLineOptions signatureLineOptions)](#insertSignatureLine-com.aspose.words.SignatureLineOptions-) | Вставляет строку подписи в текущую позицию. |
| [insertSignatureLine(SignatureLineOptions signatureLineOptions, int horzPos, double left, int vertPos, double top, int wrapType)](#insertSignatureLine-com.aspose.words.SignatureLineOptions-int-double-int-double-int-) |  |
| [insertStyleSeparator()](#insertStyleSeparator--) | Вставляет разделитель стилей в документ. |
| [insertTableOfContents(String switches)](#insertTableOfContents-java.lang.String-) | Вставляет в документ поле TOC (оглавление). |
| [insertTextInput(String name, int type, String format, String fieldValue, int maxLength)](#insertTextInput-java.lang.String-int-java.lang.String-java.lang.String-int-) |  |
| [isAtEndOfParagraph()](#isAtEndOfParagraph--) | Возвращает true, если курсор находится в конце текущего абзаца. |
| [isAtEndOfStructuredDocumentTag()](#isAtEndOfStructuredDocumentTag--) |  Возвращает**true** если курсор находится в конце тега структурированного документа. |
| [isAtStartOfParagraph()](#isAtStartOfParagraph--) | Возвращает true, если курсор находится в начале текущего абзаца (перед курсором нет текста). |
| [moveTo(Node node)](#moveTo-com.aspose.words.Node-) | Перемещает курсор на встроенный узел или в конец абзаца. |
| [moveToBookmark(String bookmarkName)](#moveToBookmark-java.lang.String-) | Перемещает курсор на закладку. |
| [moveToBookmark(String bookmarkName, boolean isStart, boolean isAfter)](#moveToBookmark-java.lang.String-boolean-boolean-) | Перемещает курсор к закладке с большей точностью. |
| [moveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex)](#moveToCell-int-int-int-int-) | Перемещает курсор на ячейку таблицы в текущем разделе. |
| [moveToDocumentEnd()](#moveToDocumentEnd--) | Перемещает курсор в конец документа. |
| [moveToDocumentStart()](#moveToDocumentStart--) | Перемещает курсор в начало документа. |
| [moveToField(Field field, boolean isAfter)](#moveToField-com.aspose.words.Field-boolean-) | Перемещает курсор в поле документа. |
| [moveToHeaderFooter(int headerFooterType)](#moveToHeaderFooter-int-) |  |
| [moveToMergeField(String fieldName)](#moveToMergeField-java.lang.String-) | Перемещает курсор в указанное поле слияния. |
| [moveToMergeField(String fieldName, boolean isAfter, boolean isDeleteField)](#moveToMergeField-java.lang.String-boolean-boolean-) | Перемещает поле слияния в указанное поле слияния. |
| [moveToParagraph(int paragraphIndex, int characterIndex)](#moveToParagraph-int-int-) | Перемещает курсор на абзац в текущем разделе. |
| [moveToSection(int sectionIndex)](#moveToSection-int-) | Перемещает курсор в начало тела в указанном разделе. |
| [moveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, int characterIndex)](#moveToStructuredDocumentTag-com.aspose.words.StructuredDocumentTag-int-) | Перемещает курсор на тег структурированного документа. |
| [moveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex)](#moveToStructuredDocumentTag-int-int-) | Перемещает курсор на тег структурированного документа в текущем разделе. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [popFont()](#popFont--) | Извлекает форматирование символов, ранее сохраненное в стеке. |
| [pushFont()](#pushFont--) | Сохраняет текущее форматирование символов в стек. |
| [removeRunAttr(int key)](#removeRunAttr-int-) |  |
| [resetToDefaultAttrs()](#resetToDefaultAttrs--) |  |
| [setBold(boolean value)](#setBold-boolean-) | Истинно, если шрифт отформатирован как полужирный. |
| [setCellAttr(int key, Object value)](#setCellAttr-int-java.lang.Object-) |  |
| [setDocument(Document value)](#setDocument-com.aspose.words.Document-) |  Устанавливает[getDocument()](../../com.aspose.words/documentbuilder\#getDocument--) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder\#setDocument-com.aspose.words.Document-) объект, к которому этот объект прикреплен. |
| [setItalic(boolean value)](#setItalic-boolean-) | Истинно, если шрифт отформатирован как курсив. |
| [setRowAttr(int key, Object value)](#setRowAttr-int-java.lang.Object-) |  |
| [setRunAttr(int fontAttr, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [setUnderline(int value)](#setUnderline-int-) | Получает/устанавливает тип подчеркивания для текущего шрифта. |
| [startBookmark(String bookmarkName)](#startBookmark-java.lang.String-) | Отмечает текущую позицию в документе как начало закладки. |
| [startColumnBookmark(String bookmarkName)](#startColumnBookmark-java.lang.String-) | Отмечает текущую позицию в документе как начало закладки столбца. |
| [startEditableRange()](#startEditableRange--) | Помечает текущую позицию в документе как начало редактируемого диапазона. |
| [startTable()](#startTable--) | Запускает таблицу в документе. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
| [write(String text)](#write-java.lang.String-) | Вставляет строку в документ в текущей позиции вставки. |
| [writeln()](#writeln--) | Вставляет разрыв абзаца в документ. |
| [writeln(String text)](#writeln-java.lang.String-) | Вставляет строку и разрыв абзаца в документ. |
### DocumentBuilder() {#DocumentBuilder--}
```
public DocumentBuilder()
```


 Инициализирует новый экземпляр этого класса. Создает новый**DocumentBuilder** объект и присоединяет его к новому[getDocument()](../../com.aspose.words/documentbuilder\#getDocument--) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder\#setDocument-com.aspose.words.Document-) объект.

### DocumentBuilder(Document doc) {#DocumentBuilder-com.aspose.words.Document-}
```
public DocumentBuilder(Document doc)
```


 Инициализирует новый экземпляр этого класса. Создает новый**DocumentBuilder** объект, присоединяется к указанному[getDocument()](../../com.aspose.words/documentbuilder\#getDocument--) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder\#setDocument-com.aspose.words.Document-) объект. Курсор находится в начале документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| doc | [Document](../../com.aspose.words/document) | Объект Document для присоединения. |

### clearCellAttrs() {#clearCellAttrs--}
```
public void clearCellAttrs()
```




### clearRowAttrs() {#clearRowAttrs--}
```
public void clearRowAttrs()
```




### clearRunAttrs() {#clearRunAttrs--}
```
public void clearRunAttrs()
```




### deleteRow(int tableIndex, int rowIndex) {#deleteRow-int-int-}
```
public Row deleteRow(int tableIndex, int rowIndex)
```


Удаляет строку из таблицы.

Если курсор находится внутри удаляемой строки, он перемещается на следующую строку или на следующий абзац после таблицы.

Если вы удалите строку из таблицы, которая содержит только одну строку, вся таблица будет удалена.

Для параметров индекса, когда индекс больше или равен 0, он указывает индекс с самого начала, где 0 является первым элементом. Когда индекс меньше 0, он указывает индекс с конца, где -1 является последним элементом.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| tableIndex | int | Индекс таблицы. |
| rowIndex | int | Индекс строки в таблице. |

**Возвращает:**
[Row](../../com.aspose.words/row) - Только что удаленный узел строки.
### endBookmark(String bookmarkName) {#endBookmark-java.lang.String-}
```
public BookmarkEnd endBookmark(String bookmarkName)
```


Отмечает текущую позицию в документе как конец закладки.

 Закладки в документе могут перекрываться и охватывать любой диапазон. Чтобы создать действительную закладку, вам нужно вызвать оба[startBookmark(java.lang.String)](../../com.aspose.words/documentbuilder\#startBookmark-java.lang.String-) а также[endBookmark(java.lang.String)](../../com.aspose.words/documentbuilder\#endBookmark-java.lang.String-) с тем же**bookmarkName** параметр.

Неправильно сформированные закладки или закладки с повторяющимися именами будут игнорироваться при сохранении документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| bookmarkName | java.lang.String | Название закладки. |

**Возвращает:**
[BookmarkEnd](../../com.aspose.words/bookmarkend) - Только что созданный конечный узел закладки.
### endColumnBookmark(String bookmarkName) {#endColumnBookmark-java.lang.String-}
```
public BookmarkEnd endColumnBookmark(String bookmarkName)
```


Отмечает текущую позицию в документе как конец закладки столбца. Позиция должна быть в ячейке таблицы.

 Закладка столбца охватывает один или несколько столбцов в диапазоне строк. Чтобы создать действительную закладку, вам нужно вызвать оба[startColumnBookmark(java.lang.String)](../../com.aspose.words/documentbuilder\#startColumnBookmark-java.lang.String-) а также[endColumnBookmark(java.lang.String)](../../com.aspose.words/documentbuilder\#endColumnBookmark-java.lang.String-) с тем же**bookmarkName** параметр.

Неправильно сформированные закладки или закладки с повторяющимися именами будут игнорироваться при сохранении документа.

 Фактическое положение вставленного[BookmarkEnd](../../com.aspose.words/bookmarkend) узел может отличаться от текущей позиции конструктора документов.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| bookmarkName | java.lang.String | Название закладки. |

**Возвращает:**
[BookmarkEnd](../../com.aspose.words/bookmarkend) - Только что созданный конечный узел закладки.
### endEditableRange() {#endEditableRange--}
```
public EditableRangeEnd endEditableRange()
```


Помечает текущую позицию в документе как редактируемый конец диапазона.

 Редактируемый диапазон в документе может перекрываться и охватывать любой диапазон. Чтобы создать действительный редактируемый диапазон, вам нужно вызвать оба[startEditableRange()](../../com.aspose.words/documentbuilder\#startEditableRange--) а также[endEditableRange()](../../com.aspose.words/documentbuilder\#endEditableRange--) или же[endEditableRange(com.aspose.words.EditableRangeStart)](../../com.aspose.words/documentbuilder\#endEditableRange-com.aspose.words.EditableRangeStart-) методы.

Неправильно сформированный редактируемый диапазон будет проигнорирован при сохранении документа.

**Возвращает:**
[EditableRangeEnd](../../com.aspose.words/editablerangeend) Только что созданный конечный узел редактируемого диапазона.
### endEditableRange(EditableRangeStart start) {#endEditableRange-com.aspose.words.EditableRangeStart-}
```
public EditableRangeEnd endEditableRange(EditableRangeStart start)
```


Помечает текущую позицию в документе как редактируемый конец диапазона.

Используйте эту перегрузку при создании вложенных редактируемых диапазонов.

 Редактируемый диапазон в документе может перекрываться и охватывать любой диапазон. Чтобы создать действительный редактируемый диапазон, вам нужно вызвать оба[startEditableRange()](../../com.aspose.words/documentbuilder\#startEditableRange--) а также[endEditableRange()](../../com.aspose.words/documentbuilder\#endEditableRange--) или же[endEditableRange(com.aspose.words.EditableRangeStart)](../../com.aspose.words/documentbuilder\#endEditableRange-com.aspose.words.EditableRangeStart-) методы.

Неправильно сформированный редактируемый диапазон будет проигнорирован при сохранении документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| start | [EditableRangeStart](../../com.aspose.words/editablerangestart) | Это начало редактируемого диапазона. |

**Возвращает:**
[EditableRangeEnd](../../com.aspose.words/editablerangeend) Только что созданный конечный узел редактируемого диапазона.
### endRow() {#endRow--}
```
public Row endRow()
```


Завершает строку таблицы в документе.

 Вызов**EndRow** для завершения строки таблицы. Если вы позвоните[insertCell()](../../com.aspose.words/documentbuilder\#insertCell--) сразу после этого таблица продолжается с новой строки.

 Использовать[getRowFormat()](../../com.aspose.words/documentbuilder\#getRowFormat--) свойство для указания форматирования строки.

**Возвращает:**
[Row](../../com.aspose.words/row) - Только что законченный узел строки.
### endTable() {#endTable--}
```
public Table endTable()
```


Завершает таблицу в документе.

 Этот метод следует вызывать только один раз после[endRow()](../../com.aspose.words/documentbuilder\#endRow--) назывался. Когда звонили,**EndTable** перемещает курсор из текущей ячейки, чтобы указать сразу после таблицы.

**Возвращает:**
[Table](../../com.aspose.words/table) - Только что законченный узел таблицы.
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
### fetchCellAttr(int key) {#fetchCellAttr-int-}
```
public Object fetchCellAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### fetchInheritedCellAttr(int key) {#fetchInheritedCellAttr-int-}
```
public Object fetchInheritedCellAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### fetchInheritedRowAttr(int key) {#fetchInheritedRowAttr-int-}
```
public Object fetchInheritedRowAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### fetchInheritedRunAttr(int fontAttr) {#fetchInheritedRunAttr-int-}
```
public Object fetchInheritedRunAttr(int fontAttr)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fontAttr | int |  |

**Возвращает:**
java.lang.Объект
### fetchRowAttr(int key) {#fetchRowAttr-int-}
```
public Object fetchRowAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### getBold() {#getBold--}
```
public boolean getBold()
```


Истинно, если шрифт отформатирован как полужирный.

**Возвращает:**
boolean - соответствующее логическое значение.
### getCellFormat() {#getCellFormat--}
```
public CellFormat getCellFormat()
```


Возвращает объект, представляющий текущие свойства форматирования ячейки таблицы.

**Возвращает:**
[CellFormat](../../com.aspose.words/cellformat) - Объект, представляющий текущие свойства форматирования ячейки таблицы.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getCurrentNode() {#getCurrentNode--}
```
public Node getCurrentNode()
```


Получает узел, выбранный в данный момент в этом DocumentBuilder.

**CurrentNode** является курсором**DocumentBuilder** и указывает на**Node** это прямой ребенок**Paragraph** . Любые операции вставки, которые вы выполняете с помощью**DocumentBuilder** будет вставлен перед**CurrentNode**.

 Если текущий абзац пуст или курсор находится непосредственно перед концом абзаца или тегом структурированного документа,**CurrentNode** возвращает ноль.

**Возвращает:**
[Node](../../com.aspose.words/node) Узел, выбранный в данный момент в этом DocumentBuilder.
### getCurrentParagraph() {#getCurrentParagraph--}
```
public Paragraph getCurrentParagraph()
```


 Получает абзац, выбранный в данный момент в этом DocumentBuilder.[getCurrentNode()](../../com.aspose.words/documentbuilder\#getCurrentNode--)

**Возвращает:**
[Paragraph](../../com.aspose.words/paragraph) - Абзац, выбранный в данный момент в этом DocumentBuilder.
### getCurrentSection() {#getCurrentSection--}
```
public Section getCurrentSection()
```


Получает раздел, выбранный в данный момент в этом DocumentBuilder.

**Возвращает:**
[Section](../../com.aspose.words/section) - Раздел, выбранный в данный момент в этом DocumentBuilder.
### getCurrentStory() {#getCurrentStory--}
```
public Story getCurrentStory()
```


Получает историю, выбранную в настоящий момент в этом DocumentBuilder.

**Возвращает:**
[Story](../../com.aspose.words/story) - История, выбранная в данный момент в этом DocumentBuilder.
### getCurrentStructuredDocumentTag() {#getCurrentStructuredDocumentTag--}
```
public StructuredDocumentTag getCurrentStructuredDocumentTag()
```


Получает тег структурированного документа, выбранный в данный момент в этом DocumentBuilder.

**Возвращает:**
[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) - Тег структурированного документа, выбранный в данный момент в этом DocumentBuilder.
### getDirectCellAttr(int key) {#getDirectCellAttr-int-}
```
public Object getDirectCellAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### getDirectRowAttr(int key) {#getDirectRowAttr-int-}
```
public Object getDirectRowAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### getDirectRunAttr(int fontAttr) {#getDirectRunAttr-int-}
```
public Object getDirectRunAttr(int fontAttr)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fontAttr | int |  |

**Возвращает:**
java.lang.Объект
### getDocument() {#getDocument--}
```
public Document getDocument()
```


 Получает[getDocument()](../../com.aspose.words/documentbuilder\#getDocument--) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder\#setDocument-com.aspose.words.Document-) объект, к которому этот объект прикреплен.

**Возвращает:**
[Document](../../com.aspose.words/document) -[getDocument()](../../com.aspose.words/documentbuilder\#getDocument--) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder\#setDocument-com.aspose.words.Document-) объект, к которому этот объект прикреплен.
### getFont() {#getFont--}
```
public Font getFont()
```


Возвращает объект, представляющий текущие свойства форматирования шрифта.

 Использовать**Font** для доступа и изменения свойств форматирования шрифта.

Укажите форматирование шрифта перед вставкой текста.

**Возвращает:**
[Font](../../com.aspose.words/font) - Объект, представляющий текущие свойства форматирования шрифта.
### getItalic() {#getItalic--}
```
public boolean getItalic()
```


Истинно, если шрифт отформатирован как курсив.

**Возвращает:**
boolean - соответствующее логическое значение.
### getListFormat() {#getListFormat--}
```
public ListFormat getListFormat()
```


Возвращает объект, представляющий текущие свойства форматирования списка.

**Возвращает:**
[ListFormat](../../com.aspose.words/listformat) - Объект, представляющий текущие свойства форматирования списка.
### getPageSetup() {#getPageSetup--}
```
public PageSetup getPageSetup()
```


Возвращает объект, представляющий текущую настройку страницы и свойства раздела.

**Возвращает:**
[PageSetup](../../com.aspose.words/pagesetup) - Объект, представляющий текущую настройку страницы и свойства раздела.
### getParagraphFormat() {#getParagraphFormat--}
```
public ParagraphFormat getParagraphFormat()
```


Возвращает объект, представляющий текущие свойства форматирования абзаца.

**Возвращает:**
[ParagraphFormat](../../com.aspose.words/paragraphformat) - Объект, представляющий текущие свойства форматирования абзаца.
### getRowFormat() {#getRowFormat--}
```
public RowFormat getRowFormat()
```


Возвращает объект, представляющий текущие свойства форматирования строки таблицы.

**Возвращает:**
[RowFormat](../../com.aspose.words/rowformat) - Объект, представляющий текущие свойства форматирования строки таблицы.
### getUnderline() {#getUnderline--}
```
public int getUnderline()
```


Получает/устанавливает тип подчеркивания для текущего шрифта.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[Underline](../../com.aspose.words/underline) константы.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### insertBreak(int breakType) {#insertBreak-int-}
```
public void insertBreak(int breakType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| breakType | int |  |

### insertCell() {#insertCell--}
```
public Cell insertCell()
```


Вставляет ячейку таблицы в документ.

 Чтобы начать стол, просто позвоните**InsertCell** После этого любой контент, который вы добавляете с помощью других методов[DocumentBuilder](../../com.aspose.words/documentbuilder) класс будет добавлен в текущую ячейку.

 Чтобы начать новую ячейку в той же строке, вызовите**InsertCell** опять таки.

 Чтобы завершить вызов строки таблицы[endRow()](../../com.aspose.words/documentbuilder\#endRow--).

 Использовать[getCellFormat()](../../com.aspose.words/documentbuilder\#getCellFormat--) свойство для указания форматирования ячейки.

**Возвращает:**
[Cell](../../com.aspose.words/cell) - Только что вставленный узел ячейки.
### insertChart(int chartType, double width, double height) {#insertChart-int-double-double-}
```
public Shape insertChart(int chartType, double width, double height)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| chartType | int |  |
| width | double |  |
| height | double |  |

**Возвращает:**
[Shape](../../com.aspose.words/shape)
### insertChart(int chartType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertChart-int-int-double-int-double-double-double-int-}
```
public Shape insertChart(int chartType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| chartType | int |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| width | double |  |
| height | double |  |
| wrapType | int |  |

**Возвращает:**
[Shape](../../com.aspose.words/shape)
### insertCheckBox(String name, boolean defaultValue, boolean checkedValue, int size) {#insertCheckBox-java.lang.String-boolean-boolean-int-}
```
public FormField insertCheckBox(String name, boolean defaultValue, boolean checkedValue, int size)
```


Вставляет поле формы флажка в текущую позицию.

Если указать имя для поля формы, то автоматически создается закладка с тем же именем.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Имя поля формы. Может быть пустой строкой. Значение длиннее 20 символов будет обрезано. |
| defaultValue | boolean | Значение по умолчанию поля формы флажка. |
| checkedValue | boolean | Текущий проверенный статус поля формы флажка. |
| size | int | Указывает размер флажка в пунктах. Укажите 0 для MS Word, чтобы автоматически рассчитать размер флажка. |

**Возвращает:**
[FormField](../../com.aspose.words/formfield) - Только что вставленный узел поля формы.
### insertCheckBox(String name, boolean checkedValue, int size) {#insertCheckBox-java.lang.String-boolean-int-}
```
public FormField insertCheckBox(String name, boolean checkedValue, int size)
```


Вставляет поле формы флажка в текущую позицию.

Если указать имя для поля формы, то автоматически создается закладка с тем же именем.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Имя поля формы. Может быть пустой строкой. Значение длиннее 20 символов будет обрезано. |
| checkedValue | boolean | Проверено состояние поля формы флажка. |
| size | int | Указывает размер флажка в пунктах. Укажите 0 для MS Word, чтобы автоматически рассчитать размер флажка. |

**Возвращает:**
[FormField](../../com.aspose.words/formfield) - Только что вставленный узел поля формы.
### insertComboBox(String name, String[] items, int selectedIndex) {#insertComboBox-java.lang.String-java.lang.String---int-}
```
public FormField insertComboBox(String name, String[] items, int selectedIndex)
```


Вставляет поле формы со списком в текущую позицию.

Если указать имя для поля формы, то автоматически создается закладка с тем же именем.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Имя поля формы. Может быть пустой строкой. Значение длиннее 20 символов будет обрезано. |
| items | java.lang.String[] | Элементы ComboBox. Максимум 25 штук. |
| selectedIndex | int | Индекс выбранного элемента в ComboBox. |

**Возвращает:**
[FormField](../../com.aspose.words/formfield) - Только что вставленный узел поля формы.
### insertDocument(Document srcDoc, int importFormatMode) {#insertDocument-com.aspose.words.Document-int-}
```
public Node insertDocument(Document srcDoc, int importFormatMode)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| srcDoc | [Document](../../com.aspose.words/document) |  |
| importFormatMode | int |  |

**Возвращает:**
[Node](../../com.aspose.words/node)
### insertDocument(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions) {#insertDocument-com.aspose.words.Document-int-com.aspose.words.ImportFormatOptions-}
```
public Node insertDocument(Document srcDoc, int importFormatMode, ImportFormatOptions importFormatOptions)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| srcDoc | [Document](../../com.aspose.words/document) |  |
| importFormatMode | int |  |
| importFormatOptions | [ImportFormatOptions](../../com.aspose.words/importformatoptions) |  |

**Возвращает:**
[Node](../../com.aspose.words/node)
### insertField(int fieldType, boolean updateField) {#insertField-int-boolean-}
```
public Field insertField(int fieldType, boolean updateField)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldType | int |  |
| updateField | boolean |  |

**Возвращает:**
[Field](../../com.aspose.words/field)
### insertField(String fieldCode) {#insertField-java.lang.String-}
```
public Field insertField(String fieldCode)
```


Вставляет поле Word в документ. Вставляет поле Word в документ и обновляет результат поля.

 Этот метод вставляет поле в документ и немедленно обновляет результат поля. Aspose.Words может обновлять поля большинства типов, но не всех. Подробнее см.[insertField(java.lang.String, java.lang.String)](../../com.aspose.words/documentbuilder\#insertField-java.lang.String--java.lang.String-) перегрузка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldCode | java.lang.String | Код поля для вставки (без фигурных скобок). |

**Возвращает:**
[Field](../../com.aspose.words/field) - А[Field](../../com.aspose.words/field) объект, представляющий вставленное поле.
### insertField(String fieldCode, String fieldValue) {#insertField-java.lang.String-java.lang.String-}
```
public Field insertField(String fieldCode, String fieldValue)
```


Вставляет поле Word в документ без обновления результата поля.

Поля в документах Microsoft Word состоят из кода поля и результата поля. Код поля подобен формуле, а результат поля подобен значению, которое выдает формула. Код поля также может содержать переключатели полей, которые являются дополнительными инструкциями для выполнения определенного действия.

 Вы можете переключаться между отображением кодов полей и результатов в документе в Microsoft Word с помощью сочетания клавиш Alt+F9. Коды полей отображаются между фигурными скобками (\ {\} ).

Чтобы создать поле, вам необходимо указать тип поля, код поля и значение поля «заполнитель». Если вы не уверены в синтаксисе определенного кода поля, сначала создайте поле в Microsoft Word и переключитесь на просмотр его кода поля.

 Aspose.Words может вычислять результаты поля для большинства типов полей, но этот метод не обновляет результат поля автоматически. Поскольку результат поля не вычисляется автоматически, ожидается, что вы передадите некоторое строковое значение (или даже пустую строку), которое будет вставлено в результат поля. Это значение останется в поле результата в качестве заполнителя, пока поле не будет обновлено. Чтобы обновить результат поля, вы можете позвонить[Field.update()](../../com.aspose.words/field\#update--) на возвращенном вам объекте поля или[Document.updateFields()](../../com.aspose.words/document\#updateFields--) для обновления полей во всем документе.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldCode | java.lang.String | Код поля для вставки (без фигурных скобок). |
| fieldValue | java.lang.String | Значение поля для вставки. Передайте null для полей, которые не имеют значения. |

**Возвращает:**
[Field](../../com.aspose.words/field) - А[Field](../../com.aspose.words/field) объект, представляющий вставленное поле.
### insertFootnote(int footnoteType, String footnoteText) {#insertFootnote-int-java.lang.String-}
```
public Footnote insertFootnote(int footnoteType, String footnoteText)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| footnoteType | int |  |
| footnoteText | java.lang.String |  |

**Возвращает:**
[Footnote](../../com.aspose.words/footnote)
### insertFootnote(int footnoteType, String footnoteText, String referenceMark) {#insertFootnote-int-java.lang.String-java.lang.String-}
```
public Footnote insertFootnote(int footnoteType, String footnoteText, String referenceMark)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| footnoteType | int |  |
| footnoteText | java.lang.String |  |
| referenceMark | java.lang.String |  |

**Возвращает:**
[Footnote](../../com.aspose.words/footnote)
### insertHorizontalRule() {#insertHorizontalRule--}
```
public Shape insertHorizontalRule()
```


Вставляет в документ фигуру горизонтальной линейки.

**Возвращает:**
[Shape](../../com.aspose.words/shape) - Форма, которая представляет собой горизонтальное правило.
### insertHtml(String html) {#insertHtml-java.lang.String-}
```
public void insertHtml(String html)
```


Вставляет строку HTML в документ.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| html | java.lang.String | Строка HTML для вставки в документ. Вы можете использовать этот метод для вставки фрагмента HTML или всего документа HTML. |

### insertHtml(String html, boolean useBuilderFormatting) {#insertHtml-java.lang.String-boolean-}
```
public void insertHtml(String html, boolean useBuilderFormatting)
```


Вставляет строку HTML в документ.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| html | java.lang.String | Строка HTML для вставки в документ. |
| useBuilderFormatting | boolean |  Значение, указывающее, является ли форматирование, указанное в[DocumentBuilder](../../com.aspose.words/documentbuilder) используется в качестве базового форматирования для текста, импортированного из HTML.

Вы можете использовать этот метод для вставки фрагмента HTML или всего документа HTML.

 Когда useBuilderFormatting имеет значение false ,[DocumentBuilder](../../com.aspose.words/documentbuilder) форматирование игнорируется, а форматирование вставленного текста основано на форматировании HTML по умолчанию. В результате текст выглядит так, как он отображается в браузерах.

 Когда useBuilderFormatting имеет значение true , форматирование вставленного текста основано на[DocumentBuilder](../../com.aspose.words/documentbuilder) форматирование, и текст выглядит так, как будто он был вставлен с[write(java.lang.String)](../../com.aspose.words/documentbuilder\#write-java.lang.String-). |

### insertHtml(String html, int options) {#insertHtml-java.lang.String-int-}
```
public void insertHtml(String html, int options)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| html | java.lang.String |  |
| options | int |  |

### insertHyperlink(String displayText, String urlOrBookmark, boolean isBookmark) {#insertHyperlink-java.lang.String-java.lang.String-boolean-}
```
public Field insertHyperlink(String displayText, String urlOrBookmark, boolean isBookmark)
```


Вставляет гиперссылку в документ.

 Обратите внимание, что вам необходимо указать форматирование шрифта для отображаемого текста гиперссылки явно с помощью параметра[getFont()](../../com.aspose.words/documentbuilder\#getFont--) имущество.

 Этот метод вызывает внутренние вызовы[insertField(java.lang.String)](../../com.aspose.words/documentbuilder\#insertField-java.lang.String-) чтобы вставить в документ поле ГИПЕРССЫЛКИ MS Word.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| displayText | java.lang.String | Текст ссылки для отображения в документе. |
| urlOrBookmark | java.lang.String | Назначение ссылки. Может быть URL-адресом или названием закладки внутри документа. Этот метод всегда добавляет апострофы в начале и в конце URL-адреса. |
| isBookmark | boolean | Истинно, если предыдущий параметр является именем закладки внутри документа; false — предыдущий параметр является URL-адресом. |

**Возвращает:**
[Field](../../com.aspose.words/field) - А[Field](../../com.aspose.words/field) объект, представляющий вставленное поле.
### insertImage(byte[] imageBytes) {#insertImage-byte---}
```
public Shape insertImage(byte[] imageBytes)
```


Вставляет изображение из массива байтов в документ. Изображение вставляется в строку и в масштабе 100%.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| imageBytes | byte[] | Массив байтов, содержащий изображение. |

**Возвращает:**
[Shape](../../com.aspose.words/shape) - Только что вставленный узел изображения.

 Вы можете изменить размер изображения, местоположение, метод позиционирования и другие параметры с помощью[Shape](../../com.aspose.words/shape) объект, возвращаемый этим методом.
### insertImage(byte[] imageBytes, double width, double height) {#insertImage-byte---double-double-}
```
public Shape insertImage(byte[] imageBytes, double width, double height)
```


Вставляет встроенное изображение из массива байтов в документ и масштабирует его до указанного размера.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| imageBytes | byte[] | Массив байтов, содержащий изображение. |
| width | double | Ширина изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | double | Высота изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |

**Возвращает:**
[Shape](../../com.aspose.words/shape) - Только что вставленный узел изображения.

 Вы можете изменить размер изображения, местоположение, метод позиционирования и другие параметры с помощью[Shape](../../com.aspose.words/shape) объект, возвращаемый этим методом.
### insertImage(byte[] imageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertImage-byte---int-double-int-double-double-double-int-}
```
public Shape insertImage(byte[] imageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| imageBytes | byte[] |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| width | double |  |
| height | double |  |
| wrapType | int |  |

**Возвращает:**
[Shape](../../com.aspose.words/shape)
### insertImage(BufferedImage image) {#insertImage-java.awt.image.BufferedImage-}
```
public Shape insertImage(BufferedImage image)
```


Вставляет изображение в документ. Вставляет изображение из объекта в документ. Изображение вставляется в строку и в масштабе 100%.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| image | java.awt.image.BufferedImage | Изображение для вставки в документ. |

**Возвращает:**
[Shape](../../com.aspose.words/shape) - Только что вставленный узел изображения.

 Вы можете изменить размер изображения, местоположение, метод позиционирования и другие параметры с помощью[Shape](../../com.aspose.words/shape) объект, возвращаемый этим методом.

Aspose.Words вставит изображение в формате PNG и с настройками по умолчанию. Если вы хотите вставить BufferedImage в другом формате или с другими настройками, вам нужно сохранить изображение в массив байтов и использовать[insertImage(byte[])](../../com.aspose.words/documentbuilder\#insertImage-byte---).
### insertImage(BufferedImage image, double width, double height) {#insertImage-java.awt.image.BufferedImage-double-double-}
```
public Shape insertImage(BufferedImage image, double width, double height)
```


Вставляет встроенное изображение из объекта в документ и масштабирует его до указанного размера.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| image | java.awt.image.BufferedImage | Изображение для вставки в документ. |
| width | double | Ширина изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | double | Высота изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |

**Возвращает:**
[Shape](../../com.aspose.words/shape) - Только что вставленный узел изображения.

 Вы можете изменить размер изображения, местоположение, метод позиционирования и другие параметры с помощью[Shape](../../com.aspose.words/shape) объект, возвращаемый этим методом.

Aspose.Words вставит изображение в формате PNG и с настройками по умолчанию. Если вы хотите вставить BufferedImage в другом формате или с другими настройками, вам нужно сохранить изображение в массив байтов и использовать[insertImage(byte[])](../../com.aspose.words/documentbuilder\#insertImage-byte---).
### insertImage(BufferedImage image, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertImage-java.awt.image.BufferedImage-int-double-int-double-double-double-int-}
```
public Shape insertImage(BufferedImage image, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| image | java.awt.image.BufferedImage |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| width | double |  |
| height | double |  |
| wrapType | int |  |

**Возвращает:**
[Shape](../../com.aspose.words/shape)
### insertImage(InputStream stream) {#insertImage-java.io.InputStream-}
```
public Shape insertImage(InputStream stream)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | java.io.InputStream |  |

**Возвращает:**
[Shape](../../com.aspose.words/shape)
### insertImage(InputStream stream, double width, double height) {#insertImage-java.io.InputStream-double-double-}
```
public Shape insertImage(InputStream stream, double width, double height)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| width | double |  |
| height | double |  |

**Возвращает:**
[Shape](../../com.aspose.words/shape)
### insertImage(InputStream stream, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertImage-java.io.InputStream-int-double-int-double-double-double-int-}
```
public Shape insertImage(InputStream stream, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| width | double |  |
| height | double |  |
| wrapType | int |  |

**Возвращает:**
[Shape](../../com.aspose.words/shape)
### insertImage(String fileName) {#insertImage-java.lang.String-}
```
public Shape insertImage(String fileName)
```


Вставляет изображение из файла или URL-адреса в документ. Изображение вставляется в строку и в масштабе 100%.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String | Файл с изображением. Может быть любым допустимым локальным или удаленным URI. |

**Возвращает:**
[Shape](../../com.aspose.words/shape) - Только что вставленный узел изображения.

Эта перегрузка автоматически загрузит изображение перед вставкой в документ, если вы укажете удаленный URI.

 Вы можете изменить размер изображения, местоположение, метод позиционирования и другие параметры с помощью[Shape](../../com.aspose.words/shape) объект, возвращаемый этим методом.
### insertImage(String fileName, double width, double height) {#insertImage-java.lang.String-double-double-}
```
public Shape insertImage(String fileName, double width, double height)
```


Вставляет встроенное изображение из файла или URL-адреса в документ и масштабирует его до указанного размера.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String | Файл, содержащий изображение. |
| width | double | Ширина изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | double | Высота изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |

**Возвращает:**
[Shape](../../com.aspose.words/shape) - Только что вставленный узел изображения.

 Вы можете изменить размер изображения, местоположение, метод позиционирования и другие параметры с помощью[Shape](../../com.aspose.words/shape) объект, возвращаемый этим методом.
### insertImage(String fileName, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertImage-java.lang.String-int-double-int-double-double-double-int-}
```
public Shape insertImage(String fileName, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| width | double |  |
| height | double |  |
| wrapType | int |  |

**Возвращает:**
[Shape](../../com.aspose.words/shape)
### insertNode(Node node) {#insertNode-com.aspose.words.Node-}
```
public void insertNode(Node node)
```


Вставляет узел перед курсором.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node) |  |

### insertOleObject(InputStream stream, String progId, boolean asIcon, InputStream presentation) {#insertOleObject-java.io.InputStream-java.lang.String-boolean-java.io.InputStream-}
```
public Shape insertOleObject(InputStream stream, String progId, boolean asIcon, InputStream presentation)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| progId | java.lang.String |  |
| asIcon | boolean |  |
| presentation | java.io.InputStream |  |

**Возвращает:**
[Shape](../../com.aspose.words/shape)
### insertOleObject(String fileName, boolean isLinked, boolean asIcon, InputStream presentation) {#insertOleObject-java.lang.String-boolean-boolean-java.io.InputStream-}
```
public Shape insertOleObject(String fileName, boolean isLinked, boolean asIcon, InputStream presentation)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String |  |
| isLinked | boolean |  |
| asIcon | boolean |  |
| presentation | java.io.InputStream |  |

**Возвращает:**
[Shape](../../com.aspose.words/shape)
### insertOleObject(String fileName, String progId, boolean isLinked, boolean asIcon, InputStream presentation) {#insertOleObject-java.lang.String-java.lang.String-boolean-boolean-java.io.InputStream-}
```
public Shape insertOleObject(String fileName, String progId, boolean isLinked, boolean asIcon, InputStream presentation)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String |  |
| progId | java.lang.String |  |
| isLinked | boolean |  |
| asIcon | boolean |  |
| presentation | java.io.InputStream |  |

**Возвращает:**
[Shape](../../com.aspose.words/shape)
### insertOleObjectAsIcon(InputStream stream, String progId, String iconFile, String iconCaption) {#insertOleObjectAsIcon-java.io.InputStream-java.lang.String-java.lang.String-java.lang.String-}
```
public Shape insertOleObjectAsIcon(InputStream stream, String progId, String iconFile, String iconCaption)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| progId | java.lang.String |  |
| iconFile | java.lang.String |  |
| iconCaption | java.lang.String |  |

**Возвращает:**
[Shape](../../com.aspose.words/shape)
### insertOleObjectAsIcon(String fileName, boolean isLinked, String iconFile, String iconCaption) {#insertOleObjectAsIcon-java.lang.String-boolean-java.lang.String-java.lang.String-}
```
public Shape insertOleObjectAsIcon(String fileName, boolean isLinked, String iconFile, String iconCaption)
```


Вставляет встроенный или связанный объект OLE в виде значка в документ. Позволяет указать файл значка и заголовок. Определяет тип объекта OLE, используя расширение файла.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String | Полный путь к файлу. |
| isLinked | boolean | Если true, то вставляется связанный объект OLE, в противном случае вставляется встроенный объект OLE. |
| iconFile | java.lang.String | Полный путь к файлу ICO. Если значение равно null, Aspose.Words будет использовать предопределенное изображение. |
| iconCaption | java.lang.String | Подпись к значку. Если значение равно null, Aspose.Words будет использовать имя файла. |

**Возвращает:**
[Shape](../../com.aspose.words/shape) Узел Shape, содержащий объект Ole и вставленный в текущую позицию Builder.
### insertOleObjectAsIcon(String fileName, String progId, boolean isLinked, String iconFile, String iconCaption) {#insertOleObjectAsIcon-java.lang.String-java.lang.String-boolean-java.lang.String-java.lang.String-}
```
public Shape insertOleObjectAsIcon(String fileName, String progId, boolean isLinked, String iconFile, String iconCaption)
```


Вставляет встроенный или связанный объект OLE в виде значка в документ. Позволяет указать файл значка и заголовок. Определяет тип объекта OLE, используя заданный параметр progID.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String | Полный путь к файлу. |
| progId | java.lang.String | ProgId объекта OLE. |
| isLinked | boolean | Если true, то вставляется связанный объект OLE, в противном случае вставляется встроенный объект OLE. |
| iconFile | java.lang.String | Полный путь к файлу ICO. Если значение равно null, Aspose.Words будет использовать предопределенное изображение. |
| iconCaption | java.lang.String | Подпись к значку. Если значение равно null, Aspose.Words будет использовать имя файла. |

**Возвращает:**
[Shape](../../com.aspose.words/shape) Узел Shape, содержащий объект Ole и вставленный в текущую позицию Builder.
### insertOnlineVideo(String videoUrl, double width, double height) {#insertOnlineVideo-java.lang.String-double-double-}
```
public Shape insertOnlineVideo(String videoUrl, double width, double height)
```


Вставляет объект онлайн-видео в документ и масштабирует его до указанного размера.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| videoUrl | java.lang.String | URL-адрес видео. |
| width | double | Ширина изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | double | Высота изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |

**Возвращает:**
[Shape](../../com.aspose.words/shape) - Только что вставленный узел изображения.

 Вы можете изменить размер изображения, местоположение, метод позиционирования и другие параметры с помощью[Shape](../../com.aspose.words/shape) объект, возвращаемый этим методом.

Поддерживается вставка онлайн-видео со следующих ресурсов:

 *  https://www.youtube.com/
 *  https://vimeo.com/

 Если ваше онлайн-видео отображается неправильно, используйте[insertOnlineVideo(java.lang.String, java.lang.String, byte[], double, double)](../../com.aspose.words/documentbuilder\#insertOnlineVideo-java.lang.String--java.lang.String--byte----double--double-), который принимает пользовательский встроенный HTML-код.

Код для встраивания видео может варьироваться в зависимости от провайдера, для получения подробной информации обратитесь к соответствующему провайдеру.
### insertOnlineVideo(String videoUrl, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertOnlineVideo-java.lang.String-int-double-int-double-double-double-int-}
```
public Shape insertOnlineVideo(String videoUrl, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| videoUrl | java.lang.String |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| width | double |  |
| height | double |  |
| wrapType | int |  |

**Возвращает:**
[Shape](../../com.aspose.words/shape)
### insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, double width, double height) {#insertOnlineVideo-java.lang.String-java.lang.String-byte---double-double-}
```
public Shape insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, double width, double height)
```


Вставляет объект онлайн-видео в документ и масштабирует его до указанного размера.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| videoUrl | java.lang.String | URL-адрес видео. |
| videoEmbedCode | java.lang.String | Код для встраивания видео. |
| thumbnailImageBytes | byte[] | Байты миниатюры изображения. |
| width | double | Ширина изображения в точках. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |
| height | double | Высота изображения в пунктах. Может быть отрицательным или нулевым значением для запроса масштаба 100%. |

**Возвращает:**
[Shape](../../com.aspose.words/shape) - Только что вставленный узел изображения.

 Вы можете изменить размер изображения, местоположение, метод позиционирования и другие параметры с помощью[Shape](../../com.aspose.words/shape) объект, возвращаемый этим методом.
### insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertOnlineVideo-java.lang.String-java.lang.String-byte---int-double-int-double-double-double-int-}
```
public Shape insertOnlineVideo(String videoUrl, String videoEmbedCode, byte[] thumbnailImageBytes, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| videoUrl | java.lang.String |  |
| videoEmbedCode | java.lang.String |  |
| thumbnailImageBytes | byte[] |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| width | double |  |
| height | double |  |
| wrapType | int |  |

**Возвращает:**
[Shape](../../com.aspose.words/shape)
### insertParagraph() {#insertParagraph--}
```
public Paragraph insertParagraph()
```


Вставляет разрыв абзаца в документ.

 Текущее форматирование абзаца, заданное параметром[getParagraphFormat()](../../com.aspose.words/documentbuilder\#getParagraphFormat--) используется свойство.

Разбивает текущий абзац на два. После вставки абзаца курсор помещается в начало нового абзаца.

**Возвращает:**
[Paragraph](../../com.aspose.words/paragraph) Только что вставленный узел абзаца. Это тот же узел, что и[getCurrentParagraph()](../../com.aspose.words/documentbuilder\#getCurrentParagraph--).
### insertShape(int shapeType, double width, double height) {#insertShape-int-double-double-}
```
public Shape insertShape(int shapeType, double width, double height)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| shapeType | int |  |
| width | double |  |
| height | double |  |

**Возвращает:**
[Shape](../../com.aspose.words/shape)
### insertShape(int shapeType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType) {#insertShape-int-int-double-int-double-double-double-int-}
```
public Shape insertShape(int shapeType, int horzPos, double left, int vertPos, double top, double width, double height, int wrapType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| shapeType | int |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| width | double |  |
| height | double |  |
| wrapType | int |  |

**Возвращает:**
[Shape](../../com.aspose.words/shape)
### insertSignatureLine(SignatureLineOptions signatureLineOptions) {#insertSignatureLine-com.aspose.words.SignatureLineOptions-}
```
public Shape insertSignatureLine(SignatureLineOptions signatureLineOptions)
```


Вставляет строку подписи в текущую позицию.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| signatureLineOptions | [SignatureLineOptions](../../com.aspose.words/signaturelineoptions) | Объект, в котором хранятся параметры создания строки подписи. |

**Возвращает:**
[Shape](../../com.aspose.words/shape) - Только что вставленный узел строки подписи.
### insertSignatureLine(SignatureLineOptions signatureLineOptions, int horzPos, double left, int vertPos, double top, int wrapType) {#insertSignatureLine-com.aspose.words.SignatureLineOptions-int-double-int-double-int-}
```
public Shape insertSignatureLine(SignatureLineOptions signatureLineOptions, int horzPos, double left, int vertPos, double top, int wrapType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| signatureLineOptions | [SignatureLineOptions](../../com.aspose.words/signaturelineoptions) |  |
| horzPos | int |  |
| left | double |  |
| vertPos | int |  |
| top | double |  |
| wrapType | int |  |

**Возвращает:**
[Shape](../../com.aspose.words/shape)
### insertStyleSeparator() {#insertStyleSeparator--}
```
public void insertStyleSeparator()
```


Вставляет разделитель стилей в документ. Этот метод позволяет применять разные стили абзаца к двум разным частям текстовой строки.

### insertTableOfContents(String switches) {#insertTableOfContents-java.lang.String-}
```
public Field insertTableOfContents(String switches)
```


Вставляет в документ поле TOC (оглавление).

Этот метод вставляет поле TOC (оглавление) в документ в текущей позиции.

Оглавление в документе Word может быть построено несколькими способами и отформатировано с использованием различных параметров. Способ построения и отображения таблицы в Microsoft Word управляется переключателями полей.

Самый простой способ указать переключатели — вставить и настроить оглавление в документе Word с помощью меню Вставка->Справочник->Указатель и таблицы, а затем включить отображение кодов полей, чтобы увидеть переключатели. Вы можете нажать Alt+F9 в Microsoft Word, чтобы включить или выключить отображение кодов полей.

Например, после создания оглавления в документ вставляется следующее поле:**\{ TOC \\o "1-3" \\h \\z \}** . Вы можете скопировать**\\o "1-3" \\h \\z** и используйте его как параметр переключателей.

 Обратите внимание, что**InsertTableOfContents** только вставит поле TOC, но фактически не создаст оглавление. Оглавление создается Microsoft Word при обновлении поля.

Если вы вставите оглавление с помощью этого метода, а затем откроете файл в Microsoft Word, вы не увидите оглавление, поскольку поле TOC еще не обновлено.

В Microsoft Word поля не обновляются автоматически при открытии документа, но вы можете обновить поля в документе в любое время, нажав F9.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| switches | java.lang.String | Поле TOC переключается. |

**Возвращает:**
[Field](../../com.aspose.words/field)
### insertTextInput(String name, int type, String format, String fieldValue, int maxLength) {#insertTextInput-java.lang.String-int-java.lang.String-java.lang.String-int-}
```
public FormField insertTextInput(String name, int type, String format, String fieldValue, int maxLength)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String |  |
| type | int |  |
| format | java.lang.String |  |
| fieldValue | java.lang.String |  |
| maxLength | int |  |

**Возвращает:**
[FormField](../../com.aspose.words/formfield)
### isAtEndOfParagraph() {#isAtEndOfParagraph--}
```
public boolean isAtEndOfParagraph()
```


Возвращает true, если курсор находится в конце текущего абзаца.

**Возвращает:**
boolean — Истинно, если курсор находится в конце текущего абзаца.
### isAtEndOfStructuredDocumentTag() {#isAtEndOfStructuredDocumentTag--}
```
public boolean isAtEndOfStructuredDocumentTag()
```


 Возвращает**true** если курсор находится в конце тега структурированного документа.

**Возвращает:**
 логический -**true** если курсор находится в конце тега структурированного документа.
### isAtStartOfParagraph() {#isAtStartOfParagraph--}
```
public boolean isAtStartOfParagraph()
```


Возвращает true, если курсор находится в начале текущего абзаца (перед курсором нет текста).

**Возвращает:**
boolean — Истинно, если курсор находится в начале текущего абзаца (перед курсором нет текста).
### moveTo(Node node) {#moveTo-com.aspose.words.Node-}
```
public void moveTo(Node node)
```


Перемещает курсор на встроенный узел или в конец абзаца.

 Когда*node* является узлом встроенного уровня, курсор перемещается на этот узел, и перед этим узлом будет вставлено дополнительное содержимое.

 Когда*node* это**Paragraph**курсор перемещается в конец абзаца, и дальнейшее содержимое будет вставлено непосредственно перед разрывом абзаца.

 Когда*node* является узлом уровня блока, но не абзацем, курсор перемещается в конец первого абзаца в узел уровня блока, а дальнейшее содержимое будет вставлено непосредственно перед разрывом абзаца.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| node | [Node](../../com.aspose.words/node) | Узел должен быть абзацем или прямым потомком абзаца. |

### moveToBookmark(String bookmarkName) {#moveToBookmark-java.lang.String-}
```
public boolean moveToBookmark(String bookmarkName)
```


Перемещает курсор на закладку.

Перемещает курсор в позицию сразу после начала закладки с указанным именем.

Сравнение не чувствительно к регистру. Если закладка не найдена, возвращается false и курсор не перемещается.

Вставка нового текста не заменяет существующий текст закладки.

Обратите внимание, что некоторые закладки в документе назначены полям формы. Переход на такую закладку и вставка туда текста вставляет текст в код поля формы. Хотя это не сделает поле формы недействительным, вставленный текст не будет виден, поскольку он становится частью кода поля.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| bookmarkName | java.lang.String | Имя закладки, на которую нужно переместить курсор. |

**Возвращает:**
boolean - Истинно, если закладка найдена; ложно в противном случае.
### moveToBookmark(String bookmarkName, boolean isStart, boolean isAfter) {#moveToBookmark-java.lang.String-boolean-boolean-}
```
public boolean moveToBookmark(String bookmarkName, boolean isStart, boolean isAfter)
```


Перемещает курсор к закладке с большей точностью.

Перемещает курсор в положение до или после начала или конца закладки.

Если нужная позиция не на встроенном уровне, выполняется переход к следующему абзацу.

Сравнение не чувствительно к регистру. Если закладка не найдена, возвращается false и курсор не перемещается.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| bookmarkName | java.lang.String | Имя закладки, на которую нужно переместить курсор. |
| isStart | boolean | При значении true курсор перемещается в начало закладки. При значении false перемещает курсор в конец закладки. |
| isAfter | boolean | При значении true курсор перемещается после начальной или конечной позиции закладки. При значении false курсор перемещается перед начальной или конечной позицией закладки. |

**Возвращает:**
boolean - Истинно, если закладка найдена; ложно в противном случае.
### moveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex) {#moveToCell-int-int-int-int-}
```
public void moveToCell(int tableIndex, int rowIndex, int columnIndex, int characterIndex)
```


Перемещает курсор на ячейку таблицы в текущем разделе.

Навигация осуществляется внутри текущей истории текущего раздела.

Для параметров индекса, когда индекс больше или равен 0, он указывает индекс с самого начала, где 0 является первым элементом. Когда индекс меньше 0, он указывает индекс с конца, где -1 является последним элементом.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| tableIndex | int | Индекс таблицы для перехода. |
| rowIndex | int | Индекс строки в таблице. |
| columnIndex | int | Индекс столбца в таблице. |
| characterIndex | int | Индекс символа внутри ячейки. Отрицательное значение позволяет указать позицию от конца ячейки. Используйте -1, чтобы перейти в конец ячейки. |

### moveToDocumentEnd() {#moveToDocumentEnd--}
```
public void moveToDocumentEnd()
```


Перемещает курсор в конец документа.

### moveToDocumentStart() {#moveToDocumentStart--}
```
public void moveToDocumentStart()
```


Перемещает курсор в начало документа.

### moveToField(Field field, boolean isAfter) {#moveToField-com.aspose.words.Field-boolean-}
```
public void moveToField(Field field, boolean isAfter)
```


Перемещает курсор в поле документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| field | [Field](../../com.aspose.words/field) | Поле для перемещения курсора. |
| isAfter | boolean | При значении true курсор перемещается после конца поля. При значении false курсор перемещается перед началом поля. |

### moveToHeaderFooter(int headerFooterType) {#moveToHeaderFooter-int-}
```
public void moveToHeaderFooter(int headerFooterType)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| headerFooterType | int |  |

### moveToMergeField(String fieldName) {#moveToMergeField-java.lang.String-}
```
public boolean moveToMergeField(String fieldName)
```


Перемещает курсор в указанное поле слияния. Перемещает курсор в положение сразу за указанным полем слияния и удаляет поле слияния.

Обратите внимание, что этот метод удаляет поле слияния из документа после перемещения курсора.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldName | java.lang.String | Нечувствительное к регистру имя поля слияния. |

**Возвращает:**
boolean - True, если поле слияния было найдено и курсор был перемещен; ложно в противном случае.
### moveToMergeField(String fieldName, boolean isAfter, boolean isDeleteField) {#moveToMergeField-java.lang.String-boolean-boolean-}
```
public boolean moveToMergeField(String fieldName, boolean isAfter, boolean isDeleteField)
```


Перемещает поле слияния в указанное поле слияния.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fieldName | java.lang.String | Нечувствительное к регистру имя поля слияния. |
| isAfter | boolean | При значении true курсор перемещается после конца поля. При значении false курсор перемещается перед началом поля. |
| isDeleteField | boolean | При значении true удаляет поле слияния. |

**Возвращает:**
boolean - True, если поле слияния было найдено и курсор был перемещен; ложно в противном случае.
### moveToParagraph(int paragraphIndex, int characterIndex) {#moveToParagraph-int-int-}
```
public void moveToParagraph(int paragraphIndex, int characterIndex)
```


Перемещает курсор на абзац в текущем разделе.

Навигация осуществляется внутри текущей истории текущего раздела. То есть, если вы переместите курсор к основному заголовку первого раздела, тогда параметр parapIndex задает индекс абзаца внутри этого заголовка этого раздела.

Когда paranIndex больше или равен 0, он указывает индекс от начала раздела, где 0 — это первый абзац. Когда paraIndex меньше 0, он указывает индекс с конца раздела, где -1 является последним абзацем.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| paragraphIndex | int | Индекс абзаца, к которому нужно перейти. |
| characterIndex | int | Индекс символа внутри абзаца. Отрицательное значение позволяет указать позицию от конца абзаца. Используйте -1, чтобы перейти в конец абзаца. |

### moveToSection(int sectionIndex) {#moveToSection-int-}
```
public void moveToSection(int sectionIndex)
```


Перемещает курсор в начало тела в указанном разделе.

Когда sectionIndex больше или равен 0, он указывает индекс с начала документа, где 0 является первым разделом. Когда sectionIndex меньше 0, он указывает индекс с конца документа, где -1 является последним разделом.

 Курсор переместится на первый абзац в**Body** указанного раздела.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| sectionIndex | int | Индекс раздела, к которому нужно перейти. |

### moveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, int characterIndex) {#moveToStructuredDocumentTag-com.aspose.words.StructuredDocumentTag-int-}
```
public void moveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, int characterIndex)
```


Перемещает курсор на тег структурированного документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| structuredDocumentTag | [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) | Тег структурированного документа, к которому нужно перейти. |
| characterIndex | int | Индекс символа внутри тега структурированного документа. Отрицательное значение позволяет указать позицию от конца тега структурированного документа. Используйте -1, чтобы перейти в конец тега структурированного документа. Если тег структурированного документа находится на уровне блока и вы хотите переместить курсор в конец его последнего абзаца, укажите -2. |

### moveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex) {#moveToStructuredDocumentTag-int-int-}
```
public void moveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex)
```


Перемещает курсор на тег структурированного документа в текущем разделе.

Навигация осуществляется внутри текущей истории текущего раздела. То есть, если вы переместите курсор к основному заголовку первого раздела, тогдаstructuredDocumentTagIndex укажет индекс тега структурированного документа внутри этого заголовка этого раздела.

Когда StructuredDocumentTagIndex больше или равен 0, он указывает индекс с начала раздела, где 0 является первым тегом структурированного документа. Когда StructuredDocumentTagIndex меньше 0, он указывает индекс с конца раздела, где -1 является последним тегом структурированного документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| structuredDocumentTagIndex | int | Индекс тега структурированного документа, к которому нужно перейти. |
| characterIndex | int | Индекс символа внутри тега структурированного документа. Отрицательное значение позволяет указать позицию от конца тега структурированного документа. Используйте -1, чтобы перейти в конец тега структурированного документа. Если тег структурированного документа находится на уровне блока и вы хотите переместить курсор в конец его последнего абзаца, укажите -2. |

### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### popFont() {#popFont--}
```
public void popFont()
```


Извлекает форматирование символов, ранее сохраненное в стеке.

### pushFont() {#pushFont--}
```
public void pushFont()
```


Сохраняет текущее форматирование символов в стек.

### removeRunAttr(int key) {#removeRunAttr-int-}
```
public void removeRunAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

### resetToDefaultAttrs() {#resetToDefaultAttrs--}
```
public void resetToDefaultAttrs()
```




### setBold(boolean value) {#setBold-boolean-}
```
public void setBold(boolean value)
```


Истинно, если шрифт отформатирован как полужирный.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setCellAttr(int key, Object value) {#setCellAttr-int-java.lang.Object-}
```
public void setCellAttr(int key, Object value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setDocument(Document value) {#setDocument-com.aspose.words.Document-}
```
public void setDocument(Document value)
```


 Устанавливает[getDocument()](../../com.aspose.words/documentbuilder\#getDocument--) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder\#setDocument-com.aspose.words.Document-) объект, к которому этот объект прикреплен.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [Document](../../com.aspose.words/document) | [getDocument()](../../com.aspose.words/documentbuilder\#getDocument--) / [setDocument(com.aspose.words.Document)](../../com.aspose.words/documentbuilder\#setDocument-com.aspose.words.Document-) объект, к которому этот объект прикреплен. |

### setItalic(boolean value) {#setItalic-boolean-}
```
public void setItalic(boolean value)
```


Истинно, если шрифт отформатирован как курсив.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setRowAttr(int key, Object value) {#setRowAttr-int-java.lang.Object-}
```
public void setRowAttr(int key, Object value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setRunAttr(int fontAttr, Object value) {#setRunAttr-int-java.lang.Object-}
```
public void setRunAttr(int fontAttr, Object value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fontAttr | int |  |
| value | java.lang.Object |  |

### setUnderline(int value) {#setUnderline-int-}
```
public void setUnderline(int value)
```


Получает/устанавливает тип подчеркивания для текущего шрифта.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[Underline](../../com.aspose.words/underline) константы. |

### startBookmark(String bookmarkName) {#startBookmark-java.lang.String-}
```
public BookmarkStart startBookmark(String bookmarkName)
```


Отмечает текущую позицию в документе как начало закладки.

 Закладки в документе могут перекрываться и охватывать любой диапазон. Чтобы создать действительную закладку, вам нужно вызвать оба[startBookmark(java.lang.String)](../../com.aspose.words/documentbuilder\#startBookmark-java.lang.String-) а также[endBookmark(java.lang.String)](../../com.aspose.words/documentbuilder\#endBookmark-java.lang.String-) с тем же**bookmarkName** параметр.

Неправильно сформированные закладки или закладки с повторяющимися именами будут игнорироваться при сохранении документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| bookmarkName | java.lang.String | Название закладки. |

**Возвращает:**
[BookmarkStart](../../com.aspose.words/bookmarkstart) Только что созданный начальный узел закладки.
### startColumnBookmark(String bookmarkName) {#startColumnBookmark-java.lang.String-}
```
public BookmarkStart startColumnBookmark(String bookmarkName)
```


Отмечает текущую позицию в документе как начало закладки столбца. Позиция должна быть в ячейке таблицы.

 Закладка столбца охватывает один или несколько столбцов в диапазоне строк. Чтобы создать действительную закладку, вам нужно вызвать оба[startColumnBookmark(java.lang.String)](../../com.aspose.words/documentbuilder\#startColumnBookmark-java.lang.String-) а также[endColumnBookmark(java.lang.String)](../../com.aspose.words/documentbuilder\#endColumnBookmark-java.lang.String-) с тем же**bookmarkName** параметр.

Неправильно сформированные закладки или закладки с повторяющимися именами будут игнорироваться при сохранении документа.

 Фактическое положение вставленного[BookmarkStart](../../com.aspose.words/bookmarkstart) узел может отличаться от текущей позиции конструктора документов.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| bookmarkName | java.lang.String | Название закладки. |

**Возвращает:**
[BookmarkStart](../../com.aspose.words/bookmarkstart) Только что созданный начальный узел закладки.
### startEditableRange() {#startEditableRange--}
```
public EditableRangeStart startEditableRange()
```


Помечает текущую позицию в документе как начало редактируемого диапазона.

 Редактируемый диапазон в документе может перекрываться и охватывать любой диапазон. Чтобы создать действительный редактируемый диапазон, вам нужно вызвать оба[startEditableRange()](../../com.aspose.words/documentbuilder\#startEditableRange--) а также[endEditableRange()](../../com.aspose.words/documentbuilder\#endEditableRange--) или же[endEditableRange(com.aspose.words.EditableRangeStart)](../../com.aspose.words/documentbuilder\#endEditableRange-com.aspose.words.EditableRangeStart-) методы.

Неправильно сформированный редактируемый диапазон будет проигнорирован при сохранении документа.

**Возвращает:**
[EditableRangeStart](../../com.aspose.words/editablerangestart) - Только что созданный начальный узел редактируемого диапазона.
### startTable() {#startTable--}
```
public Table startTable()
```


Запускает таблицу в документе.

 Следующий метод для вызова[insertCell()](../../com.aspose.words/documentbuilder\#insertCell--).

Этот метод запускает вложенную таблицу при вызове внутри ячейки.

**Возвращает:**
[Table](../../com.aspose.words/table) - Только что созданный узел таблицы.
### toString() {#toString--}
```
public String toString()
```




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

### write(String text) {#write-java.lang.String-}
```
public void write(String text)
```


 Вставляет строку в документ в текущей позиции вставки. Текущее форматирование шрифта, заданное параметром[getFont()](../../com.aspose.words/documentbuilder\#getFont--) используется свойство.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| text | java.lang.String | Строка для вставки в документ. |

### writeln() {#writeln--}
```
public void writeln()
```


Вставляет разрыв абзаца в документ.

 Звонки[insertParagraph()](../../com.aspose.words/documentbuilder\#insertParagraph--).

### writeln(String text) {#writeln-java.lang.String-}
```
public void writeln(String text)
```


 Вставляет строку и разрыв абзаца в документ. Текущий шрифт и форматирование абзаца, указанные[getFont()](../../com.aspose.words/documentbuilder\#getFont--) а также[getParagraphFormat()](../../com.aspose.words/documentbuilder\#getParagraphFormat--) используются свойства.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| text | java.lang.String | Строка для вставки в документ. |
