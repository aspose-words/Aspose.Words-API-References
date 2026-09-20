---
title: "Aspose::Words::Saving::HtmlSaveOptions class"
linktitle: "HtmlSaveOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::HtmlSaveOptions class. Может использоваться для указания дополнительных параметров при сохранении документа в форматы Html, Mhtml, Epub, Azw3 или Mobi. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words.saving/htmlsaveoptions/
---
## HtmlSaveOptions class


Можно использовать для указания дополнительных параметров при сохранении документа в форматы [Html](../../aspose.words/saveformat/), [Mhtml](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/), [Azw3](../../aspose.words/saveformat/) или [Mobi](../../aspose.words/saveformat/). Чтобы узнать больше, посетите статью документации [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class HtmlSaveOptions : public Aspose::Words::Saving::SaveOptions
```

## Методы

| Метод | Описание |
| --- | --- |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Создаёт объект параметров сохранения класса, подходящего для указанного формата сохранения. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Создаёт объект параметров сохранения класса, подходящего для расширения файла, указанного в данном имени файла. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Получает или задаёт логическое значение, указывающее, разрешено ли встраивание шрифтов с контурами PostScript при встраивании TrueType‑шрифтов в документ при его сохранении. Значение по умолчанию — **false**. |
| [get_AllowNegativeIndent](./get_allownegativeindent/)() const | Указывает, нормализуются ли отрицательные левый и правый отступы абзацев при сохранении в форматы HTML, MHTML или EPUB. Значение по умолчанию — **false**. |
| [get_CssClassNamePrefix](./get_cssclassnameprefix/)() const | Указывает префикс, который добавляется ко всем именам CSS‑классов. Значение по умолчанию — пустая строка, и сгенерированные имена CSS‑классов не имеют общего префикса. |
| [get_CssSavingCallback](./get_csssavingcallback/)() const | Позволяет управлять тем, как сохраняются стили CSS при сохранении документа в HTML, MHTML или EPUB. |
| [get_CssStyleSheetFileName](./get_cssstylesheetfilename/)() const | Указывает путь и имя каскадного [Style](../../aspose.words/style/) листа (CSS), записываемого при экспорте документа в HTML. По умолчанию — пустая строка. |
| [get_CssStyleSheetType](./get_cssstylesheettype/)() const | Указывает, как стили CSS (каскадный [Style](../../aspose.words/style/) лист) экспортируются в HTML, MHTML или EPUB. Значение по умолчанию — [Inline](../cssstylesheettype/) для HTML/MHTML и [External](../cssstylesheettype/) для EPUB. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Получает или задает пользовательский локальный часовой пояс, используемый для полей даты/времени. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Получает или задает путь к шаблону по умолчанию (включая имя файла). Значение по умолчанию для этого свойства — **empty string**. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | Получает значение, определяющее, как рендерятся 3D‑эффекты. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | Получает или задает значение, определяющее, как рендерятся эффекты DrawingML. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | Получает или задает значение, определяющее, как рендерятся фигуры DrawingML. |
| [get_DocumentPartSavingCallback](./get_documentpartsavingcallback/)() const | Позволяет управлять тем, как части документа сохраняются при сохранении документа в HTML или EPUB. |
| [get_DocumentSplitCriteria](./get_documentsplitcriteria/)() const | Указывает, как документ должен быть разбит при сохранении в формат [Html](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/) или [Azw3](../../aspose.words/saveformat/). По умолчанию — [None](../documentsplitcriteria/) для HTML и [HeadingParagraph](../documentsplitcriteria/) для EPUB и AZW3. |
| [get_DocumentSplitHeadingLevel](./get_documentsplitheadinglevel/)() const | Указывает максимальный уровень заголовков, при котором документ разбивается. Значение по умолчанию — **%2**. |
| [get_Encoding](./get_encoding/)() const | Указывает кодировку, используемую при экспорте в HTML, MHTML или EPUB. Значение по умолчанию — **new UTF8Encoding(false)** (UTF‑8 без BOM). |
| [get_ExportCidUrlsForMhtmlResources](./get_exportcidurlsformhtmlresources/)() const | Указывает, следует ли использовать CID (Content-ID) URL для ссылки на ресурсы (изображения, шрифты, CSS), включённые в документы MHTML. Значение по умолчанию — **false**. |
| [get_ExportDocumentProperties](./get_exportdocumentproperties/)() const | Указывает, следует ли экспортировать встроенные и пользовательские свойства документа в HTML, MHTML или EPUB. Значение по умолчанию — **false**. |
| [get_ExportDropDownFormFieldAsText](./get_exportdropdownformfieldastext/)() const | Управляет тем, как выпадающие поля формы сохраняются в HTML или MHTML. Значение по умолчанию — **false**. |
| [get_ExportFontResources](./get_exportfontresources/)() const | Указывает, следует ли экспортировать ресурсы шрифтов в HTML, MHTML или EPUB. По умолчанию — **false**. |
| [get_ExportFontsAsBase64](./get_exportfontsasbase64/)() const | Указывает, следует ли внедрять ресурсы шрифтов в HTML в кодировке Base64. По умолчанию — **false**. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | Когда **true**, имя и версия Aspose.Words встраиваются в создаваемые файлы. Значение по умолчанию — **true**. |
| [get_ExportHeadersFootersMode](./get_exportheadersfootersmode/)() const | Указывает, как заголовки и колонтитулы выводятся в HTML, MHTML или EPUB. Значение по умолчанию — [PerSection](../exportheadersfootersmode/) для HTML/MHTML и [None](../exportheadersfootersmode/) для EPUB. |
| [get_ExportImagesAsBase64](./get_exportimagesasbase64/)() const | Указывает, сохраняются ли изображения в формате Base64 в результирующий HTML, MHTML или EPUB. По умолчанию — **false**. |
| [get_ExportLanguageInformation](./get_exportlanguageinformation/)() const | Указывает, экспортируется ли информация о языке в HTML, MHTML или EPUB. По умолчанию — **false**. |
| [get_ExportListLabels](./get_exportlistlabels/)() const | Управляет тем, как метки списков выводятся в HTML, MHTML или EPUB. Значение по умолчанию — [Auto](../exportlistlabels/). |
| [get_ExportOriginalUrlForLinkedImages](./get_exportoriginalurlforlinkedimages/)() const | Указывает, следует ли использовать оригинальный URL в качестве URL связанных изображений. Значение по умолчанию — **false**. |
| [get_ExportPageMargins](./get_exportpagemargins/)() const | Указывает, экспортируются ли поля страницы в HTML, MHTML или EPUB. По умолчанию — **false**. |
| [get_ExportPageSetup](./get_exportpagesetup/)() const | Указывает, экспортируется ли настройка страницы в HTML, MHTML или EPUB. По умолчанию **false**. |
| [get_ExportRelativeFontSize](./get_exportrelativefontsize/)() const | Указывает, должны ли размеры шрифтов выводиться в относительных единицах при сохранении в HTML, MHTML или EPUB. По умолчанию **false**. |
| [get_ExportRoundtripInformation](./get_exportroundtripinformation/)() const | Указывает, следует ли записывать информацию о круговом проходе при сохранении в HTML, MHTML или EPUB. Значение по умолчанию **true** для HTML и **false** для MHTML и EPUB. |
| [get_ExportShapesAsSvg](./get_exportshapesassvg/)() const | Управляет тем, преобразуются ли узлы [Shape](../../aspose.words.drawing/shape/) в SVG‑изображения при сохранении в HTML, MHTML, EPUB или AZW3. Значение по умолчанию **false**. |
| [get_ExportTextInputFormFieldAsText](./get_exporttextinputformfieldastext/)() const | Управляет тем, как текстовые поля формы сохраняются в HTML или MHTML. Значение по умолчанию **false**. |
| [get_ExportTocPageNumbers](./get_exporttocpagenumbers/)() const | Указывает, следует ли записывать номера страниц в оглавление при сохранении в HTML, MHTML и EPUB. Значение по умолчанию **false**. |
| [get_ExportXhtmlTransitional](./get_exportxhtmltransitional/)() const | Указывает, следует ли записывать объявление DOCTYPE при сохранении в HTML или MHTML. Когда **true**, в документ до корневого элемента записывается объявление DOCTYPE. Значение по умолчанию **false**. При сохранении в EPUB или HTML5 ([Html5](../htmlversion/)) объявление DOCTYPE всегда записывается. |
| [get_FontResourcesSubsettingSizeThreshold](./get_fontresourcessubsettingsizethreshold/)() const | Управляет тем, какие ресурсы шрифтов требуют субсеттинга при сохранении в HTML, MHTML или EPUB. По умолчанию **%0**. |
| [get_FontSavingCallback](./get_fontsavingcallback/)() const | Позволяет управлять тем, как шрифты сохраняются при сохранении документа в HTML, MHTML или EPUB. |
| [get_FontsFolder](./get_fontsfolder/)() const | Указывает физическую папку, в которой шрифты сохраняются при экспорте документа в HTML. По умолчанию пустая строка. |
| [get_FontsFolderAlias](./get_fontsfolderalias/)() const | Указывает имя папки, используемой для построения URI шрифтов, записываемых в HTML‑документ. По умолчанию пустая строка. |
| [get_HtmlVersion](./get_htmlversion/)() const | Указывает версию стандарта HTML, которая должна использоваться при сохранении документа в HTML или MHTML. Значение по умолчанию — [Xhtml](../htmlversion/). |
| [get_ImageResolution](./get_imageresolution/)() const | Указывает разрешение вывода изображений при экспорте в HTML, MHTML или EPUB. По умолчанию **%96 dpi**. |
| [get_ImageSavingCallback](./get_imagesavingcallback/)() const | Позволяет управлять тем, как изображения сохраняются при сохранении документа в HTML, MHTML или EPUB. |
| [get_ImagesFolder](./get_imagesfolder/)() const | Указывает физическую папку, в которой изображения сохраняются при экспорте документа в формат HTML. По умолчанию пустая строка. |
| [get_ImagesFolderAlias](./get_imagesfolderalias/)() const | Указывает имя папки, используемой для построения URI изображений, записываемых в HTML‑документ. По умолчанию пустая строка. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Получает или задает значение, определяющее, как отображаются объекты чернил (InkML). |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Получает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойства **false**. |
| [get_MetafileFormat](./get_metafileformat/)() const | Указывает, в каком формате сохраняются метафайлы при экспорте в HTML, MHTML или EPUB. Значение по умолчанию — [Png](../htmlmetafileformat/), что означает, что метафайлы рендерятся в растровые PNG‑изображения. |
| [get_NavigationMapLevel](./get_navigationmaplevel/)() const | Указывает максимальный уровень заголовков, включаемых в навигационную карту при экспорте в форматы EPUB, MOBI или AZW3. Значение по умолчанию **%3**. |
| [get_OfficeMathOutputMode](./get_officemathoutputmode/)() const | Управляет тем, как объекты OfficeMath экспортируются в HTML, MHTML или EPUB. Значение по умолчанию — [Image](../htmlofficemathoutputmode/). |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | Когда **true**, вывод форматируется красиво, где это применимо. Значение по умолчанию **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Вызывается во время сохранения документа и принимает данные о прогрессе сохранения. |
| [get_RemoveJavaScriptFromLinks](./get_removejavascriptfromlinks/)() const | Указывает, будет ли JavaScript удалён из ссылок. По умолчанию **false**. |
| [get_ReplaceBackslashWithYenSign](./get_replacebackslashwithyensign/)() const | Указывает, должны ли символы обратного слеша заменяться на знаки иены. Значение по умолчанию **false**. |
| [get_ResolveFontNames](./get_resolvefontnames/)() const | Указывает, следует ли разрешать и заменять имена семейств шрифтов, используемых в документе, согласно [FontSettings](../../aspose.words/document/get_fontsettings/) при записи в форматы на основе HTML. |
| [get_ResourceFolder](./get_resourcefolder/)() const | Указывает физическую папку, в которой сохраняются все ресурсы, такие как изображения, шрифты и внешние CSS, при экспорте документа в HTML. По умолчанию это пустая строка. |
| [get_ResourceFolderAlias](./get_resourcefolderalias/)() const | Указывает имя папки, используемой для построения URI всех ресурсов, записываемых в HTML‑документ. По умолчанию это пустая строка. |
| [get_SaveFormat](./get_saveformat/)() override | Указывает формат, в котором будет сохранён документ, если используется этот объект параметров сохранения. Может быть [Html](../../aspose.words/saveformat/), [Mhtml](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/), [Azw3](../../aspose.words/saveformat/) или [Mobi](../../aspose.words/saveformat/). |
| [get_ScaleImageToShapeSize](./get_scaleimagetoshapesize/)() const | Указывает, масштабируются ли изображения Aspose.Words до размеров ограничивающей формы при экспорте в HTML, MHTML или EPUB. Значение по умолчанию — **true**. |
| [get_TableWidthOutputMode](./get_tablewidthoutputmode/)() const | Управляет тем, как экспортируются ширины таблиц, строк и ячеек в HTML, MHTML или EPUB. Значение по умолчанию — [All](../htmlelementsizeoutputmode/). |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | Указывает папку для временных файлов, используемых при сохранении в файл DOC или DOCX. По умолчанию это свойство равно **null**, и временные файлы не используются. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | Определяет, будут ли атрибуты шрифта изменяться в соответствии с используемым кодом символа. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | Получает или задаёт значение, определяющее, будет ли свойство [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) обновлено перед сохранением. Значение по умолчанию — **false**;. |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | Получает значение, определяющее, следует ли обновлять поля определённых типов перед сохранением документа в фиксированный формат страниц. Значение по умолчанию для этого свойства — **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | Получает или задаёт значение, определяющее, будет ли свойство [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) обновлено перед сохранением. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | Получает или задаёт значение, определяющее, будет ли свойство [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) обновлено перед сохранением. |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | Получает значение, определяющее, будет ли обновлено изображение представления OLE‑элементов. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | Получает или задаёт значение, определяющее, использовать ли сглаживание при рендеринге. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | Получает или задаёт значение, определяющее, использовать ли высококачественные (т.е. медленные) алгоритмы рендеринга. |
| [GetType](./gettype/)() const override |  |
| [HtmlSaveOptions](./htmlsaveoptions/)() | Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа в формате [Html](../../aspose.words/saveformat/). |
| [HtmlSaveOptions](./htmlsaveoptions/)(Aspose::Words::SaveFormat) | Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа в формате [Html](../../aspose.words/saveformat/), [Mhtml](../../aspose.words/saveformat/), [Epub](../../aspose.words/saveformat/), [Azw3](../../aspose.words/saveformat/) или [Mobi](../../aspose.words/saveformat/). |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_AllowNegativeIndent](./set_allownegativeindent/)(bool) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_AllowNegativeIndent](./get_allownegativeindent/). |
| [set_CssClassNamePrefix](./set_cssclassnameprefix/)(const System::String\&) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_CssClassNamePrefix](./get_cssclassnameprefix/). |
| [set_CssSavingCallback](./set_csssavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::ICssSavingCallback\>\&) | Позволяет управлять тем, как сохраняются стили CSS при сохранении документа в HTML, MHTML или EPUB. |
| [set_CssStyleSheetFileName](./set_cssstylesheetfilename/)(const System::String\&) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName](./get_cssstylesheetfilename/). |
| [set_CssStyleSheetType](./set_cssstylesheettype/)(Aspose::Words::Saving::CssStyleSheetType) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetType](./get_cssstylesheettype/). |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Устанавливает значение, определяющее, как рендерятся 3D‑эффекты. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_DocumentPartSavingCallback](./set_documentpartsavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentPartSavingCallback\>\&) | Позволяет управлять тем, как части документа сохраняются при сохранении документа в HTML или EPUB. |
| [set_DocumentSplitCriteria](./set_documentsplitcriteria/)(Aspose::Words::Saving::DocumentSplitCriteria) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitCriteria](./get_documentsplitcriteria/). |
| [set_DocumentSplitHeadingLevel](./set_documentsplitheadinglevel/)(int32_t) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_DocumentSplitHeadingLevel](./get_documentsplitheadinglevel/). |
| [set_Encoding](./set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_Encoding](./get_encoding/). |
| [set_ExportCidUrlsForMhtmlResources](./set_exportcidurlsformhtmlresources/)(bool) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_ExportCidUrlsForMhtmlResources](./get_exportcidurlsformhtmlresources/). |
| [set_ExportDocumentProperties](./set_exportdocumentproperties/)(bool) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_ExportDocumentProperties](./get_exportdocumentproperties/). |
| [set_ExportDropDownFormFieldAsText](./set_exportdropdownformfieldastext/)(bool) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_ExportDropDownFormFieldAsText](./get_exportdropdownformfieldastext/). |
| [set_ExportFontResources](./set_exportfontresources/)(bool) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources](./get_exportfontresources/). |
| [set_ExportFontsAsBase64](./set_exportfontsasbase64/)(bool) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontsAsBase64](./get_exportfontsasbase64/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_ExportHeadersFootersMode](./set_exportheadersfootersmode/)(Aspose::Words::Saving::ExportHeadersFootersMode) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode](./get_exportheadersfootersmode/). |
| [set_ExportImagesAsBase64](./set_exportimagesasbase64/)(bool) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_ExportImagesAsBase64](./get_exportimagesasbase64/). |
| [set_ExportLanguageInformation](./set_exportlanguageinformation/)(bool) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_ExportLanguageInformation](./get_exportlanguageinformation/). |
| [set_ExportListLabels](./set_exportlistlabels/)(Aspose::Words::Saving::ExportListLabels) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_ExportListLabels](./get_exportlistlabels/). |
| [set_ExportOriginalUrlForLinkedImages](./set_exportoriginalurlforlinkedimages/)(bool) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages](./get_exportoriginalurlforlinkedimages/). |
| [set_ExportPageMargins](./set_exportpagemargins/)(bool) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageMargins](./get_exportpagemargins/). |
| [set_ExportPageSetup](./set_exportpagesetup/)(bool) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_ExportPageSetup](./get_exportpagesetup/). |
| [set_ExportRelativeFontSize](./set_exportrelativefontsize/)(bool) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_ExportRelativeFontSize](./get_exportrelativefontsize/). |
| [set_ExportRoundtripInformation](./set_exportroundtripinformation/)(bool) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_ExportRoundtripInformation](./get_exportroundtripinformation/). |
| [set_ExportShapesAsSvg](./set_exportshapesassvg/)(bool) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_ExportShapesAsSvg](./get_exportshapesassvg/). |
| [set_ExportTextInputFormFieldAsText](./set_exporttextinputformfieldastext/)(bool) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_ExportTextInputFormFieldAsText](./get_exporttextinputformfieldastext/). |
| [set_ExportTocPageNumbers](./set_exporttocpagenumbers/)(bool) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_ExportTocPageNumbers](./get_exporttocpagenumbers/). |
| [set_ExportXhtmlTransitional](./set_exportxhtmltransitional/)(bool) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_ExportXhtmlTransitional](./get_exportxhtmltransitional/). |
| [set_FontResourcesSubsettingSizeThreshold](./set_fontresourcessubsettingsizethreshold/)(int32_t) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_FontResourcesSubsettingSizeThreshold](./get_fontresourcessubsettingsizethreshold/). |
| [set_FontSavingCallback](./set_fontsavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IFontSavingCallback\>\&) | Позволяет управлять тем, как шрифты сохраняются при сохранении документа в HTML, MHTML или EPUB. |
| [set_FontsFolder](./set_fontsfolder/)(const System::String\&) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder](./get_fontsfolder/). |
| [set_FontsFolderAlias](./set_fontsfolderalias/)(const System::String\&) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolderAlias](./get_fontsfolderalias/). |
| [set_HtmlVersion](./set_htmlversion/)(Aspose::Words::Saving::HtmlVersion) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_HtmlVersion](./get_htmlversion/). |
| [set_ImageResolution](./set_imageresolution/)(int32_t) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_ImageResolution](./get_imageresolution/). |
| [set_ImageSavingCallback](./set_imagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IImageSavingCallback\>\&) | Позволяет управлять тем, как изображения сохраняются при сохранении документа в HTML, MHTML или EPUB. |
| [set_ImagesFolder](./set_imagesfolder/)(const System::String\&) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolder](./get_imagesfolder/). |
| [set_ImagesFolderAlias](./set_imagesfolderalias/)(const System::String\&) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolderAlias](./get_imagesfolderalias/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Устанавливает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойства — **false**. |
| [set_MetafileFormat](./set_metafileformat/)(Aspose::Words::Saving::HtmlMetafileFormat) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_MetafileFormat](./get_metafileformat/). |
| [set_NavigationMapLevel](./set_navigationmaplevel/)(int32_t) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_NavigationMapLevel](./get_navigationmaplevel/). |
| [set_OfficeMathOutputMode](./set_officemathoutputmode/)(Aspose::Words::Saving::HtmlOfficeMathOutputMode) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_OfficeMathOutputMode](./get_officemathoutputmode/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_RemoveJavaScriptFromLinks](./set_removejavascriptfromlinks/)(bool) | Указывает, будет ли JavaScript удалён из ссылок. По умолчанию **false**. |
| [set_ReplaceBackslashWithYenSign](./set_replacebackslashwithyensign/)(bool) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_ReplaceBackslashWithYenSign](./get_replacebackslashwithyensign/). |
| [set_ResolveFontNames](./set_resolvefontnames/)(bool) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames](./get_resolvefontnames/). |
| [set_ResourceFolder](./set_resourcefolder/)(const System::String\&) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolder](./get_resourcefolder/). |
| [set_ResourceFolderAlias](./set_resourcefolderalias/)(const System::String\&) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_ResourceFolderAlias](./get_resourcefolderalias/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_SaveFormat](./get_saveformat/). |
| [set_ScaleImageToShapeSize](./set_scaleimagetoshapesize/)(bool) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize](./get_scaleimagetoshapesize/). |
| [set_TableWidthOutputMode](./set_tablewidthoutputmode/)(Aspose::Words::Saving::HtmlElementSizeOutputMode) | Сеттер для [Aspose::Words::Saving::HtmlSaveOptions::get_TableWidthOutputMode](./get_tablewidthoutputmode/). |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Устанавливает значение, определяющее, следует ли обновлять поля определённых типов перед сохранением документа в фиксированный формат страниц. Значение по умолчанию для этого свойства — **true**. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | Устанавливает значение, определяющее, будет ли обновлено изображение представления OLE‑элементов управления. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| static [Type](./type/)() |  |

## Примеры



Показывает, как использовать определённую кодировку при сохранении документа в .epub.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Используйте объект SaveOptions, чтобы указать кодировку для документа, который мы будем сохранять.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Epub);
saveOptions->set_Encoding(System::Text::Encoding::get_UTF8());

// По умолчанию выходной документ .epub будет содержать всё своё содержимое в одной HTML‑части.
// Критерий разбиения позволяет разделить документ на несколько HTML‑частей.
// Мы установим критерий разбиения документа на абзацы заголовков.
// Это полезно для читателей, которые не могут открывать HTML‑файлы, превышающие определённый размер.
saveOptions->set_DocumentSplitCriteria(Aspose::Words::Saving::DocumentSplitCriteria::HeadingParagraph);

// Укажите, что мы хотим экспортировать свойства документа.
saveOptions->set_ExportDocumentProperties(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```


Показывает, как указать папку для хранения связанных изображений после сохранения в .html.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

System::String imagesDir = System::IO::Path::Combine(get_ArtifactsDir(), u"SaveHtmlWithOptions");

if (System::IO::Directory::Exists(imagesDir))
{
    System::IO::Directory::Delete(imagesDir, true);
}

System::IO::Directory::CreateDirectory_(imagesDir);

// Установите параметр для экспорта полей формы как обычный текст вместо HTML‑элементов ввода.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
options->set_ExportTextInputFormFieldAsText(true);
options->set_ImagesFolder(imagesDir);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

## См. также

* Class [SaveOptions](../saveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
