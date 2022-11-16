---
title: Range
second_title: Справочник по API Aspose.Words для Java
description: Представляет непрерывную область в документе.
type: docs
weight: 472
url: /ru/java/com.aspose.words/range/
---

**Наследование:**
java.lang.Object
```
public class Range
```

Представляет непрерывную область в документе.

 Чтобы узнать больше, посетите**Working with Ranges** документальная статья.

Документ представлен деревом узлов, и узлы предоставляют операции для работы с деревом, но некоторые операции легче выполнять, если документ рассматривается как непрерывная последовательность текста.

**Range** — это «фасадный» интерфейс, предоставляющий методы, обрабатывающие документ или части документа как «плоский» текст, независимо от того факта, что узлы документа хранятся в древовидной объектной модели.

**Range** не содержит текста или узлов, это просто вид или «окно» над фрагментом документа.
## Методы

| Метод | Описание |
| --- | --- |
| [delete()](#delete--) | Удаляет все символы диапазона. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBookmarks()](#getBookmarks--) |  Возвращает[getBookmarks()](../../com.aspose.words/range\#getBookmarks--) коллекция, представляющая все закладки в диапазоне. |
| [getClass()](#getClass--) |  |
| [getFields()](#getFields--) |  Возвращает[getFields()](../../com.aspose.words/range\#getFields--) коллекция, которая представляет все поля в диапазоне. |
| [getFormFields()](#getFormFields--) |  Возвращает[getFormFields()](../../com.aspose.words/range\#getFormFields--) коллекция, которая представляет все поля формы в диапазоне. |
| [getStructuredDocumentTags()](#getStructuredDocumentTags--) |  Возвращает[getStructuredDocumentTags()](../../com.aspose.words/range\#getStructuredDocumentTags--)коллекция, которая представляет все теги структурированного документа в диапазоне. |
| [getText()](#getText--) | Получает текст диапазона. |
| [hashCode()](#hashCode--) |  |
| [normalizeFieldTypes()](#normalizeFieldTypes--) |  Изменяет значения типа поля[FieldChar.getFieldType()](../../com.aspose.words/fieldchar\#getFieldType--) из[FieldStart](../../com.aspose.words/fieldstart), [FieldSeparator](../../com.aspose.words/fieldseparator), [FieldEnd](../../com.aspose.words/fieldend) в этом диапазоне, чтобы они соответствовали типам полей, содержащимся в кодах полей. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [replace(String pattern, String replacement)](#replace-java.lang.String-java.lang.String-) | Заменяет все вхождения указанного шаблона строки символов замещающей строкой. |
| [replace(String pattern, String replacement, FindReplaceOptions options)](#replace-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions-) | Заменяет все вхождения указанного шаблона строки символов замещающей строкой. |
| [replace(Pattern pattern, String replacement)](#replace-java.util.regex.Pattern-java.lang.String-) | Заменяет все вхождения шаблона символов, заданного регулярным выражением, другой строкой. |
| [replace(Pattern pattern, String replacement, FindReplaceOptions options)](#replace-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions-) | Заменяет все вхождения шаблона символов, заданного регулярным выражением, другой строкой. |
| [toDocument()](#toDocument--) | Создает новый полностью сформированный документ, содержащий диапазон. |
| [toString()](#toString--) |  |
| [unlinkFields()](#unlinkFields--) | Разъединяет поля в этом диапазоне. |
| [updateFields()](#updateFields--) | Обновляет значения полей документа в этом диапазоне. |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### delete() {#delete--}
```
public void delete()
```


Удаляет все символы диапазона.

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
### getBookmarks() {#getBookmarks--}
```
public BookmarkCollection getBookmarks()
```


 Возвращает[getBookmarks()](../../com.aspose.words/range\#getBookmarks--) коллекция, представляющая все закладки в диапазоне.

**Возвращает:**
[BookmarkCollection](../../com.aspose.words/bookmarkcollection) - А[getBookmarks()](../../com.aspose.words/range\#getBookmarks--) коллекция, представляющая все закладки в диапазоне.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getFields() {#getFields--}
```
public FieldCollection getFields()
```


 Возвращает[getFields()](../../com.aspose.words/range\#getFields--) коллекция, которая представляет все поля в диапазоне.

**Возвращает:**
[FieldCollection](../../com.aspose.words/fieldcollection) - А[getFields()](../../com.aspose.words/range\#getFields--) коллекция, которая представляет все поля в диапазоне.
### getFormFields() {#getFormFields--}
```
public FormFieldCollection getFormFields()
```


 Возвращает[getFormFields()](../../com.aspose.words/range\#getFormFields--) коллекция, которая представляет все поля формы в диапазоне.

**Возвращает:**
[FormFieldCollection](../../com.aspose.words/formfieldcollection) - А[getFormFields()](../../com.aspose.words/range\#getFormFields--) коллекция, которая представляет все поля формы в диапазоне.
### getStructuredDocumentTags() {#getStructuredDocumentTags--}
```
public StructuredDocumentTagCollection getStructuredDocumentTags()
```


 Возвращает[getStructuredDocumentTags()](../../com.aspose.words/range\#getStructuredDocumentTags--)коллекция, которая представляет все теги структурированного документа в диапазоне.

**Возвращает:**
[StructuredDocumentTagCollection](../../com.aspose.words/structureddocumenttagcollection) - А[getStructuredDocumentTags()](../../com.aspose.words/range\#getStructuredDocumentTags--)коллекция, которая представляет все теги структурированного документа в диапазоне.
### getText() {#getText--}
```
public String getText()
```


Получает текст диапазона.

 Возвращаемая строка включает все управляющие и специальные символы, как описано в[ControlChar](../../com.aspose.words/controlchar).

**Возвращает:**
java.lang.String — текст диапазона.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### normalizeFieldTypes() {#normalizeFieldTypes--}
```
public void normalizeFieldTypes()
```


 Изменяет значения типа поля[FieldChar.getFieldType()](../../com.aspose.words/fieldchar\#getFieldType--) из[FieldStart](../../com.aspose.words/fieldstart), [FieldSeparator](../../com.aspose.words/fieldseparator), [FieldEnd](../../com.aspose.words/fieldend) в этом диапазоне, чтобы они соответствовали типам полей, содержащимся в кодах полей.

Используйте этот метод после изменений документа, влияющих на типы полей.

 Чтобы изменить значения типа поля во всем документе, используйте[Document.normalizeFieldTypes()](../../com.aspose.words/document\#normalizeFieldTypes--).

### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### replace(String pattern, String replacement) {#replace-java.lang.String-java.lang.String-}
```
public int replace(String pattern, String replacement)
```


Заменяет все вхождения указанного шаблона строки символов замещающей строкой.

 Шаблон не будет использоваться как регулярное выражение. Пожалуйста, используйте[replace(java.util.regex.Pattern, java.lang.String)](../../com.aspose.words/range\#replace-java.util.regex.Pattern--java.lang.String-) если вам нужны регулярные выражения.

Используется сравнение без учета регистра.

Метод может обрабатывать разрывы как в шаблоне, так и в заменяющих строках.

Вы должны использовать специальные метасимволы, если вам нужно работать с разрывами:

 *  **&p** \- разрыв абзаца
 *  **&b** \разрыв раздела
 *  **&m** \- разрыв страницы
 *  **&l** \- ручной разрыв строки

 Использовать метод[replace(java.lang.String, java.lang.String, com.aspose.words.FindReplaceOptions)](../../com.aspose.words/range\#replace-java.lang.String--java.lang.String--com.aspose.words.FindReplaceOptions-) иметь более гибкую настройку.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| pattern | java.lang.String | Строка для замены. |
| replacement | java.lang.String | Строка для замены всех вхождений шаблона. |

**Возвращает:**
int - Количество произведенных замен.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.Writeln("Numbers 1, 2, 3");

 // Inserts paragraph break after Numbers.
 doc.Range.Replace("Numbers", "Numbers&p", new FindReplaceOptions());
 
```
### replace(String pattern, String replacement, FindReplaceOptions options) {#replace-java.lang.String-java.lang.String-com.aspose.words.FindReplaceOptions-}
```
public int replace(String pattern, String replacement, FindReplaceOptions options)
```


Заменяет все вхождения указанного шаблона строки символов замещающей строкой.

 Шаблон не будет использоваться как регулярное выражение. Пожалуйста, используйте[replace(java.util.regex.Pattern, java.lang.String, com.aspose.words.FindReplaceOptions)](../../com.aspose.words/range\#replace-java.util.regex.Pattern--java.lang.String--com.aspose.words.FindReplaceOptions-) если вам нужны регулярные выражения.

Метод может обрабатывать разрывы как в шаблоне, так и в заменяющих строках.

Вы должны использовать специальные метасимволы, если вам нужно работать с разрывами:

 *  **&p** \- разрыв абзаца
 *  **&b** \разрыв раздела
 *  **&m** \- разрыв страницы
 *  **&l** \- ручной разрыв строки
 *  **&&** \- & персонаж

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| pattern | java.lang.String | Строка для замены. |
| replacement | java.lang.String | Строка для замены всех вхождений шаблона. |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions) | \{[FindReplaceOptions](../../com.aspose.words/findreplaceoptions) объект, чтобы указать дополнительные параметры. |

**Возвращает:**
int - Количество произведенных замен.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.Writeln("Numbers 1, 2, 3");

 // Inserts paragraph break after Numbers.
 doc.Range.Replace("Numbers", "Numbers&p", new FindReplaceOptions());
 
```
### replace(Pattern pattern, String replacement) {#replace-java.util.regex.Pattern-java.lang.String-}
```
public int replace(Pattern pattern, String replacement)
```


Заменяет все вхождения шаблона символов, заданного регулярным выражением, другой строкой.

Заменяет все совпадение, захваченное регулярным выражением.

Метод может обрабатывать разрывы как в шаблоне, так и в заменяющих строках.

Вы должны использовать специальные метасимволы, если вам нужно работать с разрывами:

 *  **&p** \- разрыв абзаца
 *  **&b** \разрыв раздела
 *  **&m** \- разрыв страницы
 *  **&l** \- ручной разрыв строки

 Использовать метод[replace(java.util.regex.Pattern, java.lang.String, com.aspose.words.FindReplaceOptions)](../../com.aspose.words/range\#replace-java.util.regex.Pattern--java.lang.String--com.aspose.words.FindReplaceOptions-) иметь более гибкую настройку.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| pattern | java.util.regex.Pattern | Шаблон регулярного выражения, используемый для поиска совпадений. |
| replacement | java.lang.String | Строка для замены всех вхождений шаблона. |

**Возвращает:**
int - Количество произведенных замен.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.Writeln("a1, b2, c3");

 // Replaces each number with paragraph break.
 doc.Range.Replace(new Regex(@"\d+"), "&p");
 
```
### replace(Pattern pattern, String replacement, FindReplaceOptions options) {#replace-java.util.regex.Pattern-java.lang.String-com.aspose.words.FindReplaceOptions-}
```
public int replace(Pattern pattern, String replacement, FindReplaceOptions options)
```


Заменяет все вхождения шаблона символов, заданного регулярным выражением, другой строкой.

Заменяет все совпадение, захваченное регулярным выражением.

Метод может обрабатывать разрывы как в шаблоне, так и в заменяющих строках.

Вы должны использовать специальные метасимволы, если вам нужно работать с разрывами:

 *  **&p** \- разрыв абзаца
 *  **&b** \разрыв раздела
 *  **&m** \- разрыв страницы
 *  **&l** \- ручной разрыв строки
 *  **&&** \- & персонаж

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| pattern | java.util.regex.Pattern | Шаблон регулярного выражения, используемый для поиска совпадений. |
| replacement | java.lang.String | Строка для замены всех вхождений шаблона. |
| options | [FindReplaceOptions](../../com.aspose.words/findreplaceoptions) | \{[FindReplaceOptions](../../com.aspose.words/findreplaceoptions) объект, чтобы указать дополнительные параметры. |

**Возвращает:**
int - Количество произведенных замен.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.Writeln("a1, b2, c3");

 // Replaces each number with paragraph break.
 doc.Range.Replace(new Regex(@"\d+"), "&p", new FindReplaceOptions());
 
```
### toDocument() {#toDocument--}
```
public Document toDocument()
```


Создает новый полностью сформированный документ, содержащий диапазон.

**Возвращает:**
[Document](../../com.aspose.words/document)
### toString() {#toString--}
```
public String toString()
```




**Возвращает:**
java.lang.String
### unlinkFields() {#unlinkFields--}
```
public void unlinkFields()
```


Разъединяет поля в этом диапазоне.

Заменяет все поля в этом диапазоне их самыми последними результатами.

 Чтобы разъединить поля во всем документе, используйте[unlinkFields()](../../com.aspose.words/range\#unlinkFields--).

### updateFields() {#updateFields--}
```
public void updateFields()
```


Обновляет значения полей документа в этом диапазоне.

Когда вы открываете, изменяете и затем сохраняете документ, Aspose.Words не обновляет поля автоматически, а сохраняет их нетронутыми. Таким образом, вы обычно хотите вызвать этот метод перед сохранением, если вы программно изменили документ и хотите убедиться, что в сохраненном документе отображаются правильные (вычисленные) значения полей.

Нет необходимости обновлять поля после выполнения слияния, потому что слияние — это своего рода обновление полей, которое автоматически обновляет все поля в документе.

Этот метод не обновляет все типы полей. Подробный список поддерживаемых типов полей см. в Руководстве программиста.

Этот метод не обновляет поля, связанные с алгоритмами макета страницы (например, PAGE, PAGES, PAGEREF). Поля, связанные с макетом страницы, обновляются при отображении документа или вызове[Document.updatePageLayout()](../../com.aspose.words/document\#updatePageLayout--).

 Чтобы обновить поля во всем документе, используйте[Document.updateFields()](../../com.aspose.words/document\#updateFields--).

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
