---
title: FieldToc
second_title: Справочник по API Aspose.Words для Java
description: Реализует поле TOC.
type: docs
weight: 255
url: /ru/java/com.aspose.words/fieldtoc/
---

**Наследование:**
java.lang.Object, [com.aspose.words.Field](../../com.aspose.words/field)
```
public class FieldToc extends Field
```

Реализует поле TOC.

 Чтобы узнать больше, посетите**Working with Fields** документальная статья.

Создает оглавление (которое также может быть таблицей рисунков), используя записи, заданные полями TC, их уровнями заголовков и указанными стилями, и вставляет эту таблицу в это место в документе.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAreCustomStylesSpecified()](#getAreCustomStylesSpecified--) |  |
| [getBookmarkName()](#getBookmarkName--) | Получает имя закладки, помечающей часть документа, используемую для построения таблицы. |
| [getCaptionlessTableOfFiguresLabel()](#getCaptionlessTableOfFiguresLabel--) | Получает имя идентификатора последовательности, используемого при построении таблицы рисунков, которая не включает метку и номер подписи. |
| [getClass()](#getClass--) |  |
| [getCustomStyles()](#getCustomStyles--) | Получает список стилей, отличных от встроенных стилей заголовков, для включения в оглавление. |
| [getDisplayResult()](#getDisplayResult--) | Получает текст, представляющий отображаемый результат поля. |
| [getEnd()](#getEnd--) | Получает узел, представляющий конец поля. |
| [getEntryIdentifier()](#getEntryIdentifier--) | Получает строку, которая должна соответствовать идентификаторам типов включаемых полей TC. |
| [getEntryLevelRange()](#getEntryLevelRange--) | Получает диапазон уровней включаемых записей оглавления. |
| [getEntrySeparator()](#getEntrySeparator--) | Получает последовательность символов, разделяющую запись и номер ее страницы. |
| [getEntryTypeCore()](#getEntryTypeCore--) |  |
| [getFieldCode()](#getFieldCode--) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет). |
| [getFieldCode(boolean includeChildFieldCodes)](#getFieldCode-boolean-) | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет). |
| [getFormat()](#getFormat--) | Получает[FieldFormat](../../com.aspose.words/fieldformat) объект, предоставляющий типизированный доступ к форматированию поля. |
| [getHeadingLevelRange()](#getHeadingLevelRange--) | Получает диапазон уровней заголовков для включения. |
| [getHideInWebLayout()](#getHideInWebLayout--) | Определяет, следует ли скрывать закладку и номера страниц в представлении веб-макета. |
| [getIncludeRefDocFields()](#getIncludeRefDocFields--) |  |
| [getIncludeTocEntryFields()](#getIncludeTocEntryFields--) |  |
| [getInsertHyperlinks()](#getInsertHyperlinks--) | Получает, следует ли сделать записи оглавления гиперссылками. |
| [getLevelForCustomStyle(Paragraph paragraph, Style style)](#getLevelForCustomStyle-com.aspose.words.Paragraph-com.aspose.words.Style-) |  |
| [getLocaleId()](#getLocaleId--) | Получает LCID поля. |
| [getPageNumberOmittingLevelRange()](#getPageNumberOmittingLevelRange--) | Получает диапазон уровней записей оглавления, из которых следует исключить номера страниц. |
| [getPrefixedSequenceIdentifier()](#getPrefixedSequenceIdentifier--) | Получает идентификатор последовательности, для которой к номеру страницы записи следует добавить префикс. |
| [getPreserveLineBreaks()](#getPreserveLineBreaks--) | Определяет, следует ли сохранять символы новой строки в записях таблицы. |
| [getPreserveTabs()](#getPreserveTabs--) | Определяет, следует ли сохранять записи вкладок в записях таблицы. |
| [getRangeBookmark()](#getRangeBookmark--) |  |
| [getResult()](#getResult--) | Получает текст, который находится между разделителем полей и концом поля. |
| [getSeparator()](#getSeparator--) | Получает узел, представляющий разделитель полей. |
| [getSequenceSeparator()](#getSequenceSeparator--) | Получает последовательность символов, используемую для разделения порядковых номеров и номеров страниц. |
| [getSkipTables()](#getSkipTables--) |  |
| [getStart()](#getStart--) | Получает узел, представляющий начало поля. |
| [getSwitchType(String switchName)](#getSwitchType-java.lang.String-) |  |
| [getTableOfFiguresLabel()](#getTableOfFiguresLabel--) | Получает имя идентификатора последовательности, используемого при построении таблицы рисунков. |
| [getType()](#getType--) | Получает тип поля Microsoft Word. |
| [getUseParagraphOutlineLevel()](#getUseParagraphOutlineLevel--) | Получает, следует ли использовать примененный уровень структуры абзаца. |
| [hashCode()](#hashCode--) |  |
| [isBookmarkRangeSpecified()](#isBookmarkRangeSpecified--) |  |
| [isDirty()](#isDirty--) | Получает информацию о том, является ли текущий результат поля неправильным (устаревшим) из-за других изменений, внесенных в документ. |
| [isDirty(boolean value)](#isDirty-boolean-) | Устанавливает, является ли текущий результат поля неправильным (устаревшим) из-за других изменений, внесенных в документ. |
| [isEntryLevelRangeSpecified()](#isEntryLevelRangeSpecified--) |  |
| [isHeadingLevelRangeSpecified()](#isHeadingLevelRangeSpecified--) |  |
| [isLocked()](#isLocked--) | Получает, заблокировано ли поле (не должно пересчитывать его результат). |
| [isLocked(boolean value)](#isLocked-boolean-) | Устанавливает, будет ли поле заблокировано (не должно пересчитывать свой результат). |
| [isTableOfFigures()](#isTableOfFigures--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove()](#remove--) | Удаляет поле из документа. |
| [setBookmarkName(String value)](#setBookmarkName-java.lang.String-) | Задает имя закладки, которая отмечает часть документа, используемую для построения таблицы. |
| [setCaptionlessTableOfFiguresLabel(String value)](#setCaptionlessTableOfFiguresLabel-java.lang.String-) | Задает имя идентификатора последовательности, используемого при построении таблицы рисунков, которая не включает метку и номер подписи. |
| [setCustomStyles(String value)](#setCustomStyles-java.lang.String-) | Задает список стилей, отличных от встроенных стилей заголовков, для включения в оглавление. |
| [setEntryIdentifier(String value)](#setEntryIdentifier-java.lang.String-) | Задает строку, которая должна соответствовать идентификаторам типов включаемых полей TC. |
| [setEntryLevelRange(String value)](#setEntryLevelRange-java.lang.String-) | Задает диапазон уровней включаемых записей оглавления. |
| [setEntrySeparator(String value)](#setEntrySeparator-java.lang.String-) | Задает последовательность символов, разделяющую запись и номер ее страницы. |
| [setHeadingLevelRange(String value)](#setHeadingLevelRange-java.lang.String-) | Устанавливает диапазон уровней заголовков для включения. |
| [setHideInWebLayout(boolean value)](#setHideInWebLayout-boolean-) | Устанавливает, следует ли скрывать закладку и номера страниц в представлении веб-макета. |
| [setInsertHyperlinks(boolean value)](#setInsertHyperlinks-boolean-) | Устанавливает, следует ли делать записи оглавления гиперссылками. |
| [setLocaleId(int value)](#setLocaleId-int-) | Устанавливает LCID поля. |
| [setPageNumberOmittingLevelRange(String value)](#setPageNumberOmittingLevelRange-java.lang.String-) | Задает диапазон уровней записей оглавления, из которых следует опускать номера страниц. |
| [setPrefixedSequenceIdentifier(String value)](#setPrefixedSequenceIdentifier-java.lang.String-) | Задает идентификатор последовательности, для которой к номеру страницы записи следует добавить префикс. |
| [setPreserveLineBreaks(boolean value)](#setPreserveLineBreaks-boolean-) | Устанавливает, сохранять ли символы новой строки в записях таблицы. |
| [setPreserveTabs(boolean value)](#setPreserveTabs-boolean-) | Устанавливает, сохранять ли записи вкладок в записях таблицы. |
| [setResult(String value)](#setResult-java.lang.String-) | Задает текст, который находится между разделителем полей и концом поля. |
| [setSequenceSeparator(String value)](#setSequenceSeparator-java.lang.String-) | Задает последовательность символов, используемую для разделения порядковых номеров и номеров страниц. |
| [setTableOfFiguresLabel(String value)](#setTableOfFiguresLabel-java.lang.String-) | Задает имя идентификатора последовательности, используемого при построении таблицы рисунков. |
| [setUseParagraphOutlineLevel(boolean value)](#setUseParagraphOutlineLevel-boolean-) | Устанавливает, следует ли использовать примененный уровень структуры абзаца. |
| [toString()](#toString--) |  |
| [unlink()](#unlink--) | Выполняет развязку поля. |
| [update()](#update--) | Выполняет обновление поля. |
| [update(boolean ignoreMergeFormat)](#update-boolean-) | Выполняет обновление поля. |
| [updatePageNumbers()](#updatePageNumbers--) | Обновляет номера страниц для элементов в этом оглавлении. |
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
### getAreCustomStylesSpecified() {#getAreCustomStylesSpecified--}
```
public boolean getAreCustomStylesSpecified()
```




**Возвращает:**
логический
### getBookmarkName() {#getBookmarkName--}
```
public String getBookmarkName()
```


Получает имя закладки, помечающей часть документа, используемую для построения таблицы.

**Возвращает:**
java.lang.String — имя закладки, которая отмечает часть документа, используемую для построения таблицы.
### getCaptionlessTableOfFiguresLabel() {#getCaptionlessTableOfFiguresLabel--}
```
public String getCaptionlessTableOfFiguresLabel()
```


Получает имя идентификатора последовательности, используемого при построении таблицы рисунков, которая не включает метку и номер подписи.

**Возвращает:**
java.lang.String — имя идентификатора последовательности, используемого при построении таблицы рисунков, которая не включает метку и номер подписи.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getCustomStyles() {#getCustomStyles--}
```
public String getCustomStyles()
```


Получает список стилей, отличных от встроенных стилей заголовков, для включения в оглавление.

**Возвращает:**
java.lang.String — список стилей, отличных от встроенных стилей заголовков, для включения в оглавление.
### getDisplayResult() {#getDisplayResult--}
```
public String getDisplayResult()
```


 Получает текст, представляющий отображаемый результат поля.[Document.updateListLabels()](../../com.aspose.words/document\#updateListLabels--) метод должен быть вызван, чтобы получить правильное значение для[FieldListNum](../../com.aspose.words/fieldlistnum), [FieldAutoNum](../../com.aspose.words/fieldautonum), [FieldAutoNumOut](../../com.aspose.words/fieldautonumout) а также[FieldAutoNumLgl](../../com.aspose.words/fieldautonumlgl) поля.

**Возвращает:**
java.lang.String — текст, представляющий результат отображаемого поля.
### getEnd() {#getEnd--}
```
public FieldEnd getEnd()
```


Получает узел, представляющий конец поля.

**Возвращает:**
[FieldEnd](../../com.aspose.words/fieldend) - Узел, представляющий конец поля.
### getEntryIdentifier() {#getEntryIdentifier--}
```
public String getEntryIdentifier()
```


Получает строку, которая должна соответствовать идентификаторам типов включаемых полей TC.

**Возвращает:**
java.lang.String — строка, которая должна соответствовать идентификаторам типов включаемых полей TC.
### getEntryLevelRange() {#getEntryLevelRange--}
```
public String getEntryLevelRange()
```


Получает диапазон уровней включаемых записей оглавления.

**Возвращает:**
java.lang.String — диапазон уровней записей оглавления, которые необходимо включить.
### getEntrySeparator() {#getEntrySeparator--}
```
public String getEntrySeparator()
```


Получает последовательность символов, разделяющую запись и номер ее страницы.

**Возвращает:**
java.lang.String — последовательность символов, разделяющая запись и номер ее страницы.
### getEntryTypeCore() {#getEntryTypeCore--}
```
public int getEntryTypeCore()
```




**Возвращает:**
инт
### getFieldCode() {#getFieldCode--}
```
public String getFieldCode()
```


Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет). Включены как код поля, так и результат дочерних полей.

**Возвращает:**
java.lang.String
### getFieldCode(boolean includeChildFieldCodes) {#getFieldCode-boolean-}
```
public String getFieldCode(boolean includeChildFieldCodes)
```


Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| includeChildFieldCodes | boolean | \{ True, если должны быть включены коды дочерних полей. |

**Возвращает:**
java.lang.String
### getFormat() {#getFormat--}
```
public FieldFormat getFormat()
```


Получает[FieldFormat](../../com.aspose.words/fieldformat) объект, предоставляющий типизированный доступ к форматированию поля.

**Возвращает:**
[FieldFormat](../../com.aspose.words/fieldformat) - А[FieldFormat](../../com.aspose.words/fieldformat) объект, предоставляющий типизированный доступ к форматированию поля.
### getHeadingLevelRange() {#getHeadingLevelRange--}
```
public String getHeadingLevelRange()
```


Получает диапазон уровней заголовков для включения.

**Возвращает:**
java.lang.String — диапазон уровней заголовков для включения.
### getHideInWebLayout() {#getHideInWebLayout--}
```
public boolean getHideInWebLayout()
```


Определяет, следует ли скрывать закладку и номера страниц в представлении веб-макета.

**Возвращает:**
boolean — следует ли скрывать закладку и номера страниц в представлении веб-макета.
### getIncludeRefDocFields() {#getIncludeRefDocFields--}
```
public boolean getIncludeRefDocFields()
```




**Возвращает:**
логический
### getIncludeTocEntryFields() {#getIncludeTocEntryFields--}
```
public boolean getIncludeTocEntryFields()
```




**Возвращает:**
логический
### getInsertHyperlinks() {#getInsertHyperlinks--}
```
public boolean getInsertHyperlinks()
```


Получает, следует ли сделать записи оглавления гиперссылками.

**Возвращает:**
boolean - Делать ли записи оглавления гиперссылками.
### getLevelForCustomStyle(Paragraph paragraph, Style style) {#getLevelForCustomStyle-com.aspose.words.Paragraph-com.aspose.words.Style-}
```
public int getLevelForCustomStyle(Paragraph paragraph, Style style)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| paragraph | [Paragraph](../../com.aspose.words/paragraph) |  |
| style | [Style](../../com.aspose.words/style) |  |

**Возвращает:**
инт
### getLocaleId() {#getLocaleId--}
```
public int getLocaleId()
```


Получает LCID поля.

**Возвращает:**
int — LCID поля.
### getPageNumberOmittingLevelRange() {#getPageNumberOmittingLevelRange--}
```
public String getPageNumberOmittingLevelRange()
```


Получает диапазон уровней записей оглавления, из которых следует исключить номера страниц.

**Возвращает:**
java.lang.String — диапазон уровней записей оглавления, из которых пропускаются номера страниц.
### getPrefixedSequenceIdentifier() {#getPrefixedSequenceIdentifier--}
```
public String getPrefixedSequenceIdentifier()
```


Получает идентификатор последовательности, для которой к номеру страницы записи следует добавить префикс.

**Возвращает:**
java.lang.String — идентификатор последовательности, для которой к номеру страницы записи следует добавить префикс.
### getPreserveLineBreaks() {#getPreserveLineBreaks--}
```
public boolean getPreserveLineBreaks()
```


Определяет, следует ли сохранять символы новой строки в записях таблицы.

**Возвращает:**
boolean — следует ли сохранять символы новой строки в записях таблицы.
### getPreserveTabs() {#getPreserveTabs--}
```
public boolean getPreserveTabs()
```


Определяет, следует ли сохранять записи вкладок в записях таблицы.

**Возвращает:**
boolean — сохранять ли записи вкладок в записях таблицы.
### getRangeBookmark() {#getRangeBookmark--}
```
public Bookmark getRangeBookmark()
```




**Возвращает:**
[Bookmark](../../com.aspose.words/bookmark)
### getResult() {#getResult--}
```
public String getResult()
```


Получает текст, который находится между разделителем полей и концом поля.

**Возвращает:**
java.lang.String — текст между разделителем полей и концом поля.
### getSeparator() {#getSeparator--}
```
public FieldSeparator getSeparator()
```


Получает узел, представляющий разделитель полей. Может быть нулевым.

**Возвращает:**
[FieldSeparator](../../com.aspose.words/fieldseparator) - Узел, представляющий разделитель полей.
### getSequenceSeparator() {#getSequenceSeparator--}
```
public String getSequenceSeparator()
```


Получает последовательность символов, используемую для разделения порядковых номеров и номеров страниц.

**Возвращает:**
java.lang.String — последовательность символов, используемая для разделения порядковых номеров и номеров страниц.
### getSkipTables() {#getSkipTables--}
```
public boolean getSkipTables()
```




**Возвращает:**
логический
### getStart() {#getStart--}
```
public FieldStart getStart()
```


Получает узел, представляющий начало поля.

**Возвращает:**
[FieldStart](../../com.aspose.words/fieldstart) - Узел, представляющий начало поля.
### getSwitchType(String switchName) {#getSwitchType-java.lang.String-}
```
public int getSwitchType(String switchName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| switchName | java.lang.String |  |

**Возвращает:**
инт
### getTableOfFiguresLabel() {#getTableOfFiguresLabel--}
```
public String getTableOfFiguresLabel()
```


Получает имя идентификатора последовательности, используемого при построении таблицы рисунков.

**Возвращает:**
java.lang.String — имя идентификатора последовательности, используемого при построении таблицы рисунков.
### getType() {#getType--}
```
public int getType()
```


Получает тип поля Microsoft Word.

**Возвращает:**
 int — тип поля Microsoft Word. Возвращаемое значение является одним из[FieldType](../../com.aspose.words/fieldtype) константы.
### getUseParagraphOutlineLevel() {#getUseParagraphOutlineLevel--}
```
public boolean getUseParagraphOutlineLevel()
```


Получает, следует ли использовать примененный уровень структуры абзаца.

**Возвращает:**
boolean — использовать ли примененный уровень контура абзаца.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### isBookmarkRangeSpecified() {#isBookmarkRangeSpecified--}
```
public boolean isBookmarkRangeSpecified()
```




**Возвращает:**
логический
### isDirty() {#isDirty--}
```
public boolean isDirty()
```


Получает информацию о том, является ли текущий результат поля неправильным (устаревшим) из-за других изменений, внесенных в документ.

**Возвращает:**
boolean - Является ли текущий результат поля более неверным (устаревшим) из-за других изменений, внесенных в документ.
### isDirty(boolean value) {#isDirty-boolean-}
```
public void isDirty(boolean value)
```


Устанавливает, является ли текущий результат поля неправильным (устаревшим) из-за других изменений, внесенных в документ.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Является ли текущий результат поля более неправильным (устаревшим) из-за других изменений, внесенных в документ. |

### isEntryLevelRangeSpecified() {#isEntryLevelRangeSpecified--}
```
public boolean isEntryLevelRangeSpecified()
```




**Возвращает:**
логический
### isHeadingLevelRangeSpecified() {#isHeadingLevelRangeSpecified--}
```
public boolean isHeadingLevelRangeSpecified()
```




**Возвращает:**
логический
### isLocked() {#isLocked--}
```
public boolean isLocked()
```


Получает, заблокировано ли поле (не должно пересчитывать его результат).

**Возвращает:**
boolean - Заблокировано ли поле (не должно пересчитывать результат).
### isLocked(boolean value) {#isLocked-boolean-}
```
public void isLocked(boolean value)
```


Устанавливает, будет ли поле заблокировано (не должно пересчитывать свой результат).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Заблокировано ли поле (не должно пересчитывать свой результат). |

### isTableOfFigures() {#isTableOfFigures--}
```
public boolean isTableOfFigures()
```




**Возвращает:**
логический
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### remove() {#remove--}
```
public Node remove()
```


 Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним дочерним элементом его родительского узла, возвращает его родительский абзац. Если поле уже удалено, возвращает**null**.

**Возвращает:**
[Node](../../com.aspose.words/node)
### setBookmarkName(String value) {#setBookmarkName-java.lang.String-}
```
public void setBookmarkName(String value)
```


Задает имя закладки, которая отмечает часть документа, используемую для построения таблицы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Имя закладки, которая отмечает часть документа, используемую для построения таблицы. |

### setCaptionlessTableOfFiguresLabel(String value) {#setCaptionlessTableOfFiguresLabel-java.lang.String-}
```
public void setCaptionlessTableOfFiguresLabel(String value)
```


Задает имя идентификатора последовательности, используемого при построении таблицы рисунков, которая не включает метку и номер подписи.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Имя идентификатора последовательности, используемого при построении таблицы рисунков, которая не включает метку подписи и номер. |

### setCustomStyles(String value) {#setCustomStyles-java.lang.String-}
```
public void setCustomStyles(String value)
```


Задает список стилей, отличных от встроенных стилей заголовков, для включения в оглавление.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Список стилей, отличных от встроенных стилей заголовков, для включения в оглавление. |

### setEntryIdentifier(String value) {#setEntryIdentifier-java.lang.String-}
```
public void setEntryIdentifier(String value)
```


Задает строку, которая должна соответствовать идентификаторам типов включаемых полей TC.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Строка, которая должна соответствовать идентификаторам типов включаемых полей TC. |

### setEntryLevelRange(String value) {#setEntryLevelRange-java.lang.String-}
```
public void setEntryLevelRange(String value)
```


Задает диапазон уровней включаемых записей оглавления.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Диапазон уровней записей оглавления, которые должны быть включены. |

### setEntrySeparator(String value) {#setEntrySeparator-java.lang.String-}
```
public void setEntrySeparator(String value)
```


Задает последовательность символов, разделяющую запись и номер ее страницы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Последовательность символов, отделяющая запись от номера страницы. |

### setHeadingLevelRange(String value) {#setHeadingLevelRange-java.lang.String-}
```
public void setHeadingLevelRange(String value)
```


Устанавливает диапазон уровней заголовков для включения.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Диапазон уровней заголовков для включения. |

### setHideInWebLayout(boolean value) {#setHideInWebLayout-boolean-}
```
public void setHideInWebLayout(boolean value)
```


Устанавливает, следует ли скрывать закладку и номера страниц в представлении веб-макета.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Следует ли скрывать закладку и номера страниц в представлении веб-макета. |

### setInsertHyperlinks(boolean value) {#setInsertHyperlinks-boolean-}
```
public void setInsertHyperlinks(boolean value)
```


Устанавливает, следует ли делать записи оглавления гиперссылками.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Делать ли записи оглавления гиперссылками. |

### setLocaleId(int value) {#setLocaleId-int-}
```
public void setLocaleId(int value)
```


Устанавливает LCID поля.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | LCID поля. |

### setPageNumberOmittingLevelRange(String value) {#setPageNumberOmittingLevelRange-java.lang.String-}
```
public void setPageNumberOmittingLevelRange(String value)
```


Задает диапазон уровней записей оглавления, из которых следует опускать номера страниц.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Диапазон уровней записей оглавления, из которых опускаются номера страниц. |

### setPrefixedSequenceIdentifier(String value) {#setPrefixedSequenceIdentifier-java.lang.String-}
```
public void setPrefixedSequenceIdentifier(String value)
```


Задает идентификатор последовательности, для которой к номеру страницы записи следует добавить префикс.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Идентификатор последовательности, для которой к номеру страницы записи следует добавить префикс. |

### setPreserveLineBreaks(boolean value) {#setPreserveLineBreaks-boolean-}
```
public void setPreserveLineBreaks(boolean value)
```


Устанавливает, сохранять ли символы новой строки в записях таблицы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Сохранять ли символы новой строки в записях таблицы. |

### setPreserveTabs(boolean value) {#setPreserveTabs-boolean-}
```
public void setPreserveTabs(boolean value)
```


Устанавливает, сохранять ли записи вкладок в записях таблицы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Сохранять ли записи вкладок в записях таблицы. |

### setResult(String value) {#setResult-java.lang.String-}
```
public void setResult(String value)
```


Задает текст, который находится между разделителем полей и концом поля.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Текст, который находится между разделителем полей и концом поля. |

### setSequenceSeparator(String value) {#setSequenceSeparator-java.lang.String-}
```
public void setSequenceSeparator(String value)
```


Задает последовательность символов, используемую для разделения порядковых номеров и номеров страниц.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Последовательность символов, используемая для разделения порядковых номеров и номеров страниц. |

### setTableOfFiguresLabel(String value) {#setTableOfFiguresLabel-java.lang.String-}
```
public void setTableOfFiguresLabel(String value)
```


Задает имя идентификатора последовательности, используемого при построении таблицы рисунков.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Имя идентификатора последовательности, используемого при построении таблицы рисунков. |

### setUseParagraphOutlineLevel(boolean value) {#setUseParagraphOutlineLevel-boolean-}
```
public void setUseParagraphOutlineLevel(boolean value)
```


Устанавливает, следует ли использовать примененный уровень структуры абзаца.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Использовать ли примененный уровень структуры абзаца. |

### toString() {#toString--}
```
public String toString()
```




**Возвращает:**
java.lang.String
### unlink() {#unlink--}
```
public boolean unlink()
```


Выполняет развязку поля.

Заменяет поле самым последним результатом.

Некоторые поля, такие как поля XE (запись индекса) и поля SEQ (последовательность), нельзя разъединить.

**Возвращает:**
 логический -\{ True, если связь с полем отсутствует, иначе false.
### update() {#update--}
```
public void update()
```


Выполняет обновление поля. Выдает, если поле уже обновляется.

### update(boolean ignoreMergeFormat) {#update-boolean-}
```
public void update(boolean ignoreMergeFormat)
```


Выполняет обновление поля. Выдает, если поле уже обновляется.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| ignoreMergeFormat | boolean | Если значение равно true, то прямое форматирование результата поля прекращается, независимо от переключателя MERGEFORMAT, в противном случае выполняется обычное обновление. |

### updatePageNumbers() {#updatePageNumbers--}
```
public boolean updatePageNumbers()
```


Обновляет номера страниц для элементов в этом оглавлении.

**Возвращает:**
boolean — Истинно, если операция выполнена успешно. Если какая-либо из связанных закладок TOC была удалена, будет возвращено значение false.
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
