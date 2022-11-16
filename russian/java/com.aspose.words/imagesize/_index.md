---
title: ImageSize
second_title: Справочник по API Aspose.Words для Java
description: Содержит информацию о размере и разрешении изображения.
type: docs
weight: 342
url: /ru/java/com.aspose.words/imagesize/
---

**Наследование:**
java.lang.Object
```
public class ImageSize
```

Содержит информацию о размере и разрешении изображения.

 Чтобы узнать больше, посетите**Working with Images** документальная статья.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [ImageSize(int widthPixels, int heightPixels)](#ImageSize-int-int-) | Инициализирует ширину и высоту заданными значениями в пикселях. |
| [ImageSize(int widthPixels, int heightPixels, double horizontalResolution, double verticalResolution)](#ImageSize-int-int-double-double-) | Инициализирует ширину, высоту и разрешение заданными значениями. |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getHeightPixels()](#getHeightPixels--) | Получает высоту изображения в пикселях. |
| [getHeightPoints()](#getHeightPoints--) | Получает высоту изображения в точках. |
| [getHorizontalResolution()](#getHorizontalResolution--) | Получает горизонтальное разрешение в DPI. |
| [getVerticalResolution()](#getVerticalResolution--) | Получает вертикальное разрешение в DPI. |
| [getWidthPixels()](#getWidthPixels--) | Получает ширину изображения в пикселях. |
| [getWidthPoints()](#getWidthPoints--) | Получает ширину изображения в пунктах. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### ImageSize(int widthPixels, int heightPixels) {#ImageSize-int-int-}
```
public ImageSize(int widthPixels, int heightPixels)
```


Инициализирует ширину и высоту заданными значениями в пикселях. Инициализирует разрешение до 96 dpi.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| widthPixels | int | Ширина в пикселях. |
| heightPixels | int | Высота в пикселях. |

### ImageSize(int widthPixels, int heightPixels, double horizontalResolution, double verticalResolution) {#ImageSize-int-int-double-double-}
```
public ImageSize(int widthPixels, int heightPixels, double horizontalResolution, double verticalResolution)
```


Инициализирует ширину, высоту и разрешение заданными значениями.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| widthPixels | int | Ширина в пикселях. |
| heightPixels | int | Высота в пикселях. |
| horizontalResolution | double | Горизонтальное разрешение в DPI. |
| verticalResolution | double | Вертикальное разрешение в DPI. |

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
### getHeightPixels() {#getHeightPixels--}
```
public int getHeightPixels()
```


Получает высоту изображения в пикселях.

**Возвращает:**
int — высота изображения в пикселях.
### getHeightPoints() {#getHeightPoints--}
```
public double getHeightPoints()
```


Получает высоту изображения в точках. 1 пункт равен 1/72 дюйма.

**Возвращает:**
double - Высота изображения в пунктах.
### getHorizontalResolution() {#getHorizontalResolution--}
```
public double getHorizontalResolution()
```


Получает горизонтальное разрешение в DPI.

**Возвращает:**
double - горизонтальное разрешение в DPI.
### getVerticalResolution() {#getVerticalResolution--}
```
public double getVerticalResolution()
```


Получает вертикальное разрешение в DPI.

**Возвращает:**
double - Вертикальное разрешение в DPI.
### getWidthPixels() {#getWidthPixels--}
```
public int getWidthPixels()
```


Получает ширину изображения в пикселях.

**Возвращает:**
int — ширина изображения в пикселях.
### getWidthPoints() {#getWidthPoints--}
```
public double getWidthPoints()
```


Получает ширину изображения в пунктах. 1 пункт равен 1/72 дюйма.

**Возвращает:**
double - Ширина изображения в пунктах.
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
