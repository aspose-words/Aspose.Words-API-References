---
title: CssSavingArgs
second_title: Справочник по API Aspose.Words для Java
description: Предоставляет данные для события.
type: docs
weight: 96
url: /ru/java/com.aspose.words/csssavingargs/
---

**Наследование:**
java.lang.Object
```
public class CssSavingArgs
```

 Предоставляет данные для[ICssSavingCallback.cssSaving(com.aspose.words.CssSavingArgs)](../../com.aspose.words/icsssavingcallback\#cssSaving-com.aspose.words.CssSavingArgs-) мероприятие.

 Чтобы узнать больше, посетите**Save a Document** документальная статья.

 По умолчанию, когда Aspose.Words сохраняет документ в формате HTML, он сохраняет встроенную информацию CSS (как значение параметра**style** атрибут каждого элемента).

[CssSavingArgs](../../com.aspose.words/csssavingargs) позволяет сохранить информацию CSS в файл, предоставив собственный объект потока.

 Чтобы сохранить CSS в поток, используйте**P:Aspose.Words.Saving.CssSavingArgs.CssStream** имущество.

 Чтобы запретить сохранение CSS в файл и встраивание в HTML-документ, используйте[isExportNeeded()](../../com.aspose.words/csssavingargs\#isExportNeeded--) / [isExportNeeded(boolean)](../../com.aspose.words/csssavingargs\#isExportNeeded-boolean-) имущество.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getCssStream()](#getCssStream--) |  |
| [getDocument()](#getDocument--) | Получает объект документа, который в данный момент сохраняется. |
| [getKeepCssStreamOpen()](#getKeepCssStreamOpen--) | Указывает, должен ли Aspose.Words оставить поток открытым или закрыть его после сохранения информации CSS. |
| [hashCode()](#hashCode--) |  |
| [isExportNeeded()](#isExportNeeded--) | Позволяет указать, будет ли CSS экспортироваться в файл и внедряться в документ HTML. |
| [isExportNeeded(boolean value)](#isExportNeeded-boolean-) | Позволяет указать, будет ли CSS экспортироваться в файл и внедряться в документ HTML. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setCssStream(OutputStream value)](#setCssStream-java.io.OutputStream-) |  |
| [setKeepCssStreamOpen(boolean value)](#setKeepCssStreamOpen-boolean-) | Указывает, должен ли Aspose.Words оставить поток открытым или закрыть его после сохранения информации CSS. |
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
### getCssStream() {#getCssStream--}
```
public OutputStream getCssStream()
```




**Возвращает:**
java.io.OutputStream
### getDocument() {#getDocument--}
```
public Document getDocument()
```


Получает объект документа, который в данный момент сохраняется.

**Возвращает:**
[Document](../../com.aspose.words/document) - Объект документа, который в данный момент сохраняется.
### getKeepCssStreamOpen() {#getKeepCssStreamOpen--}
```
public boolean getKeepCssStreamOpen()
```


Указывает, должен ли Aspose.Words оставить поток открытым или закрыть его после сохранения информации CSS.

 По умолчанию установлено значение false, и Aspose.Words закроет поток, указанный вами в**P:Aspose.Words.Saving.CssSavingArgs.CssStream** свойство после записи в него информации CSS. Укажите значение true, чтобы поток оставался открытым.

**P:Aspose.Words.Saving.CssSavingArgs.CssStream**

**Возвращает:**
boolean - соответствующее логическое значение.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### isExportNeeded() {#isExportNeeded--}
```
public boolean isExportNeeded()
```


Позволяет указать, будет ли CSS экспортироваться в файл и внедряться в документ HTML. По умолчанию верно. Если для этого свойства установлено значение false , информация CSS не будет сохранена в файле CSS и не будет встроена в документ HTML.

**Возвращает:**
boolean - соответствующее логическое значение.
### isExportNeeded(boolean value) {#isExportNeeded-boolean-}
```
public void isExportNeeded(boolean value)
```


Позволяет указать, будет ли CSS экспортироваться в файл и внедряться в документ HTML. По умолчанию верно. Если для этого свойства установлено значение false , информация CSS не будет сохранена в файле CSS и не будет встроена в документ HTML.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setCssStream(OutputStream value) {#setCssStream-java.io.OutputStream-}
```
public void setCssStream(OutputStream value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.io.OutputStream |  |

### setKeepCssStreamOpen(boolean value) {#setKeepCssStreamOpen-boolean-}
```
public void setKeepCssStreamOpen(boolean value)
```


Указывает, должен ли Aspose.Words оставить поток открытым или закрыть его после сохранения информации CSS.

 По умолчанию установлено значение false, и Aspose.Words закроет поток, указанный вами в**P:Aspose.Words.Saving.CssSavingArgs.CssStream** свойство после записи в него информации CSS. Укажите значение true, чтобы поток оставался открытым.

**P:Aspose.Words.Saving.CssSavingArgs.CssStream**

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

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
