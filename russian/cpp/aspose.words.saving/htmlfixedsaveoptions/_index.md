---
title: "класс Aspose::Words::Saving::HtmlFixedSaveOptions"
linktitle: "HtmlFixedSaveOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "класс Aspose::Words::Saving::HtmlFixedSaveOptions. Может использоваться для указания дополнительных параметров при сохранении документа в формате HtmlFixed. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words.saving/htmlfixedsaveoptions/
---
## HtmlFixedSaveOptions class


Может использоваться для указания дополнительных параметров при сохранении документа в формате [HtmlFixed](../../aspose.words/saveformat/). Чтобы узнать больше, посетите статью документации [Указать параметры сохранения](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class HtmlFixedSaveOptions : public Aspose::Words::Saving::FixedPageSaveOptions
```

## Методы

| Метод | Описание |
| --- | --- |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Создаёт объект параметров сохранения класса, подходящего для указанного формата сохранения. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Создаёт объект параметров сохранения класса, подходящего для расширения файла, указанного в данном имени файла. |
| [Equals](../fixedpagesaveoptions/equals/)(System::SharedPtr\<System::Object\>) override | Определяет, равен ли указанный объект по значению текущему объекту. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Получает или задаёт логическое значение, указывающее, разрешено ли встраивание шрифтов с контурами PostScript при встраивании TrueType‑шрифтов в документ при его сохранении. Значение по умолчанию — **false**. |
| [get_ColorMode](../fixedpagesaveoptions/get_colormode/)() const | Получает значение, определяющее способ отображения цветов. |
| [get_CssClassNamesPrefix](./get_cssclassnamesprefix/)() const | Указывает префикс, который добавляется ко всем именам классов в файле style.css. Значение по умолчанию — **%\"aw\"**. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Получает или задает пользовательский локальный часовой пояс, используемый для полей даты/времени. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Получает или задает путь к шаблону по умолчанию (включая имя файла). Значение по умолчанию для этого свойства — **empty string**. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | Получает значение, определяющее, как рендерятся 3D‑эффекты. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | Получает или задает значение, определяющее, как рендерятся эффекты DrawingML. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | Получает или задает значение, определяющее, как рендерятся фигуры DrawingML. |
| [get_Encoding](./get_encoding/)() const | Указывает кодировку, используемую при экспорте в HTML. Значение по умолчанию — **new UTF8Encoding(true)** (UTF-8 с BOM). |
| [get_ExportEmbeddedCss](./get_exportembeddedcss/)() const | Указывает, следует ли внедрять CSS (каскадные [Style](../../aspose.words/style/) листы) в документ Html. |
| [get_ExportEmbeddedFonts](./get_exportembeddedfonts/)() const | Указывает, следует ли внедрять шрифты в документ Html в формате Base64. Обратите внимание, что установка этого флага может значительно увеличить размер выходного файла Html. |
| [get_ExportEmbeddedImages](./get_exportembeddedimages/)() const | Указывает, следует ли внедрять изображения в документ Html в формате Base64. Обратите внимание, что установка этого флага может значительно увеличить размер выходного файла Html. |
| [get_ExportEmbeddedSvg](./get_exportembeddedsvg/)() const | Указывает, следует ли внедрять ресурсы SVG в документ Html. Значение по умолчанию — **true**. |
| [get_ExportFormFields](./get_exportformfields/)() const | Получает или задает индикатор того, экспортируются ли поля формы как интерактивные элементы (как тег 'input'), а не преобразуются в текст или графику. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | Когда **true**, имя и версия Aspose.Words встраиваются в создаваемые файлы. Значение по умолчанию — **true**. |
| [get_FontFormat](./get_fontformat/)() const | Получает или задает [ExportFontFormat](../exportfontformat/), используемый для экспорта шрифтов. Значение по умолчанию — [Woff](../exportfontformat/). |
| [get_IdPrefix](./get_idprefix/)() const | Указывает префикс, который добавляется ко всем сгенерированным идентификаторам элементов в выходном документе. Значение по умолчанию — null, и префикс не добавляется. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Получает или задает значение, определяющее, как отображаются объекты чернил (InkML). |
| [get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/)() const | Получает или задает значение, определяющее качество JPEG‑изображений в HTML‑документе. |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Получает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойства **false**. |
| [get_MetafileRenderingOptions](../fixedpagesaveoptions/get_metafilerenderingoptions/)() const | Позволяет указать параметры рендеринга метафайлов. |
| [get_NumeralFormat](../fixedpagesaveoptions/get_numeralformat/)() const | Получает [NumeralFormat](../numeralformat/), используемый для отображения цифр. По умолчанию используются европейские цифры. |
| [get_OptimizeOutput](./get_optimizeoutput/)() override | Флаг указывает, требуется ли оптимизировать вывод. Если этот флаг установлен, избыточные вложенные канвасы и пустые канвасы удаляются, также соседние глифы с одинаковым форматированием объединяются. Примечание: Точность отображения содержимого может быть затронута, если это свойство установлено в **true**. Значение по умолчанию — **true**. |
| [get_PageHorizontalAlignment](./get_pagehorizontalalignment/)() const | Указывает горизонтальное выравнивание страниц в документе HTML. Значение по умолчанию — [Center](../htmlfixedpagehorizontalalignment/). |
| [get_PageMargins](./get_pagemargins/)() const | Указывает отступы вокруг страниц в документе HTML. Значение отступов измеряется в пунктах и должно быть равно или больше 0. Значение по умолчанию — 10 пунктов. |
| [get_PageSavingCallback](../fixedpagesaveoptions/get_pagesavingcallback/)() const | Позволяет управлять тем, как отдельные страницы сохраняются при экспорте документа в фиксированный формат страниц. |
| [get_PageSet](../fixedpagesaveoptions/get_pageset/)() const | Получает или задает страницы для рендеринга. По умолчанию — все страницы документа. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | Когда **true**, вывод форматируется красиво, где это применимо. Значение по умолчанию **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Вызывается во время сохранения документа и принимает данные о прогрессе сохранения. |
| [get_RemoveJavaScriptFromLinks](./get_removejavascriptfromlinks/)() const | Указывает, будет ли JavaScript удалён из ссылок. По умолчанию **false**. |
| [get_ResourceSavingCallback](./get_resourcesavingcallback/)() const | Позволяет управлять тем, как ресурсы (изображения, шрифты и css) сохраняются при экспорте документа в фиксированный формат Html. |
| [get_ResourcesFolder](./get_resourcesfolder/)() const | Указывает физическую папку, в которой сохраняются ресурсы (изображения, шрифты, css) при экспорте документа в формат Html. Значение по умолчанию — **null**. |
| [get_ResourcesFolderAlias](./get_resourcesfolderalias/)() const | Указывает имя папки, используемой для построения URI изображений, записываемых в документ Html. Значение по умолчанию — **null**. |
| [get_SaveFontFaceCssSeparately](./get_savefontfacecssseparately/)() const | Флаг указывает, следует ли помещать правила CSS \"@font-face\" в отдельный файл \"fontFaces.css\", когда документ сохраняется с внешней таблицей стилей (то есть когда [ExportEmbeddedCss](./get_exportembeddedcss/) имеет значение **false**). Значение по умолчанию — **false**, все правила CSS записываются в один файл \"styles.css\". |
| [get_SaveFormat](./get_saveformat/)() override | Указывает формат, в котором будет сохранён документ при использовании этого объекта параметров сохранения. Может быть только [HtmlFixed](../../aspose.words/saveformat/). |
| [get_ShowPageBorder](./get_showpageborder/)() const | Указывает, следует ли отображать границу вокруг страниц. Значение по умолчанию — **true**. |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | Указывает папку для временных файлов, используемых при сохранении в файл DOC или DOCX. По умолчанию это свойство равно **null**, и временные файлы не используются. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | Определяет, будут ли атрибуты шрифта изменяться в соответствии с используемым кодом символа. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | Получает или задаёт значение, определяющее, будет ли свойство [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) обновлено перед сохранением. Значение по умолчанию — **false**;. |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | Получает значение, определяющее, следует ли обновлять поля определённых типов перед сохранением документа в фиксированный формат страниц. Значение по умолчанию для этого свойства — **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | Получает или задаёт значение, определяющее, будет ли свойство [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) обновлено перед сохранением. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | Получает или задаёт значение, определяющее, будет ли свойство [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) обновлено перед сохранением. |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | Получает значение, определяющее, будет ли обновлено изображение представления OLE‑элементов. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | Получает или задаёт значение, определяющее, использовать ли сглаживание при рендеринге. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | Получает или задаёт значение, определяющее, использовать ли высококачественные (т.е. медленные) алгоритмы рендеринга. |
| [get_UseTargetMachineFonts](./get_usetargetmachinefonts/)() const | Флаг указывает, должны ли использоваться шрифты целевой машины для отображения документа. Если этот флаг установлен в **true**, свойства [FontFormat](./get_fontformat/) и [ExportEmbeddedFonts](./get_exportembeddedfonts/) не действуют, также [ResourceSavingCallback](./get_resourcesavingcallback/) не вызывается для шрифтов. Значение по умолчанию — **false**. |
| [GetType](./gettype/)() const override |  |
| [HtmlFixedSaveOptions](./htmlfixedsaveoptions/)() |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_ColorMode](../fixedpagesaveoptions/set_colormode/)(Aspose::Words::Saving::ColorMode) | Устанавливает значение, определяющее, как отображаются цвета. |
| [set_CssClassNamesPrefix](./set_cssclassnamesprefix/)(const System::String\&) | Указывает префикс, который добавляется ко всем именам классов в файле style.css. Значение по умолчанию — **%\"aw\"**. |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Устанавливает значение, определяющее, как рендерятся 3D‑эффекты. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_Encoding](./set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Сеттер для [Aspose::Words::Saving::HtmlFixedSaveOptions::get_Encoding](./get_encoding/). |
| [set_ExportEmbeddedCss](./set_exportembeddedcss/)(bool) | Сеттер для [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedCss](./get_exportembeddedcss/). |
| [set_ExportEmbeddedFonts](./set_exportembeddedfonts/)(bool) | Сеттер для [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedFonts](./get_exportembeddedfonts/). |
| [set_ExportEmbeddedImages](./set_exportembeddedimages/)(bool) | Сеттер для [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedImages](./get_exportembeddedimages/). |
| [set_ExportEmbeddedSvg](./set_exportembeddedsvg/)(bool) | Сеттер для [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportEmbeddedSvg](./get_exportembeddedsvg/). |
| [set_ExportFormFields](./set_exportformfields/)(bool) | Сеттер для [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ExportFormFields](./get_exportformfields/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_FontFormat](./set_fontformat/)(Aspose::Words::Saving::ExportFontFormat) | Сеттер для [Aspose::Words::Saving::HtmlFixedSaveOptions::get_FontFormat](./get_fontformat/). |
| [set_IdPrefix](./set_idprefix/)(const System::String\&) | Сеттер для [Aspose::Words::Saving::HtmlFixedSaveOptions::get_IdPrefix](./get_idprefix/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_JpegQuality](../fixedpagesaveoptions/set_jpegquality/)(int32_t) | Сеттер для [Aspose::Words::Saving::FixedPageSaveOptions::get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Устанавливает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойства — **false**. |
| [set_MetafileRenderingOptions](../fixedpagesaveoptions/set_metafilerenderingoptions/)(const System::SharedPtr\<Aspose::Words::Saving::MetafileRenderingOptions\>\&) | Позволяет указать параметры рендеринга метафайлов. |
| [set_NumeralFormat](../fixedpagesaveoptions/set_numeralformat/)(Aspose::Words::Saving::NumeralFormat) | Устанавливает [NumeralFormat](../numeralformat/), используемый для отображения цифр. По умолчанию используются европейские цифры. |
| [set_OptimizeOutput](./set_optimizeoutput/)(bool) override | Сеттер для [Aspose::Words::Saving::HtmlFixedSaveOptions::get_OptimizeOutput](./get_optimizeoutput/). |
| [set_PageHorizontalAlignment](./set_pagehorizontalalignment/)(Aspose::Words::Saving::HtmlFixedPageHorizontalAlignment) | Сеттер для [Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageHorizontalAlignment](./get_pagehorizontalalignment/). |
| [set_PageMargins](./set_pagemargins/)(double) | Сеттер для [Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageMargins](./get_pagemargins/). |
| [set_PageSavingCallback](../fixedpagesaveoptions/set_pagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IPageSavingCallback\>\&) | Позволяет управлять тем, как отдельные страницы сохраняются при экспорте документа в фиксированный формат страниц. |
| [set_PageSet](../fixedpagesaveoptions/set_pageset/)(const System::SharedPtr\<Aspose::Words::Saving::PageSet\>\&) | Сеттер для [Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet](../fixedpagesaveoptions/get_pageset/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_RemoveJavaScriptFromLinks](./set_removejavascriptfromlinks/)(bool) | Сеттер для [Aspose::Words::Saving::HtmlFixedSaveOptions::get_RemoveJavaScriptFromLinks](./get_removejavascriptfromlinks/). |
| [set_ResourceSavingCallback](./set_resourcesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IResourceSavingCallback\>\&) | Позволяет управлять тем, как ресурсы (изображения, шрифты и css) сохраняются при экспорте документа в фиксированный формат Html. |
| [set_ResourcesFolder](./set_resourcesfolder/)(const System::String\&) | Сеттер для [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ResourcesFolder](./get_resourcesfolder/). |
| [set_ResourcesFolderAlias](./set_resourcesfolderalias/)(const System::String\&) | Сеттер для [Aspose::Words::Saving::HtmlFixedSaveOptions::get_ResourcesFolderAlias](./get_resourcesfolderalias/). |
| [set_SaveFontFaceCssSeparately](./set_savefontfacecssseparately/)(bool) | Сеттер для [Aspose::Words::Saving::HtmlFixedSaveOptions::get_SaveFontFaceCssSeparately](./get_savefontfacecssseparately/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Указывает формат, в котором будет сохранён документ при использовании этого объекта параметров сохранения. Может быть только [HtmlFixed](../../aspose.words/saveformat/). |
| [set_ShowPageBorder](./set_showpageborder/)(bool) | Указывает, следует ли отображать границу вокруг страниц. Значение по умолчанию — **true**. |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Устанавливает значение, определяющее, следует ли обновлять поля определённых типов перед сохранением документа в фиксированный формат страниц. Значение по умолчанию для этого свойства — **true**. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | Устанавливает значение, определяющее, будет ли обновлено изображение представления OLE‑элементов управления. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| [set_UseTargetMachineFonts](./set_usetargetmachinefonts/)(bool) | Сеттер для [Aspose::Words::Saving::HtmlFixedSaveOptions::get_UseTargetMachineFonts](./get_usetargetmachinefonts/). |
| static [Type](./type/)() |  |
## См. также

* Class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
