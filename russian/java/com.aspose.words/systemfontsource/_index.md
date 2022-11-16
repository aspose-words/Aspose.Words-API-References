---
title: SystemFontSource
second_title: Справочник по API Aspose.Words для Java
description: Представляет все шрифты TrueType, установленные в системе.
type: docs
weight: 543
url: /ru/java/com.aspose.words/systemfontsource/
---

**Наследование:**
java.lang.Object, [com.aspose.words.FontSourceBase](../../com.aspose.words/fontsourcebase)
```
public class SystemFontSource extends FontSourceBase
```

Представляет все шрифты TrueType, установленные в системе.

 Чтобы узнать больше, посетите**Working with Fonts** документальная статья.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [SystemFontSource()](#SystemFontSource--) | Стор. |
| [SystemFontSource(int priority)](#SystemFontSource-int-) | Стор. |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAvailableFonts()](#getAvailableFonts--) | Возвращает список шрифтов, доступных через этот источник. |
| [getClass()](#getClass--) |  |
| [getFontDataInternal()](#getFontDataInternal--) |  |
| [getPriority()](#getPriority--) | Возвращает приоритет источника шрифта. |
| [getPriorityInternal()](#getPriorityInternal--) |  |
| [getSystemFontFolders()](#getSystemFontFolders--) | Возвращает папки системных шрифтов или пустой массив, если папки недоступны. |
| [getType()](#getType--) | Возвращает тип источника шрифта. |
| [getWarningCallback()](#getWarningCallback--) | Вызывается во время обработки источника шрифта при обнаружении проблемы, которая может привести к потере точности форматирования. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback-) | Вызывается во время обработки источника шрифта при обнаружении проблемы, которая может привести к потере точности форматирования. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### SystemFontSource() {#SystemFontSource--}
```
public SystemFontSource()
```


Стор.

### SystemFontSource(int priority) {#SystemFontSource-int-}
```
public SystemFontSource(int priority)
```


Стор.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| priority | int |  Приоритет источника шрифта. См.[FontSourceBase.getPriority()](../../com.aspose.words/fontsourcebase\#getPriority--) описание свойства для получения дополнительной информации. |

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
### getAvailableFonts() {#getAvailableFonts--}
```
public ArrayList getAvailableFonts()
```


Возвращает список шрифтов, доступных через этот источник.

**Возвращает:**
java.util.ArrayList
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getFontDataInternal() {#getFontDataInternal--}
```
public Iterable getFontDataInternal()
```




**Возвращает:**
java.lang.Iterable
### getPriority() {#getPriority--}
```
public int getPriority()
```


Возвращает приоритет источника шрифта.

Это значение используется при наличии шрифтов с одинаковым именем семейства и стилем в разных источниках шрифтов. В этом случае Aspose.Words выбирает шрифт из источника с более высоким значением приоритета.

Значение по умолчанию — 0.

**Возвращает:**
int - приоритет источника шрифта.
### getPriorityInternal() {#getPriorityInternal--}
```
public int getPriorityInternal()
```




**Возвращает:**
инт
### getSystemFontFolders() {#getSystemFontFolders--}
```
public static String[] getSystemFontFolders()
```


Возвращает папки системных шрифтов или пустой массив, если папки недоступны. На некоторых платформах Aspose.Words мог искать системные шрифты не только в папках, но и в других источниках. Например, на платформе Windows Aspose.Words ищет шрифты также в реестре.

**Возвращает:**
java.lang.String[]
### getType() {#getType--}
```
public int getType()
```


Возвращает тип источника шрифта.

**Возвращает:**
 int - Тип источника шрифта. Возвращаемое значение является одним из[FontSourceType](../../com.aspose.words/fontsourcetype) константы.
### getWarningCallback() {#getWarningCallback--}
```
public IWarningCallback getWarningCallback()
```


Вызывается во время обработки источника шрифта при обнаружении проблемы, которая может привести к потере точности форматирования.

**Возвращает:**
[IWarningCallback](../../com.aspose.words/iwarningcallback) - соответствующий[IWarningCallback](../../com.aspose.words/iwarningcallback) ценность.
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




### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback-}
```
public void setWarningCallback(IWarningCallback value)
```


Вызывается во время обработки источника шрифта при обнаружении проблемы, которая может привести к потере точности форматирования.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [IWarningCallback](../../com.aspose.words/iwarningcallback) |  Соответствующий[IWarningCallback](../../com.aspose.words/iwarningcallback) ценность. |

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
