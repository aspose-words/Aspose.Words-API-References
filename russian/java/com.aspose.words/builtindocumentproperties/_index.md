---
title: BuiltInDocumentProperties
second_title: Справочник по API Aspose.Words для Java
description: Коллекция встроенных свойств документа.
type: docs
weight: 46
url: /ru/java/com.aspose.words/builtindocumentproperties/
---

**Наследование:**
java.lang.Object, [com.aspose.words.DocumentPropertyCollection](../../com.aspose.words/documentpropertycollection)
```
public class BuiltInDocumentProperties extends DocumentPropertyCollection
```

Коллекция встроенных свойств документа.

 Чтобы узнать больше, посетите**Work with Document Properties** документальная статья.

 Обеспечивает доступ к[DocumentProperty](../../com.aspose.words/documentproperty) объекты по их именам (с помощью индексатора) и через набор типизированных свойств, которые возвращают значения соответствующих типов.

Имена свойств нечувствительны к регистру.

Свойства в коллекции отсортированы в алфавитном порядке по имени.
## Методы

| Метод | Описание |
| --- | --- |
| [clear()](#clear--) | Удаляет все свойства из коллекции. |
| [contains(String name)](#contains-java.lang.String-) | Возвращает true, если свойство с указанным именем существует в коллекции. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) |  Возвращает[DocumentProperty](../../com.aspose.words/documentproperty) объект по индексу. |
| [get(String name)](#get-java.lang.String-) |  Возвращает[DocumentProperty](../../com.aspose.words/documentproperty) объект. |
| [getAuthor()](#getAuthor--) | Получает имя автора документа. |
| [getBytes()](#getBytes--) | Представляет оценку количества байтов в документе. |
| [getCategory()](#getCategory--) | Получает категорию документа. |
| [getCharacters()](#getCharacters--) | Представляет оценку количества символов в документе. |
| [getCharactersWithSpaces()](#getCharactersWithSpaces--) | Представляет оценку количества символов (включая пробелы) в документе. |
| [getClass()](#getClass--) |  |
| [getComments()](#getComments--) | Получает комментарии к документу. |
| [getCompany()](#getCompany--) | Получает имущество компании. |
| [getContentStatus()](#getContentStatus--) | Получает ContentStatus документа. |
| [getContentType()](#getContentType--) | Получает ContentStatus документа. |
| [getCount()](#getCount--) | Получает количество элементов в коллекции. |
| [getCreatedTime()](#getCreatedTime--) | Получает дату создания документа в формате UTC. |
| [getHeadingPairs()](#getHeadingPairs--) | Указывает заголовки документов и их имена. |
| [getHyperlinkBase()](#getHyperlinkBase--) | Указывает базовую строку, используемую для оценки относительных гиперссылок в этом документе. |
| [getKeywords()](#getKeywords--) | Получает ключевые слова документа. |
| [getLastPrinted()](#getLastPrinted--) | Получает дату последней печати документа в формате UTC. |
| [getLastSavedBy()](#getLastSavedBy--) | Получает имя последнего автора. |
| [getLastSavedTime()](#getLastSavedTime--) | Получает время последнего сохранения в формате UTC. |
| [getLines()](#getLines--) | Представляет оценку количества строк в документе. |
| [getLinksUpToDate()](#getLinksUpToDate--) | Указывает, являются ли гиперссылки в документе актуальными. |
| [getManager()](#getManager--) | Получает свойство менеджера. |
| [getNameOfApplication()](#getNameOfApplication--) | Получает имя приложения. |
| [getPages()](#getPages--) | Представляет оценку количества страниц в документе. |
| [getParagraphs()](#getParagraphs--) | Представляет оценку количества абзацев в документе. |
| [getRevisionNumber()](#getRevisionNumber--) | Получает номер редакции документа. |
| [getSecurity()](#getSecurity--) | Указывает уровень безопасности документа в виде числового значения. |
| [getSubject()](#getSubject--) | Получает тему документа. |
| [getTemplate()](#getTemplate--) | Получает информационное имя шаблона документа. |
| [getThumbnail()](#getThumbnail--) | Получает или задает миниатюру документа. |
| [getTitle()](#getTitle--) | Получает заголовок документа. |
| [getTitlesOfParts()](#getTitlesOfParts--) | Каждая строка в массиве указывает имя части в документе. |
| [getTotalEditingTime()](#getTotalEditingTime--) | Получает общее время редактирования в минутах. |
| [getVersion()](#getVersion--) | Представляет номер версии приложения, создавшего документ. |
| [getWords()](#getWords--) | Представляет оценку количества слов в документе. |
| [hashCode()](#hashCode--) |  |
| [indexOf(String name)](#indexOf-java.lang.String-) | Получает индекс свойства по имени. |
| [iterator()](#iterator--) | Возвращает объект итератора, который можно использовать для перебора всех элементов коллекции. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [remove(String name)](#remove-java.lang.String-) | Удаляет свойство с указанным именем из коллекции. |
| [removeAt(int index)](#removeAt-int-) | Удаляет свойство по указанному индексу. |
| [setAuthor(String value)](#setAuthor-java.lang.String-) | Устанавливает имя автора документа. |
| [setBytes(int value)](#setBytes-int-) | Представляет оценку количества байтов в документе. |
| [setCategory(String value)](#setCategory-java.lang.String-) | Устанавливает категорию документа. |
| [setCharacters(int value)](#setCharacters-int-) | Представляет оценку количества символов в документе. |
| [setCharactersWithSpaces(int value)](#setCharactersWithSpaces-int-) | Представляет оценку количества символов (включая пробелы) в документе. |
| [setComments(String value)](#setComments-java.lang.String-) | Устанавливает комментарии к документу. |
| [setCompany(String value)](#setCompany-java.lang.String-) | Задает свойство компании. |
| [setContentStatus(String value)](#setContentStatus-java.lang.String-) | Устанавливает ContentStatus документа. |
| [setContentType(String value)](#setContentType-java.lang.String-) | Устанавливает ContentStatus документа. |
| [setCreatedTime(Date value)](#setCreatedTime-java.util.Date-) | Устанавливает дату создания документа в формате UTC. |
| [setHeadingPairs(Object[] value)](#setHeadingPairs-java.lang.Object---) | Указывает заголовки документов и их имена. |
| [setHyperlinkBase(String value)](#setHyperlinkBase-java.lang.String-) | Указывает базовую строку, используемую для оценки относительных гиперссылок в этом документе. |
| [setKeywords(String value)](#setKeywords-java.lang.String-) | Устанавливает ключевые слова документа. |
| [setLastPrinted(Date value)](#setLastPrinted-java.util.Date-) | Устанавливает дату последней печати документа в формате UTC. |
| [setLastSavedBy(String value)](#setLastSavedBy-java.lang.String-) | Устанавливает имя последнего автора. |
| [setLastSavedTime(Date value)](#setLastSavedTime-java.util.Date-) | Устанавливает время последнего сохранения в формате UTC. |
| [setLines(int value)](#setLines-int-) | Представляет оценку количества строк в документе. |
| [setLinksUpToDate(boolean value)](#setLinksUpToDate-boolean-) | Указывает, являются ли гиперссылки в документе актуальными. |
| [setManager(String value)](#setManager-java.lang.String-) | Задает свойство менеджера. |
| [setNameOfApplication(String value)](#setNameOfApplication-java.lang.String-) | Задает имя приложения. |
| [setPages(int value)](#setPages-int-) | Представляет оценку количества страниц в документе. |
| [setParagraphs(int value)](#setParagraphs-int-) | Представляет оценку количества абзацев в документе. |
| [setRevisionNumber(int value)](#setRevisionNumber-int-) | Устанавливает номер редакции документа. |
| [setSecurity(int value)](#setSecurity-int-) | Указывает уровень безопасности документа в виде числового значения. |
| [setSubject(String value)](#setSubject-java.lang.String-) | Устанавливает тему документа. |
| [setTemplate(String value)](#setTemplate-java.lang.String-) | Задает информационное имя шаблона документа. |
| [setThumbnail(byte[] value)](#setThumbnail-byte---) | Получает или задает миниатюру документа. |
| [setTitle(String value)](#setTitle-java.lang.String-) | Устанавливает заголовок документа. |
| [setTitlesOfParts(String[] value)](#setTitlesOfParts-java.lang.String---) | Каждая строка в массиве указывает имя части в документе. |
| [setTotalEditingTime(int value)](#setTotalEditingTime-int-) | Устанавливает общее время редактирования в минутах. |
| [setVersion(int value)](#setVersion-int-) | Представляет номер версии приложения, создавшего документ. |
| [setWords(int value)](#setWords-int-) | Представляет оценку количества слов в документе. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clear() {#clear--}
```
public void clear()
```


Удаляет все свойства из коллекции.

### contains(String name) {#contains-java.lang.String-}
```
public boolean contains(String name)
```


Возвращает true, если свойство с указанным именем существует в коллекции.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Нечувствительное к регистру имя свойства. |

**Возвращает:**
boolean — Истинно, если свойство существует в коллекции; ложно в противном случае.
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
### get(int index) {#get-int-}
```
public DocumentProperty get(int index)
```


 Возвращает[DocumentProperty](../../com.aspose.words/documentproperty) объект по индексу.

**Note:** В Java этот метод медленный, потому что перебирает все узлы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int |  Отсчитываемый от нуля индекс[DocumentProperty](../../com.aspose.words/documentproperty) получить. |

**Возвращает:**
[DocumentProperty](../../com.aspose.words/documentproperty) - А[DocumentProperty](../../com.aspose.words/documentproperty) объект по индексу.
### get(String name) {#get-java.lang.String-}
```
public DocumentProperty get(String name)
```


 Возвращает[DocumentProperty](../../com.aspose.words/documentproperty) объект. Возвращает[DocumentProperty](../../com.aspose.words/documentproperty) объект по имени свойства.

 Строковые имена свойств соответствуют именам типизированных свойств, доступных из[BuiltInDocumentProperties](../../com.aspose.words/builtindocumentproperties).

 Если вы запрашиваете свойство, которого нет в документе, но имя свойства распознается как допустимое встроенное имя, новое[DocumentProperty](../../com.aspose.words/documentproperty) создается, добавляется в коллекцию и возвращается. Вновь созданному свойству присваивается значение по умолчанию (пустая строка, ноль, false или DateTime.MinValue в зависимости от типа встроенного свойства).

Если вы запрашиваете свойство, которого нет в документе, и имя не распознается как встроенное имя, возвращается значение NULL.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Нечувствительное к регистру имя извлекаемого свойства. |

**Возвращает:**
[DocumentProperty](../../com.aspose.words/documentproperty) - соответствующий[DocumentProperty](../../com.aspose.words/documentproperty) ценность.
### getAuthor() {#getAuthor--}
```
public String getAuthor()
```


Получает имя автора документа.

**Возвращает:**
java.lang.String — Имя автора документа.
### getBytes() {#getBytes--}
```
public int getBytes()
```


Представляет оценку количества байтов в документе.

Microsoft Word не всегда задает это свойство.

Aspose.Words не обновляет это свойство.

**Возвращает:**
int - соответствующее значение int.
### getCategory() {#getCategory--}
```
public String getCategory()
```


Получает категорию документа.

**Возвращает:**
java.lang.String — категория документа.
### getCharacters() {#getCharacters--}
```
public int getCharacters()
```


Представляет оценку количества символов в документе.

 Aspose.Words обновляет это свойство при вызове[Document.updateWordCount()](../../com.aspose.words/document\#updateWordCount--).

**Возвращает:**
int - соответствующее значение int.
### getCharactersWithSpaces() {#getCharactersWithSpaces--}
```
public int getCharactersWithSpaces()
```


Представляет оценку количества символов (включая пробелы) в документе.

 Aspose.Words обновляет это свойство при вызове[Document.updateWordCount()](../../com.aspose.words/document\#updateWordCount--).

**Возвращает:**
int - соответствующее значение int.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getComments() {#getComments--}
```
public String getComments()
```


Получает комментарии к документу.

**Возвращает:**
java.lang.String — комментарии к документу.
### getCompany() {#getCompany--}
```
public String getCompany()
```


Получает имущество компании.

**Возвращает:**
java.lang.String — свойство компании.
### getContentStatus() {#getContentStatus--}
```
public String getContentStatus()
```


Получает ContentStatus документа.

**Возвращает:**
java.lang.String — ContentStatus документа.
### getContentType() {#getContentType--}
```
public String getContentType()
```


Получает ContentStatus документа.

**Возвращает:**
java.lang.String — ContentStatus документа.
### getCount() {#getCount--}
```
public int getCount()
```


Получает количество элементов в коллекции.

**Возвращает:**
int - количество элементов в коллекции.
### getCreatedTime() {#getCreatedTime--}
```
public Date getCreatedTime()
```


Получает дату создания документа в формате UTC.

Для документов, созданных в формате RTF, это свойство возвращает местное время машины автора в момент создания документа.

Aspose.Words не обновляет это свойство.

**Возвращает:**
java.util.Date - Дата создания документа в формате UTC.
### getHeadingPairs() {#getHeadingPairs--}
```
public Object[] getHeadingPairs()
```


Указывает заголовки документов и их имена.

Каждая пара заголовков занимает два элемента в этом массиве.

 Первый элемент пары — это java.lang.String, который указывает имя заголовка. Второй элемент пары — это тип int, который определяет количество частей документа для этого заголовка в[getTitlesOfParts()](../../com.aspose.words/builtindocumentproperties\#getTitlesOfParts--) / [setTitlesOfParts(java.lang.String[])](../../com.aspose.words/builtindocumentproperties\#setTitlesOfParts-java.lang.String---) имущество.

Общая сумма счетчиков для всех пар заголовков в этом свойстве должна быть равна количеству элементов в[getTitlesOfParts()](../../com.aspose.words/builtindocumentproperties\#getTitlesOfParts--) / [setTitlesOfParts(java.lang.String[])](../../com.aspose.words/builtindocumentproperties\#setTitlesOfParts-java.lang.String---) имущество.

Aspose.Words не обновляет это свойство.

**Возвращает:**
java.lang.Объект[] — соответствующий java.lang.Object[] ценность.
### getHyperlinkBase() {#getHyperlinkBase--}
```
public String getHyperlinkBase()
```


Указывает базовую строку, используемую для оценки относительных гиперссылок в этом документе.

Aspose.Words не использует это свойство.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getKeywords() {#getKeywords--}
```
public String getKeywords()
```


Получает ключевые слова документа.

**Возвращает:**
java.lang.String — Ключевые слова документа.
### getLastPrinted() {#getLastPrinted--}
```
public Date getLastPrinted()
```


Получает дату последней печати документа в формате UTC.

Для документов, созданных в формате RTF, это свойство возвращает местное время последней операции печати.

Если документ никогда не печатался, это свойство возвращает значение DateTime.MinValue.

Aspose.Words не обновляет это свойство.

**Возвращает:**
java.util.Date — дата последней печати документа в формате UTC.
### getLastSavedBy() {#getLastSavedBy--}
```
public String getLastSavedBy()
```


Получает имя последнего автора.

Aspose.Words не обновляет это свойство.

**Возвращает:**
java.lang.String — Имя последнего автора.
### getLastSavedTime() {#getLastSavedTime--}
```
public Date getLastSavedTime()
```


Получает время последнего сохранения в формате UTC.

Для документов, созданных в формате RTF, это свойство возвращает местное время последней операции сохранения.

Aspose.Words не обновляет это свойство.

**Возвращает:**
java.util.Date — время последнего сохранения в формате UTC.
### getLines() {#getLines--}
```
public int getLines()
```


Представляет оценку количества строк в документе.

 Aspose.Words обновляет это свойство при вызове[Document.updateWordCount(boolean)](../../com.aspose.words/document\#updateWordCount-boolean-).

**Возвращает:**
int - соответствующее значение int.
### getLinksUpToDate() {#getLinksUpToDate--}
```
public boolean getLinksUpToDate()
```


Указывает, являются ли гиперссылки в документе актуальными.

Aspose.Words не обновляет это свойство.

**Возвращает:**
boolean - соответствующее логическое значение.
### getManager() {#getManager--}
```
public String getManager()
```


Получает свойство менеджера.

**Возвращает:**
java.lang.String — свойство менеджера.
### getNameOfApplication() {#getNameOfApplication--}
```
public String getNameOfApplication()
```


Получает имя приложения.

**Возвращает:**
java.lang.String — имя приложения.
### getPages() {#getPages--}
```
public int getPages()
```


Представляет оценку количества страниц в документе.

 Aspose.Words обновляет это свойство при вызове[Document.updatePageLayout()](../../com.aspose.words/document\#updatePageLayout--).

**Возвращает:**
int - соответствующее значение int.
### getParagraphs() {#getParagraphs--}
```
public int getParagraphs()
```


Представляет оценку количества абзацев в документе.

 Aspose.Words обновляет это свойство при вызове[Document.updateWordCount()](../../com.aspose.words/document\#updateWordCount--).

**Возвращает:**
int - соответствующее значение int.
### getRevisionNumber() {#getRevisionNumber--}
```
public int getRevisionNumber()
```


Получает номер редакции документа.

Aspose.Words не обновляет это свойство.

**Возвращает:**
int — номер редакции документа.
### getSecurity() {#getSecurity--}
```
public int getSecurity()
```


Указывает уровень безопасности документа в виде числового значения.

Используйте это свойство только в информационных целях, поскольку Microsoft Word не всегда задает это свойство. Это свойство доступно только в документах DOC и OOXML.

 Чтобы защитить или снять защиту с документа, используйте кнопку**M:Aspose.Words.Document.Protect(Aspose.Words.ProtectionType,System.String)** а также[Document.unprotect()](../../com.aspose.words/document\#unprotect--) методы.

Aspose.Words обновляет это свойство до правильного значения перед сохранением документа.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение представляет собой побитовую комбинацию[DocumentSecurity](../../com.aspose.words/documentsecurity) константы.
### getSubject() {#getSubject--}
```
public String getSubject()
```


Получает тему документа.

**Возвращает:**
java.lang.String — Тема документа.
### getTemplate() {#getTemplate--}
```
public String getTemplate()
```


Получает информационное имя шаблона документа.

В Microsoft Word это свойство предназначено только для информационных целей и обычно содержит только имя файла шаблона без пути.

Пустая строка означает, что документ прикреплен к шаблону Normal.

 Чтобы получить или задать фактическое имя прикрепленного шаблона, используйте[Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate--) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String-) имущество.

**Возвращает:**
java.lang.String — информационное имя шаблона документа.
### getThumbnail() {#getThumbnail--}
```
public byte[] getThumbnail()
```


Получает или задает миниатюру документа.

На данный момент это свойство используется только тогда, когда документ экспортируется в ePub, он не читается и не записывается в документы других форматов.

В это свойство можно установить изображение произвольного формата, но формат проверяется при экспорте. Исключение java.lang.IllegalStateException возникает, если изображение недействительно или его формат не поддерживается для определенного формата документа.

Для публикации ePub можно использовать только изображения в формате gif, jpeg и png.

**Возвращает:**
байт[] - соответствующий байт[] ценность.
### getTitle() {#getTitle--}
```
public String getTitle()
```


Получает заголовок документа.

**Возвращает:**
java.lang.String — заголовок документа.
### getTitlesOfParts() {#getTitlesOfParts--}
```
public String[] getTitlesOfParts()
```


Каждая строка в массиве указывает имя части в документе.

Aspose.Words не обновляет это свойство.

**Возвращает:**
java.lang.String[] — соответствующий java.lang.String[] ценность.
### getTotalEditingTime() {#getTotalEditingTime--}
```
public int getTotalEditingTime()
```


Получает общее время редактирования в минутах.

**Возвращает:**
int — общее время редактирования в минутах.
### getVersion() {#getVersion--}
```
public int getVersion()
```


Представляет номер версии приложения, создавшего документ.

Когда документ был создан в Microsoft Word, старшие 16 бит представляют собой основную версию, а младшие 16 бит — номер сборки.

**Возвращает:**
int - соответствующее значение int.
### getWords() {#getWords--}
```
public int getWords()
```


Представляет оценку количества слов в документе.

 Aspose.Words обновляет это свойство при вызове[Document.updateWordCount()](../../com.aspose.words/document\#updateWordCount--).

**Возвращает:**
int - соответствующее значение int.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### indexOf(String name) {#indexOf-java.lang.String-}
```
public int indexOf(String name)
```


Получает индекс свойства по имени.

**Note:** В Java этот метод медленный, потому что перебирает все узлы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Нечувствительное к регистру имя свойства. |

**Возвращает:**
int - индекс, основанный на нуле. Отрицательное значение, если не найдено.
### iterator() {#iterator--}
```
public Iterator iterator()
```


Возвращает объект итератора, который можно использовать для перебора всех элементов коллекции.

**Возвращает:**
java.util.Iterator
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### remove(String name) {#remove-java.lang.String-}
```
public void remove(String name)
```


Удаляет свойство с указанным именем из коллекции.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| name | java.lang.String | Нечувствительное к регистру имя свойства. |

### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


Удаляет свойство по указанному индексу.

**Note:** В Java этот метод медленный, потому что перебирает все узлы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int | Индекс с отсчетом от нуля. |

### setAuthor(String value) {#setAuthor-java.lang.String-}
```
public void setAuthor(String value)
```


Устанавливает имя автора документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Имя автора документа. |

### setBytes(int value) {#setBytes-int-}
```
public void setBytes(int value)
```


Представляет оценку количества байтов в документе.

Microsoft Word не всегда задает это свойство.

Aspose.Words не обновляет это свойство.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее целочисленное значение. |

### setCategory(String value) {#setCategory-java.lang.String-}
```
public void setCategory(String value)
```


Устанавливает категорию документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Категория документа. |

### setCharacters(int value) {#setCharacters-int-}
```
public void setCharacters(int value)
```


Представляет оценку количества символов в документе.

 Aspose.Words обновляет это свойство при вызове[Document.updateWordCount()](../../com.aspose.words/document\#updateWordCount--).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее целочисленное значение. |

### setCharactersWithSpaces(int value) {#setCharactersWithSpaces-int-}
```
public void setCharactersWithSpaces(int value)
```


Представляет оценку количества символов (включая пробелы) в документе.

 Aspose.Words обновляет это свойство при вызове[Document.updateWordCount()](../../com.aspose.words/document\#updateWordCount--).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее целочисленное значение. |

### setComments(String value) {#setComments-java.lang.String-}
```
public void setComments(String value)
```


Устанавливает комментарии к документу.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Комментарии к документу. |

### setCompany(String value) {#setCompany-java.lang.String-}
```
public void setCompany(String value)
```


Задает свойство компании.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Имущество компании. |

### setContentStatus(String value) {#setContentStatus-java.lang.String-}
```
public void setContentStatus(String value)
```


Устанавливает ContentStatus документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | ContentStatus документа. |

### setContentType(String value) {#setContentType-java.lang.String-}
```
public void setContentType(String value)
```


Устанавливает ContentStatus документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | ContentStatus документа. |

### setCreatedTime(Date value) {#setCreatedTime-java.util.Date-}
```
public void setCreatedTime(Date value)
```


Устанавливает дату создания документа в формате UTC.

Для документов, созданных в формате RTF, это свойство возвращает местное время машины автора в момент создания документа.

Aspose.Words не обновляет это свойство.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.util.Date | Дата создания документа в формате UTC. |

### setHeadingPairs(Object[] value) {#setHeadingPairs-java.lang.Object---}
```
public void setHeadingPairs(Object[] value)
```


Указывает заголовки документов и их имена.

Каждая пара заголовков занимает два элемента в этом массиве.

 Первый элемент пары — это java.lang.String, который указывает имя заголовка. Второй элемент пары — это тип int, который определяет количество частей документа для этого заголовка в[getTitlesOfParts()](../../com.aspose.words/builtindocumentproperties\#getTitlesOfParts--) / [setTitlesOfParts(java.lang.String[])](../../com.aspose.words/builtindocumentproperties\#setTitlesOfParts-java.lang.String---) имущество.

Общая сумма счетчиков для всех пар заголовков в этом свойстве должна быть равна количеству элементов в[getTitlesOfParts()](../../com.aspose.words/builtindocumentproperties\#getTitlesOfParts--) / [setTitlesOfParts(java.lang.String[])](../../com.aspose.words/builtindocumentproperties\#setTitlesOfParts-java.lang.String---) имущество.

Aspose.Words не обновляет это свойство.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.Object[] | Соответствующий java.lang.Object[] ценность. |

### setHyperlinkBase(String value) {#setHyperlinkBase-java.lang.String-}
```
public void setHyperlinkBase(String value)
```


Указывает базовую строку, используемую для оценки относительных гиперссылок в этом документе.

Aspose.Words не использует это свойство.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setKeywords(String value) {#setKeywords-java.lang.String-}
```
public void setKeywords(String value)
```


Устанавливает ключевые слова документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Ключевые слова документа. |

### setLastPrinted(Date value) {#setLastPrinted-java.util.Date-}
```
public void setLastPrinted(Date value)
```


Устанавливает дату последней печати документа в формате UTC.

Для документов, созданных в формате RTF, это свойство возвращает местное время последней операции печати.

Если документ никогда не печатался, это свойство возвращает значение DateTime.MinValue.

Aspose.Words не обновляет это свойство.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.util.Date | Дата последней печати документа в формате UTC. |

### setLastSavedBy(String value) {#setLastSavedBy-java.lang.String-}
```
public void setLastSavedBy(String value)
```


Устанавливает имя последнего автора.

Aspose.Words не обновляет это свойство.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Имя последнего автора. |

### setLastSavedTime(Date value) {#setLastSavedTime-java.util.Date-}
```
public void setLastSavedTime(Date value)
```


Устанавливает время последнего сохранения в формате UTC.

Для документов, созданных в формате RTF, это свойство возвращает местное время последней операции сохранения.

Aspose.Words не обновляет это свойство.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.util.Date | Время последнего сохранения в формате UTC. |

### setLines(int value) {#setLines-int-}
```
public void setLines(int value)
```


Представляет оценку количества строк в документе.

 Aspose.Words обновляет это свойство при вызове[Document.updateWordCount(boolean)](../../com.aspose.words/document\#updateWordCount-boolean-).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее целочисленное значение. |

### setLinksUpToDate(boolean value) {#setLinksUpToDate-boolean-}
```
public void setLinksUpToDate(boolean value)
```


Указывает, являются ли гиперссылки в документе актуальными.

Aspose.Words не обновляет это свойство.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setManager(String value) {#setManager-java.lang.String-}
```
public void setManager(String value)
```


Задает свойство менеджера.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Свойство менеджера. |

### setNameOfApplication(String value) {#setNameOfApplication-java.lang.String-}
```
public void setNameOfApplication(String value)
```


Задает имя приложения.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Название приложения. |

### setPages(int value) {#setPages-int-}
```
public void setPages(int value)
```


Представляет оценку количества страниц в документе.

 Aspose.Words обновляет это свойство при вызове[Document.updatePageLayout()](../../com.aspose.words/document\#updatePageLayout--).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее целочисленное значение. |

### setParagraphs(int value) {#setParagraphs-int-}
```
public void setParagraphs(int value)
```


Представляет оценку количества абзацев в документе.

 Aspose.Words обновляет это свойство при вызове[Document.updateWordCount()](../../com.aspose.words/document\#updateWordCount--).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее целочисленное значение. |

### setRevisionNumber(int value) {#setRevisionNumber-int-}
```
public void setRevisionNumber(int value)
```


Устанавливает номер редакции документа.

Aspose.Words не обновляет это свойство.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Номер редакции документа. |

### setSecurity(int value) {#setSecurity-int-}
```
public void setSecurity(int value)
```


Указывает уровень безопасности документа в виде числового значения.

Используйте это свойство только в информационных целях, поскольку Microsoft Word не всегда задает это свойство. Это свойство доступно только в документах DOC и OOXML.

 Чтобы защитить или снять защиту с документа, используйте кнопку**M:Aspose.Words.Document.Protect(Aspose.Words.ProtectionType,System.String)** а также[Document.unprotect()](../../com.aspose.words/document\#unprotect--) методы.

Aspose.Words обновляет это свойство до правильного значения перед сохранением документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть побитовой комбинацией[DocumentSecurity](../../com.aspose.words/documentsecurity) константы. |

### setSubject(String value) {#setSubject-java.lang.String-}
```
public void setSubject(String value)
```


Устанавливает тему документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Тема документа. |

### setTemplate(String value) {#setTemplate-java.lang.String-}
```
public void setTemplate(String value)
```


Задает информационное имя шаблона документа.

В Microsoft Word это свойство предназначено только для информационных целей и обычно содержит только имя файла шаблона без пути.

Пустая строка означает, что документ прикреплен к шаблону Normal.

 Чтобы получить или задать фактическое имя прикрепленного шаблона, используйте[Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate--) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String-) имущество.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Информационное имя шаблона документа. |

### setThumbnail(byte[] value) {#setThumbnail-byte---}
```
public void setThumbnail(byte[] value)
```


Получает или задает миниатюру документа.

На данный момент это свойство используется только тогда, когда документ экспортируется в ePub, он не читается и не записывается в документы других форматов.

В это свойство можно установить изображение произвольного формата, но формат проверяется при экспорте. Исключение java.lang.IllegalStateException возникает, если изображение недействительно или его формат не поддерживается для определенного формата документа.

Для публикации ePub можно использовать только изображения в формате gif, jpeg и png.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | byte[] | Соответствующий байт[] ценность. |

### setTitle(String value) {#setTitle-java.lang.String-}
```
public void setTitle(String value)
```


Устанавливает заголовок документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Название документа. |

### setTitlesOfParts(String[] value) {#setTitlesOfParts-java.lang.String---}
```
public void setTitlesOfParts(String[] value)
```


Каждая строка в массиве указывает имя части в документе.

Aspose.Words не обновляет это свойство.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String[] | Соответствующий java.lang.String[] ценность. |

### setTotalEditingTime(int value) {#setTotalEditingTime-int-}
```
public void setTotalEditingTime(int value)
```


Устанавливает общее время редактирования в минутах.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Общее время редактирования в минутах. |

### setVersion(int value) {#setVersion-int-}
```
public void setVersion(int value)
```


Представляет номер версии приложения, создавшего документ.

Когда документ был создан в Microsoft Word, старшие 16 бит представляют собой основную версию, а младшие 16 бит — номер сборки.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее целочисленное значение. |

### setWords(int value) {#setWords-int-}
```
public void setWords(int value)
```


Представляет оценку количества слов в документе.

 Aspose.Words обновляет это свойство при вызове[Document.updateWordCount()](../../com.aspose.words/document\#updateWordCount--).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее целочисленное значение. |

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
