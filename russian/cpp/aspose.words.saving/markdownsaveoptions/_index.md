---
title: "класс Aspose::Words::Saving::MarkdownSaveOptions"
linktitle: "MarkdownSaveOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "класс Aspose::Words::Saving::MarkdownSaveOptions. Класс для указания дополнительных параметров при сохранении документа в формате Markdown. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 13000
url: /ru/cpp/aspose.words.saving/markdownsaveoptions/
---
## MarkdownSaveOptions class


Класс для указания дополнительных параметров при сохранении документа в формате [Markdown](../../aspose.words/saveformat/). Чтобы узнать больше, посетите статью документации [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class MarkdownSaveOptions : public Aspose::Words::Saving::TxtSaveOptionsBase
```

## Методы

| Метод | Описание |
| --- | --- |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Создаёт объект параметров сохранения класса, подходящего для указанного формата сохранения. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Создаёт объект параметров сохранения класса, подходящего для расширения файла, указанного в данном имени файла. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Получает или задаёт логическое значение, указывающее, разрешено ли встраивание шрифтов с контурами PostScript при встраивании TrueType‑шрифтов в документ при его сохранении. Значение по умолчанию — **false**. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Получает или задает пользовательский локальный часовой пояс, используемый для полей даты/времени. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Получает или задает путь к шаблону по умолчанию (включая имя файла). Значение по умолчанию для этого свойства — **empty string**. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | Получает значение, определяющее, как рендерятся 3D‑эффекты. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | Получает или задает значение, определяющее, как рендерятся эффекты DrawingML. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | Получает или задает значение, определяющее, как рендерятся фигуры DrawingML. |
| [get_EmptyParagraphExportMode](./get_emptyparagraphexportmode/)() const | Указывает, как экспортировать пустые абзацы в Markdown. Значение по умолчанию — [EmptyLine](../markdownemptyparagraphexportmode/). |
| [get_Encoding](../txtsaveoptionsbase/get_encoding/)() const | Указывает кодировку, используемую при экспорте в текстовые форматы. Значение по умолчанию — **Encoding.UTF8**. |
| [get_ExportAsHtml](./get_exportashtml/)() const | Позволяет указать элементы, которые будут экспортированы в Markdown как необработанный HTML. Значение по умолчанию — [None](../markdownexportashtml/). |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | Когда **true**, имя и версия Aspose.Words встраиваются в создаваемые файлы. Значение по умолчанию — **true**. |
| [get_ExportHeadersFootersMode](../txtsaveoptionsbase/get_exportheadersfootersmode/)() const | Указывает способ экспорта колонтитулов в текстовые форматы. Значение по умолчанию — [PrimaryOnly](../txtexportheadersfootersmode/). |
| [get_ExportImagesAsBase64](./get_exportimagesasbase64/)() const | Указывает, сохраняются ли изображения в формате Base64 в выходном файле. Значение по умолчанию — **false**. |
| [get_ExportUnderlineFormatting](./get_exportunderlineformatting/)() const | Получает или задает логическое значение, указывающее, экспортировать ли подчеркивание текста как последовательность из двух знаков плюс \"++\". Значение по умолчанию — **false**. |
| [get_ForcePageBreaks](../txtsaveoptionsbase/get_forcepagebreaks/)() const | Позволяет указать, следует ли сохранять разрывы страниц при экспорте. Значение по умолчанию — **false**. |
| [get_ImageResolution](./get_imageresolution/)() const | Указывает разрешение вывода изображений при экспорте в Markdown. По умолчанию — **%96 dpi**. |
| [get_ImageSavingCallback](./get_imagesavingcallback/)() const | Позволяет контролировать, как сохраняются изображения, когда документ сохраняется в формат [Markdown](../../aspose.words/saveformat/). |
| [get_ImagesFolder](./get_imagesfolder/)() const | Указывает физическую папку, в которой сохраняются изображения при экспорте документа в формат [Markdown](../../aspose.words/saveformat/). По умолчанию — пустая строка. |
| [get_ImagesFolderAlias](./get_imagesfolderalias/)() const | Указывает имя папки, используемой для построения URI изображений, записываемых в документ. По умолчанию — пустая строка. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Получает или задает значение, определяющее, как отображаются объекты чернил (InkML). |
| [get_LinkExportMode](./get_linkexportmode/)() const | Указывает, как ссылки будут записываться в выходной файл. Значение по умолчанию — [Auto](../markdownlinkexportmode/). |
| [get_ListExportMode](./get_listexportmode/)() const | Указывает, как элементы списка будут записываться в выходной файл. Значение по умолчанию — [MarkdownSyntax](../markdownlistexportmode/). |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Получает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойства **false**. |
| [get_OfficeMathExportMode](./get_officemathexportmode/)() const | Указывает, как OfficeMath будет записываться в выходной файл. Значение по умолчанию — [Text](../markdownofficemathexportmode/). |
| [get_ParagraphBreak](../txtsaveoptionsbase/get_paragraphbreak/)() const | Указывает строку, используемую в качестве разрыва абзаца при экспорте в текстовые форматы. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | Когда **true**, вывод форматируется красиво, где это применимо. Значение по умолчанию **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Вызывается во время сохранения документа и принимает данные о прогрессе сохранения. |
| [get_ResourceSavingCallback](./get_resourcesavingcallback/)() const | Позволяет контролировать, как ресурсы сохраняются при экспорте документа в формат [Markdown](../../aspose.words/saveformat/). |
| [get_SaveFormat](./get_saveformat/)() override | Указывает формат, в котором будет сохранён документ, если используется этот объект параметров сохранения. Может быть только [Markdown](../../aspose.words/saveformat/). |
| [get_TableContentAlignment](./get_tablecontentalignment/)() const | Получает или задает значение, указывающее, как выравнивать содержимое таблиц при экспорте в формат [Markdown](../../aspose.words/saveformat/). Значение по умолчанию — [Auto](../tablecontentalignment/). |
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
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MarkdownSaveOptions](./markdownsaveoptions/)() | Инициализирует новый экземпляр этого класса, который может использоваться для сохранения документа в формате [Markdown](../../aspose.words/saveformat/). |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Устанавливает значение, определяющее, как рендерятся 3D‑эффекты. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_EmptyParagraphExportMode](./set_emptyparagraphexportmode/)(Aspose::Words::Saving::MarkdownEmptyParagraphExportMode) | Сеттер для [Aspose::Words::Saving::MarkdownSaveOptions::get_EmptyParagraphExportMode](./get_emptyparagraphexportmode/). |
| [set_Encoding](../txtsaveoptionsbase/set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Сеттер для [Aspose::Words::Saving::TxtSaveOptionsBase::get_Encoding](../txtsaveoptionsbase/get_encoding/). |
| [set_ExportAsHtml](./set_exportashtml/)(Aspose::Words::Saving::MarkdownExportAsHtml) | Сеттер для [Aspose::Words::Saving::MarkdownSaveOptions::get_ExportAsHtml](./get_exportashtml/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_ExportHeadersFootersMode](../txtsaveoptionsbase/set_exportheadersfootersmode/)(Aspose::Words::Saving::TxtExportHeadersFootersMode) | Сеттер для [Aspose::Words::Saving::TxtSaveOptionsBase::get_ExportHeadersFootersMode](../txtsaveoptionsbase/get_exportheadersfootersmode/). |
| [set_ExportImagesAsBase64](./set_exportimagesasbase64/)(bool) | Сеттер для [Aspose::Words::Saving::MarkdownSaveOptions::get_ExportImagesAsBase64](./get_exportimagesasbase64/). |
| [set_ExportUnderlineFormatting](./set_exportunderlineformatting/)(bool) | Сеттер для [Aspose::Words::Saving::MarkdownSaveOptions::get_ExportUnderlineFormatting](./get_exportunderlineformatting/). |
| [set_ForcePageBreaks](../txtsaveoptionsbase/set_forcepagebreaks/)(bool) | Сеттер для [Aspose::Words::Saving::TxtSaveOptionsBase::get_ForcePageBreaks](../txtsaveoptionsbase/get_forcepagebreaks/). |
| [set_ImageResolution](./set_imageresolution/)(int32_t) | Сеттер для [Aspose::Words::Saving::MarkdownSaveOptions::get_ImageResolution](./get_imageresolution/). |
| [set_ImageSavingCallback](./set_imagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IImageSavingCallback\>\&) | Позволяет контролировать, как сохраняются изображения, когда документ сохраняется в формат [Markdown](../../aspose.words/saveformat/). |
| [set_ImagesFolder](./set_imagesfolder/)(const System::String\&) | Сеттер для [Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolder](./get_imagesfolder/). |
| [set_ImagesFolderAlias](./set_imagesfolderalias/)(const System::String\&) | Сеттер для [Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolderAlias](./get_imagesfolderalias/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_LinkExportMode](./set_linkexportmode/)(Aspose::Words::Saving::MarkdownLinkExportMode) | Сеттер для [Aspose::Words::Saving::MarkdownSaveOptions::get_LinkExportMode](./get_linkexportmode/). |
| [set_ListExportMode](./set_listexportmode/)(Aspose::Words::Saving::MarkdownListExportMode) | Сеттер для [Aspose::Words::Saving::MarkdownSaveOptions::get_ListExportMode](./get_listexportmode/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Устанавливает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойства — **false**. |
| [set_OfficeMathExportMode](./set_officemathexportmode/)(Aspose::Words::Saving::MarkdownOfficeMathExportMode) | Сеттер для [Aspose::Words::Saving::MarkdownSaveOptions::get_OfficeMathExportMode](./get_officemathexportmode/). |
| [set_ParagraphBreak](../txtsaveoptionsbase/set_paragraphbreak/)(const System::String\&) | Сеттер для [Aspose::Words::Saving::TxtSaveOptionsBase::get_ParagraphBreak](../txtsaveoptionsbase/get_paragraphbreak/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_ResourceSavingCallback](./set_resourcesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IResourceSavingCallback\>\&) | Позволяет контролировать, как ресурсы сохраняются при экспорте документа в формат [Markdown](../../aspose.words/saveformat/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Указывает формат, в котором будет сохранён документ, если используется этот объект параметров сохранения. Может быть только [Markdown](../../aspose.words/saveformat/). |
| [set_TableContentAlignment](./set_tablecontentalignment/)(Aspose::Words::Saving::TableContentAlignment) | Сеттер для [Aspose::Words::Saving::MarkdownSaveOptions::get_TableContentAlignment](./get_tablecontentalignment/). |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Устанавливает значение, определяющее, следует ли обновлять поля определённых типов перед сохранением документа в фиксированный формат страниц. Значение по умолчанию для этого свойства — **true**. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | Устанавливает значение, определяющее, будет ли обновлено изображение представления OLE‑элементов управления. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| [TxtSaveOptionsBase](../txtsaveoptionsbase/txtsaveoptionsbase/)() |  |
| static [Type](./type/)() |  |
## См. также

* Class [TxtSaveOptionsBase](../txtsaveoptionsbase/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
