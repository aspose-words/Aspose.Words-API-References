---
title: PageSavingArgs
second_title: Справочник по API Aspose.Words для Java
description: Предоставляет данные для события.
type: docs
weight: 438
url: /ru/java/com.aspose.words/pagesavingargs/
---

**Наследование:**
java.lang.Object
```
public class PageSavingArgs
```

 Предоставляет данные для[IPageSavingCallback.pageSaving(com.aspose.words.PageSavingArgs)](../../com.aspose.words/ipagesavingcallback\#pageSaving-com.aspose.words.PageSavingArgs-) мероприятие.

 Чтобы узнать больше, посетите**Programming with Documents** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getKeepPageStreamOpen()](#getKeepPageStreamOpen--) | Указывает, должен ли Aspose.Words оставить поток открытым или закрыть его после сохранения страницы документа. |
| [getPageFileName()](#getPageFileName--) | Получает имя файла, в котором будет сохранена страница документа. |
| [getPageIndex()](#getPageIndex--) | Индекс текущей страницы. |
| [getPageStream()](#getPageStream--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setKeepPageStreamOpen(boolean value)](#setKeepPageStreamOpen-boolean-) | Указывает, должен ли Aspose.Words оставить поток открытым или закрыть его после сохранения страницы документа. |
| [setPageFileName(String value)](#setPageFileName-java.lang.String-) | Задает имя файла, в котором будет сохранена страница документа. |
| [setPageStream(OutputStream value)](#setPageStream-java.io.OutputStream-) |  |
| [toString()](#toString--) |  |
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
### getKeepPageStreamOpen() {#getKeepPageStreamOpen--}
```
public boolean getKeepPageStreamOpen()
```


Указывает, должен ли Aspose.Words оставить поток открытым или закрыть его после сохранения страницы документа.

 По умолчанию установлено значение false, и Aspose.Words закроет поток, указанный вами в**P:Aspose.Words.Saving.PageSavingArgs.PageStream** свойство после записи в него страницы документа. Укажите значение true, чтобы поток оставался открытым.

**P:Aspose.Words.Saving.PageSavingArgs.PageStream**

**Возвращает:**
boolean - соответствующее логическое значение.
### getPageFileName() {#getPageFileName--}
```
public String getPageFileName()
```


Получает имя файла, в котором будет сохранена страница документа. Если не указано, то имя файла подкачки и путь будут сгенерированы автоматически с использованием исходного имени файла.

**Возвращает:**
java.lang.String — имя файла, в котором будет сохранена страница документа.
### getPageIndex() {#getPageIndex--}
```
public int getPageIndex()
```


Индекс текущей страницы.

**Возвращает:**
int - соответствующее значение int.
### getPageStream() {#getPageStream--}
```
public OutputStream getPageStream()
```




**Возвращает:**
java.io.OutputStream
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




### setKeepPageStreamOpen(boolean value) {#setKeepPageStreamOpen-boolean-}
```
public void setKeepPageStreamOpen(boolean value)
```


Указывает, должен ли Aspose.Words оставить поток открытым или закрыть его после сохранения страницы документа.

 По умолчанию установлено значение false, и Aspose.Words закроет поток, указанный вами в**P:Aspose.Words.Saving.PageSavingArgs.PageStream** свойство после записи в него страницы документа. Укажите значение true, чтобы поток оставался открытым.

**P:Aspose.Words.Saving.PageSavingArgs.PageStream**

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setPageFileName(String value) {#setPageFileName-java.lang.String-}
```
public void setPageFileName(String value)
```


Задает имя файла, в котором будет сохранена страница документа. Если не указано, то имя файла подкачки и путь будут сгенерированы автоматически с использованием исходного имени файла.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Имя файла, в котором будет сохранена страница документа. |

### setPageStream(OutputStream value) {#setPageStream-java.io.OutputStream-}
```
public void setPageStream(OutputStream value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.io.OutputStream |  |

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
