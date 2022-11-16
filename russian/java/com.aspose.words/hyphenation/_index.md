---
title: Hyphenation
second_title: Справочник по API Aspose.Words для Java
description: Предоставляет методы для работы со словарями переносов.
type: docs
weight: 333
url: /ru/java/com.aspose.words/hyphenation/
---

**Наследование:**
java.lang.Object
```
public class Hyphenation
```

Предоставляет методы для работы со словарями переносов. Эти словари предписывают, где слова определенного языка могут быть перенесены.

 Чтобы узнать больше, посетите**Working with Hyphenation** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getCallback()](#getCallback--) | Получает интерфейс обратного вызова, используемый для запроса словарей при построении макета страницы документа. |
| [getClass()](#getClass--) |  |
| [getWarningCallback()](#getWarningCallback--) | Вызывается во время загрузки шаблонов расстановки переносов, когда обнаруживается проблема, которая может привести к потере точности форматирования. |
| [hashCode()](#hashCode--) |  |
| [isDictionaryRegistered(String language)](#isDictionaryRegistered-java.lang.String-) | Возвращает False, если для указанного языка не зарегистрирован словарь или зарегистрирован пустой словарь, в противном случае — True. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [registerDictionary(String language, InputStream stream)](#registerDictionary-java.lang.String-java.io.InputStream-) |  |
| [registerDictionary(String language, String fileName)](#registerDictionary-java.lang.String-java.lang.String-) | Регистрирует и загружает словарь переносов для указанного языка из файла. |
| [setCallback(IHyphenationCallback value)](#setCallback-com.aspose.words.IHyphenationCallback-) | Задает интерфейс обратного вызова, используемый для запроса словарей при построении макета страницы документа. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback-) | Вызывается во время загрузки шаблонов расстановки переносов, когда обнаруживается проблема, которая может привести к потере точности форматирования. |
| [toString()](#toString--) |  |
| [unregisterDictionary(String language)](#unregisterDictionary-java.lang.String-) | Отменяет регистрацию словаря переносов для указанного языка. |
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
### getCallback() {#getCallback--}
```
public static IHyphenationCallback getCallback()
```


Получает интерфейс обратного вызова, используемый для запроса словарей при построении макета страницы документа. Это позволяет откладывать загрузку словарей, что может быть полезно при обработке документов на многих языках.

**Возвращает:**
[IHyphenationCallback](../../com.aspose.words/ihyphenationcallback) - Интерфейс обратного вызова, используемый для запроса словарей при построении макета страницы документа.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getWarningCallback() {#getWarningCallback--}
```
public static IWarningCallback getWarningCallback()
```


Вызывается во время загрузки шаблонов расстановки переносов, когда обнаруживается проблема, которая может привести к потере точности форматирования.

**Возвращает:**
[IWarningCallback](../../com.aspose.words/iwarningcallback) - соответствующий[IWarningCallback](../../com.aspose.words/iwarningcallback) ценность.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### isDictionaryRegistered(String language) {#isDictionaryRegistered-java.lang.String-}
```
public static boolean isDictionaryRegistered(String language)
```


Возвращает False, если для указанного языка не зарегистрирован словарь или зарегистрирован пустой словарь, в противном случае — True.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| language | java.lang.String |  |

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




### registerDictionary(String language, InputStream stream) {#registerDictionary-java.lang.String-java.io.InputStream-}
```
public static void registerDictionary(String language, InputStream stream)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| language | java.lang.String |  |
| stream | java.io.InputStream |  |

### registerDictionary(String language, String fileName) {#registerDictionary-java.lang.String-java.lang.String-}
```
public static void registerDictionary(String language, String fileName)
```


Регистрирует и загружает словарь переносов для указанного языка из файла. Выдает, если словарь не может быть прочитан или имеет недопустимый формат.

 Этот метод также можно использовать для регистрации нулевого словаря, чтобы предотвратить[getCallback()](../../com.aspose.words/hyphenation\#getCallback--) / [setCallback(com.aspose.words.IHyphenationCallback)](../../com.aspose.words/hyphenation\#setCallback-com.aspose.words.IHyphenationCallback-) от повторного вызова на одном и том же языке.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| language | java.lang.String | Название языка, например "en-US". См. документацию .NET для «имени культуры» и RFC 4646 для получения подробной информации. |
| fileName | java.lang.String | Путь к файлу словаря в формате Open Office.

Если этот параметр имеет значение null или пустую строку, то регистрируется пустой словарь, и обратный вызов для этого языка больше не вызывается.

 Чтобы снова включить обратный вызов, используйте[unregisterDictionary(java.lang.String)](../../com.aspose.words/hyphenation\#unregisterDictionary-java.lang.String-) метод.|

### setCallback(IHyphenationCallback value) {#setCallback-com.aspose.words.IHyphenationCallback-}
```
public static void setCallback(IHyphenationCallback value)
```


Задает интерфейс обратного вызова, используемый для запроса словарей при построении макета страницы документа. Это позволяет откладывать загрузку словарей, что может быть полезно при обработке документов на многих языках.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [IHyphenationCallback](../../com.aspose.words/ihyphenationcallback) | Интерфейс обратного вызова, используемый для запроса словарей при построении макета страницы документа. |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback-}
```
public static void setWarningCallback(IWarningCallback value)
```


Вызывается во время загрузки шаблонов расстановки переносов, когда обнаруживается проблема, которая может привести к потере точности форматирования.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback) |  Соответствующий[IWarningCallback](../../com.aspose.words/iwarningcallback) ценность. |

### toString() {#toString--}
```
public String toString()
```




**Возвращает:**
java.lang.String
### unregisterDictionary(String language) {#unregisterDictionary-java.lang.String-}
```
public static void unregisterDictionary(String language)
```


Отменяет регистрацию словаря переносов для указанного языка.

Это отличается от регистрации нулевого словаря. Отмена регистрации словаря включает обратный вызов для указанного языка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| language | java.lang.String | Название языка, например "en-US". См. документацию .NET для «имени культуры» и RFC 4646 для получения подробной информации.

 Если нулевая или пустая строка, то все словари не зарегистрированы.|

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
