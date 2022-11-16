---
title: BarcodeParameters
second_title: Справочник по API Aspose.Words для Java
description: Класс-контейнер для параметров штрих-кода для передачи в BarcodeGenerator.
type: docs
weight: 26
url: /ru/java/com.aspose.words/barcodeparameters/
---

**Наследование:**
java.lang.Object
```
public class BarcodeParameters
```

Класс-контейнер для параметров штрих-кода для передачи в BarcodeGenerator.

 Чтобы узнать больше, посетите**Working with Fields** документальная статья.

 Набор параметров соответствует параметрам поля DISPLAYBARCODE. Точный список смотрите на[ ][Link 1]


[Link 1]: https://msdn.microsoft.com/en-us/library/hh745901%28v=office.12%29.aspx
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAddStartStopChar()](#getAddStartStopChar--) | Добавлять ли символы Start/Stop для типов штрих-кодов NW7 и CODE39. |
| [getBackgroundColor()](#getBackgroundColor--) | Цвет фона штрих-кода (0x000000 - 0xFFFFFF) |
| [getBarcodeType()](#getBarcodeType--) | Тип штрих-кода. |
| [getBarcodeValue()](#getBarcodeValue--) | Данные для кодирования. |
| [getCaseCodeStyle()](#getCaseCodeStyle--) | Стиль кода случая для штрих-кода типа ITF14. |
| [getClass()](#getClass--) |  |
| [getDisplayText()](#getDisplayText--) | Отображать ли данные штрих-кода (текст) вместе с изображением. |
| [getErrorCorrectionLevel()](#getErrorCorrectionLevel--) | Уровень исправления ошибок QR-кода. |
| [getFacingIdentificationMark()](#getFacingIdentificationMark--) | Тип опознавательного знака облицовки (FIM). |
| [getFixCheckDigit()](#getFixCheckDigit--) | Исправлять ли контрольную цифру, если она\\u2019s недействителен. |
| [getForegroundColor()](#getForegroundColor--) | Основной цвет штрих-кода (0x000000 - 0xFFFFFF) |
| [getPosCodeStyle()](#getPosCodeStyle--) | Стиль штрих-кода торговой точки (типы штрих-кода UPCA|UPCE|EAN13|EAN8). |
| [getPostalAddress()](#getPostalAddress--) | Почтовый адрес со штрих-кодом. |
| [getScalingFactor()](#getScalingFactor--) | Масштабный коэффициент для символа. |
| [getSymbolHeight()](#getSymbolHeight--) | Высота изображения штрих-кода (в твипах - 1/1440 дюйма) |
| [getSymbolRotation()](#getSymbolRotation--) | Вращение символа штрих-кода. |
| [hashCode()](#hashCode--) |  |
| [isBookmark()](#isBookmark--) |  Будь то[getPostalAddress()](../../com.aspose.words/barcodeparameters\#getPostalAddress--) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters\#setPostalAddress-java.lang.String-) это имя закладки. |
| [isBookmark(boolean value)](#isBookmark-boolean-) |  Будь то[getPostalAddress()](../../com.aspose.words/barcodeparameters\#getPostalAddress--) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters\#setPostalAddress-java.lang.String-) это имя закладки. |
| [isUSPostalAddress()](#isUSPostalAddress--) |  Будь то[getPostalAddress()](../../com.aspose.words/barcodeparameters\#getPostalAddress--) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters\#setPostalAddress-java.lang.String-) США |
| [isUSPostalAddress(boolean value)](#isUSPostalAddress-boolean-) |  Будь то[getPostalAddress()](../../com.aspose.words/barcodeparameters\#getPostalAddress--) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters\#setPostalAddress-java.lang.String-) США |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setAddStartStopChar(boolean value)](#setAddStartStopChar-boolean-) | Добавлять ли символы Start/Stop для типов штрих-кодов NW7 и CODE39. |
| [setBackgroundColor(String value)](#setBackgroundColor-java.lang.String-) | Цвет фона штрих-кода (0x000000 - 0xFFFFFF) |
| [setBarcodeType(String value)](#setBarcodeType-java.lang.String-) | Тип штрих-кода. |
| [setBarcodeValue(String value)](#setBarcodeValue-java.lang.String-) | Данные для кодирования. |
| [setCaseCodeStyle(String value)](#setCaseCodeStyle-java.lang.String-) | Стиль кода случая для штрих-кода типа ITF14. |
| [setDisplayText(boolean value)](#setDisplayText-boolean-) | Отображать ли данные штрих-кода (текст) вместе с изображением. |
| [setErrorCorrectionLevel(String value)](#setErrorCorrectionLevel-java.lang.String-) | Уровень исправления ошибок QR-кода. |
| [setFacingIdentificationMark(String value)](#setFacingIdentificationMark-java.lang.String-) | Тип опознавательного знака облицовки (FIM). |
| [setFixCheckDigit(boolean value)](#setFixCheckDigit-boolean-) | Исправлять ли контрольную цифру, если она\\u2019s недействителен. |
| [setForegroundColor(String value)](#setForegroundColor-java.lang.String-) | Основной цвет штрих-кода (0x000000 - 0xFFFFFF) |
| [setPosCodeStyle(String value)](#setPosCodeStyle-java.lang.String-) | Стиль штрих-кода торговой точки (типы штрих-кода UPCA|UPCE|EAN13|EAN8). |
| [setPostalAddress(String value)](#setPostalAddress-java.lang.String-) | Почтовый адрес со штрих-кодом. |
| [setScalingFactor(String value)](#setScalingFactor-java.lang.String-) | Масштабный коэффициент для символа. |
| [setSymbolHeight(String value)](#setSymbolHeight-java.lang.String-) | Высота изображения штрих-кода (в твипах - 1/1440 дюйма) |
| [setSymbolRotation(String value)](#setSymbolRotation-java.lang.String-) | Вращение символа штрих-кода. |
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
### getAddStartStopChar() {#getAddStartStopChar--}
```
public boolean getAddStartStopChar()
```


Добавлять ли символы Start/Stop для типов штрих-кодов NW7 и CODE39.

**Возвращает:**
boolean - соответствующее логическое значение.
### getBackgroundColor() {#getBackgroundColor--}
```
public String getBackgroundColor()
```


Цвет фона штрих-кода (0x000000 - 0xFFFFFF)

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getBarcodeType() {#getBarcodeType--}
```
public String getBarcodeType()
```


Тип штрих-кода.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getBarcodeValue() {#getBarcodeValue--}
```
public String getBarcodeValue()
```


Данные для кодирования.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getCaseCodeStyle() {#getCaseCodeStyle--}
```
public String getCaseCodeStyle()
```


 Стиль кода случая для штрих-кода типа ITF14. Допустимые значения[ЗППП|EXT|ADD]

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getDisplayText() {#getDisplayText--}
```
public boolean getDisplayText()
```


Отображать ли данные штрих-кода (текст) вместе с изображением.

**Возвращает:**
boolean - соответствующее логическое значение.
### getErrorCorrectionLevel() {#getErrorCorrectionLevel--}
```
public String getErrorCorrectionLevel()
```


Уровень исправления ошибок QR-кода. Допустимые значения[0, 3].

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getFacingIdentificationMark() {#getFacingIdentificationMark--}
```
public String getFacingIdentificationMark()
```


Тип опознавательного знака облицовки (FIM).

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getFixCheckDigit() {#getFixCheckDigit--}
```
public boolean getFixCheckDigit()
```


Исправлять ли контрольную цифру, если она\\u2019s недействителен.

**Возвращает:**
boolean - соответствующее логическое значение.
### getForegroundColor() {#getForegroundColor--}
```
public String getForegroundColor()
```


Основной цвет штрих-кода (0x000000 - 0xFFFFFF)

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getPosCodeStyle() {#getPosCodeStyle--}
```
public String getPosCodeStyle()
```


Стиль штрих-кода торговой точки (типы штрих-кода UPCA|UPCE|EAN13|EAN8). The valid values (case insensitive) are [STD|SUP2|SUP5|CASE].

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getPostalAddress() {#getPostalAddress--}
```
public String getPostalAddress()
```


Почтовый адрес со штрих-кодом.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getScalingFactor() {#getScalingFactor--}
```
public String getScalingFactor()
```


 Масштабный коэффициент для символа. Значение указано в целых процентах, а допустимые значения[10, 1000].

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getSymbolHeight() {#getSymbolHeight--}
```
public String getSymbolHeight()
```


Высота изображения штрих-кода (в твипах - 1/1440 дюйма)

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getSymbolRotation() {#getSymbolRotation--}
```
public String getSymbolRotation()
```


 Вращение символа штрих-кода. Допустимые значения[0, 3].

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### isBookmark() {#isBookmark--}
```
public boolean isBookmark()
```


 Будь то[getPostalAddress()](../../com.aspose.words/barcodeparameters\#getPostalAddress--) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters\#setPostalAddress-java.lang.String-) это имя закладки.

**Возвращает:**
boolean - соответствующее логическое значение.
### isBookmark(boolean value) {#isBookmark-boolean-}
```
public void isBookmark(boolean value)
```


 Будь то[getPostalAddress()](../../com.aspose.words/barcodeparameters\#getPostalAddress--) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters\#setPostalAddress-java.lang.String-) это имя закладки.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### isUSPostalAddress() {#isUSPostalAddress--}
```
public boolean isUSPostalAddress()
```


 Будь то[getPostalAddress()](../../com.aspose.words/barcodeparameters\#getPostalAddress--) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters\#setPostalAddress-java.lang.String-) является почтовым адресом США.

**Возвращает:**
boolean - соответствующее логическое значение.
### isUSPostalAddress(boolean value) {#isUSPostalAddress-boolean-}
```
public void isUSPostalAddress(boolean value)
```


 Будь то[getPostalAddress()](../../com.aspose.words/barcodeparameters\#getPostalAddress--) / [setPostalAddress(java.lang.String)](../../com.aspose.words/barcodeparameters\#setPostalAddress-java.lang.String-) является почтовым адресом США.

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




### setAddStartStopChar(boolean value) {#setAddStartStopChar-boolean-}
```
public void setAddStartStopChar(boolean value)
```


Добавлять ли символы Start/Stop для типов штрих-кодов NW7 и CODE39.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setBackgroundColor(String value) {#setBackgroundColor-java.lang.String-}
```
public void setBackgroundColor(String value)
```


Цвет фона штрих-кода (0x000000 - 0xFFFFFF)

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setBarcodeType(String value) {#setBarcodeType-java.lang.String-}
```
public void setBarcodeType(String value)
```


Тип штрих-кода.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setBarcodeValue(String value) {#setBarcodeValue-java.lang.String-}
```
public void setBarcodeValue(String value)
```


Данные для кодирования.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setCaseCodeStyle(String value) {#setCaseCodeStyle-java.lang.String-}
```
public void setCaseCodeStyle(String value)
```


 Стиль кода случая для штрих-кода типа ITF14. Допустимые значения[ЗППП|EXT|ADD]

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setDisplayText(boolean value) {#setDisplayText-boolean-}
```
public void setDisplayText(boolean value)
```


Отображать ли данные штрих-кода (текст) вместе с изображением.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setErrorCorrectionLevel(String value) {#setErrorCorrectionLevel-java.lang.String-}
```
public void setErrorCorrectionLevel(String value)
```


Уровень исправления ошибок QR-кода. Допустимые значения[0, 3].

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setFacingIdentificationMark(String value) {#setFacingIdentificationMark-java.lang.String-}
```
public void setFacingIdentificationMark(String value)
```


Тип опознавательного знака облицовки (FIM).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setFixCheckDigit(boolean value) {#setFixCheckDigit-boolean-}
```
public void setFixCheckDigit(boolean value)
```


Исправлять ли контрольную цифру, если она\\u2019s недействителен.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setForegroundColor(String value) {#setForegroundColor-java.lang.String-}
```
public void setForegroundColor(String value)
```


Основной цвет штрих-кода (0x000000 - 0xFFFFFF)

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setPosCodeStyle(String value) {#setPosCodeStyle-java.lang.String-}
```
public void setPosCodeStyle(String value)
```


Стиль штрих-кода торговой точки (типы штрих-кода UPCA|UPCE|EAN13|EAN8). The valid values (case insensitive) are [STD|SUP2|SUP5|CASE].

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setPostalAddress(String value) {#setPostalAddress-java.lang.String-}
```
public void setPostalAddress(String value)
```


Почтовый адрес со штрих-кодом.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setScalingFactor(String value) {#setScalingFactor-java.lang.String-}
```
public void setScalingFactor(String value)
```


 Масштабный коэффициент для символа. Значение указано в целых процентах, а допустимые значения[10, 1000].

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setSymbolHeight(String value) {#setSymbolHeight-java.lang.String-}
```
public void setSymbolHeight(String value)
```


Высота изображения штрих-кода (в твипах - 1/1440 дюйма)

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setSymbolRotation(String value) {#setSymbolRotation-java.lang.String-}
```
public void setSymbolRotation(String value)
```


 Вращение символа штрих-кода. Допустимые значения[0, 3].

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

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
