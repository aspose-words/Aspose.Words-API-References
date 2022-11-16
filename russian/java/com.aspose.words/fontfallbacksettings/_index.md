---
title: FontFallbackSettings
second_title: Справочник по API Aspose.Words для Java
description: Задает настройки резервного механизма шрифта.
type: docs
weight: 277
url: /ru/java/com.aspose.words/fontfallbacksettings/
---

**Наследование:**
java.lang.Object
```
public class FontFallbackSettings
```

Задает настройки резервного механизма шрифта.

 Чтобы узнать больше, посетите**Working with Fonts** документальная статья.

По умолчанию резервные настройки инициализируются предопределенными настройками, имитирующими резервные настройки Microsoft Word.
## Методы

| Метод | Описание |
| --- | --- |
| [buildAutomatic()](#buildAutomatic--) | Автоматически создает резервные настройки, сканируя доступные шрифты. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [hashCode()](#hashCode--) |  |
| [load(InputStream stream)](#load-java.io.InputStream-) |  |
| [load(String fileName)](#load-java.lang.String-) | Загружает резервные настройки шрифта из XML-файла. |
| [loadMsOfficeFallbackSettings()](#loadMsOfficeFallbackSettings--) | Загружает предопределенные резервные параметры, которые имитируют резервный вариант Microsoft Word и используют офисные шрифты Microsoft. |
| [loadNotoFallbackSettings()](#loadNotoFallbackSettings--) | Загружает предопределенные резервные настройки, в которых используются шрифты Google Noto. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [save(OutputStream outputStream)](#save-java.io.OutputStream-) |  |
| [save(String fileName)](#save-java.lang.String-) | Сохраняет текущие резервные настройки в файл. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### buildAutomatic() {#buildAutomatic--}
```
public void buildAutomatic()
```


 Автоматически создает резервные настройки, сканируя доступные шрифты. Этот метод может привести к неоптимальным резервным настройкам. Шрифты проверяются[ Unicode Character Range ][Unicode Character Range] полей, а не по фактическому наличию глифов. Также диапазоны Unicode проверяются индивидуально, и несколько диапазонов, относящихся к одному языку/сценарию, могут использовать разные резервные шрифты.


[Unicode Character Range]: https://docs.microsoft.com/en-us/typography/opentype/spec/os2#ur

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
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Возвращает:**
инт
### load(InputStream stream) {#load-java.io.InputStream-}
```
public void load(InputStream stream)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| stream | java.io.InputStream |  |

### load(String fileName) {#load-java.lang.String-}
```
public void load(String fileName)
```


Загружает резервные настройки шрифта из XML-файла.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String | Введите имя файла. |

### loadMsOfficeFallbackSettings() {#loadMsOfficeFallbackSettings--}
```
public void loadMsOfficeFallbackSettings()
```


Загружает предопределенные резервные параметры, которые имитируют резервный вариант Microsoft Word и используют офисные шрифты Microsoft.

### loadNotoFallbackSettings() {#loadNotoFallbackSettings--}
```
public void loadNotoFallbackSettings()
```


Загружает предопределенные резервные настройки, в которых используются шрифты Google Noto.

### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### save(OutputStream outputStream) {#save-java.io.OutputStream-}
```
public void save(OutputStream outputStream)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| outputStream | java.io.OutputStream |  |

### save(String fileName) {#save-java.lang.String-}
```
public void save(String fileName)
```


Сохраняет текущие резервные настройки в файл.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String | Имя выходного файла. |

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
