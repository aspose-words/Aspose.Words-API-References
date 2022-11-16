---
title: DocumentPartSavingArgs
second_title: Справочник по API Aspose.Words для Java
description: Предоставляет данные для обратного вызова.
type: docs
weight: 125
url: /ru/java/com.aspose.words/documentpartsavingargs/
---

**Наследование:**
java.lang.Object
```
public class DocumentPartSavingArgs
```

 Предоставляет данные для[IDocumentPartSavingCallback.documentPartSaving(com.aspose.words.DocumentPartSavingArgs)](../../com.aspose.words/idocumentpartsavingcallback\#documentPartSaving-com.aspose.words.DocumentPartSavingArgs-) перезвонить.

 Чтобы узнать больше, посетите**Save a Document** документальная статья.

 Когда Aspose.Words сохраняет документ в HTML или родственных форматах и[HtmlSaveOptions.getDocumentSplitCriteria()](../../com.aspose.words/htmlsaveoptions\#getDocumentSplitCriteria--) / [HtmlSaveOptions.setDocumentSplitCriteria(int)](../../com.aspose.words/htmlsaveoptions\#setDocumentSplitCriteria-int-) указан, документ разбивается на части и по умолчанию каждая часть документа сохраняется в отдельный файл.

 Учебный класс[DocumentPartSavingArgs](../../com.aspose.words/documentpartsavingargs) позволяет вам контролировать, как каждая часть документа будет сохранена. Это позволяет переопределить, как генерируются имена файлов, или полностью обойти сохранение частей документа в файлы, предоставив свои собственные потоковые объекты.

 Чтобы сохранить части документа в потоки вместо файлов, используйте**P:Aspose.Words.Saving.DocumentPartSavingArgs.DocumentPartStream** имущество.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getDocument()](#getDocument--) | Получает сохраняемый объект документа. |
| [getDocumentPartFileName()](#getDocumentPartFileName--) | Получает имя файла (без пути), в котором будет сохранена часть документа. |
| [getDocumentPartStream()](#getDocumentPartStream--) |  |
| [getKeepDocumentPartStreamOpen()](#getKeepDocumentPartStreamOpen--) | Указывает, должен ли Aspose.Words оставить поток открытым или закрыть его после сохранения части документа. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setDocumentPartFileName(String value)](#setDocumentPartFileName-java.lang.String-) | Задает имя файла (без пути), в котором будет сохранена часть документа. |
| [setDocumentPartStream(OutputStream value)](#setDocumentPartStream-java.io.OutputStream-) |  |
| [setKeepDocumentPartStreamOpen(boolean value)](#setKeepDocumentPartStreamOpen-boolean-) | Указывает, должен ли Aspose.Words оставить поток открытым или закрыть его после сохранения части документа. |
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


Получает сохраняемый объект документа.

**Возвращает:**
[Document](../../com.aspose.words/document) - Сохраняемый объект документа.
### getDocumentPartFileName() {#getDocumentPartFileName--}
```
public String getDocumentPartFileName()
```


Получает имя файла (без пути), в котором будет сохранена часть документа.

Это свойство позволяет переопределить способ генерации имен файлов частей документа во время экспорта в HTML или EPUB.

При вызове обратного вызова это свойство содержит имя файла, созданное Aspose.Words. Вы можете изменить значение этого свойства, чтобы сохранить часть документа в другой файл. Обратите внимание, что имя файла для каждой части должно быть уникальным.

[getDocumentPartFileName()](../../com.aspose.words/documentpartsavingargs\#getDocumentPartFileName--) / [setDocumentPartFileName(java.lang.String)](../../com.aspose.words/documentpartsavingargs\#setDocumentPartFileName-java.lang.String-) должен содержать только имя файла без пути. Aspose.Words определяет путь для сохранения по имени файла документа. Если имя выходного файла документа не указано, например, при сохранении в поток, это имя файла используется только для ссылок на части документа. То же самое верно и при сохранении в формате EPUB.

**P:Aspose.Words.Saving.DocumentPartSavingArgs.DocumentPartStream**

**Возвращает:**
java.lang.String — имя файла (без пути), в котором будет сохранена часть документа.
### getDocumentPartStream() {#getDocumentPartStream--}
```
public OutputStream getDocumentPartStream()
```




**Возвращает:**
java.io.OutputStream
### getKeepDocumentPartStreamOpen() {#getKeepDocumentPartStreamOpen--}
```
public boolean getKeepDocumentPartStreamOpen()
```


Указывает, должен ли Aspose.Words оставить поток открытым или закрыть его после сохранения части документа.

 По умолчанию установлено значение false, и Aspose.Words закроет поток, указанный вами в**P:Aspose.Words.Saving.DocumentPartSavingArgs.DocumentPartStream** свойство после записи в него части документа. Укажите значение true, чтобы поток оставался открытым. Обратите внимание, что основной выходной поток, указанный в вызове**M:Aspose.Words.Document.Save(System.IO.Stream,Aspose.Words.SaveFormat)** или же**M:Aspose.Words.Document.Save(System.IO.Stream,Aspose.Words.Saving.SaveOptions)** никогда не будет закрыт Aspose.Words, даже если[getKeepDocumentPartStreamOpen()](../../com.aspose.words/documentpartsavingargs\#getKeepDocumentPartStreamOpen--) / [setKeepDocumentPartStreamOpen(boolean)](../../com.aspose.words/documentpartsavingargs\#setKeepDocumentPartStreamOpen-boolean-)установлено значение false .

**P:Aspose.Words.Saving.DocumentPartSavingArgs.DocumentPartStream**

**Возвращает:**
boolean - соответствующее логическое значение.
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




### setDocumentPartFileName(String value) {#setDocumentPartFileName-java.lang.String-}
```
public void setDocumentPartFileName(String value)
```


Задает имя файла (без пути), в котором будет сохранена часть документа.

Это свойство позволяет переопределить способ генерации имен файлов частей документа во время экспорта в HTML или EPUB.

При вызове обратного вызова это свойство содержит имя файла, созданное Aspose.Words. Вы можете изменить значение этого свойства, чтобы сохранить часть документа в другой файл. Обратите внимание, что имя файла для каждой части должно быть уникальным.

[getDocumentPartFileName()](../../com.aspose.words/documentpartsavingargs\#getDocumentPartFileName--) / [setDocumentPartFileName(java.lang.String)](../../com.aspose.words/documentpartsavingargs\#setDocumentPartFileName-java.lang.String-) должен содержать только имя файла без пути. Aspose.Words определяет путь для сохранения по имени файла документа. Если имя выходного файла документа не указано, например, при сохранении в поток, это имя файла используется только для ссылок на части документа. То же самое верно и при сохранении в формате EPUB.

**P:Aspose.Words.Saving.DocumentPartSavingArgs.DocumentPartStream**

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Имя файла (без пути), в котором будет сохранена часть документа. |

### setDocumentPartStream(OutputStream value) {#setDocumentPartStream-java.io.OutputStream-}
```
public void setDocumentPartStream(OutputStream value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.io.OutputStream |  |

### setKeepDocumentPartStreamOpen(boolean value) {#setKeepDocumentPartStreamOpen-boolean-}
```
public void setKeepDocumentPartStreamOpen(boolean value)
```


Указывает, должен ли Aspose.Words оставить поток открытым или закрыть его после сохранения части документа.

 По умолчанию установлено значение false, и Aspose.Words закроет поток, указанный вами в**P:Aspose.Words.Saving.DocumentPartSavingArgs.DocumentPartStream** свойство после записи в него части документа. Укажите значение true, чтобы поток оставался открытым. Обратите внимание, что основной выходной поток, указанный в вызове**M:Aspose.Words.Document.Save(System.IO.Stream,Aspose.Words.SaveFormat)** или же**M:Aspose.Words.Document.Save(System.IO.Stream,Aspose.Words.Saving.SaveOptions)** никогда не будет закрыт Aspose.Words, даже если[getKeepDocumentPartStreamOpen()](../../com.aspose.words/documentpartsavingargs\#getKeepDocumentPartStreamOpen--) / [setKeepDocumentPartStreamOpen(boolean)](../../com.aspose.words/documentpartsavingargs\#setKeepDocumentPartStreamOpen-boolean-)установлено значение false .

**P:Aspose.Words.Saving.DocumentPartSavingArgs.DocumentPartStream**

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
