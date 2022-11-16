---
title: TableSubstitutionRule
second_title: Справочник по API Aspose.Words для Java
description: Правило подстановки табличного шрифта.
type: docs
weight: 554
url: /ru/java/com.aspose.words/tablesubstitutionrule/
---

**Наследование:**
java.lang.Object, [com.aspose.words.FontSubstitutionRule](../../com.aspose.words/fontsubstitutionrule)
```
public class TableSubstitutionRule extends FontSubstitutionRule
```

Правило подстановки табличного шрифта.

 Чтобы узнать больше, посетите**Working with Fonts** документальная статья.

 Это правило определяет список замещающих имен шрифтов, которые будут использоваться, если исходный шрифт недоступен. Заменители будут проверяться на имя шрифта и[FontInfo.getAltName()](../../com.aspose.words/fontinfo\#getAltName--) / [FontInfo.setAltName(java.lang.String)](../../com.aspose.words/fontinfo\#setAltName-java.lang.String-) (если есть).
## Методы

| Метод | Описание |
| --- | --- |
| [addSubstitutes(String originalFontName, String[] substituteFontNames)](#addSubstitutes-java.lang.String-java.lang.String...-) | Добавляет замещающие имена шрифтов для заданного исходного имени шрифта. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getEnabled()](#getEnabled--) | Указывает, включено ли правило. |
| [getSubstitutes(String originalFontName)](#getSubstitutes-java.lang.String-) | Возвращает массив, содержащий замещающие имена шрифтов для указанного исходного имени шрифта. |
| [hashCode()](#hashCode--) |  |
| [load(InputStream stream)](#load-java.io.InputStream-) |  |
| [load(String fileName)](#load-java.lang.String-) | Загружает настройки подстановки таблиц из XML-файла. |
| [loadAndroidSettings()](#loadAndroidSettings--) | Загружает предопределенные параметры подстановки таблиц для платформы Linux. |
| [loadLinuxSettings()](#loadLinuxSettings--) | Загружает предопределенные параметры подстановки таблиц для платформы Linux. |
| [loadWindowsSettings()](#loadWindowsSettings--) | Загружает предопределенные параметры подстановки таблиц для платформы Windows. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [save(OutputStream outputStream)](#save-java.io.OutputStream-) |  |
| [save(String fileName)](#save-java.lang.String-) | Сохраняет текущие настройки подстановки таблиц в файл. |
| [setEnabled(boolean value)](#setEnabled-boolean-) | Указывает, включено ли правило. |
| [setSubstitutes(String originalFontName, String[] substituteFontNames)](#setSubstitutes-java.lang.String-java.lang.String...-) | Переопределить замещающие имена шрифтов для заданного исходного имени шрифта. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### addSubstitutes(String originalFontName, String[] substituteFontNames) {#addSubstitutes-java.lang.String-java.lang.String...-}
```
public void addSubstitutes(String originalFontName, String[] substituteFontNames)
```


Добавляет замещающие имена шрифтов для заданного исходного имени шрифта.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| originalFontName | java.lang.String | Оригинальное название шрифта. |
| substituteFontNames | java.lang.String[] | Список альтернативных названий шрифтов. |

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
### getSubstitutes(String originalFontName) {#getSubstitutes-java.lang.String-}
```
public Iterable getSubstitutes(String originalFontName)
```


Возвращает массив, содержащий замещающие имена шрифтов для указанного исходного имени шрифта.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| originalFontName | java.lang.String | Оригинальное название шрифта. |

**Возвращает:**
java.lang.Iterable — Список альтернативных имен шрифтов.
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


Загружает настройки подстановки таблиц из XML-файла.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String | Введите имя файла. |

### loadAndroidSettings() {#loadAndroidSettings--}
```
public void loadAndroidSettings()
```


Загружает предопределенные параметры подстановки таблиц для платформы Linux.

### loadLinuxSettings() {#loadLinuxSettings--}
```
public void loadLinuxSettings()
```


Загружает предопределенные параметры подстановки таблиц для платформы Linux.

### loadWindowsSettings() {#loadWindowsSettings--}
```
public void loadWindowsSettings()
```


Загружает предопределенные параметры подстановки таблиц для платформы Windows.

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


Сохраняет текущие настройки подстановки таблиц в файл.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String | Имя выходного файла. |

### setEnabled(boolean value) {#setEnabled-boolean-}
```
public void setEnabled(boolean value)
```


Указывает, включено ли правило.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setSubstitutes(String originalFontName, String[] substituteFontNames) {#setSubstitutes-java.lang.String-java.lang.String...-}
```
public void setSubstitutes(String originalFontName, String[] substituteFontNames)
```


Переопределить замещающие имена шрифтов для заданного исходного имени шрифта.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| originalFontName | java.lang.String | Оригинальное название шрифта. |
| substituteFontNames | java.lang.String[] | Список альтернативных названий шрифтов. |

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
