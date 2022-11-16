---
title: ListLevel
second_title: Справочник по API Aspose.Words для Java
description: Определяет форматирование для уровня списка.
type: docs
weight: 372
url: /ru/java/com.aspose.words/listlevel/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Cloneable
```
public class ListLevel implements Cloneable
```

Определяет форматирование для уровня списка.

 Чтобы узнать больше, посетите**Working with Lists** документальная статья.

 Вы не создаете объекты этого класса. Объекты уровня списка создаются автоматически при создании списка. Вы получаете доступ[ListLevel](../../com.aspose.words/listlevel) объекты через[ListLevelCollection](../../com.aspose.words/listlevelcollection) коллекция.

 Используйте свойства[ListLevel](../../com.aspose.words/listlevel) чтобы указать форматирование списка для отдельных уровней списка.
## Методы

| Метод | Описание |
| --- | --- |
| [clearRunAttrs()](#clearRunAttrs--) |  |
| [createPictureBullet()](#createPictureBullet--) | Создает форму маркера изображения для текущего уровня списка. |
| [deletePictureBullet()](#deletePictureBullet--) | Удаляет маркер изображения для текущего уровня списка. |
| [equals(ListLevel level)](#equals-com.aspose.words.ListLevel-) | Сравнивается с указанным ListLevel. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int-) |  |
| [getAlignment()](#getAlignment--) | Получает обоснование фактического номера элемента списка. |
| [getClass()](#getClass--) |  |
| [getCustomNumberStyleFormat()](#getCustomNumberStyleFormat--) | Получает пользовательский формат числового стиля для этого уровня списка. |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int-) |  |
| [getEffectiveValue(int index, int numberStyle, String customNumberStyleFormat)](#getEffectiveValue-int-int-java.lang.String-) |  |
| [getFont()](#getFont--) | Указывает форматирование символов, используемое для метки списка. |
| [getImageData()](#getImageData--) | Возвращает данные изображения формы маркера изображения для текущего уровня списка. |
| [getLinkedStyle()](#getLinkedStyle--) | Получает стиль абзаца, связанный с этим уровнем списка. |
| [getNumberFormat()](#getNumberFormat--) | Получает числовой формат для уровня списка. |
| [getNumberPosition()](#getNumberPosition--) | Получает позицию (в пунктах) числа или маркера для уровня списка. |
| [getNumberStyle()](#getNumberStyle--) | Получает стиль номера для этого уровня списка. |
| [getRestartAfterLevel()](#getRestartAfterLevel--) | Получает уровень списка, который должен появиться до того, как указанный уровень списка перезапустит нумерацию. |
| [getStartAt()](#getStartAt--) | Получает начальный номер для этого уровня списка. |
| [getTabPosition()](#getTabPosition--) | Получает позицию табуляции (в пунктах) для уровня списка. |
| [getTextPosition()](#getTextPosition--) | Получает позицию (в пунктах) второй строки переноса текста для уровня списка. |
| [getTrailingCharacter()](#getTrailingCharacter--) | Получает символ, вставленный после числа для уровня списка. |
| [hashCode()](#hashCode--) |  |
| [isLegal()](#isLegal--) | Значение true, если уровень превращает все унаследованные числа в арабские, и значение false, если сохраняется стиль их чисел. |
| [isLegal(boolean value)](#isLegal-boolean-) | Значение true, если уровень превращает все унаследованные числа в арабские, и значение false, если сохраняется стиль их чисел. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [removeRunAttr(int key)](#removeRunAttr-int-) |  |
| [setAlignment(int value)](#setAlignment-int-) | Задает выравнивание фактического номера элемента списка. |
| [setLinkedStyle(Style value)](#setLinkedStyle-com.aspose.words.Style-) | Задает стиль абзаца, связанный с этим уровнем списка. |
| [setNumberFormat(String value)](#setNumberFormat-java.lang.String-) | Задает числовой формат для уровня списка. |
| [setNumberPosition(double value)](#setNumberPosition-double-) | Задает позицию (в пунктах) числа или маркера для уровня списка. |
| [setNumberStyle(int value)](#setNumberStyle-int-) | Задает стиль номера для этого уровня списка. |
| [setRestartAfterLevel(int value)](#setRestartAfterLevel-int-) | Задает уровень списка, который должен появиться до того, как указанный уровень списка перезапустит нумерацию. |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [setStartAt(int value)](#setStartAt-int-) | Задает начальный номер для этого уровня списка. |
| [setTabPosition(double value)](#setTabPosition-double-) | Устанавливает позицию табуляции (в пунктах) для уровня списка. |
| [setTextPosition(double value)](#setTextPosition-double-) | Задает положение (в пунктах) второй строки переноса текста для уровня списка. |
| [setTrailingCharacter(int value)](#setTrailingCharacter-int-) | Устанавливает символ, вставляемый после числа для уровня списка. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clearRunAttrs() {#clearRunAttrs--}
```
public void clearRunAttrs()
```




### createPictureBullet() {#createPictureBullet--}
```
public void createPictureBullet()
```


Создает форму маркера изображения для текущего уровня списка. Обратите внимание, что для NumberStyle будет установлено значение Bullet, а для NumberFormat значение "\\xF0B7" для правильного отображения маркера изображения. Изображение красного креста будет установлено в качестве изображения маркера изображения при создании. Чтобы изменить его, используйте[getImageData()](../../com.aspose.words/listlevel\#getImageData--).

### deletePictureBullet() {#deletePictureBullet--}
```
public void deletePictureBullet()
```


Удаляет маркер изображения для текущего уровня списка. Пуля по умолчанию будет отображаться после удаления.

### equals(ListLevel level) {#equals-com.aspose.words.ListLevel-}
```
public boolean equals(ListLevel level)
```


Сравнивается с указанным ListLevel.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| level | [ListLevel](../../com.aspose.words/listlevel) |  |

**Возвращает:**
логический
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
### fetchInheritedRunAttr(int key) {#fetchInheritedRunAttr-int-}
```
public Object fetchInheritedRunAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### getAlignment() {#getAlignment--}
```
public int getAlignment()
```


Получает обоснование фактического номера элемента списка.

 Метка списка выровнена относительно[getNumberPosition()](../../com.aspose.words/listlevel\#getNumberPosition--) / [setNumberPosition(double)](../../com.aspose.words/listlevel\#setNumberPosition-double-) имущество.

**Возвращает:**
 int - Обоснование фактического номера элемента списка. Возвращаемое значение является одним из[ListLevelAlignment](../../com.aspose.words/listlevelalignment) константы.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getCustomNumberStyleFormat() {#getCustomNumberStyleFormat--}
```
public String getCustomNumberStyleFormat()
```


 Получает пользовательский формат числового стиля для этого уровня списка. Например: «а, �,\=,...".

**Возвращает:**
java.lang.String — пользовательский формат числового стиля для этого уровня списка.
### getDirectRunAttr(int key) {#getDirectRunAttr-int-}
```
public Object getDirectRunAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

**Возвращает:**
java.lang.Объект
### getEffectiveValue(int index, int numberStyle, String customNumberStyleFormat) {#getEffectiveValue-int-int-java.lang.String-}
```
public static String getEffectiveValue(int index, int numberStyle, String customNumberStyleFormat)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int |  |
| numberStyle | int |  |
| customNumberStyleFormat | java.lang.String |  |

**Возвращает:**
java.lang.String
### getFont() {#getFont--}
```
public Font getFont()
```


Указывает форматирование символов, используемое для метки списка.

**Возвращает:**
[Font](../../com.aspose.words/font) - соответствующий[Font](../../com.aspose.words/font) ценность.
### getImageData() {#getImageData--}
```
public ImageData getImageData()
```


 Возвращает данные изображения формы маркера изображения для текущего уровня списка. Если этот уровень не определяет маркер изображения, он возвращает значение null. Перед установкой нового изображения для формы маркера без изображения используйте[createPictureBullet()](../../com.aspose.words/listlevel\#createPictureBullet--) метод первый.

**Возвращает:**
[ImageData](../../com.aspose.words/imagedata) - Данные изображения формы маркера изображения для текущего уровня списка.
### getLinkedStyle() {#getLinkedStyle--}
```
public Style getLinkedStyle()
```


Получает стиль абзаца, связанный с этим уровнем списка.

Это свойство имеет значение null, если уровень списка не связан со стилем абзаца. Для этого свойства можно установить значение null.

**Возвращает:**
[Style](../../com.aspose.words/style) Стиль абзаца, связанный с этим уровнем списка.
### getNumberFormat() {#getNumberFormat--}
```
public String getNumberFormat()
```


Получает числовой формат для уровня списка.

 Среди обычных текстовых символов строка может содержать символы-заполнители.\ \x0000 до\\x0008 представляет числа из соответствующих уровней списка.

Например, строка "\\х0000.\\x0001)" сгенерирует метку списка, которая выглядит примерно как "1.5)". Число "1" — это текущее число из 1-го уровня списка, число "5" — текущее число из 2-го уровня списка.

Null не допускается, но пустая строка означает, что число недействительно.

**Возвращает:**
java.lang.String — числовой формат для уровня списка.
### getNumberPosition() {#getNumberPosition--}
```
public double getNumberPosition()
```


Получает позицию (в пунктах) числа или маркера для уровня списка.

[getNumberPosition()](../../com.aspose.words/listlevel\#getNumberPosition--) / [setNumberPosition(double)](../../com.aspose.words/listlevel\#setNumberPosition-double-) соответствует LeftIndent плюс FirstLineIndent абзаца.

**Возвращает:**
double - Позиция (в пунктах) числа или маркера для уровня списка.
### getNumberStyle() {#getNumberStyle--}
```
public int getNumberStyle()
```


Получает стиль номера для этого уровня списка.

**Возвращает:**
 int - Стиль числа для этого уровня списка. Возвращаемое значение является одним из[NumberStyle](../../com.aspose.words/numberstyle) константы.
### getRestartAfterLevel() {#getRestartAfterLevel--}
```
public int getRestartAfterLevel()
```


Получает уровень списка, который должен появиться до того, как указанный уровень списка перезапустит нумерацию.

Значение -1 означает, что нумерация будет продолжена.

**Возвращает:**
int — уровень списка, который должен появиться до того, как указанный уровень списка перезапустит нумерацию.
### getStartAt() {#getStartAt--}
```
public int getStartAt()
```


Получает начальный номер для этого уровня списка.

Значение по умолчанию — 1.

**Возвращает:**
int — начальный номер для этого уровня списка.
### getTabPosition() {#getTabPosition--}
```
public double getTabPosition()
```


Получает позицию табуляции (в пунктах) для уровня списка.

 Имеет эффект только тогда, когда[getTrailingCharacter()](../../com.aspose.words/listlevel\#getTrailingCharacter--) / [setTrailingCharacter(int)](../../com.aspose.words/listlevel\#setTrailingCharacter-int-) это вкладка.

**Возвращает:**
double - Позиция табуляции (в пунктах) для уровня списка.
### getTextPosition() {#getTextPosition--}
```
public double getTextPosition()
```


Получает позицию (в пунктах) второй строки переноса текста для уровня списка.

[getTextPosition()](../../com.aspose.words/listlevel\#getTextPosition--) / [setTextPosition(double)](../../com.aspose.words/listlevel\#setTextPosition-double-) соответствует LeftIndent абзаца.

**Возвращает:**
double — позиция (в пунктах) второй строки переноса текста для уровня списка.
### getTrailingCharacter() {#getTrailingCharacter--}
```
public int getTrailingCharacter()
```


Получает символ, вставленный после числа для уровня списка.

**Возвращает:**
 int - Символ, вставляемый после числа для уровня списка. Возвращаемое значение является одним из[ListTrailingCharacter](../../com.aspose.words/listtrailingcharacter) константы.
### hashCode() {#hashCode--}
```
public int hashCode()
```




**Возвращает:**
инт
### isLegal() {#isLegal--}
```
public boolean isLegal()
```


Значение true, если уровень превращает все унаследованные числа в арабские, и значение false, если сохраняется стиль их чисел.

**Возвращает:**
boolean - соответствующее логическое значение.
### isLegal(boolean value) {#isLegal-boolean-}
```
public void isLegal(boolean value)
```


Значение true, если уровень превращает все унаследованные числа в арабские, и значение false, если сохраняется стиль их чисел.

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




### removeRunAttr(int key) {#removeRunAttr-int-}
```
public void removeRunAttr(int key)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |

### setAlignment(int value) {#setAlignment-int-}
```
public void setAlignment(int value)
```


Задает выравнивание фактического номера элемента списка.

 Метка списка выровнена относительно[getNumberPosition()](../../com.aspose.words/listlevel\#getNumberPosition--) / [setNumberPosition(double)](../../com.aspose.words/listlevel\#setNumberPosition-double-) имущество.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Обоснование фактического номера элемента списка. Значение должно быть одним из[ListLevelAlignment](../../com.aspose.words/listlevelalignment) константы. |

### setLinkedStyle(Style value) {#setLinkedStyle-com.aspose.words.Style-}
```
public void setLinkedStyle(Style value)
```


Задает стиль абзаца, связанный с этим уровнем списка.

Это свойство имеет значение null, если уровень списка не связан со стилем абзаца. Для этого свойства можно установить значение null.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [Style](../../com.aspose.words/style) | Стиль абзаца, связанный с этим уровнем списка. |

### setNumberFormat(String value) {#setNumberFormat-java.lang.String-}
```
public void setNumberFormat(String value)
```


Задает числовой формат для уровня списка.

 Среди обычных текстовых символов строка может содержать символы-заполнители.\ \x0000 до\\x0008 представляет числа из соответствующих уровней списка.

Например, строка "\\х0000.\\x0001)" сгенерирует метку списка, которая выглядит примерно как "1.5)". Число "1" — это текущее число из 1-го уровня списка, число "5" — текущее число из 2-го уровня списка.

Null не допускается, но пустая строка означает, что число недействительно.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Числовой формат для уровня списка. |

### setNumberPosition(double value) {#setNumberPosition-double-}
```
public void setNumberPosition(double value)
```


Задает позицию (в пунктах) числа или маркера для уровня списка.

[getNumberPosition()](../../com.aspose.words/listlevel\#getNumberPosition--) / [setNumberPosition(double)](../../com.aspose.words/listlevel\#setNumberPosition-double-) соответствует LeftIndent плюс FirstLineIndent абзаца.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Позиция (в пунктах) числа или маркера для уровня списка. |

### setNumberStyle(int value) {#setNumberStyle-int-}
```
public void setNumberStyle(int value)
```


Задает стиль номера для этого уровня списка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Стиль номера для этого уровня списка. Значение должно быть одним из[NumberStyle](../../com.aspose.words/numberstyle) константы. |

### setRestartAfterLevel(int value) {#setRestartAfterLevel-int-}
```
public void setRestartAfterLevel(int value)
```


Задает уровень списка, который должен появиться до того, как указанный уровень списка перезапустит нумерацию.

Значение -1 означает, что нумерация будет продолжена.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Уровень списка, который должен появиться до того, как указанный уровень списка перезапустит нумерацию. |

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object-}
```
public void setRunAttr(int key, Object value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

### setStartAt(int value) {#setStartAt-int-}
```
public void setStartAt(int value)
```


Задает начальный номер для этого уровня списка.

Значение по умолчанию — 1.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Начальный номер для этого уровня списка. |

### setTabPosition(double value) {#setTabPosition-double-}
```
public void setTabPosition(double value)
```


Устанавливает позицию табуляции (в пунктах) для уровня списка.

 Имеет эффект только тогда, когда[getTrailingCharacter()](../../com.aspose.words/listlevel\#getTrailingCharacter--) / [setTrailingCharacter(int)](../../com.aspose.words/listlevel\#setTrailingCharacter-int-) это вкладка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Позиция табуляции (в пунктах) для уровня списка. |

### setTextPosition(double value) {#setTextPosition-double-}
```
public void setTextPosition(double value)
```


Задает положение (в пунктах) второй строки переноса текста для уровня списка.

[getTextPosition()](../../com.aspose.words/listlevel\#getTextPosition--) / [setTextPosition(double)](../../com.aspose.words/listlevel\#setTextPosition-double-) соответствует LeftIndent абзаца.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Позиция (в пунктах) второй строки переноса текста для уровня списка. |

### setTrailingCharacter(int value) {#setTrailingCharacter-int-}
```
public void setTrailingCharacter(int value)
```


Устанавливает символ, вставляемый после числа для уровня списка.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Символ, вставляемый после номера для уровня списка. Значение должно быть одним из[ListTrailingCharacter](../../com.aspose.words/listtrailingcharacter) константы. |

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
