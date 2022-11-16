---
title: PlainTextDocument
second_title: Справочник по API Aspose.Words для Java
description: Позволяет извлекать текстовое представление содержимого документов.
type: docs
weight: 465
url: /ru/java/com.aspose.words/plaintextdocument/
---

**Наследование:**
java.lang.Object
```
public class PlainTextDocument
```

Позволяет извлекать текстовое представление содержимого документа.

 Чтобы узнать больше, посетите**Working with Text Document** документальная статья.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [PlainTextDocument(String fileName)](#PlainTextDocument-java.lang.String-) | Создает обычный текстовый документ из файла. |
| [PlainTextDocument(String fileName, LoadOptions loadOptions)](#PlainTextDocument-java.lang.String-com.aspose.words.LoadOptions-) | Создает обычный текстовый документ из файла. |
| [PlainTextDocument(InputStream stream)](#PlainTextDocument-java.io.InputStream-) | Инициализирует новый экземпляр этого класса. |
| [PlainTextDocument(InputStream stream, LoadOptions loadOptions)](#PlainTextDocument-java.io.InputStream-com.aspose.words.LoadOptions-) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBuiltInDocumentProperties()](#getBuiltInDocumentProperties--) |  Получает[getBuiltInDocumentProperties()](../../com.aspose.words/plaintextdocument\#getBuiltInDocumentProperties--) документа. |
| [getClass()](#getClass--) |  |
| [getCustomDocumentProperties()](#getCustomDocumentProperties--) |  Получает[getCustomDocumentProperties()](../../com.aspose.words/plaintextdocument\#getCustomDocumentProperties--) документа. |
| [getText()](#getText--) | Получает текстовое содержимое документа, объединенного в виде строки. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### PlainTextDocument(String fileName) {#PlainTextDocument-java.lang.String-}
```
public PlainTextDocument(String fileName)
```


Создает обычный текстовый документ из файла. Автоматически определяет формат файла.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String | Имя файла, из которого нужно извлечь текст. |

### PlainTextDocument(String fileName, LoadOptions loadOptions) {#PlainTextDocument-java.lang.String-com.aspose.words.LoadOptions-}
```
public PlainTextDocument(String fileName, LoadOptions loadOptions)
```


Создает обычный текстовый документ из файла. Позволяет указать дополнительные параметры, такие как пароль шифрования.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String | Имя файла, из которого нужно извлечь текст. |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions) | Дополнительные параметры для использования при загрузке документа. Может быть нулевым. |

### PlainTextDocument(InputStream stream) {#PlainTextDocument-java.io.InputStream-}
```
public PlainTextDocument(InputStream stream)
```


Инициализирует новый экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### PlainTextDocument(InputStream stream, LoadOptions loadOptions) {#PlainTextDocument-java.io.InputStream-com.aspose.words.LoadOptions-}
```
public PlainTextDocument(InputStream stream, LoadOptions loadOptions)
```


Инициализирует новый экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | java.io.InputStream |  |
| loadOptions | [LoadOptions](../../com.aspose.words/loadoptions) |  |

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
### getBuiltInDocumentProperties() {#getBuiltInDocumentProperties--}
```
public BuiltInDocumentProperties getBuiltInDocumentProperties()
```


 Получает[getBuiltInDocumentProperties()](../../com.aspose.words/plaintextdocument\#getBuiltInDocumentProperties--) документа.

**Возвращает:**
[BuiltInDocumentProperties](../../com.aspose.words/builtindocumentproperties) -\{[getBuiltInDocumentProperties()](../../com.aspose.words/plaintextdocument\#getBuiltInDocumentProperties--) документа.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getCustomDocumentProperties() {#getCustomDocumentProperties--}
```
public CustomDocumentProperties getCustomDocumentProperties()
```


 Получает[getCustomDocumentProperties()](../../com.aspose.words/plaintextdocument\#getCustomDocumentProperties--) документа.

**Возвращает:**
[CustomDocumentProperties](../../com.aspose.words/customdocumentproperties) -\{[getCustomDocumentProperties()](../../com.aspose.words/plaintextdocument\#getCustomDocumentProperties--) документа.
### getText() {#getText--}
```
public String getText()
```


Получает текстовое содержимое документа, объединенного в виде строки.

**Возвращает:**
java.lang.String — текстовое содержимое документа, объединенное в строку.
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
