---
title: FolderFontSource
second_title: Справочник по API Aspose.Words для Java
description: Представляет папку, содержащую файлы шрифтов TrueType.
type: docs
weight: 274
url: /ru/java/com.aspose.words/folderfontsource/
---

**Наследование:**
java.lang.Object, [com.aspose.words.FontSourceBase](../../com.aspose.words/fontsourcebase)
```
public class FolderFontSource extends FontSourceBase
```

Представляет папку, содержащую файлы шрифтов TrueType.

 Чтобы узнать больше, посетите**Working with Fonts** документальная статья.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [FolderFontSource(String folderPath, boolean scanSubfolders)](#FolderFontSource-java.lang.String-boolean-) | Стор. |
| [FolderFontSource(String folderPath, boolean scanSubfolders, int priority)](#FolderFontSource-java.lang.String-boolean-int-) | Стор. |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAvailableFonts()](#getAvailableFonts--) | Возвращает список шрифтов, доступных через этот источник. |
| [getClass()](#getClass--) |  |
| [getFolderPath()](#getFolderPath--) | Путь к папке. |
| [getFontDataInternal()](#getFontDataInternal--) |  |
| [getPriority()](#getPriority--) | Возвращает приоритет источника шрифта. |
| [getPriorityInternal()](#getPriorityInternal--) |  |
| [getScanSubfolders()](#getScanSubfolders--) | Определяет, сканировать ли вложенные папки. |
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
### FolderFontSource(String folderPath, boolean scanSubfolders) {#FolderFontSource-java.lang.String-boolean-}
```
public FolderFontSource(String folderPath, boolean scanSubfolders)
```


Стор.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| folderPath | java.lang.String | Путь к папке. |
| scanSubfolders | boolean | Определяет, сканировать ли вложенные папки. |

### FolderFontSource(String folderPath, boolean scanSubfolders, int priority) {#FolderFontSource-java.lang.String-boolean-int-}
```
public FolderFontSource(String folderPath, boolean scanSubfolders, int priority)
```


Стор.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| folderPath | java.lang.String | Путь к папке. |
| scanSubfolders | boolean | Определяет, сканировать ли вложенные папки. |
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
### getFolderPath() {#getFolderPath--}
```
public String getFolderPath()
```


Путь к папке.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
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
### getScanSubfolders() {#getScanSubfolders--}
```
public boolean getScanSubfolders()
```


Определяет, сканировать ли вложенные папки.

**Возвращает:**
boolean - соответствующее логическое значение.
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
