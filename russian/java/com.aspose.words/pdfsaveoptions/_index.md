---
title: PdfSaveOptions
second_title: Справочник по API Aspose.Words для Java
description: Может использоваться для указания дополнительных параметров при сохранении документа в формате.
type: docs
weight: 461
url: /ru/java/com.aspose.words/pdfsaveoptions/
---

**Наследование:**
java.lang.Object, [com.aspose.words.SaveOptions](../../com.aspose.words/saveoptions), [com.aspose.words.FixedPageSaveOptions](../../com.aspose.words/fixedpagesaveoptions)

**Все реализованные интерфейсы:**
java.lang.Cloneable
```
public class PdfSaveOptions extends FixedPageSaveOptions implements Cloneable
```

 Может использоваться для указания дополнительных параметров при сохранении документа в[SaveFormat.PDF](../../com.aspose.words/saveformat\#PDF) формат.

 Чтобы узнать больше, посетите**Specify Save Options** документальная статья.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [PdfSaveOptions()](#PdfSaveOptions--) |  Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа в[SaveFormat.PDF](../../com.aspose.words/saveformat\#PDF) формат. |
## Методы

| Метод | Описание |
| --- | --- |
| [createSaveOptions(int saveFormat)](#createSaveOptions-int-) |  |
| [createSaveOptions(String fileName)](#createSaveOptions-java.lang.String-) | Создает объект параметров сохранения класса, подходящего для расширения файла, указанного в данном имени файла. |
| [deepClone()](#deepClone--) | Создает глубокий клон этого объекта. |
| [equals(Object obj)](#equals-java.lang.Object-) | Определяет, равен ли указанный объект по значению текущему объекту. |
| [getAdditionalTextPositioning()](#getAdditionalTextPositioning--) | Флаг, указывающий, следует ли писать дополнительные операторы позиционирования текста или нет. |
| [getAllowEmbeddingPostScriptFonts()](#getAllowEmbeddingPostScriptFonts--) | Получает логическое значение, указывающее, разрешать ли встраивание шрифтов с контурами PostScript при встраивании шрифтов TrueType в документ после его сохранения. |
| [getCacheHeaderFooterShapes()](#getCacheHeaderFooterShapes--) | Получает значение, определяющее, следует ли кэшировать фигуры, помещенные в верхний и нижний колонтитулы документа. |
| [getClass()](#getClass--) |  |
| [getColorMode()](#getColorMode--) | Получает значение, определяющее способ отображения цветов. |
| [getCompliance()](#getCompliance--) | Указывает уровень соответствия стандартам PDF для выходных документов. |
| [getCreateNoteHyperlinks()](#getCreateNoteHyperlinks--) | Указывает, следует ли преобразовывать ссылки сносок/концевых сносок в основном текстовом материале в активные гиперссылки. |
| [getCustomPropertiesExport()](#getCustomPropertiesExport--) |  Получает значение, определяющее способ[Document.getCustomDocumentProperties()](../../com.aspose.words/document\#getCustomDocumentProperties--) экспортируются в файл PDF. |
| [getDefaultTemplate()](#getDefaultTemplate--) | Получает путь к шаблону по умолчанию (включая имя файла). |
| [getDigitalSignatureDetails()](#getDigitalSignatureDetails--) | Получает сведения для подписания выходного PDF-документа. |
| [getDisplayDocTitle()](#getDisplayDocTitle--) | Флаг, указывающий, будет ли окно\В строке заголовка должно отображаться название документа, взятое из записи Title словаря информации о документе. |
| [getDml3DEffectsRenderingMode()](#getDml3DEffectsRenderingMode--) | Получает значение, определяющее способ визуализации 3D-эффектов. |
| [getDmlEffectsRenderingMode()](#getDmlEffectsRenderingMode--) | Получает значение, определяющее способ визуализации эффектов DrawingML. |
| [getDmlRenderingMode()](#getDmlRenderingMode--) | Получает значение, определяющее способ отображения фигур DrawingML. |
| [getDownsampleOptions()](#getDownsampleOptions--) | Позволяет указать параметры понижающей дискретизации. |
| [getEmbedFullFonts()](#getEmbedFullFonts--) | Управляет тем, как шрифты внедряются в результирующие PDF-документы. |
| [getEncryptionDetails()](#getEncryptionDetails--) | Получает сведения о шифровании выходного PDF-документа. |
| [getExportDocumentStructure()](#getExportDocumentStructure--) | Получает значение, определяющее, следует ли экспортировать структуру документа. |
| [getExportGeneratorName()](#getExportGeneratorName--) | При значении true имя и версия Aspose.Words встраиваются в создаваемые файлы. |
| [getExportLanguageToSpanTag()](#getExportLanguageToSpanTag--) | Получает значение, определяющее, следует ли создавать тег «Span» в структуре документа для экспорта языка текста. |
| [getFontEmbeddingMode()](#getFontEmbeddingMode--) | Задает режим внедрения шрифта. |
| [getHeaderFooterBookmarksExportMode()](#getHeaderFooterBookmarksExportMode--) | Определяет, как экспортируются закладки в верхних/нижних колонтитулах. |
| [getImageColorSpaceExportMode()](#getImageColorSpaceExportMode--) | Указывает, как цветовое пространство будет выбрано для изображений в документе PDF. |
| [getImageCompression()](#getImageCompression--) | Указывает тип сжатия, который будет использоваться для всех изображений в документе. |
| [getImlRenderingMode()](#getImlRenderingMode--) | Получает значение, определяющее способ визуализации объектов рукописного ввода (InkML). |
| [getInterpolateImages()](#getInterpolateImages--) | Флаг, указывающий, должна ли интерполяция изображения выполняться соответствующим считывающим устройством. |
| [getJpegQuality()](#getJpegQuality--) | Получает значение, определяющее качество изображений JPEG внутри документа PDF. |
| [getMemoryOptimization()](#getMemoryOptimization--) | Получает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. |
| [getMetafileRenderingOptions()](#getMetafileRenderingOptions--) | Позволяет указать параметры рендеринга метафайла. |
| [getNumeralFormat()](#getNumeralFormat--) |  Получает[NumeralFormat](../../com.aspose.words/numeralformat) используется для отображения цифр. |
| [getOpenHyperlinksInNewWindow()](#getOpenHyperlinksInNewWindow--) | Получает значение, определяющее, будут ли гиперссылки в выходном документе Pdf принудительно открываться в новом окне (или вкладке) браузера. |
| [getOptimizeOutput()](#getOptimizeOutput--) | Флаг указывает, требуется ли оптимизация вывода. |
| [getOutlineOptions()](#getOutlineOptions--) | Позволяет указать параметры контура. |
| [getPageMode()](#getPageMode--) | Указывает, как документ PDF должен отображаться при открытии в программе чтения PDF. |
| [getPageSavingCallback()](#getPageSavingCallback--) | Позволяет управлять сохранением отдельных страниц при экспорте документа в фиксированный формат страницы. |
| [getPageSet()](#getPageSet--) | Получает страницы для отображения. |
| [getPreblendImages()](#getPreblendImages--) | Получает значение, определяющее, следует ли предварительно смешивать прозрачные изображения с черным цветом фона. |
| [getPreserveFormFields()](#getPreserveFormFields--) | Указывает, сохранять ли поля формы Microsoft Word как поля формы в формате PDF или преобразовывать их в текст. |
| [getPrettyFormat()](#getPrettyFormat--) | Когда true , красивые форматы выводятся там, где это применимо. |
| [getProgressCallback()](#getProgressCallback--) | Вызывается при сохранении документа и принимает данные о ходе сохранения. |
| [getSaveFormat()](#getSaveFormat--) | Указывает формат, в котором будет сохранен документ, если используется этот объект параметров сохранения. |
| [getTempFolder()](#getTempFolder--) | Указывает папку для временных файлов, используемых при сохранении в файл DOC или DOCX. |
| [getTextCompression()](#getTextCompression--) | Указывает тип сжатия, который будет использоваться для всего текстового содержимого в документе. |
| [getUpdateCreatedTimeProperty()](#getUpdateCreatedTimeProperty--) |  Получает значение, определяющее, является ли[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-) свойство обновляется перед сохранением. |
| [getUpdateFields()](#getUpdateFields--) | Получает значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы. |
| [getUpdateLastPrintedProperty()](#getUpdateLastPrintedProperty--) |  Получает значение, определяющее, является ли[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-) свойство обновляется перед сохранением. |
| [getUpdateLastSavedTimeProperty()](#getUpdateLastSavedTimeProperty--) |  Получает значение, определяющее, является ли[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-) свойство обновляется перед сохранением. |
| [getUpdateSdtContent()](#getUpdateSdtContent--) |  Получает значение, определяющее, будет ли содержимое[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) обновляется перед сохранением. |
| [getUseAntiAliasing()](#getUseAntiAliasing--) | Получает значение, определяющее, следует ли использовать сглаживание для рендеринга. |
| [getUseBookFoldPrintingSettings()](#getUseBookFoldPrintingSettings--) |  Получает логическое значение, указывающее, следует ли сохранять документ с использованием макета печати буклета, если он указан через[PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup\#getMultiplePages--) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup\#setMultiplePages-int-). |
| [getUseCoreFonts()](#getUseCoreFonts--) | Получает значение, определяющее, следует ли заменять шрифты TrueType Arial, Times New Roman, Courier New и Symbol базовыми шрифтами PDF Type 1. |
| [getUseHighQualityRendering()](#getUseHighQualityRendering--) | Получает значение, определяющее, следует ли использовать высокое качество (т. е. |
| [getZoomBehavior()](#getZoomBehavior--) | Получает значение, определяющее, какой тип масштабирования следует применять при открытии документа в средстве просмотра PDF. |
| [getZoomFactor()](#getZoomFactor--) | Получает значение, определяющее коэффициент масштабирования (в процентах) для документа. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setAdditionalTextPositioning(boolean value)](#setAdditionalTextPositioning-boolean-) | Флаг, указывающий, следует ли писать дополнительные операторы позиционирования текста или нет. |
| [setAllowEmbeddingPostScriptFonts(boolean value)](#setAllowEmbeddingPostScriptFonts-boolean-) | Задает логическое значение, указывающее, разрешать ли встраивание шрифтов с контурами PostScript при встраивании шрифтов TrueType в документ после его сохранения. |
| [setCacheHeaderFooterShapes(boolean value)](#setCacheHeaderFooterShapes-boolean-) | Задает значение, определяющее, следует ли кэшировать фигуры, размещенные в верхнем и нижнем колонтитулах документа. |
| [setColorMode(int value)](#setColorMode-int-) | Задает значение, определяющее способ отображения цветов. |
| [setCompliance(int value)](#setCompliance-int-) | Указывает уровень соответствия стандартам PDF для выходных документов. |
| [setCreateNoteHyperlinks(boolean value)](#setCreateNoteHyperlinks-boolean-) | Указывает, следует ли преобразовывать ссылки сносок/концевых сносок в основном текстовом материале в активные гиперссылки. |
| [setCustomPropertiesExport(int value)](#setCustomPropertiesExport-int-) |  Устанавливает значение, определяющее способ[Document.getCustomDocumentProperties()](../../com.aspose.words/document\#getCustomDocumentProperties--) экспортируются в файл PDF. |
| [setDefaultTemplate(String value)](#setDefaultTemplate-java.lang.String-) | Устанавливает путь к шаблону по умолчанию (включая имя файла). |
| [setDigitalSignatureDetails(PdfDigitalSignatureDetails value)](#setDigitalSignatureDetails-com.aspose.words.PdfDigitalSignatureDetails-) | Устанавливает детали для подписания выходного PDF-документа. |
| [setDisplayDocTitle(boolean value)](#setDisplayDocTitle-boolean-) | Флаг, указывающий, будет ли окно\В строке заголовка должно отображаться название документа, взятое из записи Title словаря информации о документе. |
| [setDml3DEffectsRenderingMode(int value)](#setDml3DEffectsRenderingMode-int-) | Задает значение, определяющее способ визуализации 3D-эффектов. |
| [setDmlEffectsRenderingMode(int value)](#setDmlEffectsRenderingMode-int-) | Задает значение, определяющее, как визуализируются эффекты DrawingML. |
| [setDmlRenderingMode(int value)](#setDmlRenderingMode-int-) | Задает значение, определяющее, как отображаются фигуры DrawingML. |
| [setDownsampleOptions(DownsampleOptions value)](#setDownsampleOptions-com.aspose.words.DownsampleOptions-) | Позволяет указать параметры понижающей дискретизации. |
| [setEmbedFullFonts(boolean value)](#setEmbedFullFonts-boolean-) | Управляет тем, как шрифты внедряются в результирующие PDF-документы. |
| [setEncryptionDetails(PdfEncryptionDetails value)](#setEncryptionDetails-com.aspose.words.PdfEncryptionDetails-) | Задает детали для шифрования выходного PDF-документа. |
| [setExportDocumentStructure(boolean value)](#setExportDocumentStructure-boolean-) | Задает значение, определяющее, экспортировать структуру документа или нет. |
| [setExportGeneratorName(boolean value)](#setExportGeneratorName-boolean-) | При значении true имя и версия Aspose.Words встраиваются в создаваемые файлы. |
| [setExportLanguageToSpanTag(boolean value)](#setExportLanguageToSpanTag-boolean-) | Задает значение, определяющее, следует ли создавать тег «Span» в структуре документа для экспорта языка текста. |
| [setFontEmbeddingMode(int value)](#setFontEmbeddingMode-int-) | Задает режим внедрения шрифта. |
| [setHeaderFooterBookmarksExportMode(int value)](#setHeaderFooterBookmarksExportMode-int-) | Определяет, как экспортируются закладки в верхних/нижних колонтитулах. |
| [setImageColorSpaceExportMode(int value)](#setImageColorSpaceExportMode-int-) | Указывает, как цветовое пространство будет выбрано для изображений в документе PDF. |
| [setImageCompression(int value)](#setImageCompression-int-) | Указывает тип сжатия, который будет использоваться для всех изображений в документе. |
| [setImlRenderingMode(int value)](#setImlRenderingMode-int-) | Задает значение, определяющее способ визуализации объектов рукописного ввода (InkML). |
| [setInterpolateImages(boolean value)](#setInterpolateImages-boolean-) | Флаг, указывающий, должна ли интерполяция изображения выполняться соответствующим считывающим устройством. |
| [setJpegQuality(int value)](#setJpegQuality-int-) | Задает значение, определяющее качество изображений JPEG внутри документа PDF. |
| [setMemoryOptimization(boolean value)](#setMemoryOptimization-boolean-) | Задает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. |
| [setMetafileRenderingOptions(MetafileRenderingOptions value)](#setMetafileRenderingOptions-com.aspose.words.MetafileRenderingOptions-) | Позволяет указать параметры рендеринга метафайла. |
| [setNumeralFormat(int value)](#setNumeralFormat-int-) |  Наборы[NumeralFormat](../../com.aspose.words/numeralformat) используется для отображения цифр. |
| [setOpenHyperlinksInNewWindow(boolean value)](#setOpenHyperlinksInNewWindow-boolean-) | Задает значение, определяющее, будут ли гиперссылки в выходном документе Pdf принудительно открываться в новом окне (или вкладке) браузера. |
| [setOptimizeOutput(boolean value)](#setOptimizeOutput-boolean-) | Флаг указывает, требуется ли оптимизация вывода. |
| [setPageMode(int value)](#setPageMode-int-) | Указывает, как документ PDF должен отображаться при открытии в программе чтения PDF. |
| [setPageSavingCallback(IPageSavingCallback value)](#setPageSavingCallback-com.aspose.words.IPageSavingCallback-) | Позволяет управлять сохранением отдельных страниц при экспорте документа в фиксированный формат страницы. |
| [setPageSet(PageSet value)](#setPageSet-com.aspose.words.PageSet-) | Устанавливает страницы для отображения. |
| [setPreblendImages(boolean value)](#setPreblendImages-boolean-) | Задает значение, определяющее, следует ли предварительно смешивать прозрачные изображения с черным цветом фона. |
| [setPreserveFormFields(boolean value)](#setPreserveFormFields-boolean-) | Указывает, сохранять ли поля формы Microsoft Word как поля формы в формате PDF или преобразовывать их в текст. |
| [setPrettyFormat(boolean value)](#setPrettyFormat-boolean-) | Когда true , красивые форматы выводятся там, где это применимо. |
| [setProgressCallback(IDocumentSavingCallback value)](#setProgressCallback-com.aspose.words.IDocumentSavingCallback-) | Вызывается при сохранении документа и принимает данные о ходе сохранения. |
| [setSaveFormat(int value)](#setSaveFormat-int-) | Указывает формат, в котором будет сохранен документ, если используется этот объект параметров сохранения. |
| [setTempFolder(String value)](#setTempFolder-java.lang.String-) | Указывает папку для временных файлов, используемых при сохранении в файл DOC или DOCX. |
| [setTextCompression(int value)](#setTextCompression-int-) | Указывает тип сжатия, который будет использоваться для всего текстового содержимого в документе. |
| [setUpdateCreatedTimeProperty(boolean value)](#setUpdateCreatedTimeProperty-boolean-) |  Устанавливает значение, определяющее, будет ли[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-) свойство обновляется перед сохранением. |
| [setUpdateFields(boolean value)](#setUpdateFields-boolean-) | Задает значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы. |
| [setUpdateLastPrintedProperty(boolean value)](#setUpdateLastPrintedProperty-boolean-) |  Устанавливает значение, определяющее, будет ли[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-) свойство обновляется перед сохранением. |
| [setUpdateLastSavedTimeProperty(boolean value)](#setUpdateLastSavedTimeProperty-boolean-) |  Устанавливает значение, определяющее, будет ли[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-) свойство обновляется перед сохранением. |
| [setUpdateSdtContent(boolean value)](#setUpdateSdtContent-boolean-) |  Устанавливает значение, определяющее, будет ли содержимое[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) обновляется перед сохранением. |
| [setUseAntiAliasing(boolean value)](#setUseAntiAliasing-boolean-) | Задает значение, определяющее, следует ли использовать сглаживание для рендеринга. |
| [setUseBookFoldPrintingSettings(boolean value)](#setUseBookFoldPrintingSettings-boolean-) |  Устанавливает логическое значение, указывающее, следует ли сохранять документ с использованием макета печати буклета, если он указан через[PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup\#getMultiplePages--) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup\#setMultiplePages-int-). |
| [setUseCoreFonts(boolean value)](#setUseCoreFonts-boolean-) | Задает значение, определяющее, следует ли заменять шрифты TrueType Arial, Times New Roman, Courier New и Symbol базовыми шрифтами PDF Type 1. |
| [setUseHighQualityRendering(boolean value)](#setUseHighQualityRendering-boolean-) | Устанавливает значение, определяющее, использовать ли высокое качество (т.е. |
| [setZoomBehavior(int value)](#setZoomBehavior-int-) | Задает значение, определяющее, какой тип масштабирования следует применять при открытии документа в программе просмотра PDF. |
| [setZoomFactor(int value)](#setZoomFactor-int-) | Задает значение, определяющее коэффициент масштабирования (в процентах) для документа. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### PdfSaveOptions() {#PdfSaveOptions--}
```
public PdfSaveOptions()
```


 Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа в[SaveFormat.PDF](../../com.aspose.words/saveformat\#PDF) формат.

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
### deepClone() {#deepClone--}
```
public PdfSaveOptions deepClone()
```


Создает глубокий клон этого объекта.

**Возвращает:**
[PdfSaveOptions](../../com.aspose.words/pdfsaveoptions)
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
### getAdditionalTextPositioning() {#getAdditionalTextPositioning--}
```
public boolean getAdditionalTextPositioning()
```


Флаг, указывающий, следует ли писать дополнительные операторы позиционирования текста или нет.

Если true , дополнительные операторы позиционирования текста записываются в выходной PDF-файл. Это может помочь решить проблемы с неточным позиционированием текста на некоторых принтерах. Недостатком является увеличенный размер PDF-документа.

Значение по умолчанию неверно .

**Возвращает:**
boolean - соответствующее логическое значение.
### getAllowEmbeddingPostScriptFonts() {#getAllowEmbeddingPostScriptFonts--}
```
public boolean getAllowEmbeddingPostScriptFonts()
```


Получает логическое значение, указывающее, разрешать ли встраивание шрифтов с контурами PostScript при встраивании шрифтов TrueType в документ после его сохранения. Значение по умолчанию**false**.

Обратите внимание: Word не встраивает шрифты PostScript, но может открывать документы со встроенными шрифтами этого типа.

 Этот вариант работает только тогда, когда[FontInfoCollection.getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection\#getEmbedTrueTypeFonts--) / [FontInfoCollection.setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection\#setEmbedTrueTypeFonts-boolean-) принадлежащий[DocumentBase.getFontInfos()](../../com.aspose.words/documentbase\#getFontInfos--) свойство имеет значение true .

**Возвращает:**
boolean — логическое значение, указывающее, разрешать ли встраивание шрифтов с контурами PostScript при встраивании шрифтов TrueType в документ после его сохранения.
### getCacheHeaderFooterShapes() {#getCacheHeaderFooterShapes--}
```
public boolean getCacheHeaderFooterShapes()
```


Получает значение, определяющее, следует ли кэшировать фигуры, помещенные в верхний и нижний колонтитулы документа.

Значение по умолчанию — false, и формы не кэшируются.

Когда значение равно true, графические фигуры записываются в документ PDF как xObject.

Некоторые фигуры не поддерживаются для кэширования (фигуры с полями, закладками, HRefs).

**Возвращает:**
логическое значение — значение, определяющее, следует ли кэшировать фигуры, размещенные в верхнем и нижнем колонтитулах документа.
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
### getCompliance() {#getCompliance--}
```
public int getCompliance()
```


Указывает уровень соответствия стандартам PDF для выходных документов.

 По умолчанию[PdfCompliance.PDF\_17](../../com.aspose.words/pdfcompliance\#PDF-17).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[PdfCompliance](../../com.aspose.words/pdfcompliance) константы.
### getCreateNoteHyperlinks() {#getCreateNoteHyperlinks--}
```
public boolean getCreateNoteHyperlinks()
```


Указывает, следует ли преобразовывать ссылки сносок/концевых сносок в основном текстовом материале в активные гиперссылки. При нажатии гиперссылка приведет к соответствующей сноске/концевой сноске. Значение по умолчанию — ложь.

**Возвращает:**
boolean - соответствующее логическое значение.
### getCustomPropertiesExport() {#getCustomPropertiesExport--}
```
public int getCustomPropertiesExport()
```


 Получает значение, определяющее способ[Document.getCustomDocumentProperties()](../../com.aspose.words/document\#getCustomDocumentProperties--) экспортируются в файл PDF.

 Значение по умолчанию[PdfCustomPropertiesExport.NONE](../../com.aspose.words/pdfcustompropertiesexport\#NONE).

[PdfCustomPropertiesExport.METADATA](../../com.aspose.words/pdfcustompropertiesexport\#METADATA) значение не поддерживается при сохранении в PDF/A.[PdfCustomPropertiesExport.STANDARD](../../com.aspose.words/pdfcustompropertiesexport\#STANDARD) вместо этого будет использоваться для PDF/A-1 и PDF/A-2 и[PdfCustomPropertiesExport.NONE](../../com.aspose.words/pdfcustompropertiesexport\#NONE) для PDF/A-4.

[PdfCustomPropertiesExport.STANDARD](../../com.aspose.words/pdfcustompropertiesexport\#STANDARD) значение не поддерживается при сохранении в PDF 2.0.[PdfCustomPropertiesExport.METADATA](../../com.aspose.words/pdfcustompropertiesexport\#METADATA) вместо этого будет использоваться.

**Возвращает:**
int - значение, определяющее способ[Document.getCustomDocumentProperties()](../../com.aspose.words/document\#getCustomDocumentProperties--) экспортируются в файл PDF. Возвращаемое значение является одним из[PdfCustomPropertiesExport](../../com.aspose.words/pdfcustompropertiesexport) константы.
### getDefaultTemplate() {#getDefaultTemplate--}
```
public String getDefaultTemplate()
```


 Получает путь к шаблону по умолчанию (включая имя файла). Значение по умолчанию для этого свойства**empty string** . Если указано, этот путь используется для загрузки шаблона, когда[Document.getAutomaticallyUpdateStyles()](../../com.aspose.words/document\#getAutomaticallyUpdateStyles--) / [Document.setAutomaticallyUpdateStyles(boolean)](../../com.aspose.words/document\#setAutomaticallyUpdateStyles-boolean-) правда, но[Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate--) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String-) пустой.

**Возвращает:**
java.lang.String — путь к шаблону по умолчанию (включая имя файла).
### getDigitalSignatureDetails() {#getDigitalSignatureDetails--}
```
public PdfDigitalSignatureDetails getDigitalSignatureDetails()
```


Получает сведения для подписания выходного PDF-документа.

 Значение по умолчанию равно null, и выходной документ не будет подписан. Когда для этого свойства задано допустимое значение[PdfDigitalSignatureDetails](../../com.aspose.words/pdfdigitalsignaturedetails) объект, то выходной PDF-документ будет подписан цифровой подписью.

**Возвращает:**
[PdfDigitalSignatureDetails](../../com.aspose.words/pdfdigitalsignaturedetails) - Детали для подписания выходного PDF-документа.
### getDisplayDocTitle() {#getDisplayDocTitle--}
```
public boolean getDisplayDocTitle()
```


Флаг, указывающий, будет ли окно\В строке заголовка должно отображаться название документа, взятое из записи Title словаря информации о документе.

Если false , вместо этого в строке заголовка должно отображаться имя файла PDF, содержащего документ.

Этот флаг требуется для соответствия PDF/UA. значение true будет использоваться автоматически при сохранении в PDF/UA.

Значение по умолчанию неверно .

**Возвращает:**
boolean - соответствующее логическое значение.
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

 Если[getCompliance()](../../com.aspose.words/pdfsaveoptions\#getCompliance--) / [setCompliance(int)](../../com.aspose.words/pdfsaveoptions\#setCompliance-int-) установлен на[PdfCompliance.PDF\_A\_1\_A](../../com.aspose.words/pdfcompliance\#PDF-A-1-A) или же[PdfCompliance.PDF\_A\_1\_B](../../com.aspose.words/pdfcompliance\#PDF-A-1-B) , свойство всегда возвращает[DmlEffectsRenderingMode.NONE](../../com.aspose.words/dmleffectsrenderingmode\#NONE).

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
### getDownsampleOptions() {#getDownsampleOptions--}
```
public DownsampleOptions getDownsampleOptions()
```


Позволяет указать параметры понижающей дискретизации.

**Возвращает:**
[DownsampleOptions](../../com.aspose.words/downsampleoptions) - соответствующий[DownsampleOptions](../../com.aspose.words/downsampleoptions) ценность.
### getEmbedFullFonts() {#getEmbedFullFonts--}
```
public boolean getEmbedFullFonts()
```


Управляет тем, как шрифты внедряются в результирующие PDF-документы.

Значение по умолчанию — false , что означает, что шрифты подмножаются перед внедрением. Подмножество полезно, если вы хотите уменьшить размер выходного файла. Подмножество удаляет все неиспользуемые глифы из шрифта.

Если для этого параметра задано значение true , в PDF-файл встраивается полный файл шрифта без подмножества. Это приведет к увеличению размера выходных файлов, но может быть полезной опцией, если вы хотите позже отредактировать полученный PDF-файл (например, добавить больше текста).

Некоторые шрифты большие (несколько мегабайт), и их встраивание без подмножества приведет к большим выходным документам.

**Возвращает:**
boolean - соответствующее логическое значение.
### getEncryptionDetails() {#getEncryptionDetails--}
```
public PdfEncryptionDetails getEncryptionDetails()
```


Получает сведения о шифровании выходного PDF-документа.

 Значение по умолчанию равно null, и выходной документ не будет зашифрован. Когда для этого свойства задано допустимое значение[PdfEncryptionDetails](../../com.aspose.words/pdfencryptiondetails) объект, то выходной PDF-документ будет зашифрован.

Алгоритм шифрования AES-128 используется при сохранении в формате PDF 1.7 (включая PDF/UA-1). Алгоритм шифрования AES-256 используется при сохранении в формате PDF 2.0.

Шифрование запрещено соответствием PDF/A. Этот параметр будет игнорироваться при сохранении в PDF/A.

[PdfPermissions.CONTENT\_COPY\_FOR\_ACCESSIBILITY](../../com.aspose.words/pdfpermissions\#CONTENT-COPY-FOR-ACCESSIBILITY) разрешение требуется в соответствии с PDF/UA, если выходной документ зашифрован. Это разрешение будет автоматически использоваться при сохранении в PDF/UA.

[PdfPermissions.CONTENT\_COPY\_FOR\_ACCESSIBILITY](../../com.aspose.words/pdfpermissions\#CONTENT-COPY-FOR-ACCESSIBILITY)разрешение устарело в формате PDF 2.0. Это разрешение будет игнорироваться при сохранении в PDF 2.0.

**Возвращает:**
[PdfEncryptionDetails](../../com.aspose.words/pdfencryptiondetails) - Подробная информация о шифровании выходного PDF-документа.
### getExportDocumentStructure() {#getExportDocumentStructure--}
```
public boolean getExportDocumentStructure()
```


Получает значение, определяющее, следует ли экспортировать структуру документа.

Это значение игнорируется при сохранении в форматах PDF/A-1a, PDF/A-2a и PDF/UA-1, поскольку для этого соответствия требуется структура документа.

Обратите внимание, что экспорт структуры документа значительно увеличивает потребление памяти, особенно для больших документов.

**Возвращает:**
логическое значение — значение, определяющее, следует ли экспортировать структуру документа.
### getExportGeneratorName() {#getExportGeneratorName--}
```
public boolean getExportGeneratorName()
```


 При значении true имя и версия Aspose.Words встраиваются в создаваемые файлы. Значение по умолчанию**true**.

**Возвращает:**
boolean - соответствующее логическое значение.
### getExportLanguageToSpanTag() {#getExportLanguageToSpanTag--}
```
public boolean getExportLanguageToSpanTag()
```


Получает значение, определяющее, следует ли создавать тег «Span» в структуре документа для экспорта языка текста.

Значение по умолчанию — false, а атрибут «Lang» прикрепляется к последовательности отмеченного содержимого в потоке содержимого страницы.

Когда значение равно true, для текста с нестандартным языком создается тег «Span», и к этому тегу прикрепляется атрибут «Lang».

 Это значение игнорируется, когда[getExportDocumentStructure()](../../com.aspose.words/pdfsaveoptions\#getExportDocumentStructure--) / [setExportDocumentStructure(boolean)](../../com.aspose.words/pdfsaveoptions\#setExportDocumentStructure-boolean-) является ложным.

**Возвращает:**
логическое значение — значение, определяющее, следует ли создавать тег «Span» в структуре документа для экспорта языка текста.
### getFontEmbeddingMode() {#getFontEmbeddingMode--}
```
public int getFontEmbeddingMode()
```


Задает режим внедрения шрифта.

 Значение по умолчанию[PdfFontEmbeddingMode.EMBED\_ALL](../../com.aspose.words/pdffontembeddingmode\#EMBED-ALL).

Этот параметр работает только для текста в кодировке ANSI (Windows-1252). Если документ содержит текст, отличный от ANSI, соответствующие шрифты будут встроены независимо от этого параметра.

 Соответствие форматам PDF/A и PDF/UA требует внедрения всех шрифтов.[PdfFontEmbeddingMode.EMBED\_ALL](../../com.aspose.words/pdffontembeddingmode\#EMBED-ALL) значение будет использоваться автоматически при сохранении в PDF/A и PDF/UA.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[PdfFontEmbeddingMode](../../com.aspose.words/pdffontembeddingmode) константы.
### getHeaderFooterBookmarksExportMode() {#getHeaderFooterBookmarksExportMode--}
```
public int getHeaderFooterBookmarksExportMode()
```


Определяет, как экспортируются закладки в верхних/нижних колонтитулах.

 Значение по умолчанию[HeaderFooterBookmarksExportMode.ALL](../../com.aspose.words/headerfooterbookmarksexportmode\#ALL).

 Это свойство используется совместно с[getOutlineOptions()](../../com.aspose.words/pdfsaveoptions\#getOutlineOptions--) вариант.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[HeaderFooterBookmarksExportMode](../../com.aspose.words/headerfooterbookmarksexportmode) константы.
### getImageColorSpaceExportMode() {#getImageColorSpaceExportMode--}
```
public int getImageColorSpaceExportMode()
```


Указывает, как цветовое пространство будет выбрано для изображений в документе PDF.

 Значение по умолчанию[PdfImageColorSpaceExportMode.AUTO](../../com.aspose.words/pdfimagecolorspaceexportmode\#AUTO).

 Если[PdfImageColorSpaceExportMode.SIMPLE\_CMYK](../../com.aspose.words/pdfimagecolorspaceexportmode\#SIMPLE-CMYK) указано значение,[getImageCompression()](../../com.aspose.words/pdfsaveoptions\#getImageCompression--) / [setImageCompression(int)](../../com.aspose.words/pdfsaveoptions\#setImageCompression-int-) параметр игнорируется, и для всех изображений в документе используется сжатие Flate.

[PdfImageColorSpaceExportMode.SIMPLE\_CMYK](../../com.aspose.words/pdfimagecolorspaceexportmode\#SIMPLE-CMYK) значение не поддерживается при сохранении в PDF/A.[PdfImageColorSpaceExportMode.AUTO](../../com.aspose.words/pdfimagecolorspaceexportmode\#AUTO) вместо этого будет использоваться значение.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[PdfImageColorSpaceExportMode](../../com.aspose.words/pdfimagecolorspaceexportmode) константы.
### getImageCompression() {#getImageCompression--}
```
public int getImageCompression()
```


Указывает тип сжатия, который будет использоваться для всех изображений в документе.

 По умолчанию[PdfImageCompression.AUTO](../../com.aspose.words/pdfimagecompression\#AUTO).

 С использованием[PdfImageCompression.JPEG](../../com.aspose.words/pdfimagecompression\#JPEG) позволяет контролировать качество изображений в выходном документе с помощью[getJpegQuality()](../../com.aspose.words/pdfsaveoptions\#getJpegQuality--) / [setJpegQuality(int)](../../com.aspose.words/pdfsaveoptions\#setJpegQuality-int-) имущество.

 С использованием[PdfImageCompression.JPEG](../../com.aspose.words/pdfimagecompression\#JPEG) обеспечивает самую высокую скорость преобразования по сравнению с производительностью других типов сжатия, но в этом случае имеет место сжатие JPEG с потерями.

 С использованием[PdfImageCompression.AUTO](../../com.aspose.words/pdfimagecompression\#AUTO) позволяет контролировать качество Jpeg в выходном документе через[getJpegQuality()](../../com.aspose.words/pdfsaveoptions\#getJpegQuality--) / [setJpegQuality(int)](../../com.aspose.words/pdfsaveoptions\#setJpegQuality-int-) свойство, но для других форматов необработанные пиксельные данные извлекаются и сохраняются с помощью сжатия Flate. Этот случай медленнее, чем преобразование Jpeg, но без потерь.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[PdfImageCompression](../../com.aspose.words/pdfimagecompression) константы.
### getImlRenderingMode() {#getImlRenderingMode--}
```
public int getImlRenderingMode()
```


 Получает значение, определяющее способ визуализации объектов рукописного ввода (InkML). Значение по умолчанию[ImlRenderingMode.INK\_ML](../../com.aspose.words/imlrenderingmode\#INK-ML).

Это свойство используется, когда документ экспортируется в фиксированные форматы страниц.

**Возвращает:**
 int — значение, определяющее способ отображения объектов рукописного ввода (InkML). Возвращаемое значение является одним из[ImlRenderingMode](../../com.aspose.words/imlrenderingmode) константы.
### getInterpolateImages() {#getInterpolateImages--}
```
public boolean getInterpolateImages()
```


Флаг, указывающий, должна ли интерполяция изображения выполняться соответствующим считывающим устройством. Если указано значение false, флаг не записывается в выходной документ, а вместо этого используется поведение читателя по умолчанию.

Когда разрешение исходного изображения значительно ниже разрешения устройства вывода, каждый исходный образец покрывает множество пикселей устройства. В результате изображения могут выглядеть неровными или блочными. Эти визуальные артефакты можно уменьшить, применяя алгоритм интерполяции изображения во время рендеринга. Вместо того, чтобы закрашивать все пиксели, покрытые исходным образцом, одним и тем же цветом, интерполяция изображения пытается создать плавный переход между соседними значениями образца.

Соответствующий Reader может не реализовывать эту функцию PDF или может использовать любую конкретную реализацию интерполяции, которую он пожелает.

Значение по умолчанию неверно .

Флаг интерполяции запрещен соответствием PDF/A. значение false будет использоваться автоматически при сохранении в PDF/A.

**Возвращает:**
boolean - соответствующее логическое значение.
### getJpegQuality() {#getJpegQuality--}
```
public int getJpegQuality()
```


Получает значение, определяющее качество изображений JPEG внутри документа PDF.

Значение по умолчанию — 100.

 Это свойство используется совместно с[getImageCompression()](../../com.aspose.words/pdfsaveoptions\#getImageCompression--) / [setImageCompression(int)](../../com.aspose.words/pdfsaveoptions\#setImageCompression-int-) вариант.

Действует, только если документ содержит изображения JPEG.

Используйте это свойство, чтобы получить или установить качество изображений внутри документа при сохранении в формате PDF. Значение может варьироваться от 0 до 100, где 0 означает худшее качество, но максимальное сжатие, а 100 — лучшее качество, но минимальное сжатие. Если качество равно 100, а исходное изображение - JPEG, это означает отсутствие сжатия - исходные байты будут сохранены.

**Возвращает:**
int — значение, определяющее качество изображений JPEG внутри документа PDF.
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
### getOpenHyperlinksInNewWindow() {#getOpenHyperlinksInNewWindow--}
```
public boolean getOpenHyperlinksInNewWindow()
```


Получает значение, определяющее, будут ли гиперссылки в выходном документе Pdf принудительно открываться в новом окне (или вкладке) браузера.

Значение по умолчанию неверно . Когда для этого значения установлено значение true, гиперссылки сохраняются с использованием кода JavaScript. Код JavaScript: app.launchURL("URL", true); , где URL — это гиперссылка.

Обратите внимание, что если для этого параметра установлено значение true, гиперссылки не могут работать в некоторых программах для чтения PDF, например, в Chrome, Firefox.

Действия JavaScript запрещены соответствием PDF/A-1 и PDF/A-2. false будет использоваться автоматически при сохранении в PDF/A-1 и PDF/A-2.

**Возвращает:**
логическое значение — значение, определяющее, будут ли гиперссылки в выходном документе Pdf принудительно открываться в новом окне (или вкладке) браузера.
### getOptimizeOutput() {#getOptimizeOutput--}
```
public boolean getOptimizeOutput()
```


Флаг указывает, требуется ли оптимизация вывода. Если этот флаг установлен, удаляются лишние вложенные холсты и пустые холсты, а также объединяются соседние глифы с одинаковым форматированием. Примечание. Точность отображения содержимого может быть снижена, если для этого свойства задано значение true. Значение по умолчанию — ложь.

**Возвращает:**
boolean - соответствующее логическое значение.
### getOutlineOptions() {#getOutlineOptions--}
```
public OutlineOptions getOutlineOptions()
```


Позволяет указать параметры контура.

Контуры могут быть созданы из заголовков и закладок.

Для заголовков уровень структуры определяется уровнем заголовка.

Можно установить максимальный уровень заголовка для включения в контуры или вообще отключить контуры заголовков.

Для закладок уровень структуры может быть установлен в опциях как значение по умолчанию для всех закладок или как индивидуальное значение для отдельных закладок.

 Кроме того, контуры можно экспортировать в формат XPS с помощью того же[getOutlineOptions()](../../com.aspose.words/pdfsaveoptions\#getOutlineOptions--) учебный класс.

**Возвращает:**
[OutlineOptions](../../com.aspose.words/outlineoptions) - соответствующий[OutlineOptions](../../com.aspose.words/outlineoptions) ценность.
### getPageMode() {#getPageMode--}
```
public int getPageMode()
```


 Указывает, как документ PDF должен отображаться при открытии в программе чтения PDF. Значение по умолчанию[PdfPageMode.USE\_OUTLINES](../../com.aspose.words/pdfpagemode\#USE-OUTLINES).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[PdfPageMode](../../com.aspose.words/pdfpagemode) константы.
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
### getPreblendImages() {#getPreblendImages--}
```
public boolean getPreblendImages()
```


Получает значение, определяющее, следует ли предварительно смешивать прозрачные изображения с черным цветом фона.

Предварительное наложение изображений может улучшить внешний вид документа PDF в Adobe Reader и удалить артефакты сглаживания.

Для правильного отображения предварительно смешанных изображений приложение для просмотра PDF должно поддерживать запись /Matte в словаре изображений программной маски. Кроме того, предварительное смешивание изображений может снизить производительность рендеринга PDF.

Значение по умолчанию неверно .

**Возвращает:**
логическое значение — значение, определяющее, следует ли предварительно смешивать прозрачные изображения с черным цветом фона.
### getPreserveFormFields() {#getPreserveFormFields--}
```
public boolean getPreserveFormFields()
```


Указывает, сохранять ли поля формы Microsoft Word как поля формы в формате PDF или преобразовывать их в текст. Значение по умолчанию — ложь.

Поля формы Microsoft Word включают ввод текста, раскрывающийся список и элементы управления флажками.

Если установлено значение false , эти поля будут экспортированы как текст в PDF. Если установлено значение true , эти поля будут экспортированы как поля формы PDF.

При экспорте полей формы в PDF в качестве полей формы может произойти некоторая потеря форматирования, поскольку поля формы PDF не поддерживают все функции полей формы Microsoft Word.

Кроме того, размер вывода зависит от размера содержимого, поскольку редактируемые формы в Microsoft Word являются встроенными объектами.

Редактируемые формы запрещены соответствием PDF/A. значение false будет использоваться автоматически при сохранении в PDF/A.

Поля формы не поддерживаются при сохранении в PDF/UA. значение false будет использоваться автоматически.

**Возвращает:**
boolean - соответствующее логическое значение.
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
### getSaveFormat() {#getSaveFormat--}
```
public int getSaveFormat()
```


 Указывает формат, в котором будет сохранен документ, если используется этот объект параметров сохранения. Может быть только[SaveFormat.PDF](../../com.aspose.words/saveformat\#PDF).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[SaveFormat](../../com.aspose.words/saveformat) константы.
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
### getTextCompression() {#getTextCompression--}
```
public int getTextCompression()
```


Указывает тип сжатия, который будет использоваться для всего текстового содержимого в документе.

 По умолчанию[PdfTextCompression.FLATE](../../com.aspose.words/pdftextcompression\#FLATE).

Значительно увеличивает размер вывода при сохранении документа без сжатия.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[PdfTextCompression](../../com.aspose.words/pdftextcompression) константы.
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
### getUseBookFoldPrintingSettings() {#getUseBookFoldPrintingSettings--}
```
public boolean getUseBookFoldPrintingSettings()
```


 Получает логическое значение, указывающее, следует ли сохранять документ с использованием макета печати буклета, если он указан через[PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup\#getMultiplePages--) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup\#setMultiplePages-int-).

 Если указан этот параметр,[FixedPageSaveOptions.getPageSet()](../../com.aspose.words/fixedpagesaveoptions\#getPageSet--) / [FixedPageSaveOptions.setPageSet(com.aspose.words.PageSet)](../../com.aspose.words/fixedpagesaveoptions\#setPageSet-com.aspose.words.PageSet-) игнорируется при сохранении. Это поведение соответствует MS Word. Если в параметрах страницы не указаны параметры печати сгибом книги, этот параметр не будет работать.

**Возвращает:**
 boolean — логическое значение, указывающее, следует ли сохранять документ с использованием макета печати буклета, если он указан через[PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup\#getMultiplePages--) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup\#setMultiplePages-int-).
### getUseCoreFonts() {#getUseCoreFonts--}
```
public boolean getUseCoreFonts()
```


Получает значение, определяющее, следует ли заменять шрифты TrueType Arial, Times New Roman, Courier New и Symbol базовыми шрифтами PDF Type 1.

Значение по умолчанию неверно . Если для этого значения установлено значение true, шрифты Arial, Times New Roman, Courier New и Symbol заменяются в документе PDF соответствующим базовым шрифтом Type 1.

Основные шрифты PDF или их метрики шрифтов и подходящие замещающие шрифты должны быть доступны для любого приложения для просмотра PDF.

Этот параметр работает только для текста в кодировке ANSI (Windows-1252). Текст, отличный от ANSI, будет написан встроенным шрифтом TrueType независимо от этого параметра.

Соответствие форматам PDF/A и PDF/UA требует внедрения всех шрифтов. значение false будет использоваться автоматически при сохранении в PDF/A и PDF/UA.

Основные шрифты не поддерживаются при сохранении в формате PDF 2.0. значение false будет использоваться автоматически при сохранении в PDF 2.0.

 Эта опция имеет более высокий приоритет, чем[getFontEmbeddingMode()](../../com.aspose.words/pdfsaveoptions\#getFontEmbeddingMode--) / [setFontEmbeddingMode(int)](../../com.aspose.words/pdfsaveoptions\#setFontEmbeddingMode-int-) вариант.

**Возвращает:**
boolean — значение, определяющее, следует ли заменять шрифты TrueType Arial, Times New Roman, Courier New и Symbol базовыми шрифтами PDF Type 1.
### getUseHighQualityRendering() {#getUseHighQualityRendering--}
```
public boolean getUseHighQualityRendering()
```


Получает значение, определяющее, следует ли использовать высококачественные (то есть медленные) алгоритмы рендеринга. Значение по умолчанию неверно .

 Это свойство используется, когда документ экспортируется в форматы изображений:[SaveFormat.TIFF](../../com.aspose.words/saveformat\#TIFF), [SaveFormat.PNG](../../com.aspose.words/saveformat\#PNG), [SaveFormat.BMP](../../com.aspose.words/saveformat\#BMP), [SaveFormat.JPEG](../../com.aspose.words/saveformat\#JPEG), [SaveFormat.EMF](../../com.aspose.words/saveformat\#EMF).

**Возвращает:**
логическое значение — значение, определяющее, следует ли использовать высокое качество (т.е.
### getZoomBehavior() {#getZoomBehavior--}
```
public int getZoomBehavior()
```


 Получает значение, определяющее, какой тип масштабирования следует применять при открытии документа в средстве просмотра PDF. Значение по умолчанию[PdfZoomBehavior.NONE](../../com.aspose.words/pdfzoombehavior\#NONE), т.е. подгонка не применяется.

**Возвращает:**
 int — значение, определяющее, какой тип масштабирования следует применять при открытии документа в программе просмотра PDF. Возвращаемое значение является одним из[PdfZoomBehavior](../../com.aspose.words/pdfzoombehavior) константы.
### getZoomFactor() {#getZoomFactor--}
```
public int getZoomFactor()
```


 Получает значение, определяющее коэффициент масштабирования (в процентах) для документа. Это значение используется только в том случае, если[getZoomBehavior()](../../com.aspose.words/pdfsaveoptions\#getZoomBehavior--) / [setZoomBehavior(int)](../../com.aspose.words/pdfsaveoptions\#setZoomBehavior-int-) установлен на[PdfZoomBehavior.ZOOM\_FACTOR](../../com.aspose.words/pdfzoombehavior\#ZOOM-FACTOR).

**Возвращает:**
int - значение, определяющее коэффициент масштабирования (в процентах) для документа.
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




### setAdditionalTextPositioning(boolean value) {#setAdditionalTextPositioning-boolean-}
```
public void setAdditionalTextPositioning(boolean value)
```


Флаг, указывающий, следует ли писать дополнительные операторы позиционирования текста или нет.

Если true , дополнительные операторы позиционирования текста записываются в выходной PDF-файл. Это может помочь решить проблемы с неточным позиционированием текста на некоторых принтерах. Недостатком является увеличенный размер PDF-документа.

Значение по умолчанию неверно .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

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

### setCacheHeaderFooterShapes(boolean value) {#setCacheHeaderFooterShapes-boolean-}
```
public void setCacheHeaderFooterShapes(boolean value)
```


Задает значение, определяющее, следует ли кэшировать фигуры, размещенные в верхнем и нижнем колонтитулах документа.

Значение по умолчанию — false, и формы не кэшируются.

Когда значение равно true, графические фигуры записываются в документ PDF как xObject.

Некоторые фигуры не поддерживаются для кэширования (фигуры с полями, закладками, HRefs).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, определяющее, следует ли кэшировать фигуры, размещенные в верхнем и нижнем колонтитулах документа. |

### setColorMode(int value) {#setColorMode-int-}
```
public void setColorMode(int value)
```


 Задает значение, определяющее способ отображения цветов. Значение по умолчанию[ColorMode.NORMAL](../../com.aspose.words/colormode\#NORMAL).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Значение, определяющее способ отображения цветов. Значение должно быть одним из[ColorMode](../../com.aspose.words/colormode) константы. |

### setCompliance(int value) {#setCompliance-int-}
```
public void setCompliance(int value)
```


Указывает уровень соответствия стандартам PDF для выходных документов.

 По умолчанию[PdfCompliance.PDF\_17](../../com.aspose.words/pdfcompliance\#PDF-17).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[PdfCompliance](../../com.aspose.words/pdfcompliance) константы. |

### setCreateNoteHyperlinks(boolean value) {#setCreateNoteHyperlinks-boolean-}
```
public void setCreateNoteHyperlinks(boolean value)
```


Указывает, следует ли преобразовывать ссылки сносок/концевых сносок в основном текстовом материале в активные гиперссылки. При нажатии гиперссылка приведет к соответствующей сноске/концевой сноске. Значение по умолчанию — ложь.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setCustomPropertiesExport(int value) {#setCustomPropertiesExport-int-}
```
public void setCustomPropertiesExport(int value)
```


 Устанавливает значение, определяющее способ[Document.getCustomDocumentProperties()](../../com.aspose.words/document\#getCustomDocumentProperties--) экспортируются в файл PDF.

 Значение по умолчанию[PdfCustomPropertiesExport.NONE](../../com.aspose.words/pdfcustompropertiesexport\#NONE).

[PdfCustomPropertiesExport.METADATA](../../com.aspose.words/pdfcustompropertiesexport\#METADATA) значение не поддерживается при сохранении в PDF/A.[PdfCustomPropertiesExport.STANDARD](../../com.aspose.words/pdfcustompropertiesexport\#STANDARD) вместо этого будет использоваться для PDF/A-1 и PDF/A-2 и[PdfCustomPropertiesExport.NONE](../../com.aspose.words/pdfcustompropertiesexport\#NONE) для PDF/A-4.

[PdfCustomPropertiesExport.STANDARD](../../com.aspose.words/pdfcustompropertiesexport\#STANDARD) значение не поддерживается при сохранении в PDF 2.0.[PdfCustomPropertiesExport.METADATA](../../com.aspose.words/pdfcustompropertiesexport\#METADATA) вместо этого будет использоваться.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Значение, определяющее путь[Document.getCustomDocumentProperties()](../../com.aspose.words/document\#getCustomDocumentProperties--) экспортируются в файл PDF. Значение должно быть одним из[PdfCustomPropertiesExport](../../com.aspose.words/pdfcustompropertiesexport) константы. |

### setDefaultTemplate(String value) {#setDefaultTemplate-java.lang.String-}
```
public void setDefaultTemplate(String value)
```


 Устанавливает путь к шаблону по умолчанию (включая имя файла). Значение по умолчанию для этого свойства**empty string** . Если указано, этот путь используется для загрузки шаблона, когда[Document.getAutomaticallyUpdateStyles()](../../com.aspose.words/document\#getAutomaticallyUpdateStyles--) / [Document.setAutomaticallyUpdateStyles(boolean)](../../com.aspose.words/document\#setAutomaticallyUpdateStyles-boolean-) правда, но[Document.getAttachedTemplate()](../../com.aspose.words/document\#getAttachedTemplate--) / [Document.setAttachedTemplate(java.lang.String)](../../com.aspose.words/document\#setAttachedTemplate-java.lang.String-) пустой.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Путь к шаблону по умолчанию (включая имя файла). |

### setDigitalSignatureDetails(PdfDigitalSignatureDetails value) {#setDigitalSignatureDetails-com.aspose.words.PdfDigitalSignatureDetails-}
```
public void setDigitalSignatureDetails(PdfDigitalSignatureDetails value)
```


Устанавливает детали для подписания выходного PDF-документа.

 Значение по умолчанию равно null, и выходной документ не будет подписан. Когда для этого свойства задано допустимое значение[PdfDigitalSignatureDetails](../../com.aspose.words/pdfdigitalsignaturedetails) объект, то выходной PDF-документ будет подписан цифровой подписью.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [PdfDigitalSignatureDetails](../../com.aspose.words/pdfdigitalsignaturedetails) | Детали для подписания выходного PDF-документа. |

### setDisplayDocTitle(boolean value) {#setDisplayDocTitle-boolean-}
```
public void setDisplayDocTitle(boolean value)
```


Флаг, указывающий, будет ли окно\В строке заголовка должно отображаться название документа, взятое из записи Title словаря информации о документе.

Если false , вместо этого в строке заголовка должно отображаться имя файла PDF, содержащего документ.

Этот флаг требуется для соответствия PDF/UA. значение true будет использоваться автоматически при сохранении в PDF/UA.

Значение по умолчанию неверно .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

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

 Если[getCompliance()](../../com.aspose.words/pdfsaveoptions\#getCompliance--) / [setCompliance(int)](../../com.aspose.words/pdfsaveoptions\#setCompliance-int-) установлен на[PdfCompliance.PDF\_A\_1\_A](../../com.aspose.words/pdfcompliance\#PDF-A-1-A) или же[PdfCompliance.PDF\_A\_1\_B](../../com.aspose.words/pdfcompliance\#PDF-A-1-B) , свойство всегда возвращает[DmlEffectsRenderingMode.NONE](../../com.aspose.words/dmleffectsrenderingmode\#NONE).

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

### setDownsampleOptions(DownsampleOptions value) {#setDownsampleOptions-com.aspose.words.DownsampleOptions-}
```
public void setDownsampleOptions(DownsampleOptions value)
```


Позволяет указать параметры понижающей дискретизации.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [DownsampleOptions](../../com.aspose.words/downsampleoptions) |  Соответствующий[DownsampleOptions](../../com.aspose.words/downsampleoptions) ценность. |

### setEmbedFullFonts(boolean value) {#setEmbedFullFonts-boolean-}
```
public void setEmbedFullFonts(boolean value)
```


Управляет тем, как шрифты внедряются в результирующие PDF-документы.

Значение по умолчанию — false , что означает, что шрифты подмножаются перед внедрением. Подмножество полезно, если вы хотите уменьшить размер выходного файла. Подмножество удаляет все неиспользуемые глифы из шрифта.

Если для этого параметра задано значение true , в PDF-файл встраивается полный файл шрифта без подмножества. Это приведет к увеличению размера выходных файлов, но может быть полезной опцией, если вы хотите позже отредактировать полученный PDF-файл (например, добавить больше текста).

Некоторые шрифты большие (несколько мегабайт), и их встраивание без подмножества приведет к большим выходным документам.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setEncryptionDetails(PdfEncryptionDetails value) {#setEncryptionDetails-com.aspose.words.PdfEncryptionDetails-}
```
public void setEncryptionDetails(PdfEncryptionDetails value)
```


Задает детали для шифрования выходного PDF-документа.

 Значение по умолчанию равно null, и выходной документ не будет зашифрован. Когда для этого свойства задано допустимое значение[PdfEncryptionDetails](../../com.aspose.words/pdfencryptiondetails) объект, то выходной PDF-документ будет зашифрован.

Алгоритм шифрования AES-128 используется при сохранении в формате PDF 1.7 (включая PDF/UA-1). Алгоритм шифрования AES-256 используется при сохранении в формате PDF 2.0.

Шифрование запрещено соответствием PDF/A. Этот параметр будет игнорироваться при сохранении в PDF/A.

[PdfPermissions.CONTENT\_COPY\_FOR\_ACCESSIBILITY](../../com.aspose.words/pdfpermissions\#CONTENT-COPY-FOR-ACCESSIBILITY) разрешение требуется в соответствии с PDF/UA, если выходной документ зашифрован. Это разрешение будет автоматически использоваться при сохранении в PDF/UA.

[PdfPermissions.CONTENT\_COPY\_FOR\_ACCESSIBILITY](../../com.aspose.words/pdfpermissions\#CONTENT-COPY-FOR-ACCESSIBILITY)разрешение устарело в формате PDF 2.0. Это разрешение будет игнорироваться при сохранении в PDF 2.0.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [PdfEncryptionDetails](../../com.aspose.words/pdfencryptiondetails) | Сведения о шифровании выходного PDF-документа. |

### setExportDocumentStructure(boolean value) {#setExportDocumentStructure-boolean-}
```
public void setExportDocumentStructure(boolean value)
```


Задает значение, определяющее, экспортировать структуру документа или нет.

Это значение игнорируется при сохранении в форматах PDF/A-1a, PDF/A-2a и PDF/UA-1, поскольку для этого соответствия требуется структура документа.

Обратите внимание, что экспорт структуры документа значительно увеличивает потребление памяти, особенно для больших документов.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, определяющее, следует ли экспортировать структуру документа. |

### setExportGeneratorName(boolean value) {#setExportGeneratorName-boolean-}
```
public void setExportGeneratorName(boolean value)
```


 При значении true имя и версия Aspose.Words встраиваются в создаваемые файлы. Значение по умолчанию**true**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setExportLanguageToSpanTag(boolean value) {#setExportLanguageToSpanTag-boolean-}
```
public void setExportLanguageToSpanTag(boolean value)
```


Задает значение, определяющее, следует ли создавать тег «Span» в структуре документа для экспорта языка текста.

Значение по умолчанию — false, а атрибут «Lang» прикрепляется к последовательности отмеченного содержимого в потоке содержимого страницы.

Когда значение равно true, для текста с нестандартным языком создается тег «Span», и к этому тегу прикрепляется атрибут «Lang».

 Это значение игнорируется, когда[getExportDocumentStructure()](../../com.aspose.words/pdfsaveoptions\#getExportDocumentStructure--) / [setExportDocumentStructure(boolean)](../../com.aspose.words/pdfsaveoptions\#setExportDocumentStructure-boolean-) является ложным.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, определяющее, следует ли создавать тег «Span» в структуре документа для экспорта языка текста. |

### setFontEmbeddingMode(int value) {#setFontEmbeddingMode-int-}
```
public void setFontEmbeddingMode(int value)
```


Задает режим внедрения шрифта.

 Значение по умолчанию[PdfFontEmbeddingMode.EMBED\_ALL](../../com.aspose.words/pdffontembeddingmode\#EMBED-ALL).

Этот параметр работает только для текста в кодировке ANSI (Windows-1252). Если документ содержит текст, отличный от ANSI, соответствующие шрифты будут встроены независимо от этого параметра.

 Соответствие форматам PDF/A и PDF/UA требует внедрения всех шрифтов.[PdfFontEmbeddingMode.EMBED\_ALL](../../com.aspose.words/pdffontembeddingmode\#EMBED-ALL) значение будет использоваться автоматически при сохранении в PDF/A и PDF/UA.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[PdfFontEmbeddingMode](../../com.aspose.words/pdffontembeddingmode) константы. |

### setHeaderFooterBookmarksExportMode(int value) {#setHeaderFooterBookmarksExportMode-int-}
```
public void setHeaderFooterBookmarksExportMode(int value)
```


Определяет, как экспортируются закладки в верхних/нижних колонтитулах.

 Значение по умолчанию[HeaderFooterBookmarksExportMode.ALL](../../com.aspose.words/headerfooterbookmarksexportmode\#ALL).

 Это свойство используется совместно с[getOutlineOptions()](../../com.aspose.words/pdfsaveoptions\#getOutlineOptions--) вариант.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[HeaderFooterBookmarksExportMode](../../com.aspose.words/headerfooterbookmarksexportmode) константы. |

### setImageColorSpaceExportMode(int value) {#setImageColorSpaceExportMode-int-}
```
public void setImageColorSpaceExportMode(int value)
```


Указывает, как цветовое пространство будет выбрано для изображений в документе PDF.

 Значение по умолчанию[PdfImageColorSpaceExportMode.AUTO](../../com.aspose.words/pdfimagecolorspaceexportmode\#AUTO).

 Если[PdfImageColorSpaceExportMode.SIMPLE\_CMYK](../../com.aspose.words/pdfimagecolorspaceexportmode\#SIMPLE-CMYK) указано значение,[getImageCompression()](../../com.aspose.words/pdfsaveoptions\#getImageCompression--) / [setImageCompression(int)](../../com.aspose.words/pdfsaveoptions\#setImageCompression-int-) параметр игнорируется, и для всех изображений в документе используется сжатие Flate.

[PdfImageColorSpaceExportMode.SIMPLE\_CMYK](../../com.aspose.words/pdfimagecolorspaceexportmode\#SIMPLE-CMYK) значение не поддерживается при сохранении в PDF/A.[PdfImageColorSpaceExportMode.AUTO](../../com.aspose.words/pdfimagecolorspaceexportmode\#AUTO) вместо этого будет использоваться значение.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[PdfImageColorSpaceExportMode](../../com.aspose.words/pdfimagecolorspaceexportmode) константы. |

### setImageCompression(int value) {#setImageCompression-int-}
```
public void setImageCompression(int value)
```


Указывает тип сжатия, который будет использоваться для всех изображений в документе.

 По умолчанию[PdfImageCompression.AUTO](../../com.aspose.words/pdfimagecompression\#AUTO).

 С использованием[PdfImageCompression.JPEG](../../com.aspose.words/pdfimagecompression\#JPEG) позволяет контролировать качество изображений в выходном документе с помощью[getJpegQuality()](../../com.aspose.words/pdfsaveoptions\#getJpegQuality--) / [setJpegQuality(int)](../../com.aspose.words/pdfsaveoptions\#setJpegQuality-int-) имущество.

 С использованием[PdfImageCompression.JPEG](../../com.aspose.words/pdfimagecompression\#JPEG) обеспечивает самую высокую скорость преобразования по сравнению с производительностью других типов сжатия, но в этом случае имеет место сжатие JPEG с потерями.

 С использованием[PdfImageCompression.AUTO](../../com.aspose.words/pdfimagecompression\#AUTO) позволяет контролировать качество Jpeg в выходном документе через[getJpegQuality()](../../com.aspose.words/pdfsaveoptions\#getJpegQuality--) / [setJpegQuality(int)](../../com.aspose.words/pdfsaveoptions\#setJpegQuality-int-) свойство, но для других форматов необработанные пиксельные данные извлекаются и сохраняются с помощью сжатия Flate. Этот случай медленнее, чем преобразование Jpeg, но без потерь.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[PdfImageCompression](../../com.aspose.words/pdfimagecompression) константы. |

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

### setInterpolateImages(boolean value) {#setInterpolateImages-boolean-}
```
public void setInterpolateImages(boolean value)
```


Флаг, указывающий, должна ли интерполяция изображения выполняться соответствующим считывающим устройством. Если указано значение false, флаг не записывается в выходной документ, а вместо этого используется поведение читателя по умолчанию.

Когда разрешение исходного изображения значительно ниже разрешения устройства вывода, каждый исходный образец покрывает множество пикселей устройства. В результате изображения могут выглядеть неровными или блочными. Эти визуальные артефакты можно уменьшить, применяя алгоритм интерполяции изображения во время рендеринга. Вместо того, чтобы закрашивать все пиксели, покрытые исходным образцом, одним и тем же цветом, интерполяция изображения пытается создать плавный переход между соседними значениями образца.

Соответствующий Reader может не реализовывать эту функцию PDF или может использовать любую конкретную реализацию интерполяции, которую он пожелает.

Значение по умолчанию неверно .

Флаг интерполяции запрещен соответствием PDF/A. значение false будет использоваться автоматически при сохранении в PDF/A.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setJpegQuality(int value) {#setJpegQuality-int-}
```
public void setJpegQuality(int value)
```


Задает значение, определяющее качество изображений JPEG внутри документа PDF.

Значение по умолчанию — 100.

 Это свойство используется совместно с[getImageCompression()](../../com.aspose.words/pdfsaveoptions\#getImageCompression--) / [setImageCompression(int)](../../com.aspose.words/pdfsaveoptions\#setImageCompression-int-) вариант.

Действует, только если документ содержит изображения JPEG.

Используйте это свойство, чтобы получить или установить качество изображений внутри документа при сохранении в формате PDF. Значение может варьироваться от 0 до 100, где 0 означает худшее качество, но максимальное сжатие, а 100 — лучшее качество, но минимальное сжатие. Если качество равно 100, а исходное изображение - JPEG, это означает отсутствие сжатия - исходные байты будут сохранены.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Значение, определяющее качество изображений JPEG внутри документа PDF. |

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

### setOpenHyperlinksInNewWindow(boolean value) {#setOpenHyperlinksInNewWindow-boolean-}
```
public void setOpenHyperlinksInNewWindow(boolean value)
```


Задает значение, определяющее, будут ли гиперссылки в выходном документе Pdf принудительно открываться в новом окне (или вкладке) браузера.

Значение по умолчанию неверно . Когда для этого значения установлено значение true, гиперссылки сохраняются с использованием кода JavaScript. Код JavaScript: app.launchURL("URL", true); , где URL — это гиперссылка.

Обратите внимание, что если для этого параметра установлено значение true, гиперссылки не могут работать в некоторых программах для чтения PDF, например, в Chrome, Firefox.

Действия JavaScript запрещены соответствием PDF/A-1 и PDF/A-2. false будет использоваться автоматически при сохранении в PDF/A-1 и PDF/A-2.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, определяющее, будут ли гиперссылки в выходном документе Pdf принудительно открываться в новом окне (или вкладке) браузера. |

### setOptimizeOutput(boolean value) {#setOptimizeOutput-boolean-}
```
public void setOptimizeOutput(boolean value)
```


Флаг указывает, требуется ли оптимизация вывода. Если этот флаг установлен, удаляются лишние вложенные холсты и пустые холсты, а также объединяются соседние глифы с одинаковым форматированием. Примечание. Точность отображения содержимого может быть снижена, если для этого свойства задано значение true. Значение по умолчанию — ложь.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setPageMode(int value) {#setPageMode-int-}
```
public void setPageMode(int value)
```


 Указывает, как документ PDF должен отображаться при открытии в программе чтения PDF. Значение по умолчанию[PdfPageMode.USE\_OUTLINES](../../com.aspose.words/pdfpagemode\#USE-OUTLINES).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[PdfPageMode](../../com.aspose.words/pdfpagemode) константы. |

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

### setPreblendImages(boolean value) {#setPreblendImages-boolean-}
```
public void setPreblendImages(boolean value)
```


Задает значение, определяющее, следует ли предварительно смешивать прозрачные изображения с черным цветом фона.

Предварительное наложение изображений может улучшить внешний вид документа PDF в Adobe Reader и удалить артефакты сглаживания.

Для правильного отображения предварительно смешанных изображений приложение для просмотра PDF должно поддерживать запись /Matte в словаре изображений программной маски. Кроме того, предварительное смешивание изображений может снизить производительность рендеринга PDF.

Значение по умолчанию неверно .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, определяющее, следует ли предварительно смешивать прозрачные изображения с черным цветом фона. |

### setPreserveFormFields(boolean value) {#setPreserveFormFields-boolean-}
```
public void setPreserveFormFields(boolean value)
```


Указывает, сохранять ли поля формы Microsoft Word как поля формы в формате PDF или преобразовывать их в текст. Значение по умолчанию — ложь.

Поля формы Microsoft Word включают ввод текста, раскрывающийся список и элементы управления флажками.

Если установлено значение false , эти поля будут экспортированы как текст в PDF. Если установлено значение true , эти поля будут экспортированы как поля формы PDF.

При экспорте полей формы в PDF в качестве полей формы может произойти некоторая потеря форматирования, поскольку поля формы PDF не поддерживают все функции полей формы Microsoft Word.

Кроме того, размер вывода зависит от размера содержимого, поскольку редактируемые формы в Microsoft Word являются встроенными объектами.

Редактируемые формы запрещены соответствием PDF/A. значение false будет использоваться автоматически при сохранении в PDF/A.

Поля формы не поддерживаются при сохранении в PDF/UA. значение false будет использоваться автоматически.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

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

### setSaveFormat(int value) {#setSaveFormat-int-}
```
public void setSaveFormat(int value)
```


 Указывает формат, в котором будет сохранен документ, если используется этот объект параметров сохранения. Может быть только[SaveFormat.PDF](../../com.aspose.words/saveformat\#PDF).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[SaveFormat](../../com.aspose.words/saveformat) константы. |

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

### setTextCompression(int value) {#setTextCompression-int-}
```
public void setTextCompression(int value)
```


Указывает тип сжатия, который будет использоваться для всего текстового содержимого в документе.

 По умолчанию[PdfTextCompression.FLATE](../../com.aspose.words/pdftextcompression\#FLATE).

Значительно увеличивает размер вывода при сохранении документа без сжатия.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[PdfTextCompression](../../com.aspose.words/pdftextcompression) константы. |

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

### setUseBookFoldPrintingSettings(boolean value) {#setUseBookFoldPrintingSettings-boolean-}
```
public void setUseBookFoldPrintingSettings(boolean value)
```


 Устанавливает логическое значение, указывающее, следует ли сохранять документ с использованием макета печати буклета, если он указан через[PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup\#getMultiplePages--) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup\#setMultiplePages-int-).

 Если указан этот параметр,[FixedPageSaveOptions.getPageSet()](../../com.aspose.words/fixedpagesaveoptions\#getPageSet--) / [FixedPageSaveOptions.setPageSet(com.aspose.words.PageSet)](../../com.aspose.words/fixedpagesaveoptions\#setPageSet-com.aspose.words.PageSet-) игнорируется при сохранении. Это поведение соответствует MS Word. Если в параметрах страницы не указаны параметры печати сгибом книги, этот параметр не будет работать.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean |  Логическое значение, указывающее, следует ли сохранять документ с использованием макета печати буклета, если он указан через[PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup\#getMultiplePages--) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup\#setMultiplePages-int-). |

### setUseCoreFonts(boolean value) {#setUseCoreFonts-boolean-}
```
public void setUseCoreFonts(boolean value)
```


Задает значение, определяющее, следует ли заменять шрифты TrueType Arial, Times New Roman, Courier New и Symbol базовыми шрифтами PDF Type 1.

Значение по умолчанию неверно . Если для этого значения установлено значение true, шрифты Arial, Times New Roman, Courier New и Symbol заменяются в документе PDF соответствующим базовым шрифтом Type 1.

Основные шрифты PDF или их метрики шрифтов и подходящие замещающие шрифты должны быть доступны для любого приложения для просмотра PDF.

Этот параметр работает только для текста в кодировке ANSI (Windows-1252). Текст, отличный от ANSI, будет написан встроенным шрифтом TrueType независимо от этого параметра.

Соответствие форматам PDF/A и PDF/UA требует внедрения всех шрифтов. значение false будет использоваться автоматически при сохранении в PDF/A и PDF/UA.

Основные шрифты не поддерживаются при сохранении в формате PDF 2.0. значение false будет использоваться автоматически при сохранении в PDF 2.0.

 Эта опция имеет более высокий приоритет, чем[getFontEmbeddingMode()](../../com.aspose.words/pdfsaveoptions\#getFontEmbeddingMode--) / [setFontEmbeddingMode(int)](../../com.aspose.words/pdfsaveoptions\#setFontEmbeddingMode-int-) вариант.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, определяющее, следует ли заменять шрифты TrueType Arial, Times New Roman, Courier New и Symbol базовыми шрифтами PDF Type 1. |

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

### setZoomBehavior(int value) {#setZoomBehavior-int-}
```
public void setZoomBehavior(int value)
```


 Задает значение, определяющее, какой тип масштабирования следует применять при открытии документа в программе просмотра PDF. Значение по умолчанию[PdfZoomBehavior.NONE](../../com.aspose.words/pdfzoombehavior\#NONE), т.е. подгонка не применяется.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Значение, определяющее, какой тип масштабирования следует применять при открытии документа в средстве просмотра PDF. Значение должно быть одним из[PdfZoomBehavior](../../com.aspose.words/pdfzoombehavior) константы. |

### setZoomFactor(int value) {#setZoomFactor-int-}
```
public void setZoomFactor(int value)
```


 Задает значение, определяющее коэффициент масштабирования (в процентах) для документа. Это значение используется только в том случае, если[getZoomBehavior()](../../com.aspose.words/pdfsaveoptions\#getZoomBehavior--) / [setZoomBehavior(int)](../../com.aspose.words/pdfsaveoptions\#setZoomBehavior-int-) установлен на[PdfZoomBehavior.ZOOM\_FACTOR](../../com.aspose.words/pdfzoombehavior\#ZOOM-FACTOR).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Значение, определяющее коэффициент масштабирования (в процентах) для документа. |

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
