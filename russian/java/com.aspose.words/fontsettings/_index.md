---
title: FontSettings
second_title: Справочник по API Aspose.Words для Java
description: Задает настройки шрифта для документа.
type: docs
weight: 286
url: /ru/java/com.aspose.words/fontsettings/
---

**Наследование:**
java.lang.Object
```
public class FontSettings
```

Задает настройки шрифта для документа.

 Чтобы узнать больше, посетите**Working with Fonts** документальная статья.

 Aspose.Words использует настройки шрифта для разрешения шрифтов в документе. Шрифты разрешаются в основном при создании макета документа или рендеринга в фиксированные форматы страниц. Но при загрузке некоторых форматов Aspose.Words также может потребовать разрешения шрифтов. Например, при загрузке HTML-документов Aspose.Words может разрешить шрифты для выполнения резервного шрифта. Поэтому рекомендуется установить настройки шрифта в[LoadOptions](../../com.aspose.words/loadoptions)при загрузке документа. Или, по крайней мере, перед созданием макета или рендерингом документа в формате фиксированной страницы.

 По умолчанию во всех документах используется один экземпляр настроек статического шрифта. Доступ к нему мог получить[getDefaultInstance()](../../com.aspose.words/fontsettings\#getDefaultInstance--) имущество.

Изменение настроек шрифта безопасно в любое время из любой темы. Но рекомендуется не изменять настройки шрифта при обработке некоторых документов, использующих эти настройки. Это может привести к тому, что один и тот же шрифт будет по-разному разрешаться в разных частях документа.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [FontSettings()](#FontSettings--) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getDefaultInstance()](#getDefaultInstance--) | Статические настройки шрифта по умолчанию. |
| [getFallbackSettings()](#getFallbackSettings--) | Настройки, связанные с резервным механизмом шрифта. |
| [getFontsSources()](#getFontsSources--) | Получает копию массива, содержащего список источников, в которых Aspose.Words ищет шрифты TrueType. |
| [getSubstitutionSettings()](#getSubstitutionSettings--) | Настройки, связанные с механизмом замены шрифтов. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [resetFontSources()](#resetFontSources--) | Сбрасывает источники шрифтов к системным значениям по умолчанию. |
| [saveSearchCache(OutputStream outputStream)](#saveSearchCache-java.io.OutputStream-) |  |
| [setFontsFolder(String fontFolder, boolean recursive)](#setFontsFolder-java.lang.String-boolean-) | Устанавливает папку, в которой Aspose.Words ищет шрифты TrueType при рендеринге документов или встраивании шрифтов. |
| [setFontsFolders(String[] fontsFolders, boolean recursive)](#setFontsFolders-java.lang.String---boolean-) | Задает папки, в которых Aspose.Words ищет шрифты TrueType при рендеринге документов или встраивании шрифтов. |
| [setFontsSources(FontSourceBase[] sources)](#setFontsSources-com.aspose.words.FontSourceBase---) | Задает источники, в которых Aspose.Words ищет шрифты TrueType при рендеринге документов или встраивании шрифтов. |
| [setFontsSources(FontSourceBase[] sources, InputStream cacheInputStream)](#setFontsSources-com.aspose.words.FontSourceBase---java.io.InputStream-) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### FontSettings() {#FontSettings--}
```
public FontSettings()
```


Инициализирует новый экземпляр этого класса.

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
### getDefaultInstance() {#getDefaultInstance--}
```
public static FontSettings getDefaultInstance()
```


 Статические настройки шрифта по умолчанию. Этот экземпляр используется по умолчанию в документе, если[Document.getFontSettings()](../../com.aspose.words/document\#getFontSettings--) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document\#setFontSettings-com.aspose.words.FontSettings-) указано.

**Возвращает:**
[FontSettings](../../com.aspose.words/fontsettings) - соответствующий[FontSettings](../../com.aspose.words/fontsettings) ценность.
### getFallbackSettings() {#getFallbackSettings--}
```
public FontFallbackSettings getFallbackSettings()
```


Настройки, связанные с резервным механизмом шрифта.

**Возвращает:**
[FontFallbackSettings](../../com.aspose.words/fontfallbacksettings) - соответствующий[FontFallbackSettings](../../com.aspose.words/fontfallbacksettings) ценность.
### getFontsSources() {#getFontsSources--}
```
public FontSourceBase[] getFontsSources()
```


Получает копию массива, содержащего список источников, в которых Aspose.Words ищет шрифты TrueType.

 Возвращаемое значение является копией данных, которые использует Aspose.Words. Если вы измените записи в возвращаемом массиве, это не повлияет на визуализацию документа. Чтобы указать новые источники шрифтов, используйте[setFontsSources(com.aspose.words.FontSourceBase[])](../../com.aspose.words/fontsettings\#setFontsSources-com.aspose.words.FontSourceBase---) метод.

**Возвращает:**
com.aspose.words.FontSourceBase[] - Копия текущих источников шрифтов.
### getSubstitutionSettings() {#getSubstitutionSettings--}
```
public FontSubstitutionSettings getSubstitutionSettings()
```


Настройки, связанные с механизмом замены шрифтов.

**Возвращает:**
[FontSubstitutionSettings](../../com.aspose.words/fontsubstitutionsettings) - соответствующий[FontSubstitutionSettings](../../com.aspose.words/fontsubstitutionsettings) ценность.
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




### resetFontSources() {#resetFontSources--}
```
public void resetFontSources()
```


Сбрасывает источники шрифтов к системным значениям по умолчанию.

### saveSearchCache(OutputStream outputStream) {#saveSearchCache-java.io.OutputStream-}
```
public void saveSearchCache(OutputStream outputStream)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| outputStream | java.io.OutputStream |  |

### setFontsFolder(String fontFolder, boolean recursive) {#setFontsFolder-java.lang.String-boolean-}
```
public void setFontsFolder(String fontFolder, boolean recursive)
```


 Устанавливает папку, в которой Aspose.Words ищет шрифты TrueType при рендеринге документов или встраивании шрифтов. Это ярлык для[setFontsFolders(java.lang.String[], boolean)](../../com.aspose.words/fontsettings\#setFontsFolders-java.lang.String----boolean-) для установки только одного каталога шрифтов.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fontFolder | java.lang.String | Папка, содержащая шрифты TrueType. |
| recursive | boolean | Значение true для рекурсивного сканирования указанных папок на наличие шрифтов. |

### setFontsFolders(String[] fontsFolders, boolean recursive) {#setFontsFolders-java.lang.String---boolean-}
```
public void setFontsFolders(String[] fontsFolders, boolean recursive)
```


Задает папки, в которых Aspose.Words ищет шрифты TrueType при рендеринге документов или встраивании шрифтов.

По умолчанию Aspose.Words ищет шрифты, установленные в системе.

Установка этого свойства сбрасывает кеш всех ранее загруженных шрифтов.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fontsFolders | java.lang.String[] | Массив папок, содержащих шрифты TrueType. |
| recursive | boolean | Значение true для рекурсивного сканирования указанных папок на наличие шрифтов. |

### setFontsSources(FontSourceBase[] sources) {#setFontsSources-com.aspose.words.FontSourceBase---}
```
public void setFontsSources(FontSourceBase[] sources)
```


Задает источники, в которых Aspose.Words ищет шрифты TrueType при рендеринге документов или встраивании шрифтов.

По умолчанию Aspose.Words ищет шрифты, установленные в системе.

Установка этого свойства сбрасывает кеш всех ранее загруженных шрифтов.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| sources | [FontSourceBase\[\]](../../com.aspose.words/fontsourcebase) | Массив источников, содержащих шрифты TrueType. |

### setFontsSources(FontSourceBase[] sources, InputStream cacheInputStream) {#setFontsSources-com.aspose.words.FontSourceBase---java.io.InputStream-}
```
public void setFontsSources(FontSourceBase[] sources, InputStream cacheInputStream)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| sources | [FontSourceBase\[\]](../../com.aspose.words/fontsourcebase) |  |
| cacheInputStream | java.io.InputStream |  |

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
