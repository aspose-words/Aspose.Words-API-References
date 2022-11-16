---
title: PageInfo
second_title: Справочник по API Aspose.Words для Java
description: Представляет информацию о конкретной странице документа.
type: docs
weight: 434
url: /ru/java/com.aspose.words/pageinfo/
---

**Наследование:**
java.lang.Object
```
public class PageInfo
```

Представляет информацию о конкретной странице документа.

 Чтобы узнать больше, посетите**Rendering** документальная статья.

Ширина и высота страницы, возвращаемые этим объектом, представляют «окончательный» размер страницы, например, они уже повернуты в правильную ориентацию.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getHeightInPoints()](#getHeightInPoints--) | Получает высоту страницы в пунктах. |
| [getLandscape()](#getLandscape--) | Возвращает true, если ориентация страницы, указанная в документе для этой страницы, является альбомной. |
| [getPaperSize()](#getPaperSize--) | Получает размер бумаги в виде перечисления. |
| [getPaperTray()](#getPaperTray--) | Получает лоток для бумаги (лоток) для этой страницы, как указано в документе. |
| [getSizeInPixels(float scale, float dpi)](#getSizeInPixels-float-float-) | Вычисляет размер страницы в пикселях для указанного коэффициента масштабирования и разрешения. |
| [getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)](#getSizeInPixels-float-float-float-) | Вычисляет размер страницы в пикселях для указанного коэффициента масштабирования и разрешения. |
| [getSizeInPoints()](#getSizeInPoints--) | Получает размер страницы в пунктах. |
| [getWidthInPoints()](#getWidthInPoints--) | Получает ширину страницы в пунктах. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
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
### getHeightInPoints() {#getHeightInPoints--}
```
public float getHeightInPoints()
```


Получает высоту страницы в пунктах.

**Возвращает:**
float — высота страницы в пунктах.
### getLandscape() {#getLandscape--}
```
public boolean getLandscape()
```


Возвращает true, если ориентация страницы, указанная в документе для этой страницы, является альбомной.

**Возвращает:**
boolean — Истинно, если ориентация страницы, указанная в документе для этой страницы, является альбомной.
### getPaperSize() {#getPaperSize--}
```
public int getPaperSize()
```


Получает размер бумаги в виде перечисления.

**Возвращает:**
 int - размер бумаги в виде перечисления. Возвращаемое значение является одним из[PaperSize](../../com.aspose.words/papersize) константы.
### getPaperTray() {#getPaperTray--}
```
public int getPaperTray()
```


Получает лоток для бумаги (лоток) для этой страницы, как указано в документе. Значение зависит от реализации (принтера).

**Возвращает:**
int — лоток для бумаги (лоток) для этой страницы, как указано в документе.
### getSizeInPixels(float scale, float dpi) {#getSizeInPixels-float-float-}
```
public Dimension getSizeInPixels(float scale, float dpi)
```


Вычисляет размер страницы в пикселях для указанного коэффициента масштабирования и разрешения.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| scale | float | Коэффициент масштабирования (1,0 соответствует 100%). |
| dpi | float | Разрешение (горизонтальное и вертикальное) для преобразования точек в пиксели (точек на дюйм). |

**Возвращает:**
java.awt.Dimension — размер страницы в пикселях.
### getSizeInPixels(float scale, float horizontalDpi, float verticalDpi) {#getSizeInPixels-float-float-float-}
```
public Dimension getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)
```


Вычисляет размер страницы в пикселях для указанного коэффициента масштабирования и разрешения.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| scale | float | Коэффициент масштабирования (1,0 соответствует 100%). |
| horizontalDpi | float | Горизонтальное разрешение для преобразования точек в пиксели (точек на дюйм). |
| verticalDpi | float | Вертикальное разрешение для преобразования точек в пиксели (точек на дюйм). |

**Возвращает:**
java.awt.Dimension — размер страницы в пикселях.
### getSizeInPoints() {#getSizeInPoints--}
```
public Point2D.Float getSizeInPoints()
```


Получает размер страницы в пунктах.

**Возвращает:**
java.awt.geom.Point2D.Float — размер страницы в пунктах.
### getWidthInPoints() {#getWidthInPoints--}
```
public float getWidthInPoints()
```


Получает ширину страницы в пунктах.

**Возвращает:**
float — ширина страницы в пунктах.
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
