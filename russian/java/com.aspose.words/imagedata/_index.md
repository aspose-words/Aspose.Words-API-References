---
title: ImageData
second_title: Справочник по API Aspose.Words для Java
description: Определяет изображение для фигуры.
type: docs
weight: 337
url: /ru/java/com.aspose.words/imagedata/
---

**Наследование:**
java.lang.Object
```
public class ImageData
```

Определяет изображение для фигуры.

 Чтобы узнать больше, посетите**Working with Images** документальная статья.

 Использовать[Shape.getImageData()](../../com.aspose.words/shape\#getImageData--) свойство для доступа и изменения изображения внутри фигуры. Вы не создаете экземпляры[ImageData](../../com.aspose.words/imagedata) класс напрямую.

Изображение может быть сохранено внутри фигуры, связано с внешним файлом или и то, и другое (связано и сохранено в документе).

 Независимо от того, хранится ли изображение внутри фигуры или связано, вы всегда можете получить доступ к фактическому изображению, используя[toByteArray()](../../com.aspose.words/imagedata\#toByteArray--), [toImage()](../../com.aspose.words/imagedata\#toImage--) или же[save(java.lang.String)](../../com.aspose.words/imagedata\#save-java.lang.String-) методы. Если изображение хранится внутри фигуры, вы также можете напрямую получить к нему доступ, используя[getImageBytes()](../../com.aspose.words/imagedata\#getImageBytes--) / [setImageBytes(byte[])](../../com.aspose.words/imagedata\#setImageBytes-byte---) имущество.

 Чтобы сохранить изображение внутри фигуры, используйте[setImage(java.lang.String)](../../com.aspose.words/imagedata\#setImage-java.lang.String-) метод. Чтобы связать изображение с фигурой, установите[getSourceFullName()](../../com.aspose.words/imagedata\#getSourceFullName--) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata\#setSourceFullName-java.lang.String-) имущество.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int-) |  |
| [getBiLevel()](#getBiLevel--) | Определяет, будет ли изображение отображаться черно-белым. |
| [getBorders()](#getBorders--) | Получает коллекцию границ изображения. |
| [getBrightness()](#getBrightness--) | Получает яркость изображения. |
| [getChromaKey()](#getChromaKey--) | Определяет значение цвета изображения, которое будет рассматриваться как прозрачное. |
| [getClass()](#getClass--) |  |
| [getContrast()](#getContrast--) | Получает контраст для указанного изображения. |
| [getCropBottom()](#getCropBottom--) | Определяет долю удаления изображения с нижней стороны. |
| [getCropLeft()](#getCropLeft--) | Определяет долю удаления изображения с левой стороны. |
| [getCropRight()](#getCropRight--) | Определяет долю удаления изображения с правой стороны. |
| [getCropTop()](#getCropTop--) | Определяет долю удаления изображения с верхней стороны. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int-) |  |
| [getGrayScale()](#getGrayScale--) | Определяет, будет ли изображение отображаться в режиме оттенков серого. |
| [getImageBytes()](#getImageBytes--) | Получает необработанные байты изображения, хранящиеся в форме. |
| [getImageSize()](#getImageSize--) | Получает информацию о размере и разрешении изображения. |
| [getImageType()](#getImageType--) | Получает тип изображения. |
| [getSourceFullName()](#getSourceFullName--) | Получает путь и имя исходного файла для связанного изображения. |
| [getTitle()](#getTitle--) | Определяет заголовок изображения. |
| [hasImage()](#hasImage--) | Возвращает true, если фигура содержит байты изображения или связывает изображение. |
| [hashCode()](#hashCode--) |  |
| [isLink()](#isLink--) |  Возвращает true, если изображение связано с фигурой (когда[getSourceFullName()](../../com.aspose.words/imagedata\#getSourceFullName--) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata\#setSourceFullName-java.lang.String-)уточняется). |
| [isLinkOnly()](#isLinkOnly--) | Возвращает true, если изображение связано и не хранится в документе. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [save(OutputStream stream)](#save-java.io.OutputStream-) |  |
| [save(String fileName)](#save-java.lang.String-) | Сохраняет изображение в файл. |
| [setBiLevel(boolean value)](#setBiLevel-boolean-) | Определяет, будет ли изображение отображаться черно-белым. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object-) |  |
| [setBrightness(double value)](#setBrightness-double-) | Устанавливает яркость изображения. |
| [setChromaKey(Color value)](#setChromaKey-java.awt.Color-) | Определяет значение цвета изображения, которое будет рассматриваться как прозрачное. |
| [setContrast(double value)](#setContrast-double-) | Устанавливает контраст для указанного изображения. |
| [setCropBottom(double value)](#setCropBottom-double-) | Определяет долю удаления изображения с нижней стороны. |
| [setCropLeft(double value)](#setCropLeft-double-) | Определяет долю удаления изображения с левой стороны. |
| [setCropRight(double value)](#setCropRight-double-) | Определяет долю удаления изображения с правой стороны. |
| [setCropTop(double value)](#setCropTop-double-) | Определяет долю удаления изображения с верхней стороны. |
| [setGrayScale(boolean value)](#setGrayScale-boolean-) | Определяет, будет ли изображение отображаться в режиме оттенков серого. |
| [setImage(BufferedImage image)](#setImage-java.awt.image.BufferedImage-) | Задает изображение, отображаемое фигурой. |
| [setImage(InputStream stream)](#setImage-java.io.InputStream-) |  |
| [setImage(String fileName)](#setImage-java.lang.String-) | Задает изображение, отображаемое фигурой. |
| [setImageBytes(byte[] value)](#setImageBytes-byte---) | Устанавливает необработанные байты изображения, хранящегося в форме. |
| [setSourceFullName(String value)](#setSourceFullName-java.lang.String-) | Задает путь и имя исходного файла для связанного изображения. |
| [setTitle(String value)](#setTitle-java.lang.String-) | Определяет заголовок изображения. |
| [toByteArray()](#toByteArray--) | Возвращает байты изображения для любого изображения, независимо от того, сохранено ли изображение или связано. |
| [toImage()](#toImage--) | Получает изображение, хранящееся в форме, как объект java BufferedImage. |
| [toStream()](#toStream--) | Создает и возвращает поток, содержащий байты изображения. |
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
### fetchInheritedBorderAttr(int key) {#fetchInheritedBorderAttr-int-}
```
public Object fetchInheritedBorderAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### getBiLevel() {#getBiLevel--}
```
public boolean getBiLevel()
```


Определяет, будет ли изображение отображаться черно-белым.

 Значение по умолчанию**false**.

**Возвращает:**
boolean - соответствующее логическое значение.
### getBorders() {#getBorders--}
```
public BorderCollection getBorders()
```


Получает коллекцию границ изображения. Границы действуют только для встроенных изображений.

**Возвращает:**
[BorderCollection](../../com.aspose.words/bordercollection) - Коллекция границ изображения.
### getBrightness() {#getBrightness--}
```
public double getBrightness()
```


Получает яркость изображения. Значение этого свойства должно быть числом от 0,0 (самый тусклый) до 1,0 (самый яркий).

Значение по умолчанию — 0,5.

**Возвращает:**
double - Яркость картинки.
### getChromaKey() {#getChromaKey--}
```
public Color getChromaKey()
```


Определяет значение цвета изображения, которое будет рассматриваться как прозрачное.

Значение по умолчанию — 0.

**Возвращает:**
java.awt.Color — соответствующее значение java.awt.Color.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getContrast() {#getContrast--}
```
public double getContrast()
```


Получает контраст для указанного изображения. Значение этого свойства должно быть числом от 0,0 (наименьший контраст) до 1,0 (наибольший контраст).

Значение по умолчанию — 0,5.

**Возвращает:**
double - Контраст для указанного изображения.
### getCropBottom() {#getCropBottom--}
```
public double getCropBottom()
```


Определяет долю удаления изображения с нижней стороны.

Величина обрезки может варьироваться от -1,0 до 1,0. Значение по умолчанию — 0. Обратите внимание, что при значении 1 изображение вообще не будет отображаться. Отрицательные значения приведут к тому, что изображение будет сжато внутрь от обрезаемого края (пустое пространство между изображением и обрезанным краем будет заполнено цветом заливки фигуры). Положительные значения меньше 1 приведут к тому, что оставшееся изображение будет растянуто, чтобы соответствовать форме.

Значение по умолчанию — 0.

**Возвращает:**
double - соответствующее двойное значение.
### getCropLeft() {#getCropLeft--}
```
public double getCropLeft()
```


Определяет долю удаления изображения с левой стороны.

Величина обрезки может варьироваться от -1,0 до 1,0. Значение по умолчанию — 0. Обратите внимание, что при значении 1 изображение вообще не будет отображаться. Отрицательные значения приведут к тому, что изображение будет сжато внутрь от обрезаемого края (пустое пространство между изображением и обрезанным краем будет заполнено цветом заливки фигуры). Положительные значения меньше 1 приведут к тому, что оставшееся изображение будет растянуто, чтобы соответствовать форме.

Значение по умолчанию — 0.

**Возвращает:**
double - соответствующее двойное значение.
### getCropRight() {#getCropRight--}
```
public double getCropRight()
```


Определяет долю удаления изображения с правой стороны.

Величина обрезки может варьироваться от -1,0 до 1,0. Значение по умолчанию — 0. Обратите внимание, что при значении 1 изображение вообще не будет отображаться. Отрицательные значения приведут к тому, что изображение будет сжато внутрь от обрезаемого края (пустое пространство между изображением и обрезанным краем будет заполнено цветом заливки фигуры). Положительные значения меньше 1 приведут к тому, что оставшееся изображение будет растянуто, чтобы соответствовать форме.

Значение по умолчанию — 0.

**Возвращает:**
double - соответствующее двойное значение.
### getCropTop() {#getCropTop--}
```
public double getCropTop()
```


Определяет долю удаления изображения с верхней стороны.

Величина обрезки может варьироваться от -1,0 до 1,0. Значение по умолчанию — 0. Обратите внимание, что при значении 1 изображение вообще не будет отображаться. Отрицательные значения приведут к тому, что изображение будет сжато внутрь от обрезаемого края (пустое пространство между изображением и обрезанным краем будет заполнено цветом заливки фигуры). Положительные значения меньше 1 приведут к тому, что оставшееся изображение будет растянуто, чтобы соответствовать форме.

Значение по умолчанию — 0.

**Возвращает:**
double - соответствующее двойное значение.
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int-}
```
public Object getDirectBorderAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### getGrayScale() {#getGrayScale--}
```
public boolean getGrayScale()
```


Определяет, будет ли изображение отображаться в режиме оттенков серого.

 Значение по умолчанию**false**.

**Возвращает:**
boolean - соответствующее логическое значение.
### getImageBytes() {#getImageBytes--}
```
public byte[] getImageBytes()
```


Получает необработанные байты изображения, хранящиеся в форме.

Установка значения null или пустого массива удалит изображение из формы.

Возвращает null, если изображение не сохранено в документе (например, в этом случае изображение, вероятно, связано).

**Возвращает:**
байт[] — необработанные байты изображения, хранящиеся в форме.
### getImageSize() {#getImageSize--}
```
public ImageSize getImageSize()
```


Получает информацию о размере и разрешении изображения. (4661,6)

Если изображение только связано и не хранится в документе, возвращается нулевой размер.

**Возвращает:**
[ImageSize](../../com.aspose.words/imagesize) - Информация о размере изображения и разрешении.
### getImageType() {#getImageType--}
```
public int getImageType()
```


Получает тип изображения. (4671,6)

**Возвращает:**
 int - Тип изображения. Возвращаемое значение является одним из[ImageType](../../com.aspose.words/imagetype) константы.
### getSourceFullName() {#getSourceFullName--}
```
public String getSourceFullName()
```


Получает путь и имя исходного файла для связанного изображения.

Значение по умолчанию — пустая строка.

 Если[getSourceFullName()](../../com.aspose.words/imagedata\#getSourceFullName--) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata\#setSourceFullName-java.lang.String-) не пустая строка, изображение связано.

**Возвращает:**
java.lang.String — путь и имя исходного файла связанного изображения.
### getTitle() {#getTitle--}
```
public String getTitle()
```


Определяет заголовок изображения.

Значение по умолчанию — пустая строка.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### hasImage() {#hasImage--}
```
public boolean hasImage()
```


Возвращает true, если фигура содержит байты изображения или связывает изображение. (4654,6)

**Возвращает:**
boolean — True, если фигура содержит байты изображения или ссылается на изображение.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### isLink() {#isLink--}
```
public boolean isLink()
```


 Возвращает true, если изображение связано с фигурой (когда[getSourceFullName()](../../com.aspose.words/imagedata\#getSourceFullName--) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata\#setSourceFullName-java.lang.String-) уточняется). (4678,6)

**Возвращает:**
 boolean — Истинно, если изображение связано с фигурой (когда[getSourceFullName()](../../com.aspose.words/imagedata\#getSourceFullName--) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata\#setSourceFullName-java.lang.String-)уточняется).
### isLinkOnly() {#isLinkOnly--}
```
public boolean isLinkOnly()
```


Возвращает true, если изображение связано и не хранится в документе. (4685,6)

**Возвращает:**
boolean — Истинно, если изображение связано и не хранится в документе.
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### save(OutputStream stream) {#save-java.io.OutputStream-}
```
public void save(OutputStream stream)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | java.io.OutputStream |  |

### save(String fileName) {#save-java.lang.String-}
```
public void save(String fileName)
```


Сохраняет изображение в файл.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String | Имя файла, куда сохранить изображение. |

### setBiLevel(boolean value) {#setBiLevel-boolean-}
```
public void setBiLevel(boolean value)
```


Определяет, будет ли изображение отображаться черно-белым.

 Значение по умолчанию**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object-}
```
public void setBorderAttr(int key, Object value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setBrightness(double value) {#setBrightness-double-}
```
public void setBrightness(double value)
```


Устанавливает яркость изображения. Значение этого свойства должно быть числом от 0,0 (самый тусклый) до 1,0 (самый яркий).

Значение по умолчанию — 0,5.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Яркость картинки. |

### setChromaKey(Color value) {#setChromaKey-java.awt.Color-}
```
public void setChromaKey(Color value)
```


Определяет значение цвета изображения, которое будет рассматриваться как прозрачное.

Значение по умолчанию — 0.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.awt.Color | Соответствующее значение java.awt.Color. |

### setContrast(double value) {#setContrast-double-}
```
public void setContrast(double value)
```


Устанавливает контраст для указанного изображения. Значение этого свойства должно быть числом от 0,0 (наименьший контраст) до 1,0 (наибольший контраст).

Значение по умолчанию — 0,5.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Контраст для указанного изображения. |

### setCropBottom(double value) {#setCropBottom-double-}
```
public void setCropBottom(double value)
```


Определяет долю удаления изображения с нижней стороны.

Величина обрезки может варьироваться от -1,0 до 1,0. Значение по умолчанию — 0. Обратите внимание, что при значении 1 изображение вообще не будет отображаться. Отрицательные значения приведут к тому, что изображение будет сжато внутрь от обрезаемого края (пустое пространство между изображением и обрезанным краем будет заполнено цветом заливки фигуры). Положительные значения меньше 1 приведут к тому, что оставшееся изображение будет растянуто, чтобы соответствовать форме.

Значение по умолчанию — 0.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Соответствующее двойное значение. |

### setCropLeft(double value) {#setCropLeft-double-}
```
public void setCropLeft(double value)
```


Определяет долю удаления изображения с левой стороны.

Величина обрезки может варьироваться от -1,0 до 1,0. Значение по умолчанию — 0. Обратите внимание, что при значении 1 изображение вообще не будет отображаться. Отрицательные значения приведут к тому, что изображение будет сжато внутрь от обрезаемого края (пустое пространство между изображением и обрезанным краем будет заполнено цветом заливки фигуры). Положительные значения меньше 1 приведут к тому, что оставшееся изображение будет растянуто, чтобы соответствовать форме.

Значение по умолчанию — 0.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Соответствующее двойное значение. |

### setCropRight(double value) {#setCropRight-double-}
```
public void setCropRight(double value)
```


Определяет долю удаления изображения с правой стороны.

Величина обрезки может варьироваться от -1,0 до 1,0. Значение по умолчанию — 0. Обратите внимание, что при значении 1 изображение вообще не будет отображаться. Отрицательные значения приведут к тому, что изображение будет сжато внутрь от обрезаемого края (пустое пространство между изображением и обрезанным краем будет заполнено цветом заливки фигуры). Положительные значения меньше 1 приведут к тому, что оставшееся изображение будет растянуто, чтобы соответствовать форме.

Значение по умолчанию — 0.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Соответствующее двойное значение. |

### setCropTop(double value) {#setCropTop-double-}
```
public void setCropTop(double value)
```


Определяет долю удаления изображения с верхней стороны.

Величина обрезки может варьироваться от -1,0 до 1,0. Значение по умолчанию — 0. Обратите внимание, что при значении 1 изображение вообще не будет отображаться. Отрицательные значения приведут к тому, что изображение будет сжато внутрь от обрезаемого края (пустое пространство между изображением и обрезанным краем будет заполнено цветом заливки фигуры). Положительные значения меньше 1 приведут к тому, что оставшееся изображение будет растянуто, чтобы соответствовать форме.

Значение по умолчанию — 0.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Соответствующее двойное значение. |

### setGrayScale(boolean value) {#setGrayScale-boolean-}
```
public void setGrayScale(boolean value)
```


Определяет, будет ли изображение отображаться в режиме оттенков серого.

 Значение по умолчанию**false**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setImage(BufferedImage image) {#setImage-java.awt.image.BufferedImage-}
```
public void setImage(BufferedImage image)
```


Задает изображение, отображаемое фигурой.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| image | java.awt.image.BufferedImage | Объект изображения. |

### setImage(InputStream stream) {#setImage-java.io.InputStream-}
```
public void setImage(InputStream stream)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### setImage(String fileName) {#setImage-java.lang.String-}
```
public void setImage(String fileName)
```


Задает изображение, отображаемое фигурой.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String | Файл изображения. Может быть именем файла или URL-адресом. |

### setImageBytes(byte[] value) {#setImageBytes-byte---}
```
public void setImageBytes(byte[] value)
```


Устанавливает необработанные байты изображения, хранящегося в форме.

Установка значения null или пустого массива удалит изображение из формы.

Возвращает null, если изображение не сохранено в документе (например, в этом случае изображение, вероятно, связано).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | byte[] | Необработанные байты изображения, хранящиеся в форме. |

### setSourceFullName(String value) {#setSourceFullName-java.lang.String-}
```
public void setSourceFullName(String value)
```


Задает путь и имя исходного файла для связанного изображения.

Значение по умолчанию — пустая строка.

 Если[getSourceFullName()](../../com.aspose.words/imagedata\#getSourceFullName--) / [setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata\#setSourceFullName-java.lang.String-) не пустая строка, изображение связано.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Путь и имя исходного файла связанного изображения. |

### setTitle(String value) {#setTitle-java.lang.String-}
```
public void setTitle(String value)
```


Определяет заголовок изображения.

Значение по умолчанию — пустая строка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### toByteArray() {#toByteArray--}
```
public byte[] toByteArray()
```


Возвращает байты изображения для любого изображения, независимо от того, сохранено ли изображение или связано.

**Возвращает:**
байт[] - Если изображение связано, загружает изображение каждый раз, когда оно вызывается.
### toImage() {#toImage--}
```
public BufferedImage toImage()
```


Получает изображение, хранящееся в форме, как объект java BufferedImage.

**Возвращает:**
java.awt.image.BufferedImage — пытается создать новый объект java.awt.image.BufferedImage из байтов изображения при каждом вызове этого метода. Если javax.imageio.ImageReader не может прочитать байты изображения (emf, wmf, tiff и т. д.), метод возвращает null.

Вызывающий объект несет ответственность за удаление объекта изображения.
### toStream() {#toStream--}
```
public InputStream toStream()
```


Создает и возвращает поток, содержащий байты изображения.

Если байты изображения хранятся в форме, создает и возвращает объект.

Если изображение связано и хранится в файле, открывает файл и возвращает объект.

Если изображение связано и сохранено во внешнем URL-адресе, открывает URL-адрес и возвращает объект.

Ответственность за удаление объекта потока лежит на вызывающем объекте.

Это еще не перенесено на Java.

**Возвращает:**
java.io.InputStream
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
