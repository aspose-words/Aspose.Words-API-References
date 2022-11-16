---
title: HtmlFixedSaveOptions
second_title: Справочник по API Aspose.Words для Java
description: Может использоваться для указания дополнительных параметров при сохранении документа в формате.
type: docs
weight: 326
url: /ru/java/com.aspose.words/htmlfixedsaveoptions/
---

**Наследование:**
java.lang.Object, [com.aspose.words.SaveOptions](../../com.aspose.words/saveoptions), [com.aspose.words.FixedPageSaveOptions](../../com.aspose.words/fixedpagesaveoptions)
```
public class HtmlFixedSaveOptions extends FixedPageSaveOptions
```

 Может использоваться для указания дополнительных параметров при сохранении документа в[SaveFormat.HTML\_FIXED](../../com.aspose.words/saveformat\#HTML-FIXED) формат.

 Чтобы узнать больше, посетите**Specify Save Options** документальная статья.
## Методы

| Метод | Описание |
| --- | --- |
| [createSaveOptions(int saveFormat)](#createSaveOptions-int-) |  |
| [createSaveOptions(String fileName)](#createSaveOptions-java.lang.String-) | Создает объект параметров сохранения класса, подходящего для расширения файла, указанного в данном имени файла. |
| [equals(Object obj)](#equals-java.lang.Object-) | Определяет, равен ли указанный объект по значению текущему объекту. |
| [getAllowEmbeddingPostScriptFonts()](#getAllowEmbeddingPostScriptFonts--) | Получает логическое значение, указывающее, разрешать ли встраивание шрифтов с контурами PostScript при встраивании шрифтов TrueType в документ после его сохранения. |
| [getClass()](#getClass--) |  |
| [getColorMode()](#getColorMode--) | Получает значение, определяющее способ отображения цветов. |
| [getCssClassNamesPrefix()](#getCssClassNamesPrefix--) | Указывает префикс, который добавляется ко всем именам классов в файле style.css. |
| [getDefaultTemplate()](#getDefaultTemplate--) | Получает путь к шаблону по умолчанию (включая имя файла). |
| [getDml3DEffectsRenderingMode()](#getDml3DEffectsRenderingMode--) | Получает значение, определяющее способ визуализации 3D-эффектов. |
| [getDmlEffectsRenderingMode()](#getDmlEffectsRenderingMode--) | Получает значение, определяющее способ визуализации эффектов DrawingML. |
| [getDmlRenderingMode()](#getDmlRenderingMode--) | Получает значение, определяющее способ отображения фигур DrawingML. |
| [getEncoding()](#getEncoding--) |  |
| [getExportEmbeddedCss()](#getExportEmbeddedCss--) | Указывает, следует ли встраивать CSS (каскадную таблицу стилей) в HTML-документ. |
| [getExportEmbeddedFonts()](#getExportEmbeddedFonts--) | Указывает, следует ли встраивать шрифты в HTML-документ в формате Base64. |
| [getExportEmbeddedImages()](#getExportEmbeddedImages--) | Указывает, следует ли встраивать изображения в HTML-документ в формате Base64. |
| [getExportEmbeddedSvg()](#getExportEmbeddedSvg--) | Указывает, следует ли встраивать ресурсы SVG в HTML-документ. |
| [getExportFormFields()](#getExportFormFields--) | Получает указание на то, экспортируются ли поля формы как интерактивные элементы (как тег input), а не преобразуются в текст или графику. |
| [getExportGeneratorName()](#getExportGeneratorName--) | При значении true имя и версия Aspose.Words встраиваются в создаваемые файлы. |
| [getFontFormat()](#getFontFormat--) |  Получает[ExportFontFormat](../../com.aspose.words/exportfontformat) используется для экспорта шрифтов. |
| [getImlRenderingMode()](#getImlRenderingMode--) | Получает значение, определяющее способ визуализации объектов рукописного ввода (InkML). |
| [getJpegQuality()](#getJpegQuality--) | Получает значение, определяющее качество изображений JPEG внутри HTML-документа. |
| [getMemoryOptimization()](#getMemoryOptimization--) | Получает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. |
| [getMetafileRenderingOptions()](#getMetafileRenderingOptions--) | Позволяет указать параметры рендеринга метафайла. |
| [getNumeralFormat()](#getNumeralFormat--) |  Получает[NumeralFormat](../../com.aspose.words/numeralformat) используется для отображения цифр. |
| [getOptimizeOutput()](#getOptimizeOutput--) | Флаг указывает, требуется ли оптимизация вывода. |
| [getPageHorizontalAlignment()](#getPageHorizontalAlignment--) | Задает горизонтальное выравнивание страниц в HTML-документе. |
| [getPageMargins()](#getPageMargins--) | Задает поля вокруг страниц в HTML-документе. |
| [getPageSavingCallback()](#getPageSavingCallback--) | Позволяет управлять сохранением отдельных страниц при экспорте документа в фиксированный формат страницы. |
| [getPageSet()](#getPageSet--) | Получает страницы для отображения. |
| [getPrettyFormat()](#getPrettyFormat--) | Когда true , красивые форматы выводятся там, где это применимо. |
| [getProgressCallback()](#getProgressCallback--) | Вызывается при сохранении документа и принимает данные о ходе сохранения. |
| [getResourceSavingCallback()](#getResourceSavingCallback--) | Позволяет управлять сохранением ресурсов (изображений, шрифтов и css) при экспорте документа в фиксированный формат страницы Html. |
| [getResourcesFolder()](#getResourcesFolder--) | Указывает физическую папку, в которой сохраняются ресурсы (изображения, шрифты, css) при экспорте документа в формат Html. |
| [getResourcesFolderAlias()](#getResourcesFolderAlias--) | Указывает имя папки, используемой для создания URI изображений, записываемых в HTML-документ. |
| [getSaveFontFaceCssSeparately()](#getSaveFontFaceCssSeparately--) |  Флаг указывает, следует ли помещать правила CSS "@font-face" в отдельный файл "fontFaces.css" при сохранении документа с внешней таблицей стилей (т.[getExportEmbeddedCss()](../../com.aspose.words/htmlfixedsaveoptions\#getExportEmbeddedCss--) / [setExportEmbeddedCss(boolean)](../../com.aspose.words/htmlfixedsaveoptions\#setExportEmbeddedCss-boolean-) является ложным). |
| [getSaveFormat()](#getSaveFormat--) | Указывает формат, в котором будет сохранен документ, если используется этот объект параметров сохранения. |
| [getShowPageBorder()](#getShowPageBorder--) | Указывает, следует ли отображать границу вокруг страниц. |
| [getTempFolder()](#getTempFolder--) | Указывает папку для временных файлов, используемых при сохранении в файл DOC или DOCX. |
| [getUpdateCreatedTimeProperty()](#getUpdateCreatedTimeProperty--) |  Получает значение, определяющее, является ли[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-) свойство обновляется перед сохранением. |
| [getUpdateFields()](#getUpdateFields--) | Получает значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы. |
| [getUpdateLastPrintedProperty()](#getUpdateLastPrintedProperty--) |  Получает значение, определяющее, является ли[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-) свойство обновляется перед сохранением. |
| [getUpdateLastSavedTimeProperty()](#getUpdateLastSavedTimeProperty--) |  Получает значение, определяющее, является ли[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-) свойство обновляется перед сохранением. |
| [getUpdateSdtContent()](#getUpdateSdtContent--) |  Получает значение, определяющее, будет ли содержимое[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) обновляется перед сохранением. |
| [getUseAntiAliasing()](#getUseAntiAliasing--) | Получает значение, определяющее, следует ли использовать сглаживание для рендеринга. |
| [getUseHighQualityRendering()](#getUseHighQualityRendering--) | Получает значение, определяющее, следует ли использовать высокое качество (т. е. |
| [getUseTargetMachineFonts()](#getUseTargetMachineFonts--) | Флаг указывает, должны ли шрифты с целевой машины использоваться для отображения документа. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setAllowEmbeddingPostScriptFonts(boolean value)](#setAllowEmbeddingPostScriptFonts-boolean-) | Задает логическое значение, указывающее, разрешать ли встраивание шрифтов с контурами PostScript при встраивании шрифтов TrueType в документ после его сохранения. |
| [setColorMode(int value)](#setColorMode-int-) | Задает значение, определяющее способ отображения цветов. |
| [setCssClassNamesPrefix(String value)](#setCssClassNamesPrefix-java.lang.String-) | Указывает префикс, который добавляется ко всем именам классов в файле style.css. |
| [setDefaultTemplate(String value)](#setDefaultTemplate-java.lang.String-) | Устанавливает путь к шаблону по умолчанию (включая имя файла). |
| [setDml3DEffectsRenderingMode(int value)](#setDml3DEffectsRenderingMode-int-) | Задает значение, определяющее способ визуализации 3D-эффектов. |
| [setDmlEffectsRenderingMode(int value)](#setDmlEffectsRenderingMode-int-) | Задает значение, определяющее, как визуализируются эффекты DrawingML. |
| [setDmlRenderingMode(int value)](#setDmlRenderingMode-int-) | Задает значение, определяющее, как отображаются фигуры DrawingML. |
| [setEncoding(Charset value)](#setEncoding-java.nio.charset.Charset-) |  |
| [setExportEmbeddedCss(boolean value)](#setExportEmbeddedCss-boolean-) | Указывает, следует ли встраивать CSS (каскадную таблицу стилей) в HTML-документ. |
| [setExportEmbeddedFonts(boolean value)](#setExportEmbeddedFonts-boolean-) | Указывает, следует ли встраивать шрифты в HTML-документ в формате Base64. |
| [setExportEmbeddedImages(boolean value)](#setExportEmbeddedImages-boolean-) | Указывает, следует ли встраивать изображения в HTML-документ в формате Base64. |
| [setExportEmbeddedSvg(boolean value)](#setExportEmbeddedSvg-boolean-) | Указывает, следует ли встраивать ресурсы SVG в HTML-документ. |
| [setExportFormFields(boolean value)](#setExportFormFields-boolean-) | Задает индикацию того, экспортируются ли поля формы как интерактивные элементы (как тег input), а не преобразуются в текст или графику. |
| [setExportGeneratorName(boolean value)](#setExportGeneratorName-boolean-) | При значении true имя и версия Aspose.Words встраиваются в создаваемые файлы. |
| [setFontFormat(int value)](#setFontFormat-int-) |  Наборы[ExportFontFormat](../../com.aspose.words/exportfontformat) используется для экспорта шрифтов. |
| [setImlRenderingMode(int value)](#setImlRenderingMode-int-) | Задает значение, определяющее способ визуализации объектов рукописного ввода (InkML). |
| [setJpegQuality(int value)](#setJpegQuality-int-) | Задает значение, определяющее качество изображений JPEG внутри HTML-документа. |
| [setMemoryOptimization(boolean value)](#setMemoryOptimization-boolean-) | Задает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. |
| [setMetafileRenderingOptions(MetafileRenderingOptions value)](#setMetafileRenderingOptions-com.aspose.words.MetafileRenderingOptions-) | Позволяет указать параметры рендеринга метафайла. |
| [setNumeralFormat(int value)](#setNumeralFormat-int-) |  Наборы[NumeralFormat](../../com.aspose.words/numeralformat) используется для отображения цифр. |
| [setOptimizeOutput(boolean value)](#setOptimizeOutput-boolean-) | Флаг указывает, требуется ли оптимизация вывода. |
| [setPageHorizontalAlignment(int value)](#setPageHorizontalAlignment-int-) | Задает горизонтальное выравнивание страниц в HTML-документе. |
| [setPageMargins(double value)](#setPageMargins-double-) | Задает поля вокруг страниц в HTML-документе. |
| [setPageSavingCallback(IPageSavingCallback value)](#setPageSavingCallback-com.aspose.words.IPageSavingCallback-) | Позволяет управлять сохранением отдельных страниц при экспорте документа в фиксированный формат страницы. |
| [setPageSet(PageSet value)](#setPageSet-com.aspose.words.PageSet-) | Устанавливает страницы для отображения. |
| [setPrettyFormat(boolean value)](#setPrettyFormat-boolean-) | Когда true , красивые форматы выводятся там, где это применимо. |
| [setProgressCallback(IDocumentSavingCallback value)](#setProgressCallback-com.aspose.words.IDocumentSavingCallback-) | Вызывается при сохранении документа и принимает данные о ходе сохранения. |
| [setResourceSavingCallback(IResourceSavingCallback value)](#setResourceSavingCallback-com.aspose.words.IResourceSavingCallback-) | Позволяет управлять сохранением ресурсов (изображений, шрифтов и css) при экспорте документа в фиксированный формат страницы Html. |
| [setResourcesFolder(String value)](#setResourcesFolder-java.lang.String-) | Указывает физическую папку, в которой сохраняются ресурсы (изображения, шрифты, css) при экспорте документа в формат Html. |
| [setResourcesFolderAlias(String value)](#setResourcesFolderAlias-java.lang.String-) | Указывает имя папки, используемой для создания URI изображений, записываемых в HTML-документ. |
| [setSaveFontFaceCssSeparately(boolean value)](#setSaveFontFaceCssSeparately-boolean-) |  Флаг указывает, следует ли помещать правила CSS "@font-face" в отдельный файл "fontFaces.css" при сохранении документа с внешней таблицей стилей (т.[getExportEmbeddedCss()](../../com.aspose.words/htmlfixedsaveoptions\#getExportEmbeddedCss--) / [setExportEmbeddedCss(boolean)](../../com.aspose.words/htmlfixedsaveoptions\#setExportEmbeddedCss-boolean-) является ложным). |
| [setSaveFormat(int value)](#setSaveFormat-int-) | Указывает формат, в котором будет сохранен документ, если используется этот объект параметров сохранения. |
| [setShowPageBorder(boolean value)](#setShowPageBorder-boolean-) | Указывает, следует ли отображать границу вокруг страниц. |
| [setTempFolder(String value)](#setTempFolder-java.lang.String-) | Указывает папку для временных файлов, используемых при сохранении в файл DOC или DOCX. |
| [setUpdateCreatedTimeProperty(boolean value)](#setUpdateCreatedTimeProperty-boolean-) |  Устанавливает значение, определяющее, будет ли[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-) свойство обновляется перед сохранением. |
| [setUpdateFields(boolean value)](#setUpdateFields-boolean-) | Задает значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы. |
| [setUpdateLastPrintedProperty(boolean value)](#setUpdateLastPrintedProperty-boolean-) |  Устанавливает значение, определяющее, будет ли[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-) свойство обновляется перед сохранением. |
| [setUpdateLastSavedTimeProperty(boolean value)](#setUpdateLastSavedTimeProperty-boolean-) |  Устанавливает значение, определяющее, будет ли[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-) свойство обновляется перед сохранением. |
| [setUpdateSdtContent(boolean value)](#setUpdateSdtContent-boolean-) |  Устанавливает значение, определяющее, будет ли содержимое[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) обновляется перед сохранением. |
| [setUseAntiAliasing(boolean value)](#setUseAntiAliasing-boolean-) | Задает значение, определяющее, следует ли использовать сглаживание для рендеринга. |
| [setUseHighQualityRendering(boolean value)](#setUseHighQualityRendering-boolean-) | Устанавливает значение, определяющее, использовать ли высокое качество (т.е. |
| [setUseTargetMachineFonts(boolean value)](#setUseTargetMachineFonts-boolean-) | Флаг указывает, должны ли шрифты с целевой машины использоваться для отображения документа. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### createSaveOptions(int saveFormat) {#createSaveOptions-int-}
```
public static SaveOptions createSaveOptions(int saveFormat)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| saveFormat | int |  |

**Возвращает:**
[SaveOptions](../../com.aspose.words/saveoptions)
### createSaveOptions(String fileName) {#createSaveOptions-java.lang.String-}
```
public static SaveOptions createSaveOptions(String fileName)
```


Создает объект параметров сохранения класса, подходящего для расширения файла, указанного в данном имени файла.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| fileName | java.lang.String | Расширение этого имени файла определяет класс создаваемого объекта параметров сохранения. |

**Возвращает:**
[SaveOptions](../../com.aspose.words/saveoptions) - Объект класса, производного от[SaveOptions](../../com.aspose.words/saveoptions).
### equals(Object obj) {#equals-java.lang.Object-}
```
public boolean equals(Object obj)
```


Определяет, равен ли указанный объект по значению текущему объекту.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Возвращает:**
логический
### getAllowEmbeddingPostScriptFonts() {#getAllowEmbeddingPostScriptFonts--}
```
public boolean getAllowEmbeddingPostScriptFonts()
```


Получает логическое значение, указывающее, разрешать ли встраивание шрифтов с контурами PostScript при встраивании шрифтов TrueType в документ после его сохранения. Значение по умолчанию**false**.

Обратите внимание: Word не встраивает шрифты PostScript, но может открывать документы со встроенными шрифтами этого типа.

 Этот вариант работает только тогда, когда[FontInfoCollection.getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection\#getEmbedTrueTypeFonts--) / [FontInfoCollection.setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection\#setEmbedTrueTypeFonts-boolean-) принадлежащий[DocumentBase.getFontInfos()](../../com.aspose.words/documentbase\#getFontInfos--) свойство имеет значение true .

**Возвращает:**
boolean — логическое значение, указывающее, разрешать ли встраивание шрифтов с контурами PostScript при встраивании шрифтов TrueType в документ после его сохранения.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getColorMode() {#getColorMode--}
```
public int getColorMode()
```


 Получает значение, определяющее способ отображения цветов. Значение по умолчанию[ColorMode.NORMAL](../../com.aspose.words/colormode\#NORMAL).

**Возвращает:**
 int — значение, определяющее способ отображения цветов. Возвращаемое значение является одним из[ColorMode](../../com.aspose.words/colormode) константы.
### getCssClassNamesPrefix() {#getCssClassNamesPrefix--}
```
public String getCssClassNamesPrefix()
```


Указывает префикс, который добавляется ко всем именам классов в файле style.css. Значение по умолчанию — «aw».

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getDefaultTemplate() {#getDefaultTemplate--}
```
public String getDefaultTemplate()
```


 Получает путь к шаблону по умолчанию (включая имя файла). Значение по умолчанию для этого свойства**empty string** . Если указано, этот путь используется для загрузки шаблона, когда[Document.getAutomaticallyUpdateStyles()](../../com.aspose.words/document\#getAutomaticallyUpdateStyles--) / [Document.setAutomaticallyUpdateStyles(boolean)](../../com.aspose.words/document\#setAutomaticallyUpdateStyles-boolean-) правда, но[Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate--) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String-) пустой.

**Возвращает:**
java.lang.String — путь к шаблону по умолчанию (включая имя файла).
### getDml3DEffectsRenderingMode() {#getDml3DEffectsRenderingMode--}
```
public int getDml3DEffectsRenderingMode()
```


Получает значение, определяющее способ визуализации 3D-эффектов. Значение по умолчанию[Dml3DEffectsRenderingMode.BASIC](../../com.aspose.words/dml3deffectsrenderingmode\#BASIC).

**Возвращает:**
 int — значение, определяющее, как визуализируются 3D-эффекты. Возвращаемое значение является одним из[Dml3DEffectsRenderingMode](../../com.aspose.words/dml3deffectsrenderingmode) константы.
### getDmlEffectsRenderingMode() {#getDmlEffectsRenderingMode--}
```
public int getDmlEffectsRenderingMode()
```


 Получает значение, определяющее способ визуализации эффектов DrawingML. Значение по умолчанию[DmlEffectsRenderingMode.SIMPLIFIED](../../com.aspose.words/dmleffectsrenderingmode\#SIMPLIFIED).

Это свойство используется, когда документ экспортируется в фиксированные форматы страниц.

**Возвращает:**
 int — значение, определяющее, как визуализируются эффекты DrawingML. Возвращаемое значение является одним из[DmlEffectsRenderingMode](../../com.aspose.words/dmleffectsrenderingmode) константы.
### getDmlRenderingMode() {#getDmlRenderingMode--}
```
public int getDmlRenderingMode()
```


 Получает значение, определяющее способ отображения фигур DrawingML. Значение по умолчанию[DmlRenderingMode.FALLBACK](../../com.aspose.words/dmlrenderingmode\#FALLBACK).

Это свойство используется, когда документ экспортируется в фиксированные форматы страниц.

**Возвращает:**
 int — значение, определяющее способ отображения фигур DrawingML. Возвращаемое значение является одним из[DmlRenderingMode](../../com.aspose.words/dmlrenderingmode) константы.
### getEncoding() {#getEncoding--}
```
public Charset getEncoding()
```




**Возвращает:**
java.nio.charset.Charset
### getExportEmbeddedCss() {#getExportEmbeddedCss--}
```
public boolean getExportEmbeddedCss()
```


Указывает, следует ли встраивать CSS (каскадную таблицу стилей) в HTML-документ.

**Возвращает:**
boolean - соответствующее логическое значение.
### getExportEmbeddedFonts() {#getExportEmbeddedFonts--}
```
public boolean getExportEmbeddedFonts()
```


Указывает, следует ли встраивать шрифты в HTML-документ в формате Base64. Обратите внимание, что установка этого флага может значительно увеличить размер выходного HTML-файла.

**Возвращает:**
boolean - соответствующее логическое значение.
### getExportEmbeddedImages() {#getExportEmbeddedImages--}
```
public boolean getExportEmbeddedImages()
```


Указывает, следует ли встраивать изображения в HTML-документ в формате Base64. Обратите внимание, что установка этого флага может значительно увеличить размер выходного HTML-файла.

**Возвращает:**
boolean - соответствующее логическое значение.
### getExportEmbeddedSvg() {#getExportEmbeddedSvg--}
```
public boolean getExportEmbeddedSvg()
```


Указывает, следует ли встраивать ресурсы SVG в HTML-документ. Значение по умолчанию — true.

**Возвращает:**
boolean - соответствующее логическое значение.
### getExportFormFields() {#getExportFormFields--}
```
public boolean getExportFormFields()
```


Получает указание на то, экспортируются ли поля формы как интерактивные элементы (как тег input), а не преобразуются в текст или графику.

**Возвращает:**
boolean — указывает, экспортируются ли поля формы как интерактивные элементы (как тег «ввод»), а не преобразуются в текст или графику.
### getExportGeneratorName() {#getExportGeneratorName--}
```
public boolean getExportGeneratorName()
```


 При значении true имя и версия Aspose.Words встраиваются в создаваемые файлы. Значение по умолчанию**true**.

**Возвращает:**
boolean - соответствующее логическое значение.
### getFontFormat() {#getFontFormat--}
```
public int getFontFormat()
```


 Получает[ExportFontFormat](../../com.aspose.words/exportfontformat) используется для экспорта шрифтов. Значение по умолчанию[ExportFontFormat.WOFF](../../com.aspose.words/exportfontformat\#WOFF).

**Возвращает:**
 инт -\{[ExportFontFormat](../../com.aspose.words/exportfontformat) используется для экспорта шрифтов. Возвращаемое значение является одним из[ExportFontFormat](../../com.aspose.words/exportfontformat) константы.
### getImlRenderingMode() {#getImlRenderingMode--}
```
public int getImlRenderingMode()
```


 Получает значение, определяющее способ визуализации объектов рукописного ввода (InkML). Значение по умолчанию[ImlRenderingMode.INK\_ML](../../com.aspose.words/imlrenderingmode\#INK-ML).

Это свойство используется, когда документ экспортируется в фиксированные форматы страниц.

**Возвращает:**
 int — значение, определяющее способ отображения объектов рукописного ввода (InkML). Возвращаемое значение является одним из[ImlRenderingMode](../../com.aspose.words/imlrenderingmode) константы.
### getJpegQuality() {#getJpegQuality--}
```
public int getJpegQuality()
```


Получает значение, определяющее качество изображений JPEG внутри HTML-документа.

Действует, только если документ содержит изображения JPEG.

Используйте это свойство, чтобы получить или установить качество изображений внутри документа при сохранении в фиксированном формате страницы. Значение может варьироваться от 0 до 100, где 0 означает худшее качество, но максимальное сжатие, а 100 — лучшее качество, но минимальное сжатие.

Значение по умолчанию — 95.

**Возвращает:**
int — значение, определяющее качество изображений JPEG внутри HTML-документа.
### getMemoryOptimization() {#getMemoryOptimization--}
```
public boolean getMemoryOptimization()
```


Получает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойства**false**. Установка для этого параметра значения true может значительно снизить потребление памяти при сохранении больших документов за счет замедления времени сохранения.

**Возвращает:**
boolean — значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа.
### getMetafileRenderingOptions() {#getMetafileRenderingOptions--}
```
public MetafileRenderingOptions getMetafileRenderingOptions()
```


Позволяет указать параметры рендеринга метафайла.

**Возвращает:**
[MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions) - соответствующий[MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions) ценность.
### getNumeralFormat() {#getNumeralFormat--}
```
public int getNumeralFormat()
```


 Получает[NumeralFormat](../../com.aspose.words/numeralformat) используется для отображения цифр. По умолчанию используются европейские цифры. Если значение этого свойства изменено, а макет страницы уже построен, то[Document.updatePageLayout()](../../com.aspose.words/document\#updatePageLayout--) вызывается автоматически для обновления любых изменений.

**Возвращает:**
 инт -\{[NumeralFormat](../../com.aspose.words/numeralformat) используется для отображения цифр. Возвращаемое значение является одним из[NumeralFormat](../../com.aspose.words/numeralformat) константы.
### getOptimizeOutput() {#getOptimizeOutput--}
```
public boolean getOptimizeOutput()
```


Флаг указывает, требуется ли оптимизация вывода. Если этот флаг установлен, удаляются избыточные вложенные холсты и пустые холсты, а также объединяются соседние глифы с одинаковым форматированием. Примечание. Точность отображения содержимого может быть снижена, если для этого свойства задано значение true. Значение по умолчанию верно.

**Возвращает:**
boolean - соответствующее логическое значение.
### getPageHorizontalAlignment() {#getPageHorizontalAlignment--}
```
public int getPageHorizontalAlignment()
```


Задает горизонтальное выравнивание страниц в HTML-документе. Значение по умолчанию — HtmlFixedHorizontalPageAlignment.Center .

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[HtmlFixedPageHorizontalAlignment](../../com.aspose.words/htmlfixedpagehorizontalalignment) константы.
### getPageMargins() {#getPageMargins--}
```
public double getPageMargins()
```


Задает поля вокруг страниц в HTML-документе. Значение поля измеряется в пунктах и должно быть больше или равно 0. Значение по умолчанию — 10 баллов.

 Зависит от значения[getPageHorizontalAlignment()](../../com.aspose.words/htmlfixedsaveoptions\#getPageHorizontalAlignment--) / [setPageHorizontalAlignment(int)](../../com.aspose.words/htmlfixedsaveoptions\#setPageHorizontalAlignment-int-) имущество:

 *   Определяет верхнее, нижнее и левое поля страницы, если значение[HtmlFixedPageHorizontalAlignment.LEFT](../../com.aspose.words/htmlfixedpagehorizontalalignment\#LEFT).
 *   Определяет верхнее, нижнее и правое поля страницы, если значение[HtmlFixedPageHorizontalAlignment.RIGHT](../../com.aspose.words/htmlfixedpagehorizontalalignment\#RIGHT).
 *   Определяет верхнее и нижнее поля страницы, если значение[HtmlFixedPageHorizontalAlignment.CENTER](../../com.aspose.words/htmlfixedpagehorizontalalignment\#CENTER).

**Возвращает:**
double - соответствующее двойное значение.
### getPageSavingCallback() {#getPageSavingCallback--}
```
public IPageSavingCallback getPageSavingCallback()
```


Позволяет управлять сохранением отдельных страниц при экспорте документа в фиксированный формат страницы.

**Возвращает:**
[IPageSavingCallback](../../com.aspose.words/ipagesavingcallback) - соответствующий[IPageSavingCallback](../../com.aspose.words/ipagesavingcallback) ценность.
### getPageSet() {#getPageSet--}
```
public PageSet getPageSet()
```


Получает страницы для отображения. По умолчанию это все страницы документа.

**Возвращает:**
[PageSet](../../com.aspose.words/pageset) - Страницы для отображения.
### getPrettyFormat() {#getPrettyFormat--}
```
public boolean getPrettyFormat()
```


 Когда true , красивые форматы выводятся там, где это применимо. Значение по умолчанию**false**.

 Установлен в**true** чтобы сделать вывод HTML, MHTML, EPUB, WordML, RTF, DOCX и ODT удобочитаемым для человека. Полезно для тестирования или отладки.

**Возвращает:**
boolean - соответствующее логическое значение.
### getProgressCallback() {#getProgressCallback--}
```
public IDocumentSavingCallback getProgressCallback()
```


Вызывается при сохранении документа и принимает данные о ходе сохранения.

 Прогресс сообщается при сохранении в[SaveFormat.DOCX](../../com.aspose.words/saveformat\#DOCX), [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC), [SaveFormat.DOCM](../../com.aspose.words/saveformat\#DOCM), [SaveFormat.DOTM](../../com.aspose.words/saveformat\#DOTM), [SaveFormat.DOTX](../../com.aspose.words/saveformat\#DOTX), [SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB), [SaveFormat.XAML\_FLOW](../../com.aspose.words/saveformat\#XAML-FLOW) , или же[SaveFormat.XAML\_FLOW\_PACK](../../com.aspose.words/saveformat\#XAML-FLOW-PACK).

**Возвращает:**
[IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback) - соответствующий[IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback) ценность.
### getResourceSavingCallback() {#getResourceSavingCallback--}
```
public IResourceSavingCallback getResourceSavingCallback()
```


Позволяет управлять сохранением ресурсов (изображений, шрифтов и css) при экспорте документа в фиксированный формат страницы Html.

**Возвращает:**
[IResourceSavingCallback](../../com.aspose.words/iresourcesavingcallback) - соответствующий[IResourceSavingCallback](../../com.aspose.words/iresourcesavingcallback) ценность.
### getResourcesFolder() {#getResourcesFolder--}
```
public String getResourcesFolder()
```


Указывает физическую папку, в которой сохраняются ресурсы (изображения, шрифты, css) при экспорте документа в формат Html. Значение по умолчанию равно нулю.

 Имеет эффект, только если[getExportEmbeddedImages()](../../com.aspose.words/htmlfixedsaveoptions\#getExportEmbeddedImages--) / [setExportEmbeddedImages(boolean)](../../com.aspose.words/htmlfixedsaveoptions\#setExportEmbeddedImages-boolean-) свойство ложно.

 Когда вы сохраняете[Document](../../com.aspose.words/document) в формате Html Aspose.Words должен сохранять все изображения, встроенные в документ, как отдельные файлы.[getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolder-java.lang.String-) позволяет указать, где изображения будут сохранены и[getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolderAlias--) / [setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolderAlias-java.lang.String-) позволяет указать, как будут создаваться URI изображения.

Если вы сохраняете документ в файл и указываете имя файла, Aspose.Words по умолчанию сохраняет изображения в той же папке, где сохранен файл документа. Использовать[getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolder-java.lang.String-) переопределить это поведение.

 Если вы сохраняете документ в потоке, Aspose.Words не имеет папки для сохранения изображений, но все же необходимо где-то сохранять изображения. В этом случае вам нужно указать доступную папку с помощью[getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolder-java.lang.String-) имущество

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getResourcesFolderAlias() {#getResourcesFolderAlias--}
```
public String getResourcesFolderAlias()
```


Указывает имя папки, используемой для создания URI изображений, записываемых в HTML-документ. Значение по умолчанию равно нулю.

 Когда вы сохраняете[Document](../../com.aspose.words/document) в формате Html Aspose.Words должен сохранять все изображения, встроенные в документ, как отдельные файлы.[getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolder-java.lang.String-) позволяет указать, где изображения будут сохранены и[getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolderAlias--) / [setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolderAlias-java.lang.String-) позволяет указать, как будут создаваться URI изображения.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getSaveFontFaceCssSeparately() {#getSaveFontFaceCssSeparately--}
```
public boolean getSaveFontFaceCssSeparately()
```


 Флаг указывает, следует ли помещать правила CSS "@font-face" в отдельный файл "fontFaces.css" при сохранении документа с внешней таблицей стилей (т.[getExportEmbeddedCss()](../../com.aspose.words/htmlfixedsaveoptions\#getExportEmbeddedCss--) / [setExportEmbeddedCss(boolean)](../../com.aspose.words/htmlfixedsaveoptions\#setExportEmbeddedCss-boolean-) является ложным). Значение по умолчанию — false , все правила CSS записываются в один файл «styles.css». Установка для этого свойства значения true восстанавливает старое поведение (отдельные файлы) для совместимости с устаревшим кодом.

**Возвращает:**
boolean - соответствующее логическое значение.
### getSaveFormat() {#getSaveFormat--}
```
public int getSaveFormat()
```


 Указывает формат, в котором будет сохранен документ, если используется этот объект параметров сохранения. Может быть только[SaveFormat.HTML\_FIXED](../../com.aspose.words/saveformat\#HTML-FIXED).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[SaveFormat](../../com.aspose.words/saveformat) константы.
### getShowPageBorder() {#getShowPageBorder--}
```
public boolean getShowPageBorder()
```


Указывает, следует ли отображать границу вокруг страниц. По умолчанию верно.

**Возвращает:**
boolean - соответствующее логическое значение.
### getTempFolder() {#getTempFolder--}
```
public String getTempFolder()
```


Указывает папку для временных файлов, используемых при сохранении в файл DOC или DOCX. По умолчанию это свойство имеет значение null, и временные файлы не используются.

Когда Aspose.Words сохраняет документ, ему необходимо создать временные внутренние структуры. По умолчанию эти внутренние структуры создаются в памяти, и использование памяти резко возрастает в течение короткого периода времени, пока документ сохраняется. Когда сохранение завершено, память освобождается и утилизируется сборщиком мусора.

 Если вы сохраняете очень большой документ (тысячи страниц) и/или обрабатываете много документов одновременно, скачок памяти во время сохранения может быть достаточно значительным, чтобы система выдала исключение java.lang.IndexOutOfBoundsException. Указание временной папки с помощью[getTempFolder()](../../com.aspose.words/saveoptions\#getTempFolder--) / [setTempFolder(java.lang.String)](../../com.aspose.words/saveoptions\#setTempFolder-java.lang.String-)приведет к тому, что Aspose.Words будет хранить внутренние структуры во временных файлах, а не в памяти. Это уменьшает использование памяти во время сохранения, но снижает производительность сохранения.

Папка должна существовать и быть доступной для записи, иначе будет выдано исключение.

Aspose.Words автоматически удаляет все временные файлы после завершения сохранения.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getUpdateCreatedTimeProperty() {#getUpdateCreatedTimeProperty--}
```
public boolean getUpdateCreatedTimeProperty()
```


 Получает значение, определяющее, является ли[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-) свойство обновляется перед сохранением. Значение по умолчанию — ложь;

**Возвращает:**
 boolean - Значение, определяющее, является ли[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-) свойство обновляется перед сохранением.
### getUpdateFields() {#getUpdateFields--}
```
public boolean getUpdateFields()
```


 Получает значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы. Значение по умолчанию для этого свойства**true**. Позволяет указать, следует ли имитировать поведение MS Word.

**Возвращает:**
boolean — значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы.
### getUpdateLastPrintedProperty() {#getUpdateLastPrintedProperty--}
```
public boolean getUpdateLastPrintedProperty()
```


 Получает значение, определяющее, является ли[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-) свойство обновляется перед сохранением.

**Возвращает:**
 boolean - Значение, определяющее, является ли[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-) свойство обновляется перед сохранением.
### getUpdateLastSavedTimeProperty() {#getUpdateLastSavedTimeProperty--}
```
public boolean getUpdateLastSavedTimeProperty()
```


 Получает значение, определяющее, является ли[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-) свойство обновляется перед сохранением.

**Возвращает:**
 boolean - Значение, определяющее, является ли[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-) свойство обновляется перед сохранением.
### getUpdateSdtContent() {#getUpdateSdtContent--}
```
public boolean getUpdateSdtContent()
```


 Получает значение, определяющее, будет ли содержимое[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) обновляется перед сохранением. Значение по умолчанию неверно .

**Возвращает:**
 boolean — значение, определяющее, будет ли содержимое[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) обновляется перед сохранением.
### getUseAntiAliasing() {#getUseAntiAliasing--}
```
public boolean getUseAntiAliasing()
```


Получает значение, определяющее, следует ли использовать сглаживание для рендеринга.

Значение по умолчанию неверно . Когда для этого значения установлено значение true, для рендеринга используется сглаживание.

Это свойство используется, когда документ экспортируется в следующие форматы:[SaveFormat.TIFF](../../com.aspose.words/saveformat\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat\#EMF) . Когда документ экспортируется в[SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB) а также[SaveFormat.AZW\_3](../../com.aspose.words/saveformat\#AZW-3) форматы эта опция используется для растровых изображений.

**Возвращает:**
логическое значение — значение, определяющее, следует ли использовать сглаживание для рендеринга.
### getUseHighQualityRendering() {#getUseHighQualityRendering--}
```
public boolean getUseHighQualityRendering()
```


Получает значение, определяющее, следует ли использовать высококачественные (то есть медленные) алгоритмы рендеринга. Значение по умолчанию неверно .

 Это свойство используется, когда документ экспортируется в форматы изображений:[SaveFormat.TIFF](../../com.aspose.words/saveformat\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat\#EMF).

**Возвращает:**
логическое значение — значение, определяющее, следует ли использовать высокое качество (т.е.
### getUseTargetMachineFonts() {#getUseTargetMachineFonts--}
```
public boolean getUseTargetMachineFonts()
```


Флаг указывает, должны ли шрифты с целевой машины использоваться для отображения документа. Если этот флаг установлен в значение true,[getFontFormat()](../../com.aspose.words/htmlfixedsaveoptions\#getFontFormat--) / [setFontFormat(int)](../../com.aspose.words/htmlfixedsaveoptions\#setFontFormat-int-) а также[getExportEmbeddedFonts()](../../com.aspose.words/htmlfixedsaveoptions\#getExportEmbeddedFonts--) / [setExportEmbeddedFonts(boolean)](../../com.aspose.words/htmlfixedsaveoptions\#setExportEmbeddedFonts-boolean-) свойства также не действуют[getResourceSavingCallback()](../../com.aspose.words/htmlfixedsaveoptions\#getResourceSavingCallback--) / [setResourceSavingCallback(com.aspose.words.IResourceSavingCallback)](../../com.aspose.words/htmlfixedsaveoptions\#setResourceSavingCallback-com.aspose.words.IResourceSavingCallback-) не срабатывает для шрифтов. Значение по умолчанию — ложь.

**Возвращает:**
boolean - соответствующее логическое значение.
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




### setAllowEmbeddingPostScriptFonts(boolean value) {#setAllowEmbeddingPostScriptFonts-boolean-}
```
public void setAllowEmbeddingPostScriptFonts(boolean value)
```


 Задает логическое значение, указывающее, разрешать ли встраивание шрифтов с контурами PostScript при встраивании шрифтов TrueType в документ после его сохранения. Значение по умолчанию**false**.

Обратите внимание: Word не встраивает шрифты PostScript, но может открывать документы со встроенными шрифтами этого типа.

 Этот вариант работает только тогда, когда[FontInfoCollection.getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection\#getEmbedTrueTypeFonts--) / [FontInfoCollection.setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection\#setEmbedTrueTypeFonts-boolean-) принадлежащий[DocumentBase.getFontInfos()](../../com.aspose.words/documentbase\#getFontInfos--) свойство имеет значение true .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Логическое значение, указывающее, разрешать ли встраивание шрифтов с контурами PostScript при встраивании шрифтов TrueType в документ после его сохранения. |

### setColorMode(int value) {#setColorMode-int-}
```
public void setColorMode(int value)
```


 Задает значение, определяющее способ отображения цветов. Значение по умолчанию[ColorMode.NORMAL](../../com.aspose.words/colormode\#NORMAL).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Значение, определяющее способ отображения цветов. Значение должно быть одним из[ColorMode](../../com.aspose.words/colormode) константы. |

### setCssClassNamesPrefix(String value) {#setCssClassNamesPrefix-java.lang.String-}
```
public void setCssClassNamesPrefix(String value)
```


Указывает префикс, который добавляется ко всем именам классов в файле style.css. Значение по умолчанию — «aw».

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setDefaultTemplate(String value) {#setDefaultTemplate-java.lang.String-}
```
public void setDefaultTemplate(String value)
```


 Устанавливает путь к шаблону по умолчанию (включая имя файла). Значение по умолчанию для этого свойства**empty string** . Если указано, этот путь используется для загрузки шаблона, когда[Document.getAutomaticallyUpdateStyles()](../../com.aspose.words/document\#getAutomaticallyUpdateStyles--) / [Document.setAutomaticallyUpdateStyles(boolean)](../../com.aspose.words/document\#setAutomaticallyUpdateStyles-boolean-) правда, но[Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate--) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String-) пустой.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Путь к шаблону по умолчанию (включая имя файла). |

### setDml3DEffectsRenderingMode(int value) {#setDml3DEffectsRenderingMode-int-}
```
public void setDml3DEffectsRenderingMode(int value)
```


 Задает значение, определяющее способ визуализации 3D-эффектов. Значение по умолчанию[Dml3DEffectsRenderingMode.BASIC](../../com.aspose.words/dml3deffectsrenderingmode\#BASIC).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Значение, определяющее способ визуализации 3D-эффектов. Значение должно быть одним из[Dml3DEffectsRenderingMode](../../com.aspose.words/dml3deffectsrenderingmode) константы. |

### setDmlEffectsRenderingMode(int value) {#setDmlEffectsRenderingMode-int-}
```
public void setDmlEffectsRenderingMode(int value)
```


 Задает значение, определяющее, как визуализируются эффекты DrawingML. Значение по умолчанию[DmlEffectsRenderingMode.SIMPLIFIED](../../com.aspose.words/dmleffectsrenderingmode\#SIMPLIFIED).

Это свойство используется, когда документ экспортируется в фиксированные форматы страниц.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Значение, определяющее, как визуализируются эффекты DrawingML. Значение должно быть одним из[DmlEffectsRenderingMode](../../com.aspose.words/dmleffectsrenderingmode) константы. |

### setDmlRenderingMode(int value) {#setDmlRenderingMode-int-}
```
public void setDmlRenderingMode(int value)
```


 Задает значение, определяющее, как отображаются фигуры DrawingML. Значение по умолчанию[DmlRenderingMode.FALLBACK](../../com.aspose.words/dmlrenderingmode\#FALLBACK).

Это свойство используется, когда документ экспортируется в фиксированные форматы страниц.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Значение, определяющее, как отображаются фигуры DrawingML. Значение должно быть одним из[DmlRenderingMode](../../com.aspose.words/dmlrenderingmode) константы. |

### setEncoding(Charset value) {#setEncoding-java.nio.charset.Charset-}
```
public void setEncoding(Charset value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.nio.charset.Charset |  |

### setExportEmbeddedCss(boolean value) {#setExportEmbeddedCss-boolean-}
```
public void setExportEmbeddedCss(boolean value)
```


Указывает, следует ли встраивать CSS (каскадную таблицу стилей) в HTML-документ.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setExportEmbeddedFonts(boolean value) {#setExportEmbeddedFonts-boolean-}
```
public void setExportEmbeddedFonts(boolean value)
```


Указывает, следует ли встраивать шрифты в HTML-документ в формате Base64. Обратите внимание, что установка этого флага может значительно увеличить размер выходного HTML-файла.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setExportEmbeddedImages(boolean value) {#setExportEmbeddedImages-boolean-}
```
public void setExportEmbeddedImages(boolean value)
```


Указывает, следует ли встраивать изображения в HTML-документ в формате Base64. Обратите внимание, что установка этого флага может значительно увеличить размер выходного HTML-файла.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setExportEmbeddedSvg(boolean value) {#setExportEmbeddedSvg-boolean-}
```
public void setExportEmbeddedSvg(boolean value)
```


Указывает, следует ли встраивать ресурсы SVG в HTML-документ. Значение по умолчанию — true.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setExportFormFields(boolean value) {#setExportFormFields-boolean-}
```
public void setExportFormFields(boolean value)
```


Задает индикацию того, экспортируются ли поля формы как интерактивные элементы (как тег input), а не преобразуются в текст или графику.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Указание того, экспортируются ли поля формы как интерактивные элементы (как тег «ввод»), а не преобразуются в текст или графику. |

### setExportGeneratorName(boolean value) {#setExportGeneratorName-boolean-}
```
public void setExportGeneratorName(boolean value)
```


 При значении true имя и версия Aspose.Words встраиваются в создаваемые файлы. Значение по умолчанию**true**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setFontFormat(int value) {#setFontFormat-int-}
```
public void setFontFormat(int value)
```


 Наборы[ExportFontFormat](../../com.aspose.words/exportfontformat) используется для экспорта шрифтов. Значение по умолчанию[ExportFontFormat.WOFF](../../com.aspose.words/exportfontformat\#WOFF).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | \{[ExportFontFormat](../../com.aspose.words/exportfontformat) используется для экспорта шрифтов. Значение должно быть одним из[ExportFontFormat](../../com.aspose.words/exportfontformat) константы. |

### setImlRenderingMode(int value) {#setImlRenderingMode-int-}
```
public void setImlRenderingMode(int value)
```


 Задает значение, определяющее способ визуализации объектов рукописного ввода (InkML). Значение по умолчанию[ImlRenderingMode.INK\_ML](../../com.aspose.words/imlrenderingmode\#INK-ML).

Это свойство используется, когда документ экспортируется в фиксированные форматы страниц.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Значение, определяющее способ визуализации объектов рукописного ввода (InkML). Значение должно быть одним из[ImlRenderingMode](../../com.aspose.words/imlrenderingmode) константы. |

### setJpegQuality(int value) {#setJpegQuality-int-}
```
public void setJpegQuality(int value)
```


Задает значение, определяющее качество изображений JPEG внутри HTML-документа.

Действует, только если документ содержит изображения JPEG.

Используйте это свойство, чтобы получить или установить качество изображений внутри документа при сохранении в фиксированном формате страницы. Значение может варьироваться от 0 до 100, где 0 означает худшее качество, но максимальное сжатие, а 100 — лучшее качество, но минимальное сжатие.

Значение по умолчанию — 95.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Значение, определяющее качество изображений JPEG внутри HTML-документа. |

### setMemoryOptimization(boolean value) {#setMemoryOptimization-boolean-}
```
public void setMemoryOptimization(boolean value)
```


 Задает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойства**false**. Установка для этого параметра значения true может значительно снизить потребление памяти при сохранении больших документов за счет замедления времени сохранения.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. |

### setMetafileRenderingOptions(MetafileRenderingOptions value) {#setMetafileRenderingOptions-com.aspose.words.MetafileRenderingOptions-}
```
public void setMetafileRenderingOptions(MetafileRenderingOptions value)
```


Позволяет указать параметры рендеринга метафайла.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions) |  Соответствующий[MetafileRenderingOptions](../../com.aspose.words/metafilerenderingoptions) ценность. |

### setNumeralFormat(int value) {#setNumeralFormat-int-}
```
public void setNumeralFormat(int value)
```


 Наборы[NumeralFormat](../../com.aspose.words/numeralformat) используется для отображения цифр. По умолчанию используются европейские цифры. Если значение этого свойства изменено, а макет страницы уже построен, то[Document.updatePageLayout()](../../com.aspose.words/document\#updatePageLayout--) вызывается автоматически для обновления любых изменений.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | \{[NumeralFormat](../../com.aspose.words/numeralformat) используется для отображения цифр. Значение должно быть одним из[NumeralFormat](../../com.aspose.words/numeralformat) константы. |

### setOptimizeOutput(boolean value) {#setOptimizeOutput-boolean-}
```
public void setOptimizeOutput(boolean value)
```


Флаг указывает, требуется ли оптимизация вывода. Если этот флаг установлен, удаляются избыточные вложенные холсты и пустые холсты, а также объединяются соседние глифы с одинаковым форматированием. Примечание. Точность отображения содержимого может быть снижена, если для этого свойства задано значение true. Значение по умолчанию верно.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setPageHorizontalAlignment(int value) {#setPageHorizontalAlignment-int-}
```
public void setPageHorizontalAlignment(int value)
```


Задает горизонтальное выравнивание страниц в HTML-документе. Значение по умолчанию — HtmlFixedHorizontalPageAlignment.Center .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[HtmlFixedPageHorizontalAlignment](../../com.aspose.words/htmlfixedpagehorizontalalignment) константы. |

### setPageMargins(double value) {#setPageMargins-double-}
```
public void setPageMargins(double value)
```


Задает поля вокруг страниц в HTML-документе. Значение поля измеряется в пунктах и должно быть больше или равно 0. Значение по умолчанию — 10 баллов.

 Зависит от значения[getPageHorizontalAlignment()](../../com.aspose.words/htmlfixedsaveoptions\#getPageHorizontalAlignment--) / [setPageHorizontalAlignment(int)](../../com.aspose.words/htmlfixedsaveoptions\#setPageHorizontalAlignment-int-) имущество:

 *   Определяет верхнее, нижнее и левое поля страницы, если значение[HtmlFixedPageHorizontalAlignment.LEFT](../../com.aspose.words/htmlfixedpagehorizontalalignment\#LEFT).
 *   Определяет верхнее, нижнее и правое поля страницы, если значение[HtmlFixedPageHorizontalAlignment.RIGHT](../../com.aspose.words/htmlfixedpagehorizontalalignment\#RIGHT).
 *   Определяет верхнее и нижнее поля страницы, если значение[HtmlFixedPageHorizontalAlignment.CENTER](../../com.aspose.words/htmlfixedpagehorizontalalignment\#CENTER).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | double | Соответствующее двойное значение. |

### setPageSavingCallback(IPageSavingCallback value) {#setPageSavingCallback-com.aspose.words.IPageSavingCallback-}
```
public void setPageSavingCallback(IPageSavingCallback value)
```


Позволяет управлять сохранением отдельных страниц при экспорте документа в фиксированный формат страницы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [IPageSavingCallback](../../com.aspose.words/ipagesavingcallback) |  Соответствующий[IPageSavingCallback](../../com.aspose.words/ipagesavingcallback) ценность. |

### setPageSet(PageSet value) {#setPageSet-com.aspose.words.PageSet-}
```
public void setPageSet(PageSet value)
```


Устанавливает страницы для отображения. По умолчанию это все страницы документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [PageSet](../../com.aspose.words/pageset) | Страницы для отображения. |

### setPrettyFormat(boolean value) {#setPrettyFormat-boolean-}
```
public void setPrettyFormat(boolean value)
```


 Когда true , красивые форматы выводятся там, где это применимо. Значение по умолчанию**false**.

 Установлен в**true** чтобы сделать вывод HTML, MHTML, EPUB, WordML, RTF, DOCX и ODT удобочитаемым для человека. Полезно для тестирования или отладки.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setProgressCallback(IDocumentSavingCallback value) {#setProgressCallback-com.aspose.words.IDocumentSavingCallback-}
```
public void setProgressCallback(IDocumentSavingCallback value)
```


Вызывается при сохранении документа и принимает данные о ходе сохранения.

 Прогресс сообщается при сохранении в[SaveFormat.DOCX](../../com.aspose.words/saveformat\#DOCX), [SaveFormat.FLAT\_OPC](../../com.aspose.words/saveformat\#FLAT-OPC), [SaveFormat.DOCM](../../com.aspose.words/saveformat\#DOCM), [SaveFormat.DOTM](../../com.aspose.words/saveformat\#DOTM), [SaveFormat.DOTX](../../com.aspose.words/saveformat\#DOTX), [SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB), [SaveFormat.XAML\_FLOW](../../com.aspose.words/saveformat\#XAML-FLOW) , или же[SaveFormat.XAML\_FLOW\_PACK](../../com.aspose.words/saveformat\#XAML-FLOW-PACK).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback) |  Соответствующий[IDocumentSavingCallback](../../com.aspose.words/idocumentsavingcallback) ценность. |

### setResourceSavingCallback(IResourceSavingCallback value) {#setResourceSavingCallback-com.aspose.words.IResourceSavingCallback-}
```
public void setResourceSavingCallback(IResourceSavingCallback value)
```


Позволяет управлять сохранением ресурсов (изображений, шрифтов и css) при экспорте документа в фиксированный формат страницы Html.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [IResourceSavingCallback](../../com.aspose.words/iresourcesavingcallback) |  Соответствующий[IResourceSavingCallback](../../com.aspose.words/iresourcesavingcallback) ценность. |

### setResourcesFolder(String value) {#setResourcesFolder-java.lang.String-}
```
public void setResourcesFolder(String value)
```


Указывает физическую папку, в которой сохраняются ресурсы (изображения, шрифты, css) при экспорте документа в формат Html. Значение по умолчанию равно нулю.

 Имеет эффект, только если[getExportEmbeddedImages()](../../com.aspose.words/htmlfixedsaveoptions\#getExportEmbeddedImages--) / [setExportEmbeddedImages(boolean)](../../com.aspose.words/htmlfixedsaveoptions\#setExportEmbeddedImages-boolean-) свойство ложно.

 Когда вы сохраняете[Document](../../com.aspose.words/document) в формате Html Aspose.Words должен сохранять все изображения, встроенные в документ, как отдельные файлы.[getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolder-java.lang.String-) позволяет указать, где изображения будут сохранены и[getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolderAlias--) / [setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolderAlias-java.lang.String-) позволяет указать, как будут создаваться URI изображения.

Если вы сохраняете документ в файл и указываете имя файла, Aspose.Words по умолчанию сохраняет изображения в той же папке, где сохранен файл документа. Использовать[getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolder-java.lang.String-) переопределить это поведение.

 Если вы сохраняете документ в потоке, Aspose.Words не имеет папки для сохранения изображений, но все же необходимо где-то сохранять изображения. В этом случае вам нужно указать доступную папку с помощью[getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolder-java.lang.String-) имущество

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setResourcesFolderAlias(String value) {#setResourcesFolderAlias-java.lang.String-}
```
public void setResourcesFolderAlias(String value)
```


Указывает имя папки, используемой для создания URI изображений, записываемых в HTML-документ. Значение по умолчанию равно нулю.

 Когда вы сохраняете[Document](../../com.aspose.words/document) в формате Html Aspose.Words должен сохранять все изображения, встроенные в документ, как отдельные файлы.[getResourcesFolder()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolder--) / [setResourcesFolder(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolder-java.lang.String-) позволяет указать, где изображения будут сохранены и[getResourcesFolderAlias()](../../com.aspose.words/htmlfixedsaveoptions\#getResourcesFolderAlias--) / [setResourcesFolderAlias(java.lang.String)](../../com.aspose.words/htmlfixedsaveoptions\#setResourcesFolderAlias-java.lang.String-) позволяет указать, как будут создаваться URI изображения.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setSaveFontFaceCssSeparately(boolean value) {#setSaveFontFaceCssSeparately-boolean-}
```
public void setSaveFontFaceCssSeparately(boolean value)
```


 Флаг указывает, следует ли помещать правила CSS "@font-face" в отдельный файл "fontFaces.css" при сохранении документа с внешней таблицей стилей (т.[getExportEmbeddedCss()](../../com.aspose.words/htmlfixedsaveoptions\#getExportEmbeddedCss--) / [setExportEmbeddedCss(boolean)](../../com.aspose.words/htmlfixedsaveoptions\#setExportEmbeddedCss-boolean-) является ложным). Значение по умолчанию — false , все правила CSS записываются в один файл «styles.css». Установка для этого свойства значения true восстанавливает старое поведение (отдельные файлы) для совместимости с устаревшим кодом.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setSaveFormat(int value) {#setSaveFormat-int-}
```
public void setSaveFormat(int value)
```


 Указывает формат, в котором будет сохранен документ, если используется этот объект параметров сохранения. Может быть только[SaveFormat.HTML\_FIXED](../../com.aspose.words/saveformat\#HTML-FIXED).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[SaveFormat](../../com.aspose.words/saveformat) константы. |

### setShowPageBorder(boolean value) {#setShowPageBorder-boolean-}
```
public void setShowPageBorder(boolean value)
```


Указывает, следует ли отображать границу вокруг страниц. По умолчанию верно.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setTempFolder(String value) {#setTempFolder-java.lang.String-}
```
public void setTempFolder(String value)
```


Указывает папку для временных файлов, используемых при сохранении в файл DOC или DOCX. По умолчанию это свойство имеет значение null, и временные файлы не используются.

Когда Aspose.Words сохраняет документ, ему необходимо создать временные внутренние структуры. По умолчанию эти внутренние структуры создаются в памяти, и использование памяти резко возрастает в течение короткого периода времени, пока документ сохраняется. Когда сохранение завершено, память освобождается и утилизируется сборщиком мусора.

 Если вы сохраняете очень большой документ (тысячи страниц) и/или обрабатываете много документов одновременно, скачок памяти во время сохранения может быть достаточно значительным, чтобы система выдала исключение java.lang.IndexOutOfBoundsException. Указание временной папки с помощью[getTempFolder()](../../com.aspose.words/saveoptions\#getTempFolder--) / [setTempFolder(java.lang.String)](../../com.aspose.words/saveoptions\#setTempFolder-java.lang.String-)приведет к тому, что Aspose.Words будет хранить внутренние структуры во временных файлах, а не в памяти. Это уменьшает использование памяти во время сохранения, но снижает производительность сохранения.

Папка должна существовать и быть доступной для записи, иначе будет выдано исключение.

Aspose.Words автоматически удаляет все временные файлы после завершения сохранения.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setUpdateCreatedTimeProperty(boolean value) {#setUpdateCreatedTimeProperty-boolean-}
```
public void setUpdateCreatedTimeProperty(boolean value)
```


 Устанавливает значение, определяющее, будет ли[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-) свойство обновляется перед сохранением. Значение по умолчанию — ложь;

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean |  Значение, определяющее, является ли[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-) свойство обновляется перед сохранением. |

### setUpdateFields(boolean value) {#setUpdateFields-boolean-}
```
public void setUpdateFields(boolean value)
```


Задает значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы. Значение по умолчанию для этого свойства**true**. Позволяет указать, следует ли имитировать поведение MS Word.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы. |

### setUpdateLastPrintedProperty(boolean value) {#setUpdateLastPrintedProperty-boolean-}
```
public void setUpdateLastPrintedProperty(boolean value)
```


 Устанавливает значение, определяющее, будет ли[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-) свойство обновляется перед сохранением.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean |  Значение, определяющее, является ли[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-) свойство обновляется перед сохранением. |

### setUpdateLastSavedTimeProperty(boolean value) {#setUpdateLastSavedTimeProperty-boolean-}
```
public void setUpdateLastSavedTimeProperty(boolean value)
```


 Устанавливает значение, определяющее, будет ли[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-) свойство обновляется перед сохранением.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean |  Значение, определяющее, является ли[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-) свойство обновляется перед сохранением. |

### setUpdateSdtContent(boolean value) {#setUpdateSdtContent-boolean-}
```
public void setUpdateSdtContent(boolean value)
```


 Устанавливает значение, определяющее, будет ли содержимое[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) обновляется перед сохранением. Значение по умолчанию неверно .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean |  Значение, определяющее, является ли содержание[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) обновляется перед сохранением. |

### setUseAntiAliasing(boolean value) {#setUseAntiAliasing-boolean-}
```
public void setUseAntiAliasing(boolean value)
```


Задает значение, определяющее, следует ли использовать сглаживание для рендеринга.

Значение по умолчанию неверно . Когда для этого значения установлено значение true, для рендеринга используется сглаживание.

Это свойство используется, когда документ экспортируется в следующие форматы:[SaveFormat.TIFF](../../com.aspose.words/saveformat\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat\#EMF) . Когда документ экспортируется в[SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB) а также[SaveFormat.AZW\_3](../../com.aspose.words/saveformat\#AZW-3) форматы эта опция используется для растровых изображений.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, определяющее, следует ли использовать сглаживание для рендеринга. |

### setUseHighQualityRendering(boolean value) {#setUseHighQualityRendering-boolean-}
```
public void setUseHighQualityRendering(boolean value)
```


Устанавливает значение, определяющее, следует ли использовать высококачественные (т.е. медленные) алгоритмы рендеринга. Значение по умолчанию неверно .

 Это свойство используется, когда документ экспортируется в форматы изображений:[SaveFormat.TIFF](../../com.aspose.words/saveformat\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat\#EMF).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, определяющее, следует ли использовать высокое качество (т.е. |

### setUseTargetMachineFonts(boolean value) {#setUseTargetMachineFonts-boolean-}
```
public void setUseTargetMachineFonts(boolean value)
```


Флаг указывает, должны ли шрифты с целевой машины использоваться для отображения документа. Если этот флаг установлен в значение true,[getFontFormat()](../../com.aspose.words/htmlfixedsaveoptions\#getFontFormat--) / [setFontFormat(int)](../../com.aspose.words/htmlfixedsaveoptions\#setFontFormat-int-) а также[getExportEmbeddedFonts()](../../com.aspose.words/htmlfixedsaveoptions\#getExportEmbeddedFonts--) / [setExportEmbeddedFonts(boolean)](../../com.aspose.words/htmlfixedsaveoptions\#setExportEmbeddedFonts-boolean-) свойства также не действуют[getResourceSavingCallback()](../../com.aspose.words/htmlfixedsaveoptions\#getResourceSavingCallback--) / [setResourceSavingCallback(com.aspose.words.IResourceSavingCallback)](../../com.aspose.words/htmlfixedsaveoptions\#setResourceSavingCallback-com.aspose.words.IResourceSavingCallback-) не срабатывает для шрифтов. Значение по умолчанию — ложь.

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
