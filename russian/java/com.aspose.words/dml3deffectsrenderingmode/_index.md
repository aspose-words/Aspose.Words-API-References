---
title: Dml3DEffectsRenderingMode
second_title: Справочник по API Aspose.Words для Java
description: Указывает, как визуализируются эффекты 3D-формы.
type: docs
weight: 116
url: /ru/java/com.aspose.words/dml3deffectsrenderingmode/
---

**Наследование:**
java.lang.Object
```
public class Dml3DEffectsRenderingMode
```

Указывает, как визуализируются эффекты 3D-формы.
## Поля

| Поле | Описание |
| --- | --- |
| [ADVANCED](#ADVANCED) | Рендеринг расширенного списка специальных эффектов, включая расширенные 3D-эффекты, такие как фаска, освещение и материалы. |
| [BASIC](#BASIC) | Легкий и стабильный рендеринг, основанный на внутреннем движке, но расширенные эффекты, такие как освещение, материалы и другие дополнительные эффекты, не отображаются при использовании этого режима. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String dml3DEffectsRenderingModeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int dml3DEffectsRenderingMode)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int dml3DEffectsRenderingMode)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### ADVANCED {#ADVANCED}
```
public static int ADVANCED
```


 Рендеринг расширенного списка специальных эффектов, включая расширенные 3D-эффекты, такие как фаска, освещение и материалы. Текущая реализация использует OpenGL. Перед использованием убедитесь, что в вашей системе установлена библиотека OpenGL версии 1.1 или выше. Этот режим все еще находится в разработке, и некоторые вещи могут не поддерживаться, поэтому рекомендуется использовать[BASIC](../../com.aspose.words/dml3deffectsrenderingmode\#BASIC) режим, если результат рендеринга неприемлем. Подробности смотрите в документации.

### BASIC {#BASIC}
```
public static int BASIC
```


Легкий и стабильный рендеринг, основанный на внутреннем движке, но расширенные эффекты, такие как освещение, материалы и другие дополнительные эффекты, не отображаются при использовании этого режима. Подробности смотрите в документации.

### length {#length}
```
public static int length
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
### fromName(String dml3DEffectsRenderingModeName) {#fromName-java.lang.String-}
```
public static int fromName(String dml3DEffectsRenderingModeName)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| dml3DEffectsRenderingModeName | java.lang.String |  |

**Возвращает:**
инт
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getName(int dml3DEffectsRenderingMode) {#getName-int-}
```
public static String getName(int dml3DEffectsRenderingMode)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| dml3DEffectsRenderingMode | int |  |

**Возвращает:**
java.lang.String
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Возвращает:**
инт[]
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
### toString(int dml3DEffectsRenderingMode) {#toString-int-}
```
public static String toString(int dml3DEffectsRenderingMode)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| dml3DEffectsRenderingMode | int |  |

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
