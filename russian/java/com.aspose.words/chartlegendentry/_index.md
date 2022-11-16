---
title: ChartLegendEntry
second_title: Справочник по API Aspose.Words для Java
description: Представляет запись легенды диаграммы.
type: docs
weight: 64
url: /ru/java/com.aspose.words/chartlegendentry/
---

**Наследование:**
java.lang.Object

**Все реализованные интерфейсы:**
java.lang.Cloneable
```
public class ChartLegendEntry implements Cloneable
```

Представляет запись легенды диаграммы.

 Чтобы узнать больше, посетите**Working with Charts** документальная статья.

Запись легенды соответствует определенной серии диаграммы или линии тренда.

Текст записи представляет собой название серии или линии тренда. Текст нельзя изменить.
## Методы

| Метод | Описание |
| --- | --- |
| [clearRunAttrs()](#clearRunAttrs--) |  |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int-) |  |
| [getClass()](#getClass--) |  |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int-) |  |
| [getFont()](#getFont--) | Предоставляет доступ к форматированию шрифта этой записи легенды. |
| [hashCode()](#hashCode--) |  |
| [isHidden()](#isHidden--) | Получает значение, указывающее, скрыта ли эта запись в легенде диаграммы. |
| [isHidden(boolean value)](#isHidden-boolean-) | Задает значение, указывающее, скрыта ли эта запись в легенде диаграммы. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [removeRunAttr(int key)](#removeRunAttr-int-) |  |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object-) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clearRunAttrs() {#clearRunAttrs--}
```
public void clearRunAttrs()
```




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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
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
### getFont() {#getFont--}
```
public Font getFont()
```


Предоставляет доступ к форматированию шрифта этой записи легенды.

**Возвращает:**
[Font](../../com.aspose.words/font) - соответствующий[Font](../../com.aspose.words/font) ценность.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### isHidden() {#isHidden--}
```
public boolean isHidden()
```


Получает значение, указывающее, скрыта ли эта запись в легенде диаграммы. Значение по умолчанию**false**. Когда запись легенды диаграммы скрыта, это не влияет на соответствующий ряд диаграммы или линию тренда, которые все еще отображаются на диаграмме.

**Возвращает:**
boolean — значение, указывающее, скрыта ли эта запись в легенде диаграммы.
### isHidden(boolean value) {#isHidden-boolean-}
```
public void isHidden(boolean value)
```


 Задает значение, указывающее, скрыта ли эта запись в легенде диаграммы. Значение по умолчанию**false**. Когда запись легенды диаграммы скрыта, это не влияет на соответствующий ряд диаграммы или линию тренда, которые все еще отображаются на диаграмме.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, указывающее, скрыта ли эта запись в легенде диаграммы. |

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

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object-}
```
public void setRunAttr(int key, Object value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

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
