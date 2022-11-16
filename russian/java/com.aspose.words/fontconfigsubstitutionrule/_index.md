---
title: FontConfigSubstitutionRule
second_title: Справочник по API Aspose.Words для Java
description: Правило подстановки конфигурации шрифта.
type: docs
weight: 276
url: /ru/java/com.aspose.words/fontconfigsubstitutionrule/
---

**Наследование:**
java.lang.Object, [com.aspose.words.FontSubstitutionRule](../../com.aspose.words/fontsubstitutionrule)
```
public class FontConfigSubstitutionRule extends FontSubstitutionRule
```

Правило подстановки конфигурации шрифта.

 Чтобы узнать больше, посетите**Working with Fonts** документальная статья.

Это правило использует утилиту fontconfig на платформах Linux (и других Unix-подобных) для получения замены, если исходный шрифт недоступен.

Если утилита fontconfig недоступна, это правило будет проигнорировано.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getEnabled()](#getEnabled--) | Указывает, включено ли правило. |
| [hashCode()](#hashCode--) |  |
| [isFontConfigAvailable()](#isFontConfigAvailable--) | Проверьте, доступна ли утилита fontconfig. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [resetCache()](#resetCache--) | Сбрасывает кэш результатов вызова fontconfig. |
| [setEnabled(boolean value)](#setEnabled-boolean-) | Указывает, включено ли правило. |
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
### getEnabled() {#getEnabled--}
```
public boolean getEnabled()
```


Указывает, включено ли правило.

**Возвращает:**
boolean - соответствующее логическое значение.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### isFontConfigAvailable() {#isFontConfigAvailable--}
```
public boolean isFontConfigAvailable()
```


Проверьте, доступна ли утилита fontconfig.

**Возвращает:**
логический
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### resetCache() {#resetCache--}
```
public void resetCache()
```


Сбрасывает кэш результатов вызова fontconfig.

### setEnabled(boolean value) {#setEnabled-boolean-}
```
public void setEnabled(boolean value)
```


Указывает, включено ли правило.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

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
