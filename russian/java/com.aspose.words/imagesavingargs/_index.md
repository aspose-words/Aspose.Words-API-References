---
title: ImageSavingArgs
second_title: Справочник по API Aspose.Words для Java
description: Предоставляет данные для события.
type: docs
weight: 341
url: /ru/java/com.aspose.words/imagesavingargs/
---

**Наследование:**
java.lang.Object
```
public class ImageSavingArgs
```

 Предоставляет данные для[IImageSavingCallback.imageSaving(com.aspose.words.ImageSavingArgs)](../../com.aspose.words/iimagesavingcallback\#imageSaving-com.aspose.words.ImageSavingArgs-) мероприятие.

 Чтобы узнать больше, посетите**Save a Document** документальная статья.

По умолчанию, когда Aspose.Words сохраняет документ в формате HTML, каждое изображение сохраняется в отдельный файл. Aspose.Words использует имя файла документа и уникальный номер для создания уникального имени файла для каждого изображения, найденного в документе.

[ImageSavingArgs](../../com.aspose.words/imagesavingargs) позволяет переопределить, как генерируются имена файлов изображений, или полностью обойти сохранение изображений в файлы, предоставив свои собственные потоковые объекты.

 Чтобы применить собственную логику для генерации имен файлов изображений, используйте[getImageFileName()](../../com.aspose.words/imagesavingargs\#getImageFileName--) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagesavingargs\#setImageFileName-java.lang.String-), [getCurrentShape()](../../com.aspose.words/imagesavingargs\#getCurrentShape--) а также[isImageAvailable()](../../com.aspose.words/imagesavingargs\#isImageAvailable--) характеристики.

 Чтобы сохранять изображения в потоки вместо файлов, используйте**P:Aspose.Words.Saving.ImageSavingArgs.ImageStream** имущество.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getCurrentShape()](#getCurrentShape--) |  Получает[ShapeBase](../../com.aspose.words/shapebase) объект, соответствующий фигуре или групповой фигуре, которую нужно сохранить. |
| [getDocument()](#getDocument--) | Получает объект документа, который в данный момент сохраняется. |
| [getImageFileName()](#getImageFileName--) | Получает имя файла (без пути), в котором будет сохранено изображение. |
| [getImageStream()](#getImageStream--) |  |
| [getKeepImageStreamOpen()](#getKeepImageStreamOpen--) | Указывает, должен ли Aspose.Words оставить поток открытым или закрыть его после сохранения изображения. |
| [hashCode()](#hashCode--) |  |
| [isImageAvailable()](#isImageAvailable--) | Возвращает true, если текущее изображение доступно для экспорта. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setImageFileName(String value)](#setImageFileName-java.lang.String-) | Задает имя файла (без пути), в котором будет сохранено изображение. |
| [setImageStream(OutputStream value)](#setImageStream-java.io.OutputStream-) |  |
| [setKeepImageStreamOpen(boolean value)](#setKeepImageStreamOpen-boolean-) | Указывает, должен ли Aspose.Words оставить поток открытым или закрыть его после сохранения изображения. |
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
### getCurrentShape() {#getCurrentShape--}
```
public ShapeBase getCurrentShape()
```


 Получает[ShapeBase](../../com.aspose.words/shapebase) объект, соответствующий фигуре или групповой фигуре, которую нужно сохранить.

[IImageSavingCallback](../../com.aspose.words/iimagesavingcallback) может быть запущен при сохранении формы или формы группы. Вот почему свойство имеет[ShapeBase](../../com.aspose.words/shapebase) тип. Вы можете проверить, является ли это формой группы, сравнивая[ShapeBase.getShapeType()](../../com.aspose.words/shapebase\#getShapeType--) с[ShapeType.GROUP](../../com.aspose.words/shapetype\#GROUP) или приведя его к одному из производных классов:[Shape](../../com.aspose.words/shape) или же[GroupShape](../../com.aspose.words/groupshape).

 Aspose.Words использует имя файла документа и уникальный номер для создания уникального имени файла для каждого изображения, найденного в документе. Вы можете использовать[getCurrentShape()](../../com.aspose.words/imagesavingargs\#getCurrentShape--) свойство для создания «лучшего» имени файла путем изучения свойств формы, таких как[ImageData.getTitle()](../../com.aspose.words/imagedata\#getTitle--) / [ImageData.setTitle(java.lang.String)](../../com.aspose.words/imagedata\#setTitle-java.lang.String-) (только форма),[ImageData.getSourceFullName()](../../com.aspose.words/imagedata\#getSourceFullName--) / [ImageData.setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata\#setSourceFullName-java.lang.String-) (только форма) и[ShapeBase.getName()](../../com.aspose.words/shapebase\#getName--) / [ShapeBase.setName(java.lang.String)](../../com.aspose.words/shapebase\#setName-java.lang.String-). Конечно, вы можете создавать имена файлов, используя любые другие свойства или критерии, но обратите внимание, что имена вспомогательных файлов должны быть уникальными в рамках операции экспорта.

 Некоторые изображения в документе могут быть недоступны. Чтобы проверить доступность изображения, используйте[isImageAvailable()](../../com.aspose.words/imagesavingargs\#isImageAvailable--) имущество.

**Возвращает:**
[ShapeBase](../../com.aspose.words/shapebase) -[ShapeBase](../../com.aspose.words/shapebase) объект, соответствующий фигуре или групповой фигуре, которую нужно сохранить.
### getDocument() {#getDocument--}
```
public Document getDocument()
```


Получает объект документа, который в данный момент сохраняется.

**Возвращает:**
[Document](../../com.aspose.words/document) - Объект документа, который в данный момент сохраняется.
### getImageFileName() {#getImageFileName--}
```
public String getImageFileName()
```


Получает имя файла (без пути), в котором будет сохранено изображение.

Это свойство позволяет переопределить способ генерации имен файлов изображений во время экспорта в HTML.

Когда событие запускается, это свойство содержит имя файла, созданное Aspose.Words. Вы можете изменить значение этого свойства, чтобы сохранить изображение в другой файл. Обратите внимание, что имена файлов должны быть уникальными.

Aspose.Words автоматически генерирует уникальное имя файла для каждого встроенного изображения при экспорте в формат HTML. Способ генерации имени файла изображения зависит от того, сохраняете ли вы документ в файл или в поток.

 При сохранении документа в файл сгенерированное имя файла изображения выглядит так:*.![Image 1][].*.

 При сохранении документа в поток сгенерированное имя файла изображения выглядит так:*Aspose.Words..![Image 1][].*.

[getImageFileName()](../../com.aspose.words/imagesavingargs\#getImageFileName--) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagesavingargs\#setImageFileName-java.lang.String-) должен содержать только имя файла без пути. Aspose.Words определяет путь для сохранения и значение атрибута src для записи в HTML по имени файла документа,[HtmlSaveOptions.getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [HtmlSaveOptions.setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-) а также[HtmlSaveOptions.getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [HtmlSaveOptions.setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-) характеристики.


[Изображение 1]: 

**Возвращает:**
java.lang.String — имя файла (без пути), в котором будет сохранено изображение.
### getImageStream() {#getImageStream--}
```
public OutputStream getImageStream()
```




**Возвращает:**
java.io.OutputStream
### getKeepImageStreamOpen() {#getKeepImageStreamOpen--}
```
public boolean getKeepImageStreamOpen()
```


Указывает, должен ли Aspose.Words оставить поток открытым или закрыть его после сохранения изображения.

 По умолчанию установлено значение false, и Aspose.Words закроет поток, указанный вами в**P:Aspose.Words.Saving.ImageSavingArgs.ImageStream**свойство после записи в него изображения. Укажите значение true, чтобы поток оставался открытым.

**P:Aspose.Words.Saving.ImageSavingArgs.ImageStream**

**Возвращает:**
boolean - соответствующее логическое значение.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### isImageAvailable() {#isImageAvailable--}
```
public boolean isImageAvailable()
```


Возвращает true, если текущее изображение доступно для экспорта.

Некоторые изображения в документе могут быть недоступны, например, потому что изображение связано, а ссылка недоступна или не указывает на действительное изображение. В этом случае Aspose.Words экспортирует значок с красным крестом. Это свойство возвращает значение true, если исходное изображение доступно; возвращает false, если исходное изображение недоступно и для сохранения будет предложен значок «нет изображения».

При сохранении фигуры группы или фигуры, не требующей изображения, это свойство всегда имеет значение true .

**Возвращает:**
 логический -\{ true, если текущее изображение доступно для экспорта.
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setImageFileName(String value) {#setImageFileName-java.lang.String-}
```
public void setImageFileName(String value)
```


Задает имя файла (без пути), в котором будет сохранено изображение.

Это свойство позволяет переопределить способ генерации имен файлов изображений во время экспорта в HTML.

Когда событие запускается, это свойство содержит имя файла, созданное Aspose.Words. Вы можете изменить значение этого свойства, чтобы сохранить изображение в другой файл. Обратите внимание, что имена файлов должны быть уникальными.

Aspose.Words автоматически генерирует уникальное имя файла для каждого встроенного изображения при экспорте в формат HTML. Способ генерации имени файла изображения зависит от того, сохраняете ли вы документ в файл или в поток.

 При сохранении документа в файл сгенерированное имя файла изображения выглядит так:*.![Image 1][].*.

 При сохранении документа в поток сгенерированное имя файла изображения выглядит так:*Aspose.Words..![Image 1][].*.

[getImageFileName()](../../com.aspose.words/imagesavingargs\#getImageFileName--) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagesavingargs\#setImageFileName-java.lang.String-) должен содержать только имя файла без пути. Aspose.Words определяет путь для сохранения и значение атрибута src для записи в HTML по имени файла документа,[HtmlSaveOptions.getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [HtmlSaveOptions.setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-) а также[HtmlSaveOptions.getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [HtmlSaveOptions.setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-) характеристики.


[Изображение 1]: 

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Имя файла (без пути), в котором будет сохранено изображение. |

### setImageStream(OutputStream value) {#setImageStream-java.io.OutputStream-}
```
public void setImageStream(OutputStream value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.io.OutputStream |  |

### setKeepImageStreamOpen(boolean value) {#setKeepImageStreamOpen-boolean-}
```
public void setKeepImageStreamOpen(boolean value)
```


Указывает, должен ли Aspose.Words оставить поток открытым или закрыть его после сохранения изображения.

 По умолчанию установлено значение false, и Aspose.Words закроет поток, указанный вами в**P:Aspose.Words.Saving.ImageSavingArgs.ImageStream**свойство после записи в него изображения. Укажите значение true, чтобы поток оставался открытым.

**P:Aspose.Words.Saving.ImageSavingArgs.ImageStream**

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
