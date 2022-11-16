---
title: HtmlSaveOptions
second_title: Справочник по API Aspose.Words для Java
description: Может использоваться для указания дополнительных параметров при сохранении документа в формате или.
type: docs
weight: 331
url: /ru/java/com.aspose.words/htmlsaveoptions/
---

**Наследование:**
java.lang.Object, [com.aspose.words.SaveOptions](../../com.aspose.words/saveoptions)

**Все реализованные интерфейсы:**
java.lang.Cloneable
```
public class HtmlSaveOptions extends SaveOptions implements Cloneable
```

 Может использоваться для указания дополнительных параметров при сохранении документа в[SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB) или же[SaveFormat.AZW\_3](../../com.aspose.words/saveformat\#AZW-3) формат.

 Чтобы узнать больше, посетите**Specify Save Options** документальная статья.
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [HtmlSaveOptions()](#HtmlSaveOptions--) |  Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа в[SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML) формат. |
| [HtmlSaveOptions(int saveFormat)](#HtmlSaveOptions-int-) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [createSaveOptions(int saveFormat)](#createSaveOptions-int-) |  |
| [createSaveOptions(String fileName)](#createSaveOptions-java.lang.String-) | Создает объект параметров сохранения класса, подходящего для расширения файла, указанного в данном имени файла. |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAllowEmbeddingPostScriptFonts()](#getAllowEmbeddingPostScriptFonts--) | Получает логическое значение, указывающее, разрешать ли встраивание шрифтов с контурами PostScript при встраивании шрифтов TrueType в документ после его сохранения. |
| [getAllowNegativeIndent()](#getAllowNegativeIndent--) | Указывает, нормализуются ли отрицательные левый и правый отступы абзацев при сохранении в HTML, MHTML или EPUB. |
| [getClass()](#getClass--) |  |
| [getCssClassNamePrefix()](#getCssClassNamePrefix--) | Указывает префикс, который добавляется ко всем именам классов CSS. |
| [getCssSavingCallback()](#getCssSavingCallback--) | Позволяет управлять сохранением стилей CSS при сохранении документа в формате HTML, MHTML или EPUB. |
| [getCssStyleSheetFileName()](#getCssStyleSheetFileName--) | Указывает путь и имя файла каскадной таблицы стилей (CSS), записываемого при экспорте документа в HTML. |
| [getCssStyleSheetType()](#getCssStyleSheetType--) | Указывает, как стили CSS (каскадные таблицы стилей) экспортируются в HTML, MHTML или EPUB. |
| [getDefaultTemplate()](#getDefaultTemplate--) | Получает путь к шаблону по умолчанию (включая имя файла). |
| [getDml3DEffectsRenderingMode()](#getDml3DEffectsRenderingMode--) | Получает значение, определяющее способ визуализации 3D-эффектов. |
| [getDmlEffectsRenderingMode()](#getDmlEffectsRenderingMode--) | Получает значение, определяющее способ визуализации эффектов DrawingML. |
| [getDmlRenderingMode()](#getDmlRenderingMode--) | Получает значение, определяющее способ отображения фигур DrawingML. |
| [getDocumentPartSavingCallback()](#getDocumentPartSavingCallback--) | Позволяет управлять сохранением частей документа при сохранении документа в формате HTML или EPUB. |
| [getDocumentSplitCriteria()](#getDocumentSplitCriteria--) | Указывает, как документ должен быть разделен при сохранении в[SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB) или же[SaveFormat.AZW\_3](../../com.aspose.words/saveformat\#AZW-3) формат. |
| [getDocumentSplitHeadingLevel()](#getDocumentSplitHeadingLevel--) | Указывает максимальный уровень заголовков, на котором можно разделить документ. |
| [getEncoding()](#getEncoding--) |  |
| [getEpubNavigationMapLevel()](#getEpubNavigationMapLevel--) | Определяет максимальный уровень заголовков, заполняемых навигационной картой при экспорте в формат IDPF EPUB. |
| [getExportCidUrlsForMhtmlResources()](#getExportCidUrlsForMhtmlResources--) | Указывает, следует ли использовать URL-адреса CID (Content-ID) для ссылки на ресурсы (изображения, шрифты, CSS), включенные в документы MHTML. |
| [getExportDocumentProperties()](#getExportDocumentProperties--) | Указывает, следует ли экспортировать встроенные и настраиваемые свойства документа в HTML, MHTML или EPUB. |
| [getExportDropDownFormFieldAsText()](#getExportDropDownFormFieldAsText--) | Определяет, как поля раскрывающихся форм сохраняются в HTML или MHTML. |
| [getExportFontResources()](#getExportFontResources--) | Указывает, следует ли экспортировать ресурсы шрифта в HTML, MHTML или EPUB. |
| [getExportFontsAsBase64()](#getExportFontsAsBase64--) | Указывает, следует ли встраивать ресурсы шрифтов в HTML в кодировке Base64. |
| [getExportGeneratorName()](#getExportGeneratorName--) | При значении true имя и версия Aspose.Words встраиваются в создаваемые файлы. |
| [getExportHeadersFootersMode()](#getExportHeadersFootersMode--) | Указывает, как верхние и нижние колонтитулы выводятся в HTML, MHTML или EPUB. |
| [getExportImagesAsBase64()](#getExportImagesAsBase64--) | Указывает, сохраняются ли изображения в формате Base64 в выходной HTML, MHTML или EPUB. |
| [getExportLanguageInformation()](#getExportLanguageInformation--) | Указывает, экспортируется ли языковая информация в HTML, MHTML или EPUB. |
| [getExportListLabels()](#getExportListLabels--) | Управляет выводом меток списков в HTML, MHTML или EPUB. |
| [getExportOriginalUrlForLinkedImages()](#getExportOriginalUrlForLinkedImages--) | Указывает, следует ли использовать исходный URL-адрес в качестве URL-адреса связанных изображений. |
| [getExportPageMargins()](#getExportPageMargins--) | Указывает, экспортируются ли поля страницы в HTML, MHTML или EPUB. |
| [getExportPageSetup()](#getExportPageSetup--) | Указывает, экспортируются ли настройки страницы в HTML, MHTML или EPUB. |
| [getExportRelativeFontSize()](#getExportRelativeFontSize--) | Указывает, должны ли размеры шрифта выводиться в относительных единицах при сохранении в HTML, MHTML или EPUB. |
| [getExportRoundtripInformation()](#getExportRoundtripInformation--) | Указывает, следует ли записывать информацию о цикле приема-передачи при сохранении в HTML, MHTML или EPUB. |
| [getExportShapesAsSvg()](#getExportShapesAsSvg--) |  Контролирует ли[Shape](../../com.aspose.words/shape) узлы преобразуются в изображения SVG при сохранении в HTML, MHTML, EPUB или AZW3. |
| [getExportTextInputFormFieldAsText()](#getExportTextInputFormFieldAsText--) | Управляет способом сохранения полей формы ввода текста в формате HTML или MHTML. |
| [getExportTocPageNumbers()](#getExportTocPageNumbers--) | Указывает, записывать ли номера страниц в оглавление при сохранении HTML, MHTML и EPUB. |
| [getExportXhtmlTransitional()](#getExportXhtmlTransitional--) | Указывает, следует ли записывать объявление DOCTYPE при сохранении в HTML или MHTML. |
| [getFontResourcesSubsettingSizeThreshold()](#getFontResourcesSubsettingSizeThreshold--) | Определяет, какие ресурсы шрифтов нуждаются в подразделении при сохранении в HTML, MHTML или EPUB. |
| [getFontSavingCallback()](#getFontSavingCallback--) | Позволяет управлять сохранением шрифтов при сохранении документа в формате HTML, MHTML или EPUB. |
| [getFontsFolder()](#getFontsFolder--) | Указывает физическую папку, в которой сохраняются шрифты при экспорте документа в HTML. |
| [getFontsFolderAlias()](#getFontsFolderAlias--) | Указывает имя папки, используемой для создания URI шрифтов, записываемых в HTML-документ. |
| [getHtmlVersion()](#getHtmlVersion--) | Указывает версию стандарта HTML, которую следует использовать при сохранении документа в формате HTML или MHTML. |
| [getImageResolution()](#getImageResolution--) | Указывает выходное разрешение для изображений при экспорте в HTML, MHTML или EPUB. |
| [getImageSavingCallback()](#getImageSavingCallback--) | Позволяет управлять способом сохранения изображений при сохранении документа в формате HTML, MHTML или EPUB. |
| [getImagesFolder()](#getImagesFolder--) | Указывает физическую папку, в которой сохраняются изображения при экспорте документа в формат HTML. |
| [getImagesFolderAlias()](#getImagesFolderAlias--) | Указывает имя папки, используемой для создания URI изображений, записываемых в HTML-документ. |
| [getImlRenderingMode()](#getImlRenderingMode--) | Получает значение, определяющее способ визуализации объектов рукописного ввода (InkML). |
| [getMemoryOptimization()](#getMemoryOptimization--) | Получает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. |
| [getMetafileFormat()](#getMetafileFormat--) | Указывает, в каком формате сохраняются метафайлы при экспорте в HTML, MHTML или EPUB. |
| [getOfficeMathOutputMode()](#getOfficeMathOutputMode--) | Управляет экспортом объектов OfficeMath в HTML, MHTML или EPUB. |
| [getPrettyFormat()](#getPrettyFormat--) | Когда true , красивые форматы выводятся там, где это применимо. |
| [getProgressCallback()](#getProgressCallback--) | Вызывается при сохранении документа и принимает данные о ходе сохранения. |
| [getResolveFontNames()](#getResolveFontNames--) | Указывает, разрешаются ли имена семейств шрифтов, используемые в документе, и заменяются ли они в соответствии с[Document.getFontSettings()](../../com.aspose.words/document\#getFontSettings--) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document\#setFontSettings-com.aspose.words.FontSettings-) при записи в форматы на основе HTML. |
| [getResourceFolder()](#getResourceFolder--) | Указывает физическую папку, в которой сохраняются все ресурсы, такие как изображения, шрифты и внешний CSS, при экспорте документа в HTML. |
| [getResourceFolderAlias()](#getResourceFolderAlias--) | Задает имя папки, используемой для создания URI всех ресурсов, записываемых в HTML-документ. |
| [getSaveFormat()](#getSaveFormat--) | Указывает формат, в котором будет сохранен документ, если используется этот объект параметров сохранения. |
| [getScaleImageToShapeSize()](#getScaleImageToShapeSize--) | Указывает, масштабируются ли изображения с помощью Aspose.Words до размера ограничивающей фигуры при экспорте в HTML, MHTML или EPUB. |
| [getTableWidthOutputMode()](#getTableWidthOutputMode--) | Определяет, как ширина таблицы, строки и ячейки экспортируется в HTML, MHTML или EPUB. |
| [getTempFolder()](#getTempFolder--) | Указывает папку для временных файлов, используемых при сохранении в файл DOC или DOCX. |
| [getUpdateCreatedTimeProperty()](#getUpdateCreatedTimeProperty--) |  Получает значение, определяющее, является ли[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-) свойство обновляется перед сохранением. |
| [getUpdateFields()](#getUpdateFields--) | Получает значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы. |
| [getUpdateLastPrintedProperty()](#getUpdateLastPrintedProperty--) |  Получает значение, определяющее, является ли[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-) свойство обновляется перед сохранением. |
| [getUpdateLastSavedTimeProperty()](#getUpdateLastSavedTimeProperty--) |  Получает значение, определяющее, является ли[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-) свойство обновляется перед сохранением. |
| [getUpdateSdtContent()](#getUpdateSdtContent--) |  Получает значение, определяющее, будет ли содержимое[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) обновляется перед сохранением. |
| [getUseAntiAliasing()](#getUseAntiAliasing--) | Получает значение, определяющее, следует ли использовать сглаживание для рендеринга. |
| [getUseHighQualityRendering()](#getUseHighQualityRendering--) | Получает значение, определяющее, следует ли использовать высокое качество (т. е. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setAllowEmbeddingPostScriptFonts(boolean value)](#setAllowEmbeddingPostScriptFonts-boolean-) | Задает логическое значение, указывающее, разрешать ли встраивание шрифтов с контурами PostScript при встраивании шрифтов TrueType в документ после его сохранения. |
| [setAllowNegativeIndent(boolean value)](#setAllowNegativeIndent-boolean-) | Указывает, нормализуются ли отрицательные левый и правый отступы абзацев при сохранении в HTML, MHTML или EPUB. |
| [setCssClassNamePrefix(String value)](#setCssClassNamePrefix-java.lang.String-) | Указывает префикс, который добавляется ко всем именам классов CSS. |
| [setCssSavingCallback(ICssSavingCallback value)](#setCssSavingCallback-com.aspose.words.ICssSavingCallback-) | Позволяет управлять сохранением стилей CSS при сохранении документа в формате HTML, MHTML или EPUB. |
| [setCssStyleSheetFileName(String value)](#setCssStyleSheetFileName-java.lang.String-) | Указывает путь и имя файла каскадной таблицы стилей (CSS), записываемого при экспорте документа в HTML. |
| [setCssStyleSheetType(int value)](#setCssStyleSheetType-int-) | Указывает, как стили CSS (каскадные таблицы стилей) экспортируются в HTML, MHTML или EPUB. |
| [setDefaultTemplate(String value)](#setDefaultTemplate-java.lang.String-) | Устанавливает путь к шаблону по умолчанию (включая имя файла). |
| [setDml3DEffectsRenderingMode(int value)](#setDml3DEffectsRenderingMode-int-) | Задает значение, определяющее способ визуализации 3D-эффектов. |
| [setDmlEffectsRenderingMode(int value)](#setDmlEffectsRenderingMode-int-) | Задает значение, определяющее, как визуализируются эффекты DrawingML. |
| [setDmlRenderingMode(int value)](#setDmlRenderingMode-int-) | Задает значение, определяющее, как отображаются фигуры DrawingML. |
| [setDocumentPartSavingCallback(IDocumentPartSavingCallback value)](#setDocumentPartSavingCallback-com.aspose.words.IDocumentPartSavingCallback-) | Позволяет управлять сохранением частей документа при сохранении документа в формате HTML или EPUB. |
| [setDocumentSplitCriteria(int value)](#setDocumentSplitCriteria-int-) | Указывает, как документ должен быть разделен при сохранении в[SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB) или же[SaveFormat.AZW\_3](../../com.aspose.words/saveformat\#AZW-3) формат. |
| [setDocumentSplitHeadingLevel(int value)](#setDocumentSplitHeadingLevel-int-) | Указывает максимальный уровень заголовков, на котором можно разделить документ. |
| [setEncoding(Charset value)](#setEncoding-java.nio.charset.Charset-) |  |
| [setEpubNavigationMapLevel(int value)](#setEpubNavigationMapLevel-int-) | Определяет максимальный уровень заголовков, заполняемых навигационной картой при экспорте в формат IDPF EPUB. |
| [setExportCidUrlsForMhtmlResources(boolean value)](#setExportCidUrlsForMhtmlResources-boolean-) | Указывает, следует ли использовать URL-адреса CID (Content-ID) для ссылки на ресурсы (изображения, шрифты, CSS), включенные в документы MHTML. |
| [setExportDocumentProperties(boolean value)](#setExportDocumentProperties-boolean-) | Указывает, следует ли экспортировать встроенные и настраиваемые свойства документа в HTML, MHTML или EPUB. |
| [setExportDropDownFormFieldAsText(boolean value)](#setExportDropDownFormFieldAsText-boolean-) | Определяет, как поля раскрывающихся форм сохраняются в HTML или MHTML. |
| [setExportFontResources(boolean value)](#setExportFontResources-boolean-) | Указывает, следует ли экспортировать ресурсы шрифта в HTML, MHTML или EPUB. |
| [setExportFontsAsBase64(boolean value)](#setExportFontsAsBase64-boolean-) | Указывает, следует ли встраивать ресурсы шрифтов в HTML в кодировке Base64. |
| [setExportGeneratorName(boolean value)](#setExportGeneratorName-boolean-) | При значении true имя и версия Aspose.Words встраиваются в создаваемые файлы. |
| [setExportHeadersFootersMode(int value)](#setExportHeadersFootersMode-int-) | Указывает, как верхние и нижние колонтитулы выводятся в HTML, MHTML или EPUB. |
| [setExportImagesAsBase64(boolean value)](#setExportImagesAsBase64-boolean-) | Указывает, сохраняются ли изображения в формате Base64 в выходной HTML, MHTML или EPUB. |
| [setExportLanguageInformation(boolean value)](#setExportLanguageInformation-boolean-) | Указывает, экспортируется ли языковая информация в HTML, MHTML или EPUB. |
| [setExportListLabels(int value)](#setExportListLabels-int-) | Управляет выводом меток списков в HTML, MHTML или EPUB. |
| [setExportOriginalUrlForLinkedImages(boolean value)](#setExportOriginalUrlForLinkedImages-boolean-) | Указывает, следует ли использовать исходный URL-адрес в качестве URL-адреса связанных изображений. |
| [setExportPageMargins(boolean value)](#setExportPageMargins-boolean-) | Указывает, экспортируются ли поля страницы в HTML, MHTML или EPUB. |
| [setExportPageSetup(boolean value)](#setExportPageSetup-boolean-) | Указывает, экспортируются ли настройки страницы в HTML, MHTML или EPUB. |
| [setExportRelativeFontSize(boolean value)](#setExportRelativeFontSize-boolean-) | Указывает, должны ли размеры шрифта выводиться в относительных единицах при сохранении в HTML, MHTML или EPUB. |
| [setExportRoundtripInformation(boolean value)](#setExportRoundtripInformation-boolean-) | Указывает, следует ли записывать информацию о цикле приема-передачи при сохранении в HTML, MHTML или EPUB. |
| [setExportShapesAsSvg(boolean value)](#setExportShapesAsSvg-boolean-) |  Контролирует ли[Shape](../../com.aspose.words/shape) узлы преобразуются в изображения SVG при сохранении в HTML, MHTML, EPUB или AZW3. |
| [setExportTextInputFormFieldAsText(boolean value)](#setExportTextInputFormFieldAsText-boolean-) | Управляет способом сохранения полей формы ввода текста в формате HTML или MHTML. |
| [setExportTocPageNumbers(boolean value)](#setExportTocPageNumbers-boolean-) | Указывает, записывать ли номера страниц в оглавление при сохранении HTML, MHTML и EPUB. |
| [setExportXhtmlTransitional(boolean value)](#setExportXhtmlTransitional-boolean-) | Указывает, следует ли записывать объявление DOCTYPE при сохранении в HTML или MHTML. |
| [setFontResourcesSubsettingSizeThreshold(int value)](#setFontResourcesSubsettingSizeThreshold-int-) | Определяет, какие ресурсы шрифтов нуждаются в подразделении при сохранении в HTML, MHTML или EPUB. |
| [setFontSavingCallback(IFontSavingCallback value)](#setFontSavingCallback-com.aspose.words.IFontSavingCallback-) | Позволяет управлять сохранением шрифтов при сохранении документа в формате HTML, MHTML или EPUB. |
| [setFontsFolder(String value)](#setFontsFolder-java.lang.String-) | Указывает физическую папку, в которой сохраняются шрифты при экспорте документа в HTML. |
| [setFontsFolderAlias(String value)](#setFontsFolderAlias-java.lang.String-) | Указывает имя папки, используемой для создания URI шрифтов, записываемых в HTML-документ. |
| [setHtmlVersion(int value)](#setHtmlVersion-int-) | Указывает версию стандарта HTML, которую следует использовать при сохранении документа в формате HTML или MHTML. |
| [setImageResolution(int value)](#setImageResolution-int-) | Указывает выходное разрешение для изображений при экспорте в HTML, MHTML или EPUB. |
| [setImageSavingCallback(IImageSavingCallback value)](#setImageSavingCallback-com.aspose.words.IImageSavingCallback-) | Позволяет управлять способом сохранения изображений при сохранении документа в формате HTML, MHTML или EPUB. |
| [setImagesFolder(String value)](#setImagesFolder-java.lang.String-) | Указывает физическую папку, в которой сохраняются изображения при экспорте документа в формат HTML. |
| [setImagesFolderAlias(String value)](#setImagesFolderAlias-java.lang.String-) | Указывает имя папки, используемой для создания URI изображений, записываемых в HTML-документ. |
| [setImlRenderingMode(int value)](#setImlRenderingMode-int-) | Задает значение, определяющее способ визуализации объектов рукописного ввода (InkML). |
| [setMemoryOptimization(boolean value)](#setMemoryOptimization-boolean-) | Задает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. |
| [setMetafileFormat(int value)](#setMetafileFormat-int-) | Указывает, в каком формате сохраняются метафайлы при экспорте в HTML, MHTML или EPUB. |
| [setOfficeMathOutputMode(int value)](#setOfficeMathOutputMode-int-) | Управляет экспортом объектов OfficeMath в HTML, MHTML или EPUB. |
| [setPrettyFormat(boolean value)](#setPrettyFormat-boolean-) | Когда true , красивые форматы выводятся там, где это применимо. |
| [setProgressCallback(IDocumentSavingCallback value)](#setProgressCallback-com.aspose.words.IDocumentSavingCallback-) | Вызывается при сохранении документа и принимает данные о ходе сохранения. |
| [setResolveFontNames(boolean value)](#setResolveFontNames-boolean-) | Указывает, разрешаются ли имена семейств шрифтов, используемые в документе, и заменяются ли они в соответствии с[Document.getFontSettings()](../../com.aspose.words/document\#getFontSettings--) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document\#setFontSettings-com.aspose.words.FontSettings-) при записи в форматы на основе HTML. |
| [setResourceFolder(String value)](#setResourceFolder-java.lang.String-) | Указывает физическую папку, в которой сохраняются все ресурсы, такие как изображения, шрифты и внешний CSS, при экспорте документа в HTML. |
| [setResourceFolderAlias(String value)](#setResourceFolderAlias-java.lang.String-) | Задает имя папки, используемой для создания URI всех ресурсов, записываемых в HTML-документ. |
| [setSaveFormat(int value)](#setSaveFormat-int-) | Указывает формат, в котором будет сохранен документ, если используется этот объект параметров сохранения. |
| [setScaleImageToShapeSize(boolean value)](#setScaleImageToShapeSize-boolean-) | Указывает, масштабируются ли изображения с помощью Aspose.Words до размера ограничивающей фигуры при экспорте в HTML, MHTML или EPUB. |
| [setTableWidthOutputMode(int value)](#setTableWidthOutputMode-int-) | Определяет, как ширина таблицы, строки и ячейки экспортируется в HTML, MHTML или EPUB. |
| [setTempFolder(String value)](#setTempFolder-java.lang.String-) | Указывает папку для временных файлов, используемых при сохранении в файл DOC или DOCX. |
| [setUpdateCreatedTimeProperty(boolean value)](#setUpdateCreatedTimeProperty-boolean-) |  Устанавливает значение, определяющее, будет ли[BuiltInDocumentProperties.getCreatedTime()](../../com.aspose.words/builtindocumentproperties\#getCreatedTime--) / [BuiltInDocumentProperties.setCreatedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setCreatedTime-java.util.Date-) свойство обновляется перед сохранением. |
| [setUpdateFields(boolean value)](#setUpdateFields-boolean-) | Задает значение, определяющее, следует ли обновлять поля определенных типов перед сохранением документа в фиксированном формате страницы. |
| [setUpdateLastPrintedProperty(boolean value)](#setUpdateLastPrintedProperty-boolean-) |  Устанавливает значение, определяющее, будет ли[BuiltInDocumentProperties.getLastPrinted()](../../com.aspose.words/builtindocumentproperties\#getLastPrinted--) / [BuiltInDocumentProperties.setLastPrinted(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastPrinted-java.util.Date-) свойство обновляется перед сохранением. |
| [setUpdateLastSavedTimeProperty(boolean value)](#setUpdateLastSavedTimeProperty-boolean-) |  Устанавливает значение, определяющее, будет ли[BuiltInDocumentProperties.getLastSavedTime()](../../com.aspose.words/builtindocumentproperties\#getLastSavedTime--) / [BuiltInDocumentProperties.setLastSavedTime(java.util.Date)](../../com.aspose.words/builtindocumentproperties\#setLastSavedTime-java.util.Date-) свойство обновляется перед сохранением. |
| [setUpdateSdtContent(boolean value)](#setUpdateSdtContent-boolean-) |  Устанавливает значение, определяющее, будет ли содержимое[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) обновляется перед сохранением. |
| [setUseAntiAliasing(boolean value)](#setUseAntiAliasing-boolean-) | Задает значение, определяющее, следует ли использовать сглаживание для рендеринга. |
| [setUseHighQualityRendering(boolean value)](#setUseHighQualityRendering-boolean-) | Устанавливает значение, определяющее, использовать ли высокое качество (т.е. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### HtmlSaveOptions() {#HtmlSaveOptions--}
```
public HtmlSaveOptions()
```


 Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа в[SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML) формат.

### HtmlSaveOptions(int saveFormat) {#HtmlSaveOptions-int-}
```
public HtmlSaveOptions(int saveFormat)
```


Инициализирует новый экземпляр этого класса.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| saveFormat | int |  |

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
### getAllowEmbeddingPostScriptFonts() {#getAllowEmbeddingPostScriptFonts--}
```
public boolean getAllowEmbeddingPostScriptFonts()
```


Получает логическое значение, указывающее, разрешать ли встраивание шрифтов с контурами PostScript при встраивании шрифтов TrueType в документ после его сохранения. Значение по умолчанию**false**.

Обратите внимание: Word не встраивает шрифты PostScript, но может открывать документы со встроенными шрифтами этого типа.

 Этот вариант работает только тогда, когда[FontInfoCollection.getEmbedTrueTypeFonts()](../../com.aspose.words/fontinfocollection\#getEmbedTrueTypeFonts--) / [FontInfoCollection.setEmbedTrueTypeFonts(boolean)](../../com.aspose.words/fontinfocollection\#setEmbedTrueTypeFonts-boolean-) принадлежащий[DocumentBase.getFontInfos()](../../com.aspose.words/documentbase\#getFontInfos--) свойство имеет значение true .

**Возвращает:**
boolean — логическое значение, указывающее, разрешать ли встраивание шрифтов с контурами PostScript при встраивании шрифтов TrueType в документ после его сохранения.
### getAllowNegativeIndent() {#getAllowNegativeIndent--}
```
public boolean getAllowNegativeIndent()
```


Указывает, нормализуются ли отрицательные левый и правый отступы абзацев при сохранении в HTML, MHTML или EPUB. Значение по умолчанию — ложь.

Если отрицательный отступ не разрешен, он экспортируется как нулевое поле в HTML. Если разрешен отрицательный отступ, абзац может частично отображаться за пределами окна браузера.

**Возвращает:**
boolean - соответствующее логическое значение.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Возвращает:**
java.lang.Класс<?>
### getCssClassNamePrefix() {#getCssClassNamePrefix--}
```
public String getCssClassNamePrefix()
```


Указывает префикс, который добавляется ко всем именам классов CSS. Значение по умолчанию — пустая строка, а сгенерированные имена классов CSS не имеют общего префикса.

Если это значение не пустое, все классы CSS, сгенерированные Aspose.Words, будут начинаться с указанного префикса. Это может быть полезно, например, если вы добавляете пользовательский CSS в сгенерированные документы и хотите предотвратить конфликты имен классов.

Если значение не является нулевым или пустым, оно должно быть допустимым идентификатором CSS.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getCssSavingCallback() {#getCssSavingCallback--}
```
public ICssSavingCallback getCssSavingCallback()
```


Позволяет управлять сохранением стилей CSS при сохранении документа в формате HTML, MHTML или EPUB.

**Возвращает:**
[ICssSavingCallback](../../com.aspose.words/icsssavingcallback) - соответствующий[ICssSavingCallback](../../com.aspose.words/icsssavingcallback) ценность.
### getCssStyleSheetFileName() {#getCssStyleSheetFileName--}
```
public String getCssStyleSheetFileName()
```


Указывает путь и имя файла каскадной таблицы стилей (CSS), записываемого при экспорте документа в HTML. По умолчанию это пустая строка.

 Это свойство действует только при сохранении документа в формате HTML и запросе внешней таблицы стилей CSS с помощью[getCssStyleSheetType()](../../com.aspose.words/htmlsaveoptions\#getCssStyleSheetType--) / [setCssStyleSheetType(int)](../../com.aspose.words/htmlsaveoptions\#setCssStyleSheetType-int-).

Если это свойство пусто, файл CSS будет сохранен в той же папке и с тем же именем, что и документ HTML, но с расширением «.css».

Если в этом свойстве указан только путь, но не имя файла, файл CSS будет сохранен в указанную папку и будет иметь то же имя, что и документ HTML, но с расширением «.css».

Если папка, указанная этим свойством, не существует, она будет создана автоматически перед сохранением файла CSS.

 Другой способ указать папку, в которой сохраняется внешний файл CSS, — использовать[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-).

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getCssStyleSheetType() {#getCssStyleSheetType--}
```
public int getCssStyleSheetType()
```


 Указывает, как стили CSS (каскадные таблицы стилей) экспортируются в HTML, MHTML или EPUB. Значение по умолчанию[CssStyleSheetType.INLINE](../../com.aspose.words/cssstylesheettype\#INLINE) для HTML/MHTML и[CssStyleSheetType.EXTERNAL](../../com.aspose.words/cssstylesheettype\#EXTERNAL) для EPUB.

 Сохранение таблицы стилей CSS во внешний файл поддерживается только при сохранении в формате HTML. При экспорте в один из форматов контейнера (EPUB или MHTML) и указании[CssStyleSheetType.EXTERNAL](../../com.aspose.words/cssstylesheettype\#EXTERNAL), файл CSS будет инкапсулирован в выходной пакет.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[CssStyleSheetType](../../com.aspose.words/cssstylesheettype) константы.
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
### getDocumentPartSavingCallback() {#getDocumentPartSavingCallback--}
```
public IDocumentPartSavingCallback getDocumentPartSavingCallback()
```


Позволяет управлять сохранением частей документа при сохранении документа в формате HTML или EPUB.

**Возвращает:**
[IDocumentPartSavingCallback](../../com.aspose.words/idocumentpartsavingcallback) - соответствующий[IDocumentPartSavingCallback](../../com.aspose.words/idocumentpartsavingcallback) ценность.
### getDocumentSplitCriteria() {#getDocumentSplitCriteria--}
```
public int getDocumentSplitCriteria()
```


Указывает, как документ должен быть разделен при сохранении в[SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB) или же[SaveFormat.AZW\_3](../../com.aspose.words/saveformat\#AZW-3) формат. По умолчанию[DocumentSplitCriteria.NONE](../../com.aspose.words/documentsplitcriteria\#NONE) для HTML и[DocumentSplitCriteria.HEADING\_PARAGRAPH](../../com.aspose.words/documentsplitcriteria\#HEADING-PARAGRAPH) для EPUB и AZW3.

Обычно вы хотите, чтобы документ был сохранен в HTML как один файл. Но в некоторых случаях предпочтительнее разделить вывод на несколько меньших HTML-страниц. При сохранении в формате HTML эти страницы будут выводиться в отдельные файлы или потоки. При сохранении в формате EPUB они будут объединены в соответствующие пакеты.

Документ нельзя разделить при сохранении в формате MHTML.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение представляет собой побитовую комбинацию[DocumentSplitCriteria](../../com.aspose.words/documentsplitcriteria) константы.
### getDocumentSplitHeadingLevel() {#getDocumentSplitHeadingLevel--}
```
public int getDocumentSplitHeadingLevel()
```


Указывает максимальный уровень заголовков, на котором можно разделить документ. Значение по умолчанию — 2.

 Когда[getDocumentSplitCriteria()](../../com.aspose.words/htmlsaveoptions\#getDocumentSplitCriteria--) / [setDocumentSplitCriteria(int)](../../com.aspose.words/htmlsaveoptions\#setDocumentSplitCriteria-int-) включает[DocumentSplitCriteria.HEADING\_PARAGRAPH](../../com.aspose.words/documentsplitcriteria\#HEADING-PARAGRAPH) и этому свойству присвоено значение от 1 до 9, документ будет разбит на абзацы, отформатированные с использованием**Heading 1**, **Heading 2** , **Heading 3** и т. д. стили до указанного уровня заголовка.

 По умолчанию только**Heading 1** а также**Heading 2** абзацы приводят к разделению документа. Установка этого свойства в ноль приведет к тому, что документ вообще не будет разбиваться на абзацы заголовков.

**Возвращает:**
int - соответствующее значение int.
### getEncoding() {#getEncoding--}
```
public Charset getEncoding()
```




**Возвращает:**
java.nio.charset.Charset
### getEpubNavigationMapLevel() {#getEpubNavigationMapLevel--}
```
public int getEpubNavigationMapLevel()
```


Определяет максимальный уровень заголовков, заполняемых навигационной картой при экспорте в формат IDPF EPUB. Значение по умолчанию — 3.

Карта навигации в формате IDPF EPUB позволяет агентам пользователя обеспечивать простой способ навигации по структуре документа. Обычно точки навигации соответствуют заголовкам в документе. Чтобы заполнить заголовки до уровня**N** присвоить это значение[getEpubNavigationMapLevel()](../../com.aspose.words/htmlsaveoptions\#getEpubNavigationMapLevel--) / [setEpubNavigationMapLevel(int)](../../com.aspose.words/htmlsaveoptions\#setEpubNavigationMapLevel-int-).

 По умолчанию заполняются три уровня заголовков: абзацы стилей**Heading 1**, **Heading 2** а также**Heading 3**. Вы можете установить для этого свойства значение от 1 до 9, чтобы запросить соответствующий максимальный уровень. Установка его на ноль уменьшит карту навигации только до корня документа или корней частей документа.

**Возвращает:**
int - соответствующее значение int.
### getExportCidUrlsForMhtmlResources() {#getExportCidUrlsForMhtmlResources--}
```
public boolean getExportCidUrlsForMhtmlResources()
```


Указывает, следует ли использовать URL-адреса CID (Content-ID) для ссылки на ресурсы (изображения, шрифты, CSS), включенные в документы MHTML. Значение по умолчанию — ложь.

Этот параметр влияет только на документы, сохраняемые в формате MHTML.

По умолчанию на ресурсы в документах MHTML ссылаются по имени файла (например, «image.png»), которое сопоставляется с заголовками «Content-Location» частей MIME.

Этот параметр включает альтернативный метод, при котором ссылки на файлы ресурсов записываются как URL-адреса CID (Content-ID) (например, «cid:image.png») и сопоставляются с заголовками «Content-ID».

Теоретически не должно быть никакой разницы между двумя способами ссылки, и любой из них должен нормально работать в любом браузере или почтовом агенте. Однако на практике некоторым агентам не удается получить ресурсы по имени файла. Если ваш браузер или почтовый агент отказывается загружать ресурсы, включенные в документ MTHML (не показывает изображения или не загружает стили CSS), попробуйте экспортировать документ с URL-адресами CID.

**Возвращает:**
boolean - соответствующее логическое значение.
### getExportDocumentProperties() {#getExportDocumentProperties--}
```
public boolean getExportDocumentProperties()
```


Указывает, следует ли экспортировать встроенные и настраиваемые свойства документа в HTML, MHTML или EPUB. Значение по умолчанию — ложь.

**Возвращает:**
boolean - соответствующее логическое значение.
### getExportDropDownFormFieldAsText() {#getExportDropDownFormFieldAsText--}
```
public boolean getExportDropDownFormFieldAsText()
```


Определяет, как поля раскрывающихся форм сохраняются в HTML или MHTML. Значение по умолчанию — ложь.

Если установлено значение true , поля раскрывающейся формы экспортируются как обычный текст. При значении false экспортирует раскрывающиеся поля формы как элемент SELECT в HTML.

При экспорте в EPUB текстовые поля выпадающей формы всегда сохраняются как текст из-за требований этого формата.

**Возвращает:**
boolean - соответствующее логическое значение.
### getExportFontResources() {#getExportFontResources--}
```
public boolean getExportFontResources()
```


Указывает, следует ли экспортировать ресурсы шрифта в HTML, MHTML или EPUB. Значение по умолчанию — ложь.

Экспорт ресурсов шрифтов обеспечивает согласованную визуализацию документов независимо от шрифтов, доступных в среде данного пользователя.

 Если[getExportFontResources()](../../com.aspose.words/htmlsaveoptions\#getExportFontResources--) / [setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportFontResources-boolean-) установлено значение true , основной HTML-документ будет ссылаться на каждый шрифт через CSS 3**@font-face** at-rule и шрифты будут выводиться отдельными файлами. При экспорте в форматы IDPF EPUB или MHTML шрифты будут встроены в соответствующий пакет вместе с другими вспомогательными файлами.

 Если[getExportFontsAsBase64()](../../com.aspose.words/htmlsaveoptions\#getExportFontsAsBase64--) / [setExportFontsAsBase64(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportFontsAsBase64-boolean-) установлено значение true , шрифты не будут сохраняться в отдельные файлы. Вместо этого они будут встроены в**@font-face** at-правила в кодировке Base64.

**Important!**При экспорте ресурсов шрифтов следует учитывать вопросы лицензирования шрифтов. Авторы, которые хотят использовать определенные шрифты с помощью загружаемого механизма шрифтов, должны всегда тщательно проверять, что их предполагаемое использование находится в рамках лицензии на шрифт. Многие коммерческие шрифты в настоящее время не позволяют загружать свои шрифты из Интернета в любой форме. В лицензионных соглашениях, распространяющихся на некоторые шрифты, особо отмечается, что использование через**@font-face** правила в таблицах стилей CSS не разрешены. Подмножество шрифтов также может нарушать условия лицензии.

**Возвращает:**
boolean - соответствующее логическое значение.
### getExportFontsAsBase64() {#getExportFontsAsBase64--}
```
public boolean getExportFontsAsBase64()
```


Указывает, следует ли встраивать ресурсы шрифтов в HTML в кодировке Base64. Значение по умолчанию — ложь.

По умолчанию шрифты записываются в отдельные файлы. Если для этого параметра установлено значение true , шрифты будут встроены в CSS документа в кодировке Base64.

**Возвращает:**
boolean - соответствующее логическое значение.
### getExportGeneratorName() {#getExportGeneratorName--}
```
public boolean getExportGeneratorName()
```


 При значении true имя и версия Aspose.Words встраиваются в создаваемые файлы. Значение по умолчанию**true**.

**Возвращает:**
boolean - соответствующее логическое значение.
### getExportHeadersFootersMode() {#getExportHeadersFootersMode--}
```
public int getExportHeadersFootersMode()
```


 Указывает, как верхние и нижние колонтитулы выводятся в HTML, MHTML или EPUB. Значение по умолчанию[ExportHeadersFootersMode.PER\_SECTION](../../com.aspose.words/exportheadersfootersmode\#PER-SECTION) для HTML/MHTML и[ExportHeadersFootersMode.NONE](../../com.aspose.words/exportheadersfootersmode\#NONE) для EPUB.

Трудно осмысленно выводить верхние и нижние колонтитулы в HTML, потому что HTML не разбит на страницы.

 Когда это свойство[ExportHeadersFootersMode.PER\_SECTION](../../com.aspose.words/exportheadersfootersmode\#PER-SECTION)Aspose.Words экспортирует только основные верхние и нижние колонтитулы в начале и в конце каждого раздела.

 Когда он является[ExportHeadersFootersMode.FIRST\_SECTION\_HEADER\_LAST\_SECTION\_FOOTER](../../com.aspose.words/exportheadersfootersmode\#FIRST-SECTION-HEADER-LAST-SECTION-FOOTER) экспортируются только первый основной заголовок и последний основной нижний колонтитул (включая ссылку на предыдущий).

 Вы можете полностью отключить экспорт верхних и нижних колонтитулов, установив для этого свойства значение[ExportHeadersFootersMode.NONE](../../com.aspose.words/exportheadersfootersmode\#NONE).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[ExportHeadersFootersMode](../../com.aspose.words/exportheadersfootersmode) константы.
### getExportImagesAsBase64() {#getExportImagesAsBase64--}
```
public boolean getExportImagesAsBase64()
```


Указывает, сохраняются ли изображения в формате Base64 в выходной HTML, MHTML или EPUB. Значение по умолчанию — ложь.

 Когда для этого свойства установлено значение true, данные изображений экспортируются непосредственно в**img** элементы и отдельные файлы не создаются.

**Возвращает:**
boolean - соответствующее логическое значение.
### getExportLanguageInformation() {#getExportLanguageInformation--}
```
public boolean getExportLanguageInformation()
```


Указывает, экспортируется ли языковая информация в HTML, MHTML или EPUB. Значение по умолчанию — ложь.

 Когда для этого свойства установлено значение true, выходные данные Aspose.Words**lang** Атрибут HTML в элементах документа, указывающий язык. Это может быть необходимо для сохранения семантики, связанной с языком.

**Возвращает:**
boolean - соответствующее логическое значение.
### getExportListLabels() {#getExportListLabels--}
```
public int getExportListLabels()
```


 Управляет выводом меток списков в HTML, MHTML или EPUB. Значение по умолчанию[ExportListLabels.AUTO](../../com.aspose.words/exportlistlabels\#AUTO).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[ExportListLabels](../../com.aspose.words/exportlistlabels) константы.
### getExportOriginalUrlForLinkedImages() {#getExportOriginalUrlForLinkedImages--}
```
public boolean getExportOriginalUrlForLinkedImages()
```


Указывает, следует ли использовать исходный URL-адрес в качестве URL-адреса связанных изображений. Значение по умолчанию — ложь.

 Если установлено значение true[ImageData.getSourceFullName()](../../com.aspose.words/imagedata\#getSourceFullName--) / [ImageData.setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata\#setSourceFullName-java.lang.String-) значение используется в качестве URL-адреса связанных изображений, а связанные изображения не загружаются в папку документа или[getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-).

 Если установлено значение false, связанные изображения загружаются в папку документа или[getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-) и URL каждого связанного изображения строится в зависимости от папки документа,[getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-) а также[getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-) характеристики.

**Возвращает:**
boolean - соответствующее логическое значение.
### getExportPageMargins() {#getExportPageMargins--}
```
public boolean getExportPageMargins()
```


Указывает, экспортируются ли поля страницы в HTML, MHTML или EPUB. Значение по умолчанию — ложь. По умолчанию Aspose.Words не показывает область полей страницы. Если какие-либо элементы полностью или частично обрезаны краем документа, с помощью этой опции можно расширить отображаемую область.

**Возвращает:**
boolean - соответствующее логическое значение.
### getExportPageSetup() {#getExportPageSetup--}
```
public boolean getExportPageSetup()
```


Указывает, экспортируются ли настройки страницы в HTML, MHTML или EPUB. Значение по умолчанию — ложь.

 Каждый[Section](../../com.aspose.words/section) в модели документа Aspose.Words предоставляет информацию о настройках страницы через[PageSetup](../../com.aspose.words/pagesetup)учебный класс. При экспорте документа в формат HTML может потребоваться сохранить эту информацию для дальнейшего использования. В частности, настройка страницы может быть важна для рендеринга на постраничный носитель (печать) или последующего преобразования в исходные форматы файлов Microsoft Word (DOCX, DOC, RTF, WML).

В большинстве случаев HTML предназначен для просмотра в браузерах, где не выполняется пагинация. Так что эта функция неактивна по умолчанию.

**Возвращает:**
boolean - соответствующее логическое значение.
### getExportRelativeFontSize() {#getExportRelativeFontSize--}
```
public boolean getExportRelativeFontSize()
```


Указывает, должны ли размеры шрифта выводиться в относительных единицах при сохранении в HTML, MHTML или EPUB. Значение по умолчанию — ложь.

 Во многих существующих документах (HTML, IDPF EPUB) размеры шрифтов указаны в относительных единицах. Это позволяет приложениям настраивать размер текста при просмотре/обработке документов. Например, в Microsoft Internet Explorer есть подменю «Вид->Размер текста», в Adobe Digital Editions есть две кнопки: Увеличить/Уменьшить размер текста. Если вы ожидаете, что эта функция будет работать, установите[getExportRelativeFontSize()](../../com.aspose.words/htmlsaveoptions\#getExportRelativeFontSize--) / [setExportRelativeFontSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportRelativeFontSize-boolean-) свойство истинное.

Модель документа Aspose Words содержит и работает только с единицами абсолютного размера шрифта. Относительные единицы нуждаются в дополнительной логике для пересчета от некоторого начального (стандартного) размера. Размер шрифта**Normal** стиль документа принимается за стандартный. Например, если**Normal** имеет шрифт 12pt, а некоторый текст имеет размер 18pt, тогда он будет выводиться как**1.5em.** к HTML.

 Когда этот параметр включен, элементы документа, кроме текста, по-прежнему будут иметь абсолютные размеры. Также некоторые атрибуты, связанные с текстом, могут быть выражены абсолютно. В частности, межстрочный интервал, указанный с помощью правила «точно», может привести к нежелательным результатам при масштабировании текста. Таким образом, исходные документы должны быть правильно оформлены и протестированы при экспорте с помощью[getExportRelativeFontSize()](../../com.aspose.words/htmlsaveoptions\#getExportRelativeFontSize--) / [setExportRelativeFontSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportRelativeFontSize-boolean-) установить на истину.

**Возвращает:**
boolean - соответствующее логическое значение.
### getExportRoundtripInformation() {#getExportRoundtripInformation--}
```
public boolean getExportRoundtripInformation()
```


Указывает, следует ли записывать информацию о цикле приема-передачи при сохранении в HTML, MHTML или EPUB. Значение по умолчанию — true для HTML и false для MHTML и EPUB.

Сохранение информации об обходе позволяет восстанавливать свойства документа, такие как позиции табуляции, комментарии, верхние и нижние колонтитулы, во время загрузки HTML-документов обратно в формат.[Document](../../com.aspose.words/document) объект.

Когда true , информация о пути туда и обратно экспортируется как -aw-\* Свойства CSS соответствующих элементов HTML.

При значении false информация о циклическом обходе не выводится в создаваемые файлы.

**Возвращает:**
boolean - соответствующее логическое значение.
### getExportShapesAsSvg() {#getExportShapesAsSvg--}
```
public boolean getExportShapesAsSvg()
```


 Контролирует ли[Shape](../../com.aspose.words/shape) узлы преобразуются в изображения SVG при сохранении в HTML, MHTML, EPUB или AZW3. Значение по умолчанию — ложь.

 Если для этой опции установлено значение true ,[Shape](../../com.aspose.words/shape) узлы экспортируются как элементы. В противном случае они преобразуются в растровые изображения и экспортируются как![Изображение 1][] элементы.


[Изображение 1]: 

**Возвращает:**
boolean - соответствующее логическое значение.
### getExportTextInputFormFieldAsText() {#getExportTextInputFormFieldAsText--}
```
public boolean getExportTextInputFormFieldAsText()
```


Управляет способом сохранения полей формы ввода текста в формате HTML или MHTML. Значение по умолчанию — ложь.

Если установлено значение true , поля формы ввода текста экспортируются как обычный текст. При значении false экспортирует поля формы ввода текста Word как элементы INPUT в HTML.

При экспорте в EPUB поля формы ввода текста всегда сохраняются как текст из-за требований этого формата.

**Возвращает:**
boolean - соответствующее логическое значение.
### getExportTocPageNumbers() {#getExportTocPageNumbers--}
```
public boolean getExportTocPageNumbers()
```


Указывает, записывать ли номера страниц в оглавление при сохранении HTML, MHTML и EPUB. Значение по умолчанию — ложь.

**Возвращает:**
boolean - соответствующее логическое значение.
### getExportXhtmlTransitional() {#getExportXhtmlTransitional--}
```
public boolean getExportXhtmlTransitional()
```


 Указывает, следует ли записывать объявление DOCTYPE при сохранении в HTML или MHTML. При значении true записывает объявление DOCTYPE в документ перед корневым элементом. Значение по умолчанию — ложь. При сохранении в EPUB или HTML5 ([HtmlVersion.HTML\_5](../../com.aspose.words/htmlversion\#HTML-5)) всегда записывается объявление DOCTYPE.

Aspose.Words всегда пишет правильно сформированный HTML, независимо от этой настройки.

При значении true начало выходного HTML-документа будет выглядеть так:

```

 
 
 
 
```

Aspose.Words стремится выводить XHTML в соответствии со спецификацией XHTML 1.0 Transitional, но вывод не всегда будет проверяться на соответствие DTD. Некоторые структуры внутри документа Microsoft Word трудно или невозможно сопоставить с документом, который будет проверяться на соответствие схеме XHTML. Например, XHTML не допускает вложенных списков (UL не может быть вложен в другой элемент UL), но в документах Microsoft Word довольно часто встречаются многоуровневые списки.

**Возвращает:**
boolean - соответствующее логическое значение.
### getFontResourcesSubsettingSizeThreshold() {#getFontResourcesSubsettingSizeThreshold--}
```
public int getFontResourcesSubsettingSizeThreshold()
```


Определяет, какие ресурсы шрифтов нуждаются в подразделении при сохранении в HTML, MHTML или EPUB. По умолчанию 0 .

[getExportFontResources()](../../com.aspose.words/htmlsaveoptions\#getExportFontResources--) / [setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportFontResources-boolean-) позволяет экспортировать шрифты как вспомогательные файлы или как части выходного пакета. Если в документе используется много шрифтов, особенно с большим количеством глифов, размер вывода может значительно увеличиться. Подмножество шрифтов уменьшает размер экспортируемого ресурса шрифта, отфильтровывая глифы, которые не используются текущим документом.

Подмножество шрифтов работает следующим образом:

 *  По умолчанию все экспортируемые шрифты являются подмножествами.
 *   Параметр[getFontResourcesSubsettingSizeThreshold()](../../com.aspose.words/htmlsaveoptions\#getFontResourcesSubsettingSizeThreshold--) / [setFontResourcesSubsettingSizeThreshold(int)](../../com.aspose.words/htmlsaveoptions\#setFontResourcesSubsettingSizeThreshold-int-)положительное значение указывает Aspose.Words на подмножество шрифтов, размер файла которых превышает указанное значение.
 *  Установка свойства подавляет подмножество шрифта.

**Important!**При экспорте ресурсов шрифтов следует учитывать вопросы лицензирования шрифтов. Авторы, которые хотят использовать определенные шрифты с помощью загружаемого механизма шрифтов, должны всегда тщательно проверять, что их предполагаемое использование находится в рамках лицензии на шрифт. Многие коммерческие шрифты в настоящее время не позволяют загружать свои шрифты из Интернета в любой форме. В лицензионных соглашениях, распространяющихся на некоторые шрифты, особо отмечается, что использование через**@font-face** правила в таблицах стилей CSS не разрешены. Подмножество шрифтов также может нарушать условия лицензии.

**Возвращает:**
int - соответствующее значение int.
### getFontSavingCallback() {#getFontSavingCallback--}
```
public IFontSavingCallback getFontSavingCallback()
```


Позволяет управлять сохранением шрифтов при сохранении документа в формате HTML, MHTML или EPUB.

**Возвращает:**
[IFontSavingCallback](../../com.aspose.words/ifontsavingcallback) - соответствующий[IFontSavingCallback](../../com.aspose.words/ifontsavingcallback) ценность.
### getFontsFolder() {#getFontsFolder--}
```
public String getFontsFolder()
```


Указывает физическую папку, в которой сохраняются шрифты при экспорте документа в HTML. По умолчанию это пустая строка.

 Когда вы сохраняете[Document](../../com.aspose.words/document) в формате HTML и[getExportFontResources()](../../com.aspose.words/htmlsaveoptions\#getExportFontResources--) / [setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportFontResources-boolean-) установлено значение true , Aspose.Words необходимо сохранить шрифты, используемые в документе, как отдельные файлы.[getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-) позволяет указать, где будут сохранены шрифты и[getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) позволяет указать, как будут создаваться URI шрифта.

 Если вы сохраняете документ в файл и указываете имя файла, Aspose.Words по умолчанию сохраняет шрифты в той же папке, где сохранен файл документа. Использовать[getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-) переопределить это поведение.

 Если вы сохраняете документ в поток, Aspose.Words не имеет папки для сохранения шрифтов, но все равно должен где-то сохранять шрифты. В этом случае необходимо указать доступную папку в[getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-) свойство или предоставлять пользовательские потоки через[getFontSavingCallback()](../../com.aspose.words/htmlsaveoptions\#getFontSavingCallback--) / [setFontSavingCallback(com.aspose.words.IFontSavingCallback)](../../com.aspose.words/htmlsaveoptions\#setFontSavingCallback-com.aspose.words.IFontSavingCallback-) обработчик события.

Если папка, указанная[getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-) не существует, он будет создан автоматически.

[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-) — это еще один способ указать папку, в которой следует сохранять шрифты.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getFontsFolderAlias() {#getFontsFolderAlias--}
```
public String getFontsFolderAlias()
```


Указывает имя папки, используемой для создания URI шрифтов, записываемых в HTML-документ. По умолчанию это пустая строка.

 Когда вы сохраняете[Document](../../com.aspose.words/document) в формате HTML и[getExportFontResources()](../../com.aspose.words/htmlsaveoptions\#getExportFontResources--) / [setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportFontResources-boolean-) установлено значение true , Aspose.Words необходимо сохранить шрифты, используемые в документе, как отдельные файлы.[getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-) позволяет указать, где будут сохранены шрифты и[getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) позволяет указать, как будут создаваться URI шрифта.

 Если[getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) не является пустой строкой, тогда URI шрифта, записанный в HTML, будет*FontsFolderAlias +* . 

 Если[getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) является пустой строкой, тогда URI шрифта, записанный в HTML, будет*FontsFolder +* . 

 Если[getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) установлен в '.' (точка), то имя файла шрифта будет записано в HTML без указания пути независимо от других параметров.

 Альтернативный способ указать имя папки для создания URI шрифта — использовать[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-).

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getHtmlVersion() {#getHtmlVersion--}
```
public int getHtmlVersion()
```


 Указывает версию стандарта HTML, которую следует использовать при сохранении документа в формате HTML или MHTML. Значение по умолчанию[HtmlVersion.XHTML](../../com.aspose.words/htmlversion\#XHTML).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[HtmlVersion](../../com.aspose.words/htmlversion) константы.
### getImageResolution() {#getImageResolution--}
```
public int getImageResolution()
```


Указывает выходное разрешение для изображений при экспорте в HTML, MHTML или EPUB. По умолчанию — 96 dpi.

 Это свойство влияет на растровые изображения, когда[getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions\#getScaleImageToShapeSize--) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setScaleImageToShapeSize-boolean-)имеет значение true и влияет на метафайлы, экспортируемые как растровые изображения. Некоторые свойства изображения, такие как обрезка или поворот, требуют сохранения преобразованных изображений, и в этом случае преобразованные изображения создаются в заданном разрешении.

**Возвращает:**
int - соответствующее значение int.
### getImageSavingCallback() {#getImageSavingCallback--}
```
public IImageSavingCallback getImageSavingCallback()
```


Позволяет управлять способом сохранения изображений при сохранении документа в формате HTML, MHTML или EPUB.

**Возвращает:**
[IImageSavingCallback](../../com.aspose.words/iimagesavingcallback) - соответствующий[IImageSavingCallback](../../com.aspose.words/iimagesavingcallback) ценность.
### getImagesFolder() {#getImagesFolder--}
```
public String getImagesFolder()
```


Указывает физическую папку, в которой сохраняются изображения при экспорте документа в формат HTML. По умолчанию это пустая строка.

 Когда вы сохраняете[Document](../../com.aspose.words/document) в формате HTML Aspose.Words должен сохранять все изображения, встроенные в документ, как отдельные файлы.[getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-) позволяет указать, где изображения будут сохранены и[getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-) позволяет указать, как будут создаваться URI изображения.

Если вы сохраняете документ в файл и указываете имя файла, Aspose.Words по умолчанию сохраняет изображения в той же папке, где сохранен файл документа. Использовать[getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-) переопределить это поведение.

 Если вы сохраняете документ в потоке, Aspose.Words не имеет папки для сохранения изображений, но все же необходимо где-то сохранять изображения. В этом случае необходимо указать доступную папку в[getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-) свойство или предоставлять пользовательские потоки через[getImageSavingCallback()](../../com.aspose.words/htmlsaveoptions\#getImageSavingCallback--) / [setImageSavingCallback(com.aspose.words.IImageSavingCallback)](../../com.aspose.words/htmlsaveoptions\#setImageSavingCallback-com.aspose.words.IImageSavingCallback-) обработчик события.

Если папка, указанная[getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-) не существует, он будет создан автоматически.

[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-) — это еще один способ указать папку, в которую следует сохранять изображения.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getImagesFolderAlias() {#getImagesFolderAlias--}
```
public String getImagesFolderAlias()
```


Указывает имя папки, используемой для создания URI изображений, записываемых в HTML-документ. По умолчанию это пустая строка.

 Когда вы сохраняете[Document](../../com.aspose.words/document) в формате HTML Aspose.Words должен сохранять все изображения, встроенные в документ, как отдельные файлы.[getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-) позволяет указать, где изображения будут сохранены и[getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-) позволяет указать, как будут создаваться URI изображения.

 Если[getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-) не является пустой строкой, тогда URI изображения, записанный в HTML, будет*ImagesFolderAlias + ![Image 1][]*.

 Если[getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-) является пустой строкой, тогда URI изображения, записанный в HTML, будет*ImagesFolder + ![Image 1][]*.

 Если[getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-)установлен в '.' (точка), то имя файла изображения будет записано в HTML без указания пути независимо от других параметров.

 Альтернативный способ указать имя папки для создания URI изображений — использовать[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-).


[Изображение 1]: 

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getImlRenderingMode() {#getImlRenderingMode--}
```
public int getImlRenderingMode()
```


 Получает значение, определяющее способ визуализации объектов рукописного ввода (InkML). Значение по умолчанию[ImlRenderingMode.INK\_ML](../../com.aspose.words/imlrenderingmode\#INK-ML).

Это свойство используется, когда документ экспортируется в фиксированные форматы страниц.

**Возвращает:**
 int — значение, определяющее способ отображения объектов рукописного ввода (InkML). Возвращаемое значение является одним из[ImlRenderingMode](../../com.aspose.words/imlrenderingmode) константы.
### getMemoryOptimization() {#getMemoryOptimization--}
```
public boolean getMemoryOptimization()
```


Получает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойства**false**. Установка для этого параметра значения true может значительно снизить потребление памяти при сохранении больших документов за счет замедления времени сохранения.

**Возвращает:**
boolean — значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа.
### getMetafileFormat() {#getMetafileFormat--}
```
public int getMetafileFormat()
```


 Указывает, в каком формате сохраняются метафайлы при экспорте в HTML, MHTML или EPUB. Значение по умолчанию[HtmlMetafileFormat.PNG](../../com.aspose.words/htmlmetafileformat\#PNG), что означает, что метафайлы преобразуются в растровые изображения PNG.

Метафайлы изначально не отображаются браузерами HTML. По умолчанию Aspose.Words конвертирует изображения WMF и EMF в файлы PNG при экспорте в HTML. Другие варианты — преобразовать метафайлы в изображения SVG или экспортировать их как есть без преобразования.

Некоторые преобразования изображений, в частности обрезка изображений, не будут применяться к изображениям метафайлов, если они экспортируются в HTML без преобразования.

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[HtmlMetafileFormat](../../com.aspose.words/htmlmetafileformat) константы.
### getOfficeMathOutputMode() {#getOfficeMathOutputMode--}
```
public int getOfficeMathOutputMode()
```


Управляет экспортом объектов OfficeMath в HTML, MHTML или EPUB. Значение по умолчанию — HtmlOfficeMathOutputMode.Image .

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[HtmlOfficeMathOutputMode](../../com.aspose.words/htmlofficemathoutputmode) константы.
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
### getResolveFontNames() {#getResolveFontNames--}
```
public boolean getResolveFontNames()
```


Указывает, разрешаются ли имена семейств шрифтов, используемые в документе, и заменяются ли они в соответствии с[Document.getFontSettings()](../../com.aspose.words/document\#getFontSettings--) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document\#setFontSettings-com.aspose.words.FontSettings-) при записи в форматы на основе HTML.

По умолчанию для этого параметра установлено значение false, и имена семейств шрифтов записываются в HTML, как указано в исходных документах. То есть,[Document.getFontSettings()](../../com.aspose.words/document\#getFontSettings--) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document\#setFontSettings-com.aspose.words.FontSettings-) игнорируются, и разрешение или замена имен семейств шрифтов не выполняются.

 Если для этого параметра установлено значение true , Aspose.Words использует[Document.getFontSettings()](../../com.aspose.words/document\#getFontSettings--) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document\#setFontSettings-com.aspose.words.FontSettings-) преобразовать каждое имя семейства шрифтов, указанное в исходном документе, в имя доступного семейства шрифтов, выполняя замену шрифта по мере необходимости.

**Возвращает:**
boolean - соответствующее логическое значение.
### getResourceFolder() {#getResourceFolder--}
```
public String getResourceFolder()
```


Указывает физическую папку, в которой сохраняются все ресурсы, такие как изображения, шрифты и внешний CSS, при экспорте документа в HTML. По умолчанию это пустая строка.

[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-) это самый простой способ указать папку, в которую должны быть записаны все ресурсы. Другой способ — использовать отдельные свойства[getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-), [getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-) , а также[getCssStyleSheetFileName()](../../com.aspose.words/htmlsaveoptions\#getCssStyleSheetFileName--) / [setCssStyleSheetFileName(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setCssStyleSheetFileName-java.lang.String-).

[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-) имеет более низкий приоритет, чем папки, указанные через[getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-), [getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-) , а также[getCssStyleSheetFileName()](../../com.aspose.words/htmlsaveoptions\#getCssStyleSheetFileName--) / [setCssStyleSheetFileName(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setCssStyleSheetFileName-java.lang.String-) . Например, если оба[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-) а также[getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-) указаны, шрифты будут сохранены в[getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-) , а изображения и CSS будут сохранены в[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-).

Если папка, указанная[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-) не существует, он будет создан автоматически.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getResourceFolderAlias() {#getResourceFolderAlias--}
```
public String getResourceFolderAlias()
```


Задает имя папки, используемой для создания URI всех ресурсов, записываемых в HTML-документ. По умолчанию это пустая строка.

[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-) — это самый простой способ указать, как должны быть созданы URI для всех файлов ресурсов. Та же информация может быть указана для изображений и шрифтов отдельно через[getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-) а также[getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) свойства соответственно. Однако для CSS нет отдельного свойства.

[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-) имеет более низкий приоритет, чем[getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) а также[getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-) . Например, если оба[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-) а также[getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) указаны, URI шрифтов будут построены с использованием[getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) , а URI изображений и CSS будут создаваться с использованием[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-).

 Если[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-) пусто, т.[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-) значение свойства будет использоваться для создания URI ресурсов.

 Если[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-) установлен в '.' (точка), URI ресурсов будут содержать только имена файлов без указания пути.

**Возвращает:**
java.lang.String — соответствующее значение java.lang.String.
### getSaveFormat() {#getSaveFormat--}
```
public int getSaveFormat()
```


 Указывает формат, в котором будет сохранен документ, если используется этот объект параметров сохранения. Может быть[SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB) или же[SaveFormat.AZW\_3](../../com.aspose.words/saveformat\#AZW-3).

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[SaveFormat](../../com.aspose.words/saveformat) константы.
### getScaleImageToShapeSize() {#getScaleImageToShapeSize--}
```
public boolean getScaleImageToShapeSize()
```


Указывает, масштабируются ли изображения с помощью Aspose.Words до размера ограничивающей фигуры при экспорте в HTML, MHTML или EPUB. Значение по умолчанию — true.

Изображение в документе Microsoft Word представляет собой фигуру. Форма имеет размер, а изображение имеет собственный размер. Размеры напрямую не связаны. Например, изображение может иметь размер 1024x786 пикселей, а форма, отображающая это изображение, может иметь размер 400x300 точек.

 Чтобы изображение отображалось в браузере, оно должно быть масштабировано до размера фигуры.[getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions\#getScaleImageToShapeSize--) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setScaleImageToShapeSize-boolean-) Свойство управляет тем, где происходит масштабирование изображения: в Aspose.Words при экспорте в HTML или в браузере при отображении документа.

 Когда[getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions\#getScaleImageToShapeSize--) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setScaleImageToShapeSize-boolean-) true , Aspose.Words масштабирует изображение с использованием высококачественного масштабирования при экспорте в HTML. Когда[getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions\#getScaleImageToShapeSize--) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setScaleImageToShapeSize-boolean-) false , изображение выводится с исходным размером, и браузер должен масштабировать его.

 Как правило, браузеры делают быстрое и некачественное масштабирование. В результате вы обычно получаете лучшее качество отображения в браузере и меньший размер файла при[getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions\#getScaleImageToShapeSize--) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setScaleImageToShapeSize-boolean-) верно, но лучшее качество печати и более быстрое преобразование при[getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions\#getScaleImageToShapeSize--) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setScaleImageToShapeSize-boolean-) является ложным.

**Возвращает:**
boolean - соответствующее логическое значение.
### getTableWidthOutputMode() {#getTableWidthOutputMode--}
```
public int getTableWidthOutputMode()
```


Определяет, как ширина таблицы, строки и ячейки экспортируется в HTML, MHTML или EPUB. Значение по умолчанию[HtmlElementSizeOutputMode.ALL](../../com.aspose.words/htmlelementsizeoutputmode\#ALL).

В формате HTML элементы таблицы, строки и ячейки ( 

    | -- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
    | ,  | ) can have their widths specified either in relative (percentage) or in absolute units. In a document in Aspose.Words, tables, rows and cells can have their widths specified using either relative or absolute units too.
 
 Когда вы конвертируете документ в HTML с помощью Aspose.Words, вы можете захотеть контролировать, как экспортируется ширина таблицы, строки и ячейки, чтобы влиять на то, как результирующий документ отображается в визуальном агенте (например, в браузере или средстве просмотра).
 
  Используйте это свойство в качестве фильтра, чтобы указать, какие значения ширины таблицы экспортируются в целевой документ. Например, если вы конвертируете документ в формат EPUB и собираетесь просматривать его на мобильном устройстве для чтения, вам, вероятно, следует избегать экспорта абсолютных значений ширины. Для этого нужно указать режим вывода[HtmlElementSizeOutputMode.RELATIVE\_ONLY](../../com.aspose.words/htmlelementsizeoutputmode\#RELATIVE-ONLY) или же[HtmlElementSizeOutputMode.NONE](../../com.aspose.words/htmlelementsizeoutputmode\#NONE) Таким образом, зритель на мобильном устройстве может расположить таблицу так, чтобы она соответствовала ширине экрана, насколько это возможно.|

**Возвращает:**
 int - соответствующее значение int. Возвращаемое значение является одним из[HtmlElementSizeOutputMode](../../com.aspose.words/htmlelementsizeoutputmode) константы.
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

### setAllowNegativeIndent(boolean value) {#setAllowNegativeIndent-boolean-}
```
public void setAllowNegativeIndent(boolean value)
```


Указывает, нормализуются ли отрицательные левый и правый отступы абзацев при сохранении в HTML, MHTML или EPUB. Значение по умолчанию — ложь.

Если отрицательный отступ не разрешен, он экспортируется как нулевое поле в HTML. Если разрешен отрицательный отступ, абзац может частично отображаться за пределами окна браузера.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setCssClassNamePrefix(String value) {#setCssClassNamePrefix-java.lang.String-}
```
public void setCssClassNamePrefix(String value)
```


Указывает префикс, который добавляется ко всем именам классов CSS. Значение по умолчанию — пустая строка, а сгенерированные имена классов CSS не имеют общего префикса.

Если это значение не пустое, все классы CSS, сгенерированные Aspose.Words, будут начинаться с указанного префикса. Это может быть полезно, например, если вы добавляете пользовательский CSS в сгенерированные документы и хотите предотвратить конфликты имен классов.

Если значение не является нулевым или пустым, оно должно быть допустимым идентификатором CSS.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setCssSavingCallback(ICssSavingCallback value) {#setCssSavingCallback-com.aspose.words.ICssSavingCallback-}
```
public void setCssSavingCallback(ICssSavingCallback value)
```


Позволяет управлять сохранением стилей CSS при сохранении документа в формате HTML, MHTML или EPUB.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [ICssSavingCallback](../../com.aspose.words/icsssavingcallback) |  Соответствующий[ICssSavingCallback](../../com.aspose.words/icsssavingcallback) ценность. |

### setCssStyleSheetFileName(String value) {#setCssStyleSheetFileName-java.lang.String-}
```
public void setCssStyleSheetFileName(String value)
```


Указывает путь и имя файла каскадной таблицы стилей (CSS), записываемого при экспорте документа в HTML. По умолчанию это пустая строка.

 Это свойство действует только при сохранении документа в формате HTML и запросе внешней таблицы стилей CSS с помощью[getCssStyleSheetType()](../../com.aspose.words/htmlsaveoptions\#getCssStyleSheetType--) / [setCssStyleSheetType(int)](../../com.aspose.words/htmlsaveoptions\#setCssStyleSheetType-int-).

Если это свойство пусто, файл CSS будет сохранен в той же папке и с тем же именем, что и документ HTML, но с расширением «.css».

Если в этом свойстве указан только путь, но не имя файла, файл CSS будет сохранен в указанную папку и будет иметь то же имя, что и документ HTML, но с расширением «.css».

Если папка, указанная этим свойством, не существует, она будет создана автоматически перед сохранением файла CSS.

 Другой способ указать папку, в которой сохраняется внешний файл CSS, — использовать[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setCssStyleSheetType(int value) {#setCssStyleSheetType-int-}
```
public void setCssStyleSheetType(int value)
```


 Указывает, как стили CSS (каскадные таблицы стилей) экспортируются в HTML, MHTML или EPUB. Значение по умолчанию[CssStyleSheetType.INLINE](../../com.aspose.words/cssstylesheettype\#INLINE) для HTML/MHTML и[CssStyleSheetType.EXTERNAL](../../com.aspose.words/cssstylesheettype\#EXTERNAL) для EPUB.

 Сохранение таблицы стилей CSS во внешний файл поддерживается только при сохранении в формате HTML. При экспорте в один из форматов контейнера (EPUB или MHTML) и указании[CssStyleSheetType.EXTERNAL](../../com.aspose.words/cssstylesheettype\#EXTERNAL), файл CSS будет инкапсулирован в выходной пакет.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[CssStyleSheetType](../../com.aspose.words/cssstylesheettype) константы. |

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

### setDocumentPartSavingCallback(IDocumentPartSavingCallback value) {#setDocumentPartSavingCallback-com.aspose.words.IDocumentPartSavingCallback-}
```
public void setDocumentPartSavingCallback(IDocumentPartSavingCallback value)
```


Позволяет управлять сохранением частей документа при сохранении документа в формате HTML или EPUB.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [IDocumentPartSavingCallback](../../com.aspose.words/idocumentpartsavingcallback) |  Соответствующий[IDocumentPartSavingCallback](../../com.aspose.words/idocumentpartsavingcallback) ценность. |

### setDocumentSplitCriteria(int value) {#setDocumentSplitCriteria-int-}
```
public void setDocumentSplitCriteria(int value)
```


Указывает, как документ должен быть разделен при сохранении в[SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB) или же[SaveFormat.AZW\_3](../../com.aspose.words/saveformat\#AZW-3) формат. По умолчанию[DocumentSplitCriteria.NONE](../../com.aspose.words/documentsplitcriteria\#NONE) для HTML и[DocumentSplitCriteria.HEADING\_PARAGRAPH](../../com.aspose.words/documentsplitcriteria\#HEADING-PARAGRAPH) для EPUB и AZW3.

Обычно вы хотите, чтобы документ был сохранен в HTML как один файл. Но в некоторых случаях предпочтительнее разделить вывод на несколько меньших HTML-страниц. При сохранении в формате HTML эти страницы будут выводиться в отдельные файлы или потоки. При сохранении в формате EPUB они будут объединены в соответствующие пакеты.

Документ нельзя разделить при сохранении в формате MHTML.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть побитовой комбинацией[DocumentSplitCriteria](../../com.aspose.words/documentsplitcriteria) константы. |

### setDocumentSplitHeadingLevel(int value) {#setDocumentSplitHeadingLevel-int-}
```
public void setDocumentSplitHeadingLevel(int value)
```


Указывает максимальный уровень заголовков, на котором можно разделить документ. Значение по умолчанию — 2.

 Когда[getDocumentSplitCriteria()](../../com.aspose.words/htmlsaveoptions\#getDocumentSplitCriteria--) / [setDocumentSplitCriteria(int)](../../com.aspose.words/htmlsaveoptions\#setDocumentSplitCriteria-int-) включает[DocumentSplitCriteria.HEADING\_PARAGRAPH](../../com.aspose.words/documentsplitcriteria\#HEADING-PARAGRAPH) и этому свойству присвоено значение от 1 до 9, документ будет разбит на абзацы, отформатированные с использованием**Heading 1**, **Heading 2** , **Heading 3** и т. д. стили до указанного уровня заголовка.

 По умолчанию только**Heading 1** а также**Heading 2** абзацы приводят к разделению документа. Установка этого свойства в ноль приведет к тому, что документ вообще не будет разбиваться на абзацы заголовков.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее целочисленное значение. |

### setEncoding(Charset value) {#setEncoding-java.nio.charset.Charset-}
```
public void setEncoding(Charset value)
```




**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.nio.charset.Charset |  |

### setEpubNavigationMapLevel(int value) {#setEpubNavigationMapLevel-int-}
```
public void setEpubNavigationMapLevel(int value)
```


Определяет максимальный уровень заголовков, заполняемых навигационной картой при экспорте в формат IDPF EPUB. Значение по умолчанию — 3.

Карта навигации в формате IDPF EPUB позволяет агентам пользователя обеспечивать простой способ навигации по структуре документа. Обычно точки навигации соответствуют заголовкам в документе. Чтобы заполнить заголовки до уровня**N** присвоить это значение[getEpubNavigationMapLevel()](../../com.aspose.words/htmlsaveoptions\#getEpubNavigationMapLevel--) / [setEpubNavigationMapLevel(int)](../../com.aspose.words/htmlsaveoptions\#setEpubNavigationMapLevel-int-).

 По умолчанию заполняются три уровня заголовков: абзацы стилей**Heading 1**, **Heading 2** а также**Heading 3**. Вы можете установить для этого свойства значение от 1 до 9, чтобы запросить соответствующий максимальный уровень. Установка его на ноль уменьшит карту навигации только до корня документа или корней частей документа.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее целочисленное значение. |

### setExportCidUrlsForMhtmlResources(boolean value) {#setExportCidUrlsForMhtmlResources-boolean-}
```
public void setExportCidUrlsForMhtmlResources(boolean value)
```


Указывает, следует ли использовать URL-адреса CID (Content-ID) для ссылки на ресурсы (изображения, шрифты, CSS), включенные в документы MHTML. Значение по умолчанию — ложь.

Этот параметр влияет только на документы, сохраняемые в формате MHTML.

По умолчанию на ресурсы в документах MHTML ссылаются по имени файла (например, «image.png»), которое сопоставляется с заголовками «Content-Location» частей MIME.

Этот параметр включает альтернативный метод, при котором ссылки на файлы ресурсов записываются как URL-адреса CID (Content-ID) (например, «cid:image.png») и сопоставляются с заголовками «Content-ID».

Теоретически не должно быть никакой разницы между двумя способами ссылки, и любой из них должен нормально работать в любом браузере или почтовом агенте. Однако на практике некоторым агентам не удается получить ресурсы по имени файла. Если ваш браузер или почтовый агент отказывается загружать ресурсы, включенные в документ MTHML (не показывает изображения или не загружает стили CSS), попробуйте экспортировать документ с URL-адресами CID.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setExportDocumentProperties(boolean value) {#setExportDocumentProperties-boolean-}
```
public void setExportDocumentProperties(boolean value)
```


Указывает, следует ли экспортировать встроенные и настраиваемые свойства документа в HTML, MHTML или EPUB. Значение по умолчанию — ложь.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setExportDropDownFormFieldAsText(boolean value) {#setExportDropDownFormFieldAsText-boolean-}
```
public void setExportDropDownFormFieldAsText(boolean value)
```


Определяет, как поля раскрывающихся форм сохраняются в HTML или MHTML. Значение по умолчанию — ложь.

Если установлено значение true , поля раскрывающейся формы экспортируются как обычный текст. При значении false экспортирует раскрывающиеся поля формы как элемент SELECT в HTML.

При экспорте в EPUB текстовые поля выпадающей формы всегда сохраняются как текст из-за требований этого формата.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setExportFontResources(boolean value) {#setExportFontResources-boolean-}
```
public void setExportFontResources(boolean value)
```


Указывает, следует ли экспортировать ресурсы шрифта в HTML, MHTML или EPUB. Значение по умолчанию — ложь.

Экспорт ресурсов шрифтов обеспечивает согласованную визуализацию документов независимо от шрифтов, доступных в среде данного пользователя.

 Если[getExportFontResources()](../../com.aspose.words/htmlsaveoptions\#getExportFontResources--) / [setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportFontResources-boolean-) установлено значение true , основной HTML-документ будет ссылаться на каждый шрифт через CSS 3**@font-face** at-rule и шрифты будут выводиться отдельными файлами. При экспорте в форматы IDPF EPUB или MHTML шрифты будут встроены в соответствующий пакет вместе с другими вспомогательными файлами.

 Если[getExportFontsAsBase64()](../../com.aspose.words/htmlsaveoptions\#getExportFontsAsBase64--) / [setExportFontsAsBase64(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportFontsAsBase64-boolean-) установлено значение true , шрифты не будут сохраняться в отдельные файлы. Вместо этого они будут встроены в**@font-face** at-правила в кодировке Base64.

**Important!**При экспорте ресурсов шрифтов следует учитывать вопросы лицензирования шрифтов. Авторы, которые хотят использовать определенные шрифты с помощью загружаемого механизма шрифтов, должны всегда тщательно проверять, что их предполагаемое использование находится в рамках лицензии на шрифт. Многие коммерческие шрифты в настоящее время не позволяют загружать свои шрифты из Интернета в любой форме. В лицензионных соглашениях, распространяющихся на некоторые шрифты, особо отмечается, что использование через**@font-face** правила в таблицах стилей CSS не разрешены. Подмножество шрифтов также может нарушать условия лицензии.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setExportFontsAsBase64(boolean value) {#setExportFontsAsBase64-boolean-}
```
public void setExportFontsAsBase64(boolean value)
```


Указывает, следует ли встраивать ресурсы шрифтов в HTML в кодировке Base64. Значение по умолчанию — ложь.

По умолчанию шрифты записываются в отдельные файлы. Если для этого параметра установлено значение true , шрифты будут встроены в CSS документа в кодировке Base64.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setExportGeneratorName(boolean value) {#setExportGeneratorName-boolean-}
```
public void setExportGeneratorName(boolean value)
```


 При значении true имя и версия Aspose.Words встраиваются в создаваемые файлы. Значение по умолчанию**true**.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setExportHeadersFootersMode(int value) {#setExportHeadersFootersMode-int-}
```
public void setExportHeadersFootersMode(int value)
```


 Указывает, как верхние и нижние колонтитулы выводятся в HTML, MHTML или EPUB. Значение по умолчанию[ExportHeadersFootersMode.PER\_SECTION](../../com.aspose.words/exportheadersfootersmode\#PER-SECTION) для HTML/MHTML и[ExportHeadersFootersMode.NONE](../../com.aspose.words/exportheadersfootersmode\#NONE) для EPUB.

Трудно осмысленно выводить верхние и нижние колонтитулы в HTML, потому что HTML не разбит на страницы.

 Когда это свойство[ExportHeadersFootersMode.PER\_SECTION](../../com.aspose.words/exportheadersfootersmode\#PER-SECTION)Aspose.Words экспортирует только основные верхние и нижние колонтитулы в начале и в конце каждого раздела.

 Когда он является[ExportHeadersFootersMode.FIRST\_SECTION\_HEADER\_LAST\_SECTION\_FOOTER](../../com.aspose.words/exportheadersfootersmode\#FIRST-SECTION-HEADER-LAST-SECTION-FOOTER) экспортируются только первый основной заголовок и последний основной нижний колонтитул (включая ссылку на предыдущий).

 Вы можете полностью отключить экспорт верхних и нижних колонтитулов, установив для этого свойства значение[ExportHeadersFootersMode.NONE](../../com.aspose.words/exportheadersfootersmode\#NONE).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[ExportHeadersFootersMode](../../com.aspose.words/exportheadersfootersmode) константы. |

### setExportImagesAsBase64(boolean value) {#setExportImagesAsBase64-boolean-}
```
public void setExportImagesAsBase64(boolean value)
```


Указывает, сохраняются ли изображения в формате Base64 в выходной HTML, MHTML или EPUB. Значение по умолчанию — ложь.

 Когда для этого свойства установлено значение true, данные изображений экспортируются непосредственно в**img** элементы и отдельные файлы не создаются.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setExportLanguageInformation(boolean value) {#setExportLanguageInformation-boolean-}
```
public void setExportLanguageInformation(boolean value)
```


Указывает, экспортируется ли языковая информация в HTML, MHTML или EPUB. Значение по умолчанию — ложь.

 Когда для этого свойства установлено значение true, выходные данные Aspose.Words**lang** Атрибут HTML в элементах документа, указывающий язык. Это может быть необходимо для сохранения семантики, связанной с языком.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setExportListLabels(int value) {#setExportListLabels-int-}
```
public void setExportListLabels(int value)
```


 Управляет выводом меток списков в HTML, MHTML или EPUB. Значение по умолчанию[ExportListLabels.AUTO](../../com.aspose.words/exportlistlabels\#AUTO).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[ExportListLabels](../../com.aspose.words/exportlistlabels) константы. |

### setExportOriginalUrlForLinkedImages(boolean value) {#setExportOriginalUrlForLinkedImages-boolean-}
```
public void setExportOriginalUrlForLinkedImages(boolean value)
```


Указывает, следует ли использовать исходный URL-адрес в качестве URL-адреса связанных изображений. Значение по умолчанию — ложь.

 Если установлено значение true[ImageData.getSourceFullName()](../../com.aspose.words/imagedata\#getSourceFullName--) / [ImageData.setSourceFullName(java.lang.String)](../../com.aspose.words/imagedata\#setSourceFullName-java.lang.String-) значение используется в качестве URL-адреса связанных изображений, а связанные изображения не загружаются в папку документа или[getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-).

 Если установлено значение false, связанные изображения загружаются в папку документа или[getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-) и URL каждого связанного изображения строится в зависимости от папки документа,[getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-) а также[getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-) характеристики.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setExportPageMargins(boolean value) {#setExportPageMargins-boolean-}
```
public void setExportPageMargins(boolean value)
```


Указывает, экспортируются ли поля страницы в HTML, MHTML или EPUB. Значение по умолчанию — ложь. По умолчанию Aspose.Words не показывает область полей страницы. Если какие-либо элементы полностью или частично обрезаны краем документа, с помощью этой опции можно расширить отображаемую область.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setExportPageSetup(boolean value) {#setExportPageSetup-boolean-}
```
public void setExportPageSetup(boolean value)
```


Указывает, экспортируются ли настройки страницы в HTML, MHTML или EPUB. Значение по умолчанию — ложь.

 Каждый[Section](../../com.aspose.words/section) в модели документа Aspose.Words предоставляет информацию о настройках страницы через[PageSetup](../../com.aspose.words/pagesetup)учебный класс. При экспорте документа в формат HTML может потребоваться сохранить эту информацию для дальнейшего использования. В частности, настройка страницы может быть важна для рендеринга на постраничный носитель (печать) или последующего преобразования в исходные форматы файлов Microsoft Word (DOCX, DOC, RTF, WML).

В большинстве случаев HTML предназначен для просмотра в браузерах, где не выполняется пагинация. Так что эта функция неактивна по умолчанию.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setExportRelativeFontSize(boolean value) {#setExportRelativeFontSize-boolean-}
```
public void setExportRelativeFontSize(boolean value)
```


Указывает, должны ли размеры шрифта выводиться в относительных единицах при сохранении в HTML, MHTML или EPUB. Значение по умолчанию — ложь.

 Во многих существующих документах (HTML, IDPF EPUB) размеры шрифтов указаны в относительных единицах. Это позволяет приложениям настраивать размер текста при просмотре/обработке документов. Например, в Microsoft Internet Explorer есть подменю «Вид->Размер текста», в Adobe Digital Editions есть две кнопки: Увеличить/Уменьшить размер текста. Если вы ожидаете, что эта функция будет работать, установите[getExportRelativeFontSize()](../../com.aspose.words/htmlsaveoptions\#getExportRelativeFontSize--) / [setExportRelativeFontSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportRelativeFontSize-boolean-) свойство истинное.

Модель документа Aspose Words содержит и работает только с единицами абсолютного размера шрифта. Относительные единицы нуждаются в дополнительной логике для пересчета от некоторого начального (стандартного) размера. Размер шрифта**Normal** стиль документа принимается за стандартный. Например, если**Normal** имеет шрифт 12pt, а некоторый текст имеет размер 18pt, тогда он будет выводиться как**1.5em.** к HTML.

 Когда этот параметр включен, элементы документа, кроме текста, по-прежнему будут иметь абсолютные размеры. Также некоторые атрибуты, связанные с текстом, могут быть выражены абсолютно. В частности, межстрочный интервал, указанный с помощью правила «точно», может привести к нежелательным результатам при масштабировании текста. Таким образом, исходные документы должны быть правильно оформлены и протестированы при экспорте с помощью[getExportRelativeFontSize()](../../com.aspose.words/htmlsaveoptions\#getExportRelativeFontSize--) / [setExportRelativeFontSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportRelativeFontSize-boolean-) установить на истину.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setExportRoundtripInformation(boolean value) {#setExportRoundtripInformation-boolean-}
```
public void setExportRoundtripInformation(boolean value)
```


Указывает, следует ли записывать информацию о цикле приема-передачи при сохранении в HTML, MHTML или EPUB. Значение по умолчанию — true для HTML и false для MHTML и EPUB.

Сохранение информации об обходе позволяет восстанавливать свойства документа, такие как позиции табуляции, комментарии, верхние и нижние колонтитулы, во время загрузки HTML-документов обратно в формат.[Document](../../com.aspose.words/document) объект.

Когда true , информация о пути туда и обратно экспортируется как -aw-\* Свойства CSS соответствующих элементов HTML.

При значении false информация о циклическом обходе не выводится в создаваемые файлы.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setExportShapesAsSvg(boolean value) {#setExportShapesAsSvg-boolean-}
```
public void setExportShapesAsSvg(boolean value)
```


 Контролирует ли[Shape](../../com.aspose.words/shape) узлы преобразуются в изображения SVG при сохранении в HTML, MHTML, EPUB или AZW3. Значение по умолчанию — ложь.

 Если для этой опции установлено значение true ,[Shape](../../com.aspose.words/shape) узлы экспортируются как элементы. В противном случае они преобразуются в растровые изображения и экспортируются как![Изображение 1][] элементы.


[Изображение 1]: 

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setExportTextInputFormFieldAsText(boolean value) {#setExportTextInputFormFieldAsText-boolean-}
```
public void setExportTextInputFormFieldAsText(boolean value)
```


Управляет способом сохранения полей формы ввода текста в формате HTML или MHTML. Значение по умолчанию — ложь.

Если установлено значение true , поля формы ввода текста экспортируются как обычный текст. При значении false экспортирует поля формы ввода текста Word как элементы INPUT в HTML.

При экспорте в EPUB поля формы ввода текста всегда сохраняются как текст из-за требований этого формата.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setExportTocPageNumbers(boolean value) {#setExportTocPageNumbers-boolean-}
```
public void setExportTocPageNumbers(boolean value)
```


Указывает, записывать ли номера страниц в оглавление при сохранении HTML, MHTML и EPUB. Значение по умолчанию — ложь.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setExportXhtmlTransitional(boolean value) {#setExportXhtmlTransitional-boolean-}
```
public void setExportXhtmlTransitional(boolean value)
```


 Указывает, следует ли записывать объявление DOCTYPE при сохранении в HTML или MHTML. При значении true записывает объявление DOCTYPE в документ перед корневым элементом. Значение по умолчанию — ложь. При сохранении в EPUB или HTML5 ([HtmlVersion.HTML\_5](../../com.aspose.words/htmlversion\#HTML-5)) всегда записывается объявление DOCTYPE.

Aspose.Words всегда пишет правильно сформированный HTML, независимо от этой настройки.

При значении true начало выходного HTML-документа будет выглядеть так:

```

 
 
 
 
```

Aspose.Words стремится выводить XHTML в соответствии со спецификацией XHTML 1.0 Transitional, но вывод не всегда будет проверяться на соответствие DTD. Некоторые структуры внутри документа Microsoft Word трудно или невозможно сопоставить с документом, который будет проверяться на соответствие схеме XHTML. Например, XHTML не допускает вложенных списков (UL не может быть вложен в другой элемент UL), но в документах Microsoft Word довольно часто встречаются многоуровневые списки.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setFontResourcesSubsettingSizeThreshold(int value) {#setFontResourcesSubsettingSizeThreshold-int-}
```
public void setFontResourcesSubsettingSizeThreshold(int value)
```


Определяет, какие ресурсы шрифтов нуждаются в подразделении при сохранении в HTML, MHTML или EPUB. По умолчанию 0 .

[getExportFontResources()](../../com.aspose.words/htmlsaveoptions\#getExportFontResources--) / [setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportFontResources-boolean-) позволяет экспортировать шрифты как вспомогательные файлы или как части выходного пакета. Если в документе используется много шрифтов, особенно с большим количеством глифов, размер вывода может значительно увеличиться. Подмножество шрифтов уменьшает размер экспортируемого ресурса шрифта, отфильтровывая глифы, которые не используются текущим документом.

Подмножество шрифтов работает следующим образом:

 *  По умолчанию все экспортируемые шрифты являются подмножествами.
 *   Параметр[getFontResourcesSubsettingSizeThreshold()](../../com.aspose.words/htmlsaveoptions\#getFontResourcesSubsettingSizeThreshold--) / [setFontResourcesSubsettingSizeThreshold(int)](../../com.aspose.words/htmlsaveoptions\#setFontResourcesSubsettingSizeThreshold-int-)положительное значение указывает Aspose.Words на подмножество шрифтов, размер файла которых превышает указанное значение.
 *  Установка свойства подавляет подмножество шрифта.

**Important!**При экспорте ресурсов шрифтов следует учитывать вопросы лицензирования шрифтов. Авторы, которые хотят использовать определенные шрифты с помощью загружаемого механизма шрифтов, должны всегда тщательно проверять, что их предполагаемое использование находится в рамках лицензии на шрифт. Многие коммерческие шрифты в настоящее время не позволяют загружать свои шрифты из Интернета в любой форме. В лицензионных соглашениях, распространяющихся на некоторые шрифты, особо отмечается, что использование через**@font-face** правила в таблицах стилей CSS не разрешены. Подмножество шрифтов также может нарушать условия лицензии.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее целочисленное значение. |

### setFontSavingCallback(IFontSavingCallback value) {#setFontSavingCallback-com.aspose.words.IFontSavingCallback-}
```
public void setFontSavingCallback(IFontSavingCallback value)
```


Позволяет управлять сохранением шрифтов при сохранении документа в формате HTML, MHTML или EPUB.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [IFontSavingCallback](../../com.aspose.words/ifontsavingcallback) |  Соответствующий[IFontSavingCallback](../../com.aspose.words/ifontsavingcallback) ценность. |

### setFontsFolder(String value) {#setFontsFolder-java.lang.String-}
```
public void setFontsFolder(String value)
```


Указывает физическую папку, в которой сохраняются шрифты при экспорте документа в HTML. По умолчанию это пустая строка.

 Когда вы сохраняете[Document](../../com.aspose.words/document) в формате HTML и[getExportFontResources()](../../com.aspose.words/htmlsaveoptions\#getExportFontResources--) / [setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportFontResources-boolean-) установлено значение true , Aspose.Words необходимо сохранить шрифты, используемые в документе, как отдельные файлы.[getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-) позволяет указать, где будут сохранены шрифты и[getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) позволяет указать, как будут создаваться URI шрифта.

 Если вы сохраняете документ в файл и указываете имя файла, Aspose.Words по умолчанию сохраняет шрифты в той же папке, где сохранен файл документа. Использовать[getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-) переопределить это поведение.

 Если вы сохраняете документ в поток, Aspose.Words не имеет папки для сохранения шрифтов, но все равно должен где-то сохранять шрифты. В этом случае необходимо указать доступную папку в[getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-) свойство или предоставлять пользовательские потоки через[getFontSavingCallback()](../../com.aspose.words/htmlsaveoptions\#getFontSavingCallback--) / [setFontSavingCallback(com.aspose.words.IFontSavingCallback)](../../com.aspose.words/htmlsaveoptions\#setFontSavingCallback-com.aspose.words.IFontSavingCallback-) обработчик события.

Если папка, указанная[getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-) не существует, он будет создан автоматически.

[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-) — это еще один способ указать папку, в которой следует сохранять шрифты.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setFontsFolderAlias(String value) {#setFontsFolderAlias-java.lang.String-}
```
public void setFontsFolderAlias(String value)
```


Указывает имя папки, используемой для создания URI шрифтов, записываемых в HTML-документ. По умолчанию это пустая строка.

 Когда вы сохраняете[Document](../../com.aspose.words/document) в формате HTML и[getExportFontResources()](../../com.aspose.words/htmlsaveoptions\#getExportFontResources--) / [setExportFontResources(boolean)](../../com.aspose.words/htmlsaveoptions\#setExportFontResources-boolean-) установлено значение true , Aspose.Words необходимо сохранить шрифты, используемые в документе, как отдельные файлы.[getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-) позволяет указать, где будут сохранены шрифты и[getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) позволяет указать, как будут создаваться URI шрифта.

 Если[getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) не является пустой строкой, тогда URI шрифта, записанный в HTML, будет*FontsFolderAlias +* . 

 Если[getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) является пустой строкой, тогда URI шрифта, записанный в HTML, будет*FontsFolder +* . 

 Если[getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) установлен в '.' (точка), то имя файла шрифта будет записано в HTML без указания пути независимо от других параметров.

 Альтернативный способ указать имя папки для создания URI шрифта — использовать[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setHtmlVersion(int value) {#setHtmlVersion-int-}
```
public void setHtmlVersion(int value)
```


 Указывает версию стандарта HTML, которую следует использовать при сохранении документа в формате HTML или MHTML. Значение по умолчанию[HtmlVersion.XHTML](../../com.aspose.words/htmlversion\#XHTML).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[HtmlVersion](../../com.aspose.words/htmlversion) константы. |

### setImageResolution(int value) {#setImageResolution-int-}
```
public void setImageResolution(int value)
```


Указывает выходное разрешение для изображений при экспорте в HTML, MHTML или EPUB. По умолчанию — 96 dpi.

 Это свойство влияет на растровые изображения, когда[getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions\#getScaleImageToShapeSize--) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setScaleImageToShapeSize-boolean-)имеет значение true и влияет на метафайлы, экспортируемые как растровые изображения. Некоторые свойства изображения, такие как обрезка или поворот, требуют сохранения преобразованных изображений, и в этом случае преобразованные изображения создаются в заданном разрешении.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Соответствующее целочисленное значение. |

### setImageSavingCallback(IImageSavingCallback value) {#setImageSavingCallback-com.aspose.words.IImageSavingCallback-}
```
public void setImageSavingCallback(IImageSavingCallback value)
```


Позволяет управлять способом сохранения изображений при сохранении документа в формате HTML, MHTML или EPUB.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [IImageSavingCallback](../../com.aspose.words/iimagesavingcallback) |  Соответствующий[IImageSavingCallback](../../com.aspose.words/iimagesavingcallback) ценность. |

### setImagesFolder(String value) {#setImagesFolder-java.lang.String-}
```
public void setImagesFolder(String value)
```


Указывает физическую папку, в которой сохраняются изображения при экспорте документа в формат HTML. По умолчанию это пустая строка.

 Когда вы сохраняете[Document](../../com.aspose.words/document) в формате HTML Aspose.Words должен сохранять все изображения, встроенные в документ, как отдельные файлы.[getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-) позволяет указать, где изображения будут сохранены и[getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-) позволяет указать, как будут создаваться URI изображения.

Если вы сохраняете документ в файл и указываете имя файла, Aspose.Words по умолчанию сохраняет изображения в той же папке, где сохранен файл документа. Использовать[getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-) переопределить это поведение.

 Если вы сохраняете документ в потоке, Aspose.Words не имеет папки для сохранения изображений, но все же необходимо где-то сохранять изображения. В этом случае необходимо указать доступную папку в[getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-) свойство или предоставлять пользовательские потоки через[getImageSavingCallback()](../../com.aspose.words/htmlsaveoptions\#getImageSavingCallback--) / [setImageSavingCallback(com.aspose.words.IImageSavingCallback)](../../com.aspose.words/htmlsaveoptions\#setImageSavingCallback-com.aspose.words.IImageSavingCallback-) обработчик события.

Если папка, указанная[getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-) не существует, он будет создан автоматически.

[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-) — это еще один способ указать папку, в которую следует сохранять изображения.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setImagesFolderAlias(String value) {#setImagesFolderAlias-java.lang.String-}
```
public void setImagesFolderAlias(String value)
```


Указывает имя папки, используемой для создания URI изображений, записываемых в HTML-документ. По умолчанию это пустая строка.

 Когда вы сохраняете[Document](../../com.aspose.words/document) в формате HTML Aspose.Words должен сохранять все изображения, встроенные в документ, как отдельные файлы.[getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-) позволяет указать, где изображения будут сохранены и[getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-) позволяет указать, как будут создаваться URI изображения.

 Если[getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-) не является пустой строкой, тогда URI изображения, записанный в HTML, будет*ImagesFolderAlias + ![Image 1][]*.

 Если[getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-) является пустой строкой, тогда URI изображения, записанный в HTML, будет*ImagesFolder + ![Image 1][]*.

 Если[getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-)установлен в '.' (точка), то имя файла изображения будет записано в HTML без указания пути независимо от других параметров.

 Альтернативный способ указать имя папки для создания URI изображений — использовать[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-).


[Изображение 1]: 

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

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

### setMemoryOptimization(boolean value) {#setMemoryOptimization-boolean-}
```
public void setMemoryOptimization(boolean value)
```


 Задает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойства**false**. Установка для этого параметра значения true может значительно снизить потребление памяти при сохранении больших документов за счет замедления времени сохранения.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. |

### setMetafileFormat(int value) {#setMetafileFormat-int-}
```
public void setMetafileFormat(int value)
```


 Указывает, в каком формате сохраняются метафайлы при экспорте в HTML, MHTML или EPUB. Значение по умолчанию[HtmlMetafileFormat.PNG](../../com.aspose.words/htmlmetafileformat\#PNG), что означает, что метафайлы преобразуются в растровые изображения PNG.

Метафайлы изначально не отображаются браузерами HTML. По умолчанию Aspose.Words конвертирует изображения WMF и EMF в файлы PNG при экспорте в HTML. Другие варианты — преобразовать метафайлы в изображения SVG или экспортировать их как есть без преобразования.

Некоторые преобразования изображений, в частности обрезка изображений, не будут применяться к изображениям метафайлов, если они экспортируются в HTML без преобразования.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[HtmlMetafileFormat](../../com.aspose.words/htmlmetafileformat) константы. |

### setOfficeMathOutputMode(int value) {#setOfficeMathOutputMode-int-}
```
public void setOfficeMathOutputMode(int value)
```


Управляет экспортом объектов OfficeMath в HTML, MHTML или EPUB. Значение по умолчанию — HtmlOfficeMathOutputMode.Image .

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[HtmlOfficeMathOutputMode](../../com.aspose.words/htmlofficemathoutputmode) константы. |

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

### setResolveFontNames(boolean value) {#setResolveFontNames-boolean-}
```
public void setResolveFontNames(boolean value)
```


Указывает, разрешаются ли имена семейств шрифтов, используемые в документе, и заменяются ли они в соответствии с[Document.getFontSettings()](../../com.aspose.words/document\#getFontSettings--) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document\#setFontSettings-com.aspose.words.FontSettings-) при записи в форматы на основе HTML.

По умолчанию для этого параметра установлено значение false, и имена семейств шрифтов записываются в HTML, как указано в исходных документах. То есть,[Document.getFontSettings()](../../com.aspose.words/document\#getFontSettings--) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document\#setFontSettings-com.aspose.words.FontSettings-) игнорируются, и разрешение или замена имен семейств шрифтов не выполняются.

 Если для этого параметра установлено значение true , Aspose.Words использует[Document.getFontSettings()](../../com.aspose.words/document\#getFontSettings--) / [Document.setFontSettings(com.aspose.words.FontSettings)](../../com.aspose.words/document\#setFontSettings-com.aspose.words.FontSettings-) преобразовать каждое имя семейства шрифтов, указанное в исходном документе, в имя доступного семейства шрифтов, выполняя замену шрифта по мере необходимости.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setResourceFolder(String value) {#setResourceFolder-java.lang.String-}
```
public void setResourceFolder(String value)
```


Указывает физическую папку, в которой сохраняются все ресурсы, такие как изображения, шрифты и внешний CSS, при экспорте документа в HTML. По умолчанию это пустая строка.

[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-) это самый простой способ указать папку, в которую должны быть записаны все ресурсы. Другой способ — использовать отдельные свойства[getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-), [getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-) , а также[getCssStyleSheetFileName()](../../com.aspose.words/htmlsaveoptions\#getCssStyleSheetFileName--) / [setCssStyleSheetFileName(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setCssStyleSheetFileName-java.lang.String-).

[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-) имеет более низкий приоритет, чем папки, указанные через[getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-), [getImagesFolder()](../../com.aspose.words/htmlsaveoptions\#getImagesFolder--) / [setImagesFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolder-java.lang.String-) , а также[getCssStyleSheetFileName()](../../com.aspose.words/htmlsaveoptions\#getCssStyleSheetFileName--) / [setCssStyleSheetFileName(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setCssStyleSheetFileName-java.lang.String-) . Например, если оба[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-) а также[getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-) указаны, шрифты будут сохранены в[getFontsFolder()](../../com.aspose.words/htmlsaveoptions\#getFontsFolder--) / [setFontsFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolder-java.lang.String-) , а изображения и CSS будут сохранены в[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-).

Если папка, указанная[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-) не существует, он будет создан автоматически.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setResourceFolderAlias(String value) {#setResourceFolderAlias-java.lang.String-}
```
public void setResourceFolderAlias(String value)
```


Задает имя папки, используемой для создания URI всех ресурсов, записываемых в HTML-документ. По умолчанию это пустая строка.

[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-) — это самый простой способ указать, как должны быть созданы URI для всех файлов ресурсов. Та же информация может быть указана для изображений и шрифтов отдельно через[getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-) а также[getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) свойства соответственно. Однако для CSS нет отдельного свойства.

[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-) имеет более низкий приоритет, чем[getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) а также[getImagesFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getImagesFolderAlias--) / [setImagesFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setImagesFolderAlias-java.lang.String-) . Например, если оба[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-) а также[getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) указаны, URI шрифтов будут построены с использованием[getFontsFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getFontsFolderAlias--) / [setFontsFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setFontsFolderAlias-java.lang.String-) , а URI изображений и CSS будут создаваться с использованием[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-).

 Если[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-) пусто, т.[getResourceFolder()](../../com.aspose.words/htmlsaveoptions\#getResourceFolder--) / [setResourceFolder(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolder-java.lang.String-) значение свойства будет использоваться для создания URI ресурсов.

 Если[getResourceFolderAlias()](../../com.aspose.words/htmlsaveoptions\#getResourceFolderAlias--) / [setResourceFolderAlias(java.lang.String)](../../com.aspose.words/htmlsaveoptions\#setResourceFolderAlias-java.lang.String-) установлен в '.' (точка), URI ресурсов будут содержать только имена файлов без указания пути.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | java.lang.String | Соответствующее значение java.lang.String. |

### setSaveFormat(int value) {#setSaveFormat-int-}
```
public void setSaveFormat(int value)
```


 Указывает формат, в котором будет сохранен документ, если используется этот объект параметров сохранения. Может быть[SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML), [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML), [SaveFormat.EPUB](../../com.aspose.words/saveformat\#EPUB) или же[SaveFormat.AZW\_3](../../com.aspose.words/saveformat\#AZW-3).

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[SaveFormat](../../com.aspose.words/saveformat) константы. |

### setScaleImageToShapeSize(boolean value) {#setScaleImageToShapeSize-boolean-}
```
public void setScaleImageToShapeSize(boolean value)
```


Указывает, масштабируются ли изображения с помощью Aspose.Words до размера ограничивающей фигуры при экспорте в HTML, MHTML или EPUB. Значение по умолчанию — true.

Изображение в документе Microsoft Word представляет собой фигуру. Форма имеет размер, а изображение имеет собственный размер. Размеры напрямую не связаны. Например, изображение может иметь размер 1024x786 пикселей, а форма, отображающая это изображение, может иметь размер 400x300 точек.

 Чтобы изображение отображалось в браузере, оно должно быть масштабировано до размера фигуры.[getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions\#getScaleImageToShapeSize--) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setScaleImageToShapeSize-boolean-) Свойство управляет тем, где происходит масштабирование изображения: в Aspose.Words при экспорте в HTML или в браузере при отображении документа.

 Когда[getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions\#getScaleImageToShapeSize--) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setScaleImageToShapeSize-boolean-) true , Aspose.Words масштабирует изображение с использованием высококачественного масштабирования при экспорте в HTML. Когда[getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions\#getScaleImageToShapeSize--) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setScaleImageToShapeSize-boolean-) false , изображение выводится с исходным размером, и браузер должен масштабировать его.

 Как правило, браузеры делают быстрое и некачественное масштабирование. В результате вы обычно получаете лучшее качество отображения в браузере и меньший размер файла при[getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions\#getScaleImageToShapeSize--) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setScaleImageToShapeSize-boolean-) верно, но лучшее качество печати и более быстрое преобразование при[getScaleImageToShapeSize()](../../com.aspose.words/htmlsaveoptions\#getScaleImageToShapeSize--) / [setScaleImageToShapeSize(boolean)](../../com.aspose.words/htmlsaveoptions\#setScaleImageToShapeSize-boolean-) является ложным.

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | boolean | Соответствующее логическое значение. |

### setTableWidthOutputMode(int value) {#setTableWidthOutputMode-int-}
```
public void setTableWidthOutputMode(int value)
```


Определяет, как ширина таблицы, строки и ячейки экспортируется в HTML, MHTML или EPUB. Значение по умолчанию[HtmlElementSizeOutputMode.ALL](../../com.aspose.words/htmlelementsizeoutputmode\#ALL).

В формате HTML элементы таблицы, строки и ячейки ( 

    | -- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
    | ,  | ) can have their widths specified either in relative (percentage) or in absolute units. In a document in Aspose.Words, tables, rows and cells can have their widths specified using either relative or absolute units too.
 
 Когда вы конвертируете документ в HTML с помощью Aspose.Words, вы можете захотеть контролировать, как экспортируется ширина таблицы, строки и ячейки, чтобы влиять на то, как результирующий документ отображается в визуальном агенте (например, в браузере или средстве просмотра).
 
  Используйте это свойство в качестве фильтра, чтобы указать, какие значения ширины таблицы экспортируются в целевой документ. Например, если вы конвертируете документ в формат EPUB и собираетесь просматривать его на мобильном устройстве для чтения, вам, вероятно, следует избегать экспорта абсолютных значений ширины. Для этого нужно указать режим вывода[HtmlElementSizeOutputMode.RELATIVE\_ONLY](../../com.aspose.words/htmlelementsizeoutputmode\#RELATIVE-ONLY) или же[HtmlElementSizeOutputMode.NONE](../../com.aspose.words/htmlelementsizeoutputmode\#NONE) Таким образом, зритель на мобильном устройстве может расположить таблицу так, чтобы она соответствовала ширине экрана, насколько это возможно.|

**Параметры:**

| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int |  Соответствующее целочисленное значение. Значение должно быть одним из[HtmlElementSizeOutputMode](../../com.aspose.words/htmlelementsizeoutputmode) константы. |

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
