---
title: HtmlLoadOptions
second_title: Справочник по API Aspose.Words для Java
description: Позволяет указать дополнительные параметры при загрузке HTML-документа в объект.
type: docs
weight: 328
url: /ru/java/com.aspose.words/htmlloadoptions/
---

**Наследование:**
java.lang.Object, [com.aspose.words.LoadOptions](../../com.aspose.words/loadoptions)
```
public class HtmlLoadOptions extends LoadOptions
```

 Позволяет указать дополнительные параметры при загрузке HTML-документа в[Document](../../com.aspose.words/document) объект.

 Чтобы узнать больше, посетите**Specify Load Options** документальная статья.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [HtmlLoadOptions()](#HtmlLoadOptions--) | Инициализирует новый экземпляр этого класса со значениями по умолчанию. |
| [HtmlLoadOptions(String password)](#HtmlLoadOptions-java.lang.String-) | Ярлык для инициализации нового экземпляра этого класса с указанным паролем для загрузки зашифрованного документа. |
| [HtmlLoadOptions(int loadFormat, String password, String baseUri)](#HtmlLoadOptions-int-java.lang.String-java.lang.String-) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBaseUri()](#getBaseUri--) | Получает строку, которая будет использоваться для преобразования относительных URI, найденных в документе, в абсолютные URI, когда это необходимо. |
| [getBlockImportMode()](#getBlockImportMode--) | Получает значение, указывающее, как импортируются свойства элементов уровня блока. |
| [getClass()](#getClass--) |  |
| [getConvertMetafilesToPng()](#getConvertMetafilesToPng--) |  Получает, следует ли преобразовывать метафайл (**F:Aspose.FileFormat.Wmf** или же**F:Aspose.FileFormat.Emf** ) изображения в**F:Aspose.FileFormat.Png** формат изображения. |
| [getConvertShapeToOfficeMath()](#getConvertShapeToOfficeMath--) | Определяет, следует ли преобразовывать фигуры с помощью EquationXML в объекты Office Math. |
| [getConvertSvgToEmf()](#getConvertSvgToEmf--) | Получает значение, указывающее, следует ли преобразовывать загруженные изображения SVG в формат EMF. |
| [getEncoding()](#getEncoding--) | Получает кодировку, которая будет использоваться для загрузки документа HTML, TXT или CHM, если кодировка не указана внутри документа. |
| [getFontSettings()](#getFontSettings--) | Позволяет указать настройки шрифта документа. |
| [getIgnoreNoscriptElements()](#getIgnoreNoscriptElements--) | Получает значение, указывающее, следует ли игнорировать элементы HTML. |
| [getLanguagePreferences()](#getLanguagePreferences--) | Получает языковые настройки, которые будут использоваться при загрузке документа. |
| [getLoadFormat()](#getLoadFormat--) | Задает формат загружаемого документа. |
| [getMswVersion()](#getMswVersion--) | Позволяет указать, что процесс загрузки документа должен соответствовать конкретной версии MS Word. |
| [getPassword()](#getPassword--) | Получает пароль для открытия зашифрованного документа. |
| [getPreferredControlType()](#getPreferredControlType--) | Получает предпочтительный тип узлов документа, которые будут представлять импортированные и элементы. |
| [getPreserveIncludePictureField()](#getPreserveIncludePictureField--) | Определяет, следует ли сохранять поле INCLUDEPICTURE при чтении форматов Microsoft Word. |
| [getProgressCallback()](#getProgressCallback--) | Вызывается во время загрузки документа и принимает данные о ходе загрузки. |
| [getResourceLoadingCallback()](#getResourceLoadingCallback--) | Позволяет управлять загрузкой внешних ресурсов (изображений, таблиц стилей) при импорте документа из HTML, MHTML. |
| [getSupportVml()](#getSupportVml--) | Получает значение, указывающее, следует ли поддерживать изображения VML. |
| [getTempFolder()](#getTempFolder--) | Позволяет использовать временные файлы при чтении документа. |
| [getUpdateDirtyFields()](#getUpdateDirtyFields--) | Указывает, следует ли обновлять поля с грязным атрибутом. |
| [getWarningCallback()](#getWarningCallback--) | Вызывается во время операции загрузки при обнаружении проблемы, которая может привести к потере точности данных или форматирования. |
| [getWebRequestTimeout()](#getWebRequestTimeout--) | Количество миллисекунд ожидания до истечения времени ожидания веб-запроса. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setBaseUri(String value)](#setBaseUri-java.lang.String-) | Задает строку, которая будет использоваться для преобразования относительных URI, найденных в документе, в абсолютные URI, когда это необходимо. |
| [setBlockImportMode(int value)](#setBlockImportMode-int-) | Задает значение, указывающее, как импортируются свойства элементов уровня блока. |
| [setConvertMetafilesToPng(boolean value)](#setConvertMetafilesToPng-boolean-) |  Устанавливает, следует ли преобразовывать метафайл (**F:Aspose.FileFormat.Wmf** или же**F:Aspose.FileFormat.Emf** ) изображения в**F:Aspose.FileFormat.Png** формат изображения. |
| [setConvertShapeToOfficeMath(boolean value)](#setConvertShapeToOfficeMath-boolean-) | Устанавливает, следует ли преобразовывать фигуры с EquationXML в объекты Office Math. |
| [setConvertSvgToEmf(boolean value)](#setConvertSvgToEmf-boolean-) | Задает значение, указывающее, следует ли преобразовывать загруженные изображения SVG в формат EMF. |
| [setEncoding(Charset value)](#setEncoding-java.nio.charset.Charset-) | Задает кодировку, которая будет использоваться для загрузки документа HTML, TXT или CHM, если кодировка не указана внутри документа. |
| [setFontSettings(FontSettings value)](#setFontSettings-com.aspose.words.FontSettings-) | Позволяет указать настройки шрифта документа. |
| [setIgnoreNoscriptElements(boolean value)](#setIgnoreNoscriptElements-boolean-) | Задает значение, указывающее, следует ли игнорировать элементы HTML. |
| [setLoadFormat(int value)](#setLoadFormat-int-) | Задает формат загружаемого документа. |
| [setMswVersion(int value)](#setMswVersion-int-) | Позволяет указать, что процесс загрузки документа должен соответствовать конкретной версии MS Word. |
| [setPassword(String value)](#setPassword-java.lang.String-) | Устанавливает пароль для открытия зашифрованного документа. |
| [setPreferredControlType(int value)](#setPreferredControlType-int-) | Задает предпочтительный тип узлов документа, которые будут представлять импортированные элементы. |
| [setPreserveIncludePictureField(boolean value)](#setPreserveIncludePictureField-boolean-) | Устанавливает, сохранять ли поле INCLUDEPICTURE при чтении форматов Microsoft Word. |
| [setProgressCallback(IDocumentLoadingCallback value)](#setProgressCallback-com.aspose.words.IDocumentLoadingCallback-) | Вызывается во время загрузки документа и принимает данные о ходе загрузки. |
| [setResourceLoadingCallback(IResourceLoadingCallback value)](#setResourceLoadingCallback-com.aspose.words.IResourceLoadingCallback-) | Позволяет управлять загрузкой внешних ресурсов (изображений, таблиц стилей) при импорте документа из HTML, MHTML. |
| [setSupportVml(boolean value)](#setSupportVml-boolean-) | Задает значение, указывающее, поддерживать ли образы VML. |
| [setTempFolder(String value)](#setTempFolder-java.lang.String-) | Позволяет использовать временные файлы при чтении документа. |
| [setUpdateDirtyFields(boolean value)](#setUpdateDirtyFields-boolean-) | Указывает, следует ли обновлять поля с грязным атрибутом. |
| [setWarningCallback(IWarningCallback value)](#setWarningCallback-com.aspose.words.IWarningCallback-) | Вызывается во время операции загрузки при обнаружении проблемы, которая может привести к потере точности данных или форматирования. |
| [setWebRequestTimeout(int value)](#setWebRequestTimeout-int-) | Количество миллисекунд ожидания до истечения времени ожидания веб-запроса. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### HtmlLoadOptions() {#HtmlLoadOptions--}
```
public HtmlLoadOptions()
```


Инициализирует новый экземпляр этого класса со значениями по умолчанию.

### HtmlLoadOptions(String password) {#HtmlLoadOptions-java.lang.String-}
```
public HtmlLoadOptions(String password)
```


Ярлык для инициализации нового экземпляра этого класса с указанным паролем для загрузки зашифрованного документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| password | java.lang.String | Пароль для открытия зашифрованного документа. Может быть нулевой или пустой строкой. |

### HtmlLoadOptions(int loadFormat, String password, String baseUri) {#HtmlLoadOptions-int-java.lang.String-java.lang.String-}
```
public HtmlLoadOptions(int loadFormat, String password, String baseUri)
```


Инициализирует новый экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| loadFormat | int |  |
| password | java.lang.String |  |
| baseUri | java.lang.String |  |

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
### getBlockImportMode() {#getBlockImportMode--}
```
public int getBlockImportMode()
```


Получает значение, указывающее, как импортируются свойства элементов уровня блока. Значение по умолчанию[BlockImportMode.MERGE](../../com.aspose.words/blockimportmode\#MERGE).

**Возвращает:**
 int — значение, указывающее, как импортируются свойства элементов уровня блока. Возвращаемое значение является одним из[BlockImportMode](../../com.aspose.words/blockimportmode) константы.
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
### getConvertSvgToEmf() {#getConvertSvgToEmf--}
```
public boolean getConvertSvgToEmf()
```


Получает значение, указывающее, следует ли преобразовывать загруженные изображения SVG в формат EMF. Значение по умолчанию — false, и, если возможно, загруженные изображения SVG сохраняются как есть без преобразования.

Более новые версии MS Word изначально поддерживают изображения SVG. Если версия MS Word, указанная в параметрах загрузки, поддерживает SVG, Aspose.Words будет хранить изображения SVG как есть без преобразования. Если SVG не поддерживается, загруженные изображения SVG будут преобразованы в формат EMF.

Однако, если для этой опции установлено значение true , Aspose.Words будет преобразовывать загруженные изображения SVG в EMF, даже если изображения SVG поддерживаются указанной версией MS Word.

**Возвращает:**
логическое значение — значение, указывающее, следует ли преобразовывать загруженные изображения SVG в формат EMF.
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
### getIgnoreNoscriptElements() {#getIgnoreNoscriptElements--}
```
public boolean getIgnoreNoscriptElements()
```


Получает значение, указывающее, следует ли игнорировать элементы HTML. Значение по умолчанию — ложь. Как и MS Word, Aspose.Words не поддерживает скрипты и по умолчанию загружает содержимое элементов в результирующий документ. Однако в большинстве браузеров сценарии поддерживаются, и содержимое из них не отображается. Установка этого свойства в значение true заставляет Aspose.Words игнорировать все элементы и помогает создавать документы, которые выглядят ближе к тому, что видно в браузерах.

**Возвращает:**
boolean — значение, указывающее, следует ли игнорировать элементы HTML.
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
### getPassword() {#getPassword--}
```
public String getPassword()
```


Получает пароль для открытия зашифрованного документа. Может быть нулевой или пустой строкой. Значение по умолчанию равно нулю.

Вам нужно знать пароль, чтобы открыть зашифрованный документ. Если документ не зашифрован, установите для этого параметра значение null или пустую строку.

**Возвращает:**
java.lang.String — пароль для открытия зашифрованного документа.
### getPreferredControlType() {#getPreferredControlType--}
```
public int getPreferredControlType()
```


 Получает предпочтительный тип узлов документа, которые будут представлять импортированные и элементы. Значение по умолчанию[HtmlControlType.FORM\_FIELD](../../com.aspose.words/htmlcontroltype\#FORM-FIELD) . Обратите внимание, что установка этого свойства не гарантирует, что все импортированные элементы управления будут иметь указанный тип. Если элемент управления HTML не может быть представлен узлами документа предпочтительного типа, Aspose.Words будет использовать совместимый[HtmlControlType](../../com.aspose.words/htmlcontroltype) для этого контроля.

**Возвращает:**
 int — предпочтительный тип узлов документа, которые будут представлять импортированные элементы. Возвращаемое значение является одним из[HtmlControlType](../../com.aspose.words/htmlcontroltype) константы.
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
### getSupportVml() {#getSupportVml--}
```
public boolean getSupportVml()
```


Получает значение, указывающее, следует ли поддерживать изображения VML.

**Возвращает:**
boolean — значение, указывающее, следует ли поддерживать образы VML.
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
### getWebRequestTimeout() {#getWebRequestTimeout--}
```
public int getWebRequestTimeout()
```


Количество миллисекунд ожидания до истечения времени ожидания веб-запроса. Значение по умолчанию — 100000 миллисекунд (100 секунд). Количество миллисекунд, в течение которых Aspose.Words ожидает ответа при загрузке внешних ресурсов (изображений, таблиц стилей), связанных в документах HTML и MHTML.

**Возвращает:**
int - соответствующее значение int.
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

### setBlockImportMode(int value) {#setBlockImportMode-int-}
```
public void setBlockImportMode(int value)
```


 Задает значение, указывающее, как импортируются свойства элементов уровня блока. Значение по умолчанию[BlockImportMode.MERGE](../../com.aspose.words/blockimportmode\#MERGE).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Значение, указывающее, как импортируются свойства элементов уровня блока. Значение должно быть одним из[BlockImportMode](../../com.aspose.words/blockimportmode) константы. |

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

### setConvertSvgToEmf(boolean value) {#setConvertSvgToEmf-boolean-}
```
public void setConvertSvgToEmf(boolean value)
```


Задает значение, указывающее, следует ли преобразовывать загруженные изображения SVG в формат EMF. Значение по умолчанию — false, и, если возможно, загруженные изображения SVG сохраняются как есть без преобразования.

Более новые версии MS Word изначально поддерживают изображения SVG. Если версия MS Word, указанная в параметрах загрузки, поддерживает SVG, Aspose.Words будет хранить изображения SVG как есть без преобразования. Если SVG не поддерживается, загруженные изображения SVG будут преобразованы в формат EMF.

Однако, если для этой опции установлено значение true , Aspose.Words будет преобразовывать загруженные изображения SVG в EMF, даже если изображения SVG поддерживаются указанной версией MS Word.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, указывающее, следует ли преобразовывать загруженные изображения SVG в формат EMF. |

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

### setIgnoreNoscriptElements(boolean value) {#setIgnoreNoscriptElements-boolean-}
```
public void setIgnoreNoscriptElements(boolean value)
```


Задает значение, указывающее, следует ли игнорировать элементы HTML. Значение по умолчанию — ложь. Как и MS Word, Aspose.Words не поддерживает скрипты и по умолчанию загружает содержимое элементов в результирующий документ. Однако в большинстве браузеров сценарии поддерживаются, и содержимое из них не отображается. Установка этого свойства в значение true заставляет Aspose.Words игнорировать все элементы и помогает создавать документы, которые выглядят ближе к тому, что видно в браузерах.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, указывающее, следует ли игнорировать элементы HTML. |

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

### setPreferredControlType(int value) {#setPreferredControlType-int-}
```
public void setPreferredControlType(int value)
```


 Задает предпочтительный тип узлов документа, которые будут представлять импортированные элементы. Значение по умолчанию[HtmlControlType.FORM\_FIELD](../../com.aspose.words/htmlcontroltype\#FORM-FIELD) . Обратите внимание, что установка этого свойства не гарантирует, что все импортированные элементы управления будут иметь указанный тип. Если элемент управления HTML не может быть представлен узлами документа предпочтительного типа, Aspose.Words будет использовать совместимый[HtmlControlType](../../com.aspose.words/htmlcontroltype) для этого контроля.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Предпочтительный тип узлов документа, которые будут представлять импортированные элементы. Значение должно быть одним из[HtmlControlType](../../com.aspose.words/htmlcontroltype) константы. |

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

### setSupportVml(boolean value) {#setSupportVml-boolean-}
```
public void setSupportVml(boolean value)
```


Задает значение, указывающее, поддерживать ли образы VML.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, указывающее, поддерживать ли образы VML. |

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

### setWebRequestTimeout(int value) {#setWebRequestTimeout-int-}
```
public void setWebRequestTimeout(int value)
```


Количество миллисекунд ожидания до истечения времени ожидания веб-запроса. Значение по умолчанию — 100000 миллисекунд (100 секунд). Количество миллисекунд, в течение которых Aspose.Words ожидает ответа при загрузке внешних ресурсов (изображений, таблиц стилей), связанных в документах HTML и MHTML.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее целочисленное значение. |

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
