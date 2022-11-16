---
title: PdfLoadOptions
second_title: Справочник по API Aspose.Words для Java
description: Позволяет указать дополнительные параметры при загрузке документа Pdf в объект.
type: docs
weight: 458
url: /ru/java/com.aspose.words/pdfloadoptions/
---

**Наследование:**
java.lang.Object, [com.aspose.words.LoadOptions](../../com.aspose.words/loadoptions)
```
public class PdfLoadOptions extends LoadOptions
```

 Позволяет указать дополнительные параметры при загрузке документа Pdf в[Document](../../com.aspose.words/document) объект.

 Чтобы узнать больше, посетите**Specify Load Options** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBaseUri()](#getBaseUri--) | Получает строку, которая будет использоваться для преобразования относительных URI, найденных в документе, в абсолютные URI, когда это необходимо. |
| [getClass()](#getClass--) |  |
| [getConvertMetafilesToPng()](#getConvertMetafilesToPng--) |  Получает, следует ли преобразовывать метафайл (**F:Aspose.FileFormat.Wmf** или же**F:Aspose.FileFormat.Emf** ) изображения в**F:Aspose.FileFormat.Png** формат изображения. |
| [getConvertShapeToOfficeMath()](#getConvertShapeToOfficeMath--) | Определяет, следует ли преобразовывать фигуры с помощью EquationXML в объекты Office Math. |
| [getEncoding()](#getEncoding--) | Получает кодировку, которая будет использоваться для загрузки документа HTML, TXT или CHM, если кодировка не указана внутри документа. |
| [getFontSettings()](#getFontSettings--) | Позволяет указать настройки шрифта документа. |
| [getLanguagePreferences()](#getLanguagePreferences--) | Получает языковые настройки, которые будут использоваться при загрузке документа. |
| [getLoadFormat()](#getLoadFormat--) | Задает формат загружаемого документа. |
| [getMswVersion()](#getMswVersion--) | Позволяет указать, что процесс загрузки документа должен соответствовать конкретной версии MS Word. |
| [getPageCount()](#getPageCount--) | Получает количество страниц для чтения. |
| [getPageIndex()](#getPageIndex--) | Получает отсчитываемый от 0 индекс первой страницы для чтения. |
| [getPassword()](#getPassword--) | Получает пароль для открытия зашифрованного документа. |
| [getPreserveIncludePictureField()](#getPreserveIncludePictureField--) | Определяет, следует ли сохранять поле INCLUDEPICTURE при чтении форматов Microsoft Word. |
| [getProgressCallback()](#getProgressCallback--) | Вызывается во время загрузки документа и принимает данные о ходе загрузки. |
| [getResourceLoadingCallback()](#getResourceLoadingCallback--) | Позволяет управлять загрузкой внешних ресурсов (изображений, таблиц стилей) при импорте документа из HTML, MHTML. |
| [getSkipPdfImages()](#getSkipPdfImages--) | Получает флаг, указывающий, нужно ли пропускать изображения при загрузке документа PDF. |
| [getTempFolder()](#getTempFolder--) | Позволяет использовать временные файлы при чтении документа. |
| [getUpdateDirtyFields()](#getUpdateDirtyFields--) | Указывает, следует ли обновлять поля с грязным атрибутом. |
| [getWarningCallback()](#getWarningCallback--) | Вызывается во время операции загрузки при обнаружении проблемы, которая может привести к потере точности данных или форматирования. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setBaseUri(String value)](#setBaseUri-java.lang.String-) | Задает строку, которая будет использоваться для преобразования относительных URI, найденных в документе, в абсолютные URI, когда это необходимо. |
| [setConvertMetafilesToPng(boolean value)](#setConvertMetafilesToPng-boolean-) |  Устанавливает, следует ли преобразовывать метафайл (**F:Aspose.FileFormat.Wmf** или же**F:Aspose.FileFormat.Emf** ) изображения в**F:Aspose.FileFormat.Png** формат изображения. |
| [setConvertShapeToOfficeMath(boolean value)](#setConvertShapeToOfficeMath-boolean-) | Устанавливает, следует ли преобразовывать фигуры с EquationXML в объекты Office Math. |
| [setEncoding(Charset value)](#setEncoding-java.nio.charset.Charset-) | Задает кодировку, которая будет использоваться для загрузки документа HTML, TXT или CHM, если кодировка не указана внутри документа. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings-) | Позволяет указать настройки шрифта документа. |
| [setLoadFormat(int value)](#setLoadFormat-int-) | Задает формат загружаемого документа. |
| [setMswVersion(int value)](#setMswVersion-int-) | Позволяет указать, что процесс загрузки документа должен соответствовать конкретной версии MS Word. |
| [setPageCount(int value)](#setPageCount-int-) | Устанавливает количество страниц для чтения. |
| [setPageIndex(int value)](#setPageIndex-int-) | Устанавливает отсчитываемый от 0 индекс первой страницы для чтения. |
| [setPassword(String value)](#setPassword-java.lang.String-) | Устанавливает пароль для открытия зашифрованного документа. |
| [setPreserveIncludePictureField(boolean value)](#setPreserveIncludePictureField-boolean-) | Устанавливает, сохранять ли поле INCLUDEPICTURE при чтении форматов Microsoft Word. |
| [setProgressCallback(IDocumentLoadingCallback value)](#setProgressCallback-com.aspose.words.IDocumentLoadingCallback-) | Вызывается во время загрузки документа и принимает данные о ходе загрузки. |
| [setResourceLoadingCallback(IResourceLoadingCallback value)](#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback-) | Позволяет управлять загрузкой внешних ресурсов (изображений, таблиц стилей) при импорте документа из HTML, MHTML. |
| [setSkipPdfImages(boolean value)](#setSkipPdfImages-boolean-) | Устанавливает флаг, указывающий, нужно ли пропускать изображения при загрузке PDF-документа. |
| [setTempFolder(String value)](#setTempFolder-java.lang.String-) | Позволяет использовать временные файлы при чтении документа. |
| [setUpdateDirtyFields(boolean value)](#setUpdateDirtyFields-boolean-) | Указывает, следует ли обновлять поля с грязным атрибутом. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback-) | Вызывается во время операции загрузки при обнаружении проблемы, которая может привести к потере точности данных или форматирования. |
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
### getBaseUri() {#getBaseUri--}
```
public String getBaseUri()
```


Получает строку, которая будет использоваться для преобразования относительных URI, найденных в документе, в абсолютные URI, когда это необходимо. Может быть нулевой или пустой строкой. Значение по умолчанию равно нулю.

Это свойство используется для преобразования относительных URI в абсолютные в следующих случаях:

1.  При загрузке HTML-документа из потока, когда документ содержит изображения с относительными URI и не имеет базового URI, указанного в элементе BASE HTML.
2.  При сохранении документа в PDF и других форматах для извлечения изображений, связанных с использованием относительных URI, чтобы изображения можно было сохранить в выходной документ.

**Возвращает:**
java.lang.String — строка, которая будет использоваться для преобразования относительных URI, найденных в документе, в абсолютные URI, когда это необходимо.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getConvertMetafilesToPng() {#getConvertMetafilesToPng--}
```
public boolean getConvertMetafilesToPng()
```


 Получает, следует ли преобразовывать метафайл (**F:Aspose.FileFormat.Wmf** или же**F:Aspose.FileFormat.Emf** ) изображения в**F:Aspose.FileFormat.Png** формат изображения. Метафайлы (**F:Aspose.FileFormat.Wmf** или же**F:Aspose.FileFormat.Emf** ) представляет собой несжатый формат изображения и иногда требует много оперативной памяти для хранения и обработки документа. Эта опция позволяет преобразовать все изображения метафайла в**F:Aspose.FileFormat.Png** при загрузке документа. Обратите внимание - преобразование векторной графики в растровую снижает качество изображений.

**Возвращает:**
 boolean — конвертировать ли метафайл (**F:Aspose.FileFormat.Wmf** или же**F:Aspose.FileFormat.Emf** ) изображения в**F:Aspose.FileFormat.Png** формат изображения.
### getConvertShapeToOfficeMath() {#getConvertShapeToOfficeMath--}
```
public boolean getConvertShapeToOfficeMath()
```


Определяет, следует ли преобразовывать фигуры с помощью EquationXML в объекты Office Math.

**Возвращает:**
boolean — следует ли преобразовывать фигуры с помощью EquationXML в объекты Office Math.
### getEncoding() {#getEncoding--}
```
public Charset getEncoding()
```


Получает кодировку, которая будет использоваться для загрузки документа HTML, TXT или CHM, если кодировка не указана внутри документа. Может быть нулевым. Значение по умолчанию равно нулю.

Это свойство используется только при загрузке документов HTML, TXT или CHM.

Если кодировка внутри документа не указана и это свойство равно null , то система попытается автоматически определить кодировку.

**Возвращает:**
java.nio.charset.Charset — кодировка, которая будет использоваться для загрузки документа HTML, TXT или CHM, если кодировка не указана внутри документа.
### getFontSettings() {#getFontSettings--}
```
public FontSettings getFontSettings()
```


Позволяет указать настройки шрифта документа.

При загрузке некоторых форматов Aspose.Words может потребовать разрешения шрифтов. Например, при загрузке HTML-документов Aspose.Words может разрешить шрифты для выполнения резервного шрифта.

 Если установлено значение null, настройки статического шрифта по умолчанию[FontSettings.getDefaultInstance()](../../com.aspose.words/fontsettings\#getDefaultInstance--) будет использован.

Значение по умолчанию равно нулю.

**Возвращает:**
[FontSettings](../../com.aspose.words/fontsettings) - соответствующий[FontSettings](../../com.aspose.words/fontsettings) ценность.
### getLanguagePreferences() {#getLanguagePreferences--}
```
public LanguagePreferences getLanguagePreferences()
```


Получает языковые настройки, которые будут использоваться при загрузке документа.

**Возвращает:**
[LanguagePreferences](../../com.aspose.words/languagepreferences) - Языковые настройки, которые будут использоваться при загрузке документа.
### getLoadFormat() {#getLoadFormat--}
```
public int getLoadFormat()
```


 Задает формат загружаемого документа. По умолчанию[LoadFormat.AUTO](../../com.aspose.words/loadformat\#AUTO).

 Рекомендуется указать[LoadFormat.AUTO](../../com.aspose.words/loadformat\#AUTO)значение и позволить Aspose.Words автоматически определить формат файла. Если вы знаете формат документа, который собираетесь загрузить, вы можете явно указать формат, и это немного сократит время загрузки за счет накладных расходов, связанных с автоматическим определением формата. Если вы укажете явный формат загрузки, и он окажется неверным, сработает автоопределение и будет предпринята вторая попытка загрузить файл.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[LoadFormat](../../com.aspose.words/loadformat) константы.
### getMswVersion() {#getMswVersion--}
```
public int getMswVersion()
```


 Позволяет указать, что процесс загрузки документа должен соответствовать конкретной версии MS Word. Значение по умолчанию[MsWordVersion.WORD\_2019](../../com.aspose.words/mswordversion\#WORD-2019) Различные версии Word могут немного по-разному обрабатывать некоторые аспекты содержимого и форматирования документа в процессе загрузки, что может привести к незначительным различиям в объектной модели документа.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[MsWordVersion](../../com.aspose.words/mswordversion) константы.
### getPageCount() {#getPageCount--}
```
public int getPageCount()
```


Получает количество страниц для чтения. По умолчанию установлено значение MaxValue, что означает, что будут прочитаны все страницы документа.

**Возвращает:**
int - количество страниц для чтения.
### getPageIndex() {#getPageIndex--}
```
public int getPageIndex()
```


Получает отсчитываемый от 0 индекс первой страницы для чтения. По умолчанию 0.

**Возвращает:**
int - Индекс первой страницы для чтения, начинающийся с 0.
### getPassword() {#getPassword--}
```
public String getPassword()
```


Получает пароль для открытия зашифрованного документа. Может быть нулевой или пустой строкой. Значение по умолчанию равно нулю.

Вам нужно знать пароль, чтобы открыть зашифрованный документ. Если документ не зашифрован, установите для этого параметра значение null или пустую строку.

**Возвращает:**
java.lang.String — пароль для открытия зашифрованного документа.
### getPreserveIncludePictureField() {#getPreserveIncludePictureField--}
```
public boolean getPreserveIncludePictureField()
```


Определяет, следует ли сохранять поле INCLUDEPICTURE при чтении форматов Microsoft Word. Значение по умолчанию неверно.

По умолчанию поле INCLUDEPICTURE преобразуется в объект формы. Вы можете переопределить это, если вам нужно сохранить поле, например, если вы хотите обновить его программно. Обратите внимание, однако, что этот подход не является общим для Aspose.Words. Используйте его на свой страх и риск.

Одним из возможных вариантов использования может быть использование MERGEFIELD в качестве дочернего поля для динамического изменения исходного пути изображения. В этом случае вам нужно сохранить INCLUDEPICTURE в модели.

**Возвращает:**
boolean — сохранять ли поле INCLUDEPICTURE при чтении форматов Microsoft Word.
### getProgressCallback() {#getProgressCallback--}
```
public IDocumentLoadingCallback getProgressCallback()
```


Вызывается во время загрузки документа и принимает данные о ходе загрузки.

[LoadFormat.DOCX](../../com.aspose.words/loadformat\#DOCX), [LoadFormat.FLAT\_OPC](../../com.aspose.words/loadformat\#FLAT-OPC), [LoadFormat.DOCM](../../com.aspose.words/loadformat\#DOCM), [LoadFormat.DOTM](../../com.aspose.words/loadformat\#DOTM), [LoadFormat.DOTX](../../com.aspose.words/loadformat\#DOTX), [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat\#MARKDOWN), [LoadFormat.RTF](../../com.aspose.words/loadformat\#RTF), [LoadFormat.WORD\_ML](../../com.aspose.words/loadformat\#WORD-ML), [LoadFormat.DOC](../../com.aspose.words/loadformat\#DOC), [LoadFormat.DOT](../../com.aspose.words/loadformat\#DOT), [LoadFormat.ODT](../../com.aspose.words/loadformat\#ODT), [LoadFormat.OTT](../../com.aspose.words/loadformat\#OTT) поддерживаемые форматы.

**Возвращает:**
[IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback) - соответствующий[IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback) ценность.
### getResourceLoadingCallback() {#getResourceLoadingCallback--}
```
public IResourceLoadingCallback getResourceLoadingCallback()
```


Позволяет управлять загрузкой внешних ресурсов (изображений, таблиц стилей) при импорте документа из HTML, MHTML.

**Возвращает:**
[IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback) - соответствующий[IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback) ценность.
### getSkipPdfImages() {#getSkipPdfImages--}
```
public boolean getSkipPdfImages()
```


Получает флаг, указывающий, нужно ли пропускать изображения при загрузке документа PDF. По умолчанию — Ложь.

**Возвращает:**
boolean — Флаг, указывающий, нужно ли пропускать изображения при загрузке PDF-документа.
### getTempFolder() {#getTempFolder--}
```
public String getTempFolder()
```


Позволяет использовать временные файлы при чтении документа. По умолчанию это свойство имеет значение null, и временные файлы не используются.

Папка должна существовать и быть доступной для записи, иначе будет выдано исключение.

Aspose.Words автоматически удаляет все временные файлы после завершения чтения.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getUpdateDirtyFields() {#getUpdateDirtyFields--}
```
public boolean getUpdateDirtyFields()
```


Указывает, следует ли обновлять поля с грязным атрибутом.

**Возвращает:**
boolean - соответствующее логическое значение.
### getWarningCallback() {#getWarningCallback--}
```
public IWarningCallback getWarningCallback()
```


Вызывается во время операции загрузки при обнаружении проблемы, которая может привести к потере точности данных или форматирования.

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




### setBaseUri(String value) {#setBaseUri-java.lang.String-}
```
public void setBaseUri(String value)
```


Задает строку, которая будет использоваться для преобразования относительных URI, найденных в документе, в абсолютные URI, когда это необходимо. Может быть нулевой или пустой строкой. Значение по умолчанию равно нулю.

Это свойство используется для преобразования относительных URI в абсолютные в следующих случаях:

1.  При загрузке HTML-документа из потока, когда документ содержит изображения с относительными URI и не имеет базового URI, указанного в элементе BASE HTML.
2.  При сохранении документа в PDF и других форматах для извлечения изображений, связанных с использованием относительных URI, чтобы изображения можно было сохранить в выходной документ.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Строка, которая будет использоваться для преобразования относительных URI, найденных в документе, в абсолютные URI, когда это необходимо. |

### setConvertMetafilesToPng(boolean value) {#setConvertMetafilesToPng-boolean-}
```
public void setConvertMetafilesToPng(boolean value)
```


 Устанавливает, следует ли преобразовывать метафайл (**F:Aspose.FileFormat.Wmf** или же**F:Aspose.FileFormat.Emf** ) изображения в**F:Aspose.FileFormat.Png** формат изображения. Метафайлы (**F:Aspose.FileFormat.Wmf** или же**F:Aspose.FileFormat.Emf** ) представляет собой несжатый формат изображения и иногда требует много оперативной памяти для хранения и обработки документа. Эта опция позволяет преобразовать все изображения метафайла в**F:Aspose.FileFormat.Png** при загрузке документа. Обратите внимание - преобразование векторной графики в растровую снижает качество изображений.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean |  Преобразовывать ли метафайл (**F:Aspose.FileFormat.Wmf** или же**F:Aspose.FileFormat.Emf** ) изображения в**F:Aspose.FileFormat.Png** формат изображения. |

### setConvertShapeToOfficeMath(boolean value) {#setConvertShapeToOfficeMath-boolean-}
```
public void setConvertShapeToOfficeMath(boolean value)
```


Устанавливает, следует ли преобразовывать фигуры с EquationXML в объекты Office Math.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Следует ли преобразовывать фигуры с помощью EquationXML в объекты Office Math. |

### setEncoding(Charset value) {#setEncoding-java.nio.charset.Charset-}
```
public void setEncoding(Charset value)
```


Задает кодировку, которая будет использоваться для загрузки документа HTML, TXT или CHM, если кодировка не указана внутри документа. Может быть нулевым. Значение по умолчанию равно нулю.

Это свойство используется только при загрузке документов HTML, TXT или CHM.

Если кодировка внутри документа не указана и это свойство равно null , то система попытается автоматически определить кодировку.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.nio.charset.Charset | Кодировка, которая будет использоваться для загрузки документа HTML, TXT или CHM, если кодировка не указана внутри документа. |

### setFontSettings(FontSettings value) {#setFontSettings-com.aspose.words.FontSettings-}
```
public void setFontSettings(FontSettings value)
```


Позволяет указать настройки шрифта документа.

При загрузке некоторых форматов Aspose.Words может потребовать разрешения шрифтов. Например, при загрузке HTML-документов Aspose.Words может разрешить шрифты для выполнения резервного шрифта.

 Если установлено значение null, настройки статического шрифта по умолчанию[FontSettings.getDefaultInstance()](../../com.aspose.words/fontsettings\#getDefaultInstance--) будет использован.

Значение по умолчанию равно нулю.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [FontSettings](../../com.aspose.words/fontsettings) |  Соответствующий[FontSettings](../../com.aspose.words/fontsettings) ценность. |

### setLoadFormat(int value) {#setLoadFormat-int-}
```
public void setLoadFormat(int value)
```


 Задает формат загружаемого документа. По умолчанию[LoadFormat.AUTO](../../com.aspose.words/loadformat\#AUTO).

 Рекомендуется указать[LoadFormat.AUTO](../../com.aspose.words/loadformat\#AUTO)значение и позволить Aspose.Words автоматически определить формат файла. Если вы знаете формат документа, который собираетесь загрузить, вы можете явно указать формат, и это немного сократит время загрузки за счет накладных расходов, связанных с автоматическим определением формата. Если вы укажете явный формат загрузки, и он окажется неверным, сработает автоопределение и будет предпринята вторая попытка загрузить файл.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[LoadFormat](../../com.aspose.words/loadformat) константы. |

### setMswVersion(int value) {#setMswVersion-int-}
```
public void setMswVersion(int value)
```


 Позволяет указать, что процесс загрузки документа должен соответствовать конкретной версии MS Word. Значение по умолчанию[MsWordVersion.WORD\_2019](../../com.aspose.words/mswordversion\#WORD-2019) Различные версии Word могут немного по-разному обрабатывать некоторые аспекты содержимого и форматирования документа в процессе загрузки, что может привести к незначительным различиям в объектной модели документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[MsWordVersion](../../com.aspose.words/mswordversion) константы. |

### setPageCount(int value) {#setPageCount-int-}
```
public void setPageCount(int value)
```


Устанавливает количество страниц для чтения. По умолчанию установлено значение MaxValue, что означает, что будут прочитаны все страницы документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Количество страниц для чтения. |

### setPageIndex(int value) {#setPageIndex-int-}
```
public void setPageIndex(int value)
```


Устанавливает отсчитываемый от 0 индекс первой страницы для чтения. По умолчанию 0.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Отсчитываемый от 0 индекс первой страницы для чтения. |

### setPassword(String value) {#setPassword-java.lang.String-}
```
public void setPassword(String value)
```


Устанавливает пароль для открытия зашифрованного документа. Может быть нулевой или пустой строкой. Значение по умолчанию равно нулю.

Вам нужно знать пароль, чтобы открыть зашифрованный документ. Если документ не зашифрован, установите для этого параметра значение null или пустую строку.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Пароль для открытия зашифрованного документа. |

### setPreserveIncludePictureField(boolean value) {#setPreserveIncludePictureField-boolean-}
```
public void setPreserveIncludePictureField(boolean value)
```


Устанавливает, сохранять ли поле INCLUDEPICTURE при чтении форматов Microsoft Word. Значение по умолчанию неверно.

По умолчанию поле INCLUDEPICTURE преобразуется в объект формы. Вы можете переопределить это, если вам нужно сохранить поле, например, если вы хотите обновить его программно. Обратите внимание, однако, что этот подход не является общим для Aspose.Words. Используйте его на свой страх и риск.

Одним из возможных вариантов использования может быть использование MERGEFIELD в качестве дочернего поля для динамического изменения исходного пути изображения. В этом случае вам нужно сохранить INCLUDEPICTURE в модели.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Сохранять ли поле INCLUDEPICTURE при чтении форматов Microsoft Word. |

### setProgressCallback(IDocumentLoadingCallback value) {#setProgressCallback-com.aspose.words.IDocumentLoadingCallback-}
```
public void setProgressCallback(IDocumentLoadingCallback value)
```


Вызывается во время загрузки документа и принимает данные о ходе загрузки.

[LoadFormat.DOCX](../../com.aspose.words/loadformat\#DOCX), [LoadFormat.FLAT\_OPC](../../com.aspose.words/loadformat\#FLAT-OPC), [LoadFormat.DOCM](../../com.aspose.words/loadformat\#DOCM), [LoadFormat.DOTM](../../com.aspose.words/loadformat\#DOTM), [LoadFormat.DOTX](../../com.aspose.words/loadformat\#DOTX), [LoadFormat.MARKDOWN](../../com.aspose.words/loadformat\#MARKDOWN), [LoadFormat.RTF](../../com.aspose.words/loadformat\#RTF), [LoadFormat.WORD\_ML](../../com.aspose.words/loadformat\#WORD-ML), [LoadFormat.DOC](../../com.aspose.words/loadformat\#DOC), [LoadFormat.DOT](../../com.aspose.words/loadformat\#DOT), [LoadFormat.ODT](../../com.aspose.words/loadformat\#ODT), [LoadFormat.OTT](../../com.aspose.words/loadformat\#OTT) поддерживаемые форматы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback) |  Соответствующий[IDocumentLoadingCallback](../../com.aspose.words/idocumentloadingcallback) ценность. |

### setResourceLoadingCallback(IResourceLoadingCallback value) {#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback-}
```
public void setResourceLoadingCallback(IResourceLoadingCallback value)
```


Позволяет управлять загрузкой внешних ресурсов (изображений, таблиц стилей) при импорте документа из HTML, MHTML.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback) |  Соответствующий[IResourceLoadingCallback](../../com.aspose.words/iresourceloadingcallback) ценность. |

### setSkipPdfImages(boolean value) {#setSkipPdfImages-boolean-}
```
public void setSkipPdfImages(boolean value)
```


Устанавливает флаг, указывающий, нужно ли пропускать изображения при загрузке PDF-документа. По умолчанию — Ложь.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Флаг, указывающий, нужно ли пропускать изображения при загрузке документа PDF. |

### setTempFolder(String value) {#setTempFolder-java.lang.String-}
```
public void setTempFolder(String value)
```


Позволяет использовать временные файлы при чтении документа. По умолчанию это свойство имеет значение null, и временные файлы не используются.

Папка должна существовать и быть доступной для записи, иначе будет выдано исключение.

Aspose.Words автоматически удаляет все временные файлы после завершения чтения.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setUpdateDirtyFields(boolean value) {#setUpdateDirtyFields-boolean-}
```
public void setUpdateDirtyFields(boolean value)
```


Указывает, следует ли обновлять поля с грязным атрибутом.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setWarningCallback(IWarningCallback value) {#setWarningCallback-com.aspose.words.IWarningCallback-}
```
public void setWarningCallback(IWarningCallback value)
```


Вызывается во время операции загрузки при обнаружении проблемы, которая может привести к потере точности данных или форматирования.

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
