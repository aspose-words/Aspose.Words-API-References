---
title: ImageFieldMergingArgs
second_title: Справочник по API Aspose.Words для Java
description: Предоставляет данные для события.
type: docs
weight: 338
url: /ru/java/com.aspose.words/imagefieldmergingargs/
---

**Наследование:**
java.lang.Object, [com.aspose.words.FieldMergingArgsBase](../../com.aspose.words/fieldmergingargsbase)
```
public class ImageFieldMergingArgs extends FieldMergingArgsBase
```

 Предоставляет данные для[IFieldMergingCallback.imageFieldMerging(com.aspose.words.ImageFieldMergingArgs)](../../com.aspose.words/ifieldmergingcallback\#imageFieldMerging-com.aspose.words.ImageFieldMergingArgs-) мероприятие.

 Чтобы узнать больше, посетите**Mail Merge and Reporting** документальная статья.

Это событие происходит во время слияния, когда в документе встречается поле слияния изображения. Вы можете отреагировать на это событие, чтобы вернуть имя файла, поток или объект java.awt.image.BufferedImage механизму слияния, чтобы он был вставлен в документ.

 Доступны три свойства[getImageFileName()](../../com.aspose.words/imagefieldmergingargs\#getImageFileName--) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagefieldmergingargs\#setImageFileName-java.lang.String-), **P:Aspose.Words.MailMerging.ImageFieldMergingArgs.ImageStream** а также[getImage()](../../com.aspose.words/imagefieldmergingargs\#getImage--) / [setImage(java.awt.image.BufferedImage)](../../com.aspose.words/imagefieldmergingargs\#setImage-java.awt.image.BufferedImage-) чтобы указать, откуда должно быть взято изображение. Установите только одно из этих свойств.

Чтобы вставить поле слияния с изображением в документ Word, выберите команду «Вставить/Поле», затем выберите MergeField и введите Image:MyFieldName.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getDocument()](#getDocument--) |  Возвращает[getDocument()](../../com.aspose.words/fieldmergingargsbase\#getDocument--) объект, для которого выполняется слияние. |
| [getDocumentFieldName()](#getDocumentFieldName--) | Получает имя поля слияния, указанное в документе. |
| [getField()](#getField--) | Получает объект, представляющий текущее поле слияния. |
| [getFieldName()](#getFieldName--) | Получает имя поля слияния в источнике данных. |
| [getFieldValue()](#getFieldValue--) | Получает значение поля из источника данных. |
| [getImage()](#getImage--) | Указывает изображение, которое механизм слияния должен вставить в документ. |
| [getImageFileName()](#getImageFileName--) | Задает имя файла изображения, которое механизм слияния должен вставить в документ. |
| [getImageHeight()](#getImageHeight--) | Задает высоту изображения для вставки в документ. |
| [getImageStream()](#getImageStream--) |  |
| [getImageWidth()](#getImageWidth--) | Указывает ширину изображения для вставки изображения в документ. |
| [getRecordIndex()](#getRecordIndex--) | Получает отсчитываемый от нуля индекс объединяемой записи. |
| [getShape()](#getShape--) | Указывает форму, которую механизм слияния должен вставить в документ. |
| [getTableName()](#getTableName--) | Получает имя таблицы данных для текущей операции слияния или пустую строку, если имя недоступно. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setFieldValue(Object value)](#setFieldValue-java.lang.Object-) | Задает значение поля из источника данных. |
| [setImage(BufferedImage value)](#setImage-java.awt.image.BufferedImage-) | Указывает изображение, которое механизм слияния должен вставить в документ. |
| [setImageFileName(String value)](#setImageFileName-java.lang.String-) | Задает имя файла изображения, которое механизм слияния должен вставить в документ. |
| [setImageHeight(MergeFieldImageDimension value)](#setImageHeight-com.aspose.words.MergeFieldImageDimension-) | Задает высоту изображения для вставки в документ. |
| [setImageStream(InputStream value)](#setImageStream-java.io.InputStream-) |  |
| [setImageWidth(MergeFieldImageDimension value)](#setImageWidth-com.aspose.words.MergeFieldImageDimension-) | Указывает ширину изображения для вставки изображения в документ. |
| [setShape(Shape value)](#setShape-com.aspose.words.Shape-) | Указывает форму, которую механизм слияния должен вставить в документ. |
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


 Возвращает[getDocument()](../../com.aspose.words/fieldmergingargsbase\#getDocument--) объект, для которого выполняется слияние.

**Возвращает:**
[Document](../../com.aspose.words/document) -[getDocument()](../../com.aspose.words/fieldmergingargsbase\#getDocument--) объект, для которого выполняется слияние.
### getDocumentFieldName() {#getDocumentFieldName--}
```
public String getDocumentFieldName()
```


Получает имя поля слияния, указанное в документе.

Если у вас есть сопоставление имени поля документа с другим именем поля источника данных, то это исходное имя поля, указанное в документе.

 Если вы указали в документе префикс имени поля, например «Image:MyFieldName», то**DocumentFieldName** возвращает имя поля без префикса, то есть "MyFieldName".

**Возвращает:**
java.lang.String — имя поля слияния, указанное в документе.
### getField() {#getField--}
```
public FieldMergeField getField()
```


Получает объект, представляющий текущее поле слияния.

**Возвращает:**
[FieldMergeField](../../com.aspose.words/fieldmergefield) - Объект, представляющий текущее поле слияния.
### getFieldName() {#getFieldName--}
```
public String getFieldName()
```


Получает имя поля слияния в источнике данных.

Если у вас есть сопоставление имени поля документа с другим именем поля источника данных, то это имя сопоставленного поля.

 Если вы указали в документе префикс имени поля, например «Image:MyFieldName», то**FieldName** возвращает имя поля без префикса, то есть "MyFieldName".

**Возвращает:**
java.lang.String — имя поля слияния в источнике данных.
### getFieldValue() {#getFieldValue--}
```
public Object getFieldValue()
```


Получает значение поля из источника данных. Это свойство содержит значение, которое только что было выбрано из вашего источника данных для этого поля механизмом слияния. Вы также можете заменить значение, установив свойство.

**Возвращает:**
java.lang.Object — значение поля из источника данных.
### getImage() {#getImage--}
```
public BufferedImage getImage()
```


Указывает изображение, которое механизм слияния должен вставить в документ.

**Возвращает:**
java.awt.image.BufferedImage — соответствующее значение java.awt.image.BufferedImage.
### getImageFileName() {#getImageFileName--}
```
public String getImageFileName()
```


Задает имя файла изображения, которое механизм слияния должен вставить в документ.

**Возвращает:**
java.lang.String — имя файла изображения, которое механизм слияния должен вставить в документ.
### getImageHeight() {#getImageHeight--}
```
public MergeFieldImageDimension getImageHeight()
```


Задает высоту изображения для вставки в документ.

 Значение этого свойства исходно исходит из соответствующего кода MERGEFIELD, содержащегося в шаблоне документа. Чтобы переопределить начальное значение, вы должны назначить экземпляр[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) класса к этому свойству или установить свойства для экземпляра[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) класс, возвращаемый этим свойством.

 Чтобы указать, что исходное значение высоты изображения должно быть применено, вы должны назначить**null** значение этого свойства или установите[MergeFieldImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension\#getValue--) / [MergeFieldImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension\#setValue-double-) свойство для экземпляра[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension)класс, возвращаемый этим свойством, к отрицательному значению.

**Возвращает:**
[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) - соответствующий[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) ценность.
### getImageStream() {#getImageStream--}
```
public InputStream getImageStream()
```




**Возвращает:**
java.io.InputStream
### getImageWidth() {#getImageWidth--}
```
public MergeFieldImageDimension getImageWidth()
```


Указывает ширину изображения для вставки изображения в документ.

 Значение этого свойства исходно исходит из соответствующего кода MERGEFIELD, содержащегося в шаблоне документа. Чтобы переопределить начальное значение, вы должны назначить экземпляр[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) класса к этому свойству или установить свойства для экземпляра[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) класс, возвращаемый этим свойством.

 Чтобы указать, что исходное значение ширины изображения должно быть применено, вы должны назначить**null** значение этого свойства или установите[MergeFieldImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension\#getValue--) / [MergeFieldImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension\#setValue-double-) свойство для экземпляра[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension)класс, возвращаемый этим свойством, к отрицательному значению.

**Возвращает:**
[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) - соответствующий[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) ценность.
### getRecordIndex() {#getRecordIndex--}
```
public int getRecordIndex()
```


Получает отсчитываемый от нуля индекс объединяемой записи.

**Возвращает:**
int — индекс объединяемой записи с отсчетом от нуля.
### getShape() {#getShape--}
```
public Shape getShape()
```


Указывает форму, которую механизм слияния должен вставить в документ.

 Когда это свойство указано, механизм слияния игнорирует все другие свойства, такие как[getImageFileName()](../../com.aspose.words/imagefieldmergingargs\#getImageFileName--) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagefieldmergingargs\#setImageFileName-java.lang.String-) или же**P:Aspose.Words.MailMerging.ImageFieldMergingArgs.ImageStream** и просто вставляет фигуру в документ.

 Используйте это свойство, чтобы полностью контролировать процесс слияния поля слияния изображений. Например, вы можете указать[ShapeBase.getWrapType()](../../com.aspose.words/shapebase\#getWrapType--) / [ShapeBase.setWrapType(int)](../../com.aspose.words/shapebase\#setWrapType-int-) или любое другое свойство формы для точной настройки результирующего узла. Однако обратите внимание, что вы несете ответственность за предоставление содержимого формы.

**Возвращает:**
[Shape](../../com.aspose.words/shape) - соответствующий[Shape](../../com.aspose.words/shape) ценность.
### getTableName() {#getTableName--}
```
public String getTableName()
```


Получает имя таблицы данных для текущей операции слияния или пустую строку, если имя недоступно.

**Возвращает:**
java.lang.String — имя таблицы данных для текущей операции слияния или пустая строка, если имя недоступно.
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




### setFieldValue(Object value) {#setFieldValue-java.lang.Object-}
```
public void setFieldValue(Object value)
```


Задает значение поля из источника данных. Это свойство содержит значение, которое только что было выбрано из вашего источника данных для этого поля механизмом слияния. Вы также можете заменить значение, установив свойство.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.Object | Значение поля из источника данных. |

### setImage(BufferedImage value) {#setImage-java.awt.image.BufferedImage-}
```
public void setImage(BufferedImage value)
```


Указывает изображение, которое механизм слияния должен вставить в документ.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.awt.image.BufferedImage | Соответствующее значение java.awt.image.BufferedImage. |

### setImageFileName(String value) {#setImageFileName-java.lang.String-}
```
public void setImageFileName(String value)
```


Задает имя файла изображения, которое механизм слияния должен вставить в документ.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Имя файла изображения, которое механизм слияния должен вставить в документ. |

### setImageHeight(MergeFieldImageDimension value) {#setImageHeight-com.aspose.words.MergeFieldImageDimension-}
```
public void setImageHeight(MergeFieldImageDimension value)
```


Задает высоту изображения для вставки в документ.

 Значение этого свойства исходно исходит из соответствующего кода MERGEFIELD, содержащегося в шаблоне документа. Чтобы переопределить начальное значение, вы должны назначить экземпляр[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) класса к этому свойству или установить свойства для экземпляра[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) класс, возвращаемый этим свойством.

 Чтобы указать, что исходное значение высоты изображения должно быть применено, вы должны назначить**null** значение этого свойства или установите[MergeFieldImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension\#getValue--) / [MergeFieldImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension\#setValue-double-) свойство для экземпляра[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension)класс, возвращаемый этим свойством, к отрицательному значению.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) |  Соответствующий[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) ценность. |

### setImageStream(InputStream value) {#setImageStream-java.io.InputStream-}
```
public void setImageStream(InputStream value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.io.InputStream |  |

### setImageWidth(MergeFieldImageDimension value) {#setImageWidth-com.aspose.words.MergeFieldImageDimension-}
```
public void setImageWidth(MergeFieldImageDimension value)
```


Указывает ширину изображения для вставки изображения в документ.

 Значение этого свойства исходно исходит из соответствующего кода MERGEFIELD, содержащегося в шаблоне документа. Чтобы переопределить начальное значение, вы должны назначить экземпляр[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) класса к этому свойству или установить свойства для экземпляра[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) класс, возвращаемый этим свойством.

 Чтобы указать, что исходное значение ширины изображения должно быть применено, вы должны назначить**null** значение этого свойства или установите[MergeFieldImageDimension.getValue()](../../com.aspose.words/mergefieldimagedimension\#getValue--) / [MergeFieldImageDimension.setValue(double)](../../com.aspose.words/mergefieldimagedimension\#setValue-double-) свойство для экземпляра[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension)класс, возвращаемый этим свойством, к отрицательному значению.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) |  Соответствующий[MergeFieldImageDimension](../../com.aspose.words/mergefieldimagedimension) ценность. |

### setShape(Shape value) {#setShape-com.aspose.words.Shape-}
```
public void setShape(Shape value)
```


Указывает форму, которую механизм слияния должен вставить в документ.

 Когда это свойство указано, механизм слияния игнорирует все другие свойства, такие как[getImageFileName()](../../com.aspose.words/imagefieldmergingargs\#getImageFileName--) / [setImageFileName(java.lang.String)](../../com.aspose.words/imagefieldmergingargs\#setImageFileName-java.lang.String-) или же**P:Aspose.Words.MailMerging.ImageFieldMergingArgs.ImageStream** и просто вставляет фигуру в документ.

 Используйте это свойство, чтобы полностью контролировать процесс слияния поля слияния изображений. Например, вы можете указать[ShapeBase.getWrapType()](../../com.aspose.words/shapebase\#getWrapType--) / [ShapeBase.setWrapType(int)](../../com.aspose.words/shapebase\#setWrapType-int-) или любое другое свойство формы для точной настройки результирующего узла. Однако обратите внимание, что вы несете ответственность за предоставление содержимого формы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [Shape](../../com.aspose.words/shape) |  Соответствующий[Shape](../../com.aspose.words/shape) ценность. |

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
