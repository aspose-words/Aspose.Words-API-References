---
title: GraphicsQualityOptions
second_title: Справочник по API Aspose.Words для Java
description: Позволяет указать доп.
type: docs
weight: 313
url: /ru/java/com.aspose.words/graphicsqualityoptions/
---

**Наследование:**
java.lang.Object
```
public class GraphicsQualityOptions
```

Позволяет указать доп.

 Чтобы узнать больше, посетите**Save a Document** документальная статья.

Получает текущий для просмотра или добавления новых подсказок. Перезаписывает текущий .
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getRenderingHints()](#getRenderingHints--) |  |
| [getUseTileFlipMode()](#getUseTileFlipMode--) | Получает флаг, указывающий, является ли WrapMode TileFlipXY. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setRenderingHints(RenderingHints renderingHints)](#setRenderingHints-java.awt.RenderingHints-) |  |
| [setUseTileFlipMode(boolean value)](#setUseTileFlipMode-boolean-) | Устанавливает флаг, указывающий, является ли WrapMode TileFlipXY. |
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
### getRenderingHints() {#getRenderingHints--}
```
public RenderingHints getRenderingHints()
```




**Возвращает:**
java.awt.RenderingHints
### getUseTileFlipMode() {#getUseTileFlipMode--}
```
public boolean getUseTileFlipMode()
```


Получает флаг, указывающий, является ли WrapMode TileFlipXY.

WrapMode указывает, как текстура или градиент укладываются мозаикой, когда они меньше, чем заполняемая область.

По умолчанию использует WrapMode\#TILE.TILE (указывает мозаику без отражения). Это вызывает неточную визуализацию масштабированного изображения (с высоким разрешением).

Это свойство позволяет переключить WrapMode на WrapMode.\#КАФЕЛЬНАЯ ПЛИТКА\_КУВЫРОК\_XY.TILE\_КУВЫРОК\_XY (указывает, что плитки переворачиваются по горизонтали при перемещении по строке и переворачиваются по вертикали при перемещении по столбцу).

**Возвращает:**
boolean — Флаг, указывающий, является ли WrapMode TileFlipXY.
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




### setRenderingHints(RenderingHints renderingHints) {#setRenderingHints-java.awt.RenderingHints-}
```
public void setRenderingHints(RenderingHints renderingHints)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| renderingHints | java.awt.RenderingHints |  |

### setUseTileFlipMode(boolean value) {#setUseTileFlipMode-boolean-}
```
public void setUseTileFlipMode(boolean value)
```


Устанавливает флаг, указывающий, является ли WrapMode TileFlipXY.

WrapMode указывает, как текстура или градиент укладываются мозаикой, когда они меньше, чем заполняемая область.

По умолчанию использует WrapMode\#TILE.TILE (указывает мозаику без отражения). Это вызывает неточную визуализацию масштабированного изображения (с высоким разрешением).

Это свойство позволяет переключить WrapMode на WrapMode.\#КАФЕЛЬНАЯ ПЛИТКА\_КУВЫРОК\_XY.TILE\_КУВЫРОК\_XY (указывает, что плитки переворачиваются по горизонтали при перемещении по строке и переворачиваются по вертикали при перемещении по столбцу).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Флаг, указывающий, является ли WrapMode TileFlipXY. |

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
