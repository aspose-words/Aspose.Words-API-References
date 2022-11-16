---
title: WarningInfo
second_title: Справочник по API Aspose.Words для Java
description: Содержит информацию о предупреждении, выданном Aspose.Words при загрузке или сохранении документа.
type: docs
weight: 604
url: /ru/java/com.aspose.words/warninginfo/
---

**Наследование:**
java.lang.Object
```
public class WarningInfo
```

Содержит информацию о предупреждении, выданном Aspose.Words при загрузке или сохранении документа.

 Чтобы узнать больше, посетите**Programming with Documents** документальная статья.

 Вы не создаете экземпляры этого класса. Объекты этого класса создаются и передаются Aspose.Words в[IWarningCallback.warning(com.aspose.words.WarningInfo)](../../com.aspose.words/iwarningcallback\#warning-com.aspose.words.WarningInfo-) метод.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getDescription()](#getDescription--) | Возвращает описание предупреждения. |
| [getSource()](#getSource--) | Возвращает источник предупреждения. |
| [getWarningType()](#getWarningType--) | Возвращает тип предупреждения. |
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
### getDescription() {#getDescription--}
```
public String getDescription()
```


Возвращает описание предупреждения.

**Возвращает:**
java.lang.String — Описание предупреждения.
### getSource() {#getSource--}
```
public int getSource()
```


Возвращает источник предупреждения.

**Возвращает:**
 int - Источник предупреждения. Возвращаемое значение является одним из[WarningSource](../../com.aspose.words/warningsource) константы.
### getWarningType() {#getWarningType--}
```
public int getWarningType()
```


Возвращает тип предупреждения.

**Возвращает:**
 int - Тип предупреждения. Возвращаемое значение представляет собой побитовую комбинацию[WarningType](../../com.aspose.words/warningtype) константы.
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
