---
title: ResourceSavingArgs
second_title: Справочник по API Aspose.Words для Java
description: Предоставляет данные для события.
type: docs
weight: 481
url: /ru/java/com.aspose.words/resourcesavingargs/
---

**Наследование:**
java.lang.Object
```
public class ResourceSavingArgs
```

 Предоставляет данные для[IResourceSavingCallback.resourceSaving(com.aspose.words.ResourceSavingArgs)](../../com.aspose.words/iresourcesavingcallback\#resourceSaving-com.aspose.words.ResourceSavingArgs-) мероприятие.

 Чтобы узнать больше, посетите**Save a Document** документальная статья.

По умолчанию, когда Aspose.Words сохраняет документ на фиксированную страницу HTML или SVG, он сохраняет каждый ресурс в отдельный файл. Aspose.Words использует имя файла документа и уникальный номер для создания уникального имени файла для каждого ресурса, найденного в документе.

[ResourceSavingArgs](../../com.aspose.words/resourcesavingargs) позволяет переопределить, как генерируются имена файлов ресурсов, или полностью обойти сохранение ресурсов в файлы, предоставив свои собственные потоковые объекты.

 Чтобы применить собственную логику для генерации имен файлов ресурсов, используйте[getResourceFileName()](../../com.aspose.words/resourcesavingargs\#getResourceFileName--) / [setResourceFileName(java.lang.String)](../../com.aspose.words/resourcesavingargs\#setResourceFileName-java.lang.String-) имущество.

Чтобы сохранять ресурсы в потоки, а не в файлы, используйте**P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream** имущество.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getDocument()](#getDocument--) | Получает объект документа, который в данный момент сохраняется. |
| [getKeepResourceStreamOpen()](#getKeepResourceStreamOpen--) | Указывает, должен ли Aspose.Words оставить поток открытым или закрыть его после сохранения ресурса. |
| [getResourceFileName()](#getResourceFileName--) | Получает имя файла (без пути), в котором будет сохранен ресурс. |
| [getResourceFileUri()](#getResourceFileUri--) | Получает универсальный идентификатор ресурса (URI), используемый для ссылки на файл ресурсов из документа. |
| [getResourceStream()](#getResourceStream--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setKeepResourceStreamOpen(boolean value)](#setKeepResourceStreamOpen-boolean-) | Указывает, должен ли Aspose.Words оставить поток открытым или закрыть его после сохранения ресурса. |
| [setResourceFileName(String value)](#setResourceFileName-java.lang.String-) | Задает имя файла (без пути), в котором будет сохранен ресурс. |
| [setResourceFileUri(String value)](#setResourceFileUri-java.lang.String-) | Задает универсальный идентификатор ресурса (URI), используемый для ссылки на файл ресурсов из документа. |
| [setResourceStream(OutputStream value)](#setResourceStream-java.io.OutputStream-) |  |
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
### getDocument() {#getDocument--}
```
public Document getDocument()
```


Получает объект документа, который в данный момент сохраняется.

**Возвращает:**
[Document](../../com.aspose.words/document) - Объект документа, который в данный момент сохраняется.
### getKeepResourceStreamOpen() {#getKeepResourceStreamOpen--}
```
public boolean getKeepResourceStreamOpen()
```


Указывает, должен ли Aspose.Words оставить поток открытым или закрыть его после сохранения ресурса.

 По умолчанию установлено значение false, и Aspose.Words закроет поток, указанный вами в**P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream** свойство после записи в него ресурса. Укажите значение true, чтобы поток оставался открытым.

**P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream**

**Возвращает:**
boolean - соответствующее логическое значение.
### getResourceFileName() {#getResourceFileName--}
```
public String getResourceFileName()
```


Получает имя файла (без пути), в котором будет сохранен ресурс.

Это свойство позволяет переопределить способ генерации имен файлов ресурсов во время экспорта в HTML или SVG с фиксированной страницей.

Когда событие запускается, это свойство содержит имя файла, созданное Aspose.Words. Вы можете изменить значение этого свойства, чтобы сохранить ресурс в другой файл. Обратите внимание, что имена файлов должны быть уникальными.

Aspose.Words автоматически генерирует уникальное имя файла для каждого ресурса при экспорте в формат фиксированной страницы HTML или SVG. Способ генерации имени файла ресурсов зависит от того, сохраняете ли вы документ в файл или в поток.

 При сохранении документа в файл сгенерированное имя файла ресурсов выглядит так:*.![Image 1][].*.

 При сохранении документа в поток сгенерированное имя файла ресурсов выглядит так:*Aspose.Words..![Image 1][].*.

[getResourceFileName()](../../com.aspose.words/resourcesavingargs\#getResourceFileName--) / [setResourceFileName(java.lang.String)](../../com.aspose.words/resourcesavingargs\#setResourceFileName-java.lang.String-) должен содержать только имя файла без пути. Aspose.Words определяет путь для сохранения и значение атрибута src для записи на фиксированную страницу HTML или SVG, используя имя файла документа,[HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolder--) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolder-java.lang.String-) или же[SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions\#getResourcesFolder--) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions\#setResourcesFolder-java.lang.String-) а также[HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolderAlias--) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolderAlias-java.lang.String-) или же[SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions\#getResourcesFolderAlias--) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions\#setResourcesFolderAlias-java.lang.String-) характеристики.

**P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream** [HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolder--) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolder-java.lang.String-) [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions\#getResourcesFolder--) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions\#setResourcesFolder-java.lang.String-) [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolderAlias--) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolderAlias-java.lang.String-) [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions\#getResourcesFolderAlias--) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions\#setResourcesFolderAlias-java.lang.String-)


[Изображение 1]: 

**Возвращает:**
java.lang.String — имя файла (без пути), в котором будет сохранен ресурс.
### getResourceFileUri() {#getResourceFileUri--}
```
public String getResourceFileUri()
```


Получает универсальный идентификатор ресурса (URI), используемый для ссылки на файл ресурсов из документа.

Это свойство позволяет изменять URI файлов ресурсов, экспортируемых в документы HTML или SVG с фиксированной страницей.

Aspose.Words автоматически генерирует URI для каждого файла ресурсов во время экспорта в фиксированный формат страницы HTML или SVG. Сгенерированные URI ссылаются на файлы ресурсов, сохраненные Aspose.Words. Однако URI могут быть неверными, если файлы ресурсов должны быть перемещены в другое место или если файлы ресурсов сохранены в потоки. Это свойство позволяет исправлять URI в таких случаях.

Когда событие запускается, это свойство содержит URI, сгенерированный Aspose.Words. Вы можете изменить значение этого свойства, чтобы предоставить настраиваемый URI для файла ресурсов.

[HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolder--) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolder-java.lang.String-) [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions\#getResourcesFolder--) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions\#setResourcesFolder-java.lang.String-) [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolderAlias--) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolderAlias-java.lang.String-) [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions\#getResourcesFolderAlias--) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions\#setResourcesFolderAlias-java.lang.String-)

**Возвращает:**
java.lang.String — универсальный идентификатор ресурса (URI), используемый для ссылки на файл ресурсов из документа.
### getResourceStream() {#getResourceStream--}
```
public OutputStream getResourceStream()
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




### setKeepResourceStreamOpen(boolean value) {#setKeepResourceStreamOpen-boolean-}
```
public void setKeepResourceStreamOpen(boolean value)
```


Указывает, должен ли Aspose.Words оставить поток открытым или закрыть его после сохранения ресурса.

 По умолчанию установлено значение false, и Aspose.Words закроет поток, указанный вами в**P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream** свойство после записи в него ресурса. Укажите значение true, чтобы поток оставался открытым.

**P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream**

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setResourceFileName(String value) {#setResourceFileName-java.lang.String-}
```
public void setResourceFileName(String value)
```


Задает имя файла (без пути), в котором будет сохранен ресурс.

Это свойство позволяет переопределить способ генерации имен файлов ресурсов во время экспорта в HTML или SVG с фиксированной страницей.

Когда событие запускается, это свойство содержит имя файла, созданное Aspose.Words. Вы можете изменить значение этого свойства, чтобы сохранить ресурс в другой файл. Обратите внимание, что имена файлов должны быть уникальными.

Aspose.Words автоматически генерирует уникальное имя файла для каждого ресурса при экспорте в формат фиксированной страницы HTML или SVG. Способ генерации имени файла ресурсов зависит от того, сохраняете ли вы документ в файл или в поток.

 При сохранении документа в файл сгенерированное имя файла ресурсов выглядит так:*.![Image 1][].*.

 При сохранении документа в поток сгенерированное имя файла ресурсов выглядит так:*Aspose.Words..![Image 1][].*.

[getResourceFileName()](../../com.aspose.words/resourcesavingargs\#getResourceFileName--) / [setResourceFileName(java.lang.String)](../../com.aspose.words/resourcesavingargs\#setResourceFileName-java.lang.String-) должен содержать только имя файла без пути. Aspose.Words определяет путь для сохранения и значение атрибута src для записи на фиксированную страницу HTML или SVG, используя имя файла документа,[HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolder--) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolder-java.lang.String-) или же[SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions\#getResourcesFolder--) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions\#setResourcesFolder-java.lang.String-) а также[HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolderAlias--) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolderAlias-java.lang.String-) или же[SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions\#getResourcesFolderAlias--) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions\#setResourcesFolderAlias-java.lang.String-) характеристики.

**P:Aspose.Words.Saving.ResourceSavingArgs.ResourceStream** [HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolder--) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolder-java.lang.String-) [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions\#getResourcesFolder--) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions\#setResourcesFolder-java.lang.String-) [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolderAlias--) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolderAlias-java.lang.String-) [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions\#getResourcesFolderAlias--) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions\#setResourcesFolderAlias-java.lang.String-)


[Изображение 1]: 

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Имя файла (без пути), в котором будет сохранен ресурс. |

### setResourceFileUri(String value) {#setResourceFileUri-java.lang.String-}
```
public void setResourceFileUri(String value)
```


Задает универсальный идентификатор ресурса (URI), используемый для ссылки на файл ресурсов из документа.

Это свойство позволяет изменять URI файлов ресурсов, экспортируемых в документы HTML или SVG с фиксированной страницей.

Aspose.Words автоматически генерирует URI для каждого файла ресурсов во время экспорта в фиксированный формат страницы HTML или SVG. Сгенерированные URI ссылаются на файлы ресурсов, сохраненные Aspose.Words. Однако URI могут быть неверными, если файлы ресурсов должны быть перемещены в другое место или если файлы ресурсов сохранены в потоки. Это свойство позволяет исправлять URI в таких случаях.

Когда событие запускается, это свойство содержит URI, сгенерированный Aspose.Words. Вы можете изменить значение этого свойства, чтобы предоставить настраиваемый URI для файла ресурсов.

[HtmlFixedSaveOptions.getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolder--) / [HtmlFixedSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolder-java.lang.String-) [SvgSaveOptions.getResourcesFolder()](../../com.aspose.words/svgsaveoptions\#getResourcesFolder--) / [SvgSaveOptions.setResourcesFolder(java.lang.String)](../../com.aspose.words/svgsaveoptions\#setResourcesFolder-java.lang.String-) [HtmlFixedSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolderAlias--) / [HtmlFixedSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolderAlias-java.lang.String-) [SvgSaveOptions.getResourcesFolderAlias()](../../com.aspose.words/svgsaveoptions\#getResourcesFolderAlias--) / [SvgSaveOptions.setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/svgsaveoptions\#setResourcesFolderAlias-java.lang.String-)

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Универсальный идентификатор ресурса (URI), используемый для ссылки на файл ресурсов из документа. |

### setResourceStream(OutputStream value) {#setResourceStream-java.io.OutputStream-}
```
public void setResourceStream(OutputStream value)
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
