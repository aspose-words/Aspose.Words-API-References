---
title: "Aspose::Words::Saving::PdfSaveOptions класс"
linktitle: "PdfSaveOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Saving::PdfSaveOptions класс. Может использоваться для указания дополнительных параметров при сохранении документа в формат Pdf. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 25000
url: /ru/cpp/aspose.words.saving/pdfsaveoptions/
---
## PdfSaveOptions class


Можно использовать для указания дополнительных параметров при сохранении документа в формат [Pdf](../../aspose.words/saveformat/). Чтобы узнать больше, посетите статью документации [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class PdfSaveOptions : public Aspose::Words::Saving::FixedPageSaveOptions
```

## Методы

| Метод | Описание |
| --- | --- |
| [Clone](./clone/)() | Создаёт глубокую копию этого объекта. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Создаёт объект параметров сохранения класса, подходящего для указанного формата сохранения. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Создаёт объект параметров сохранения класса, подходящего для расширения файла, указанного в данном имени файла. |
| [Equals](../fixedpagesaveoptions/equals/)(System::SharedPtr\<System::Object\>) override | Определяет, равен ли указанный объект по значению текущему объекту. |
| [get_AdditionalTextPositioning](./get_additionaltextpositioning/)() const | Флаг, указывающий, следует ли записывать дополнительные операторы позиционирования текста или нет. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Получает или задаёт логическое значение, указывающее, разрешено ли встраивание шрифтов с контурами PostScript при встраивании TrueType‑шрифтов в документ при его сохранении. Значение по умолчанию — **false**. |
| [get_AttachmentsEmbeddingMode](./get_attachmentsembeddingmode/)() const | Получает или задаёт значение, определяющее, как вложения встраиваются в PDF‑документ. |
| [get_CacheBackgroundGraphics](./get_cachebackgroundgraphics/)() const | Получает или задаёт значение, определяющее, кэшировать ли графику, размещённую в фоне документа. |
| [get_ColorMode](../fixedpagesaveoptions/get_colormode/)() const | Получает значение, определяющее способ отображения цветов. |
| [get_Compliance](./get_compliance/)() const | Указывает уровень соответствия стандартам PDF для выходных документов. |
| [get_CreateNoteHyperlinks](./get_createnotehyperlinks/)() const | Указывает, следует ли преобразовывать ссылки на сноски/концевые сноски в основном тексте в активные гиперссылки. При щелчке гиперссылка приведёт к соответствующей сноске/концевой сноске. По умолчанию **false**. |
| [get_CustomPropertiesExport](./get_custompropertiesexport/)() const | Получает или задаёт значение, определяющее способ экспорта [CustomDocumentProperties](../../aspose.words/document/get_customdocumentproperties/) в PDF‑файл. |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Получает или задает пользовательский локальный часовой пояс, используемый для полей даты/времени. |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Получает или задает путь к шаблону по умолчанию (включая имя файла). Значение по умолчанию для этого свойства — **empty string**. |
| [get_DigitalSignatureDetails](./get_digitalsignaturedetails/)() const | Получает или задаёт детали подписи выходного PDF‑документа. |
| [get_DisplayDocTitle](./get_displaydoctitle/)() const | Флаг, указывающий, должно ли заголовок окна отображать название документа, взятое из записи Title словаря информации о документе. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | Получает значение, определяющее, как рендерятся 3D‑эффекты. |
| [get_DmlEffectsRenderingMode](./get_dmleffectsrenderingmode/)() override | Получает или задает значение, определяющее, как рендерятся эффекты DrawingML. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | Получает или задает значение, определяющее, как рендерятся фигуры DrawingML. |
| [get_DownsampleOptions](./get_downsampleoptions/)() const | Позволяет указать параметры понижения дискретизации. |
| [get_EmbedFullFonts](./get_embedfullfonts/)() const | Контролирует, как шрифты встраиваются в получаемые PDF‑документы. |
| [get_EncryptionDetails](./get_encryptiondetails/)() const | Получает или задаёт детали шифрования выходного PDF‑документа. |
| [get_ExportDocumentStructure](./get_exportdocumentstructure/)() const | Получает или задаёт значение, определяющее, экспортировать ли структуру документа. |
| [get_ExportFloatingShapesAsInlineTag](./get_exportfloatingshapesasinlinetag/)() const | Получает или задаёт значение, определяющее, экспортировать ли плавающие фигуры как встроенные теги в структуре документа. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | Когда **true**, имя и версия Aspose.Words встраиваются в создаваемые файлы. Значение по умолчанию — **true**. |
| [get_ExportLanguageToSpanTag](./get_exportlanguagetospantag/)() const | Получает или задаёт значение, определяющее, создавать ли тег "Span" в структуре документа для экспорта языка текста. |
| [get_ExportParagraphGraphicsToArtifact](./get_exportparagraphgraphicstoartifact/)() const | Получает или задаёт значение, определяющее, следует ли помечать графику абзаца как артефакт. |
| [get_FontEmbeddingMode](./get_fontembeddingmode/)() const | Указывает режим встраивания шрифтов. |
| [get_GenerateFormFieldScripts](./get_generateformfieldscripts/)() const | Указывает, генерировать ли скрипты, имитирующие поведение определённых полей формы Microsoft Word в PDF. По умолчанию **false**. |
| [get_HeaderFooterBookmarksExportMode](./get_headerfooterbookmarksexportmode/)() const | Определяет, как экспортируются закладки в колонтитулах. |
| [get_ImageColorSpaceExportMode](./get_imagecolorspaceexportmode/)() const | Указывает, как будет выбран цветовое пространство для изображений в PDF‑документе. |
| [get_ImageCompression](./get_imagecompression/)() const | Указывает тип сжатия, используемый для всех изображений в документе. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Получает или задает значение, определяющее, как отображаются объекты чернил (InkML). |
| [get_InterpolateImages](./get_interpolateimages/)() const | Флаг, указывающий, должна ли интерполяция изображения выполняться совместимым просмотрщиком. Когда указано **false**, флаг не записывается в выходной документ, и используется поведение просмотрщика по умолчанию. |
| [get_JpegQuality](./get_jpegquality/)() | Получает или задаёт значение, определяющее качество JPEG‑изображений внутри PDF‑документа. |
| [get_JpegQuality](../fixedpagesaveoptions/get_jpegquality/)() const | Получает или задает значение, определяющее качество JPEG‑изображений в HTML‑документе. |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Получает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойства **false**. |
| [get_MetafileRenderingOptions](../fixedpagesaveoptions/get_metafilerenderingoptions/)() const | Позволяет указать параметры рендеринга метафайлов. |
| [get_NumeralFormat](../fixedpagesaveoptions/get_numeralformat/)() const | Получает [NumeralFormat](../numeralformat/), используемый для отображения цифр. По умолчанию используются европейские цифры. |
| [get_OpenHyperlinksInNewWindow](./get_openhyperlinksinnewwindow/)() const | Получает или задаёт значение, определяющее, принудительно ли открывать гиперссылки в выходном Pdf‑документе в новом окне (или вкладке) браузера. |
| virtual [get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/)() | Флаг указывает, требуется ли оптимизировать вывод. Если этот флаг установлен, избыточные вложенные канвасы и пустые канвасы удаляются, также соседние глифы с одинаковым форматированием объединяются. Примечание: Точность отображения содержимого может быть снижена, если это свойство установлено в **true**. По умолчанию — **false**. |
| [get_OutlineOptions](./get_outlineoptions/)() const | Позволяет указать параметры контура. |
| [get_PageLayout](./get_pagelayout/)() const | Указывает макет страницы, который будет использоваться при открытии документа в PDF‑читалке. |
| [get_PageMode](./get_pagemode/)() const | Указывает, как PDF‑документ должен отображаться при открытии в PDF‑просмотрщике. |
| [get_PageSavingCallback](../fixedpagesaveoptions/get_pagesavingcallback/)() const | Позволяет управлять тем, как отдельные страницы сохраняются при экспорте документа в фиксированный формат страниц. |
| [get_PageSet](../fixedpagesaveoptions/get_pageset/)() const | Получает или задает страницы для рендеринга. По умолчанию — все страницы документа. |
| [get_PreblendImages](./get_preblendimages/)() const | Получает или задает значение, определяющее, следует ли предварительно смешивать прозрачные изображения с черным фоном. |
| [get_PreserveFormFields](./get_preserveformfields/)() const | Указывает, следует ли сохранять поля формы Microsoft Word как поля формы в PDF или преобразовывать их в текст. По умолчанию **false**. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | Когда **true**, вывод форматируется красиво, где это применимо. Значение по умолчанию **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Вызывается во время сохранения документа и принимает данные о прогрессе сохранения. |
| [get_RenderChoiceFormFieldBorder](./get_renderchoiceformfieldborder/)() const | Указывает, следует ли отображать границу поля выбора формы PDF. |
| [get_SaveFormat](./get_saveformat/)() override | Указывает формат, в котором будет сохранён документ, если используется этот объект параметров сохранения. Может быть только [Pdf](../../aspose.words/saveformat/). |
| [get_TempFolder](../saveoptions/get_tempfolder/)() const | Указывает папку для временных файлов, используемых при сохранении в файл DOC или DOCX. По умолчанию это свойство равно **null**, и временные файлы не используются. |
| [get_TextCompression](./get_textcompression/)() const | Указывает тип сжатия, который будет использоваться для всего текстового содержимого документа. |
| [get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/)() const | Определяет, будут ли атрибуты шрифта изменяться в соответствии с используемым кодом символа. |
| [get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/)() const | Получает или задаёт значение, определяющее, будет ли свойство [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) обновлено перед сохранением. Значение по умолчанию — **false**;. |
| [get_UpdateFields](../saveoptions/get_updatefields/)() const | Получает значение, определяющее, следует ли обновлять поля определённых типов перед сохранением документа в фиксированный формат страниц. Значение по умолчанию для этого свойства — **true**. |
| [get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/)() const | Получает или задаёт значение, определяющее, будет ли свойство [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) обновлено перед сохранением. |
| [get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/)() const | Получает или задаёт значение, определяющее, будет ли свойство [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) обновлено перед сохранением. |
| [get_UpdateOleControlImages](../saveoptions/get_updateolecontrolimages/)() const | Получает значение, определяющее, будет ли обновлено изображение представления OLE‑элементов. |
| [get_UseAntiAliasing](../saveoptions/get_useantialiasing/)() const | Получает или задаёт значение, определяющее, использовать ли сглаживание при рендеринге. |
| [get_UseBookFoldPrintingSettings](./get_usebookfoldprintingsettings/)() const | Получает или задает логическое значение, указывающее, следует ли сохранять документ с использованием книжного макета печати, если он указан через [MultiplePages](../../aspose.words/pagesetup/get_multiplepages/). |
| [get_UseCoreFonts](./get_usecorefonts/)() const | Получает или задает значение, определяющее, следует ли заменять шрифты TrueType Arial, Times New Roman, Courier New и Symbol на базовые шрифты PDF Type 1. |
| [get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/)() const | Получает или задаёт значение, определяющее, использовать ли высококачественные (т.е. медленные) алгоритмы рендеринга. |
| [get_UseSdtTagAsFormFieldName](./get_usesdttagasformfieldname/)() const | Указывает, следует ли использовать свойство Tag или Id элемента управления SDT в качестве имени поля формы в PDF. |
| [get_ZoomBehavior](./get_zoombehavior/)() const | Получает значение, определяющее, какой тип масштабирования следует применять при открытии документа в просмотрщике PDF. |
| [get_ZoomFactor](./get_zoomfactor/)() const | Получает значение, определяющее коэффициент масштабирования (в процентах) для документа. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PdfSaveOptions](./pdfsaveoptions/)() | Инициализирует новый экземпляр этого класса, который можно использовать для сохранения документа в формате [Pdf](../../aspose.words/saveformat/). |
| [set_AdditionalTextPositioning](./set_additionaltextpositioning/)(bool) | Сеттер для [Aspose::Words::Saving::PdfSaveOptions::get_AdditionalTextPositioning](./get_additionaltextpositioning/). |
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_AttachmentsEmbeddingMode](./set_attachmentsembeddingmode/)(Aspose::Words::Saving::PdfAttachmentsEmbeddingMode) | Сеттер для [Aspose::Words::Saving::PdfSaveOptions::get_AttachmentsEmbeddingMode](./get_attachmentsembeddingmode/). |
| [set_CacheBackgroundGraphics](./set_cachebackgroundgraphics/)(bool) | Сеттер для [Aspose::Words::Saving::PdfSaveOptions::get_CacheBackgroundGraphics](./get_cachebackgroundgraphics/). |
| [set_ColorMode](../fixedpagesaveoptions/set_colormode/)(Aspose::Words::Saving::ColorMode) | Устанавливает значение, определяющее, как отображаются цвета. |
| [set_Compliance](./set_compliance/)(Aspose::Words::Saving::PdfCompliance) | Указывает уровень соответствия стандартам PDF для выходных документов. |
| [set_CreateNoteHyperlinks](./set_createnotehyperlinks/)(bool) | Указывает, следует ли преобразовывать ссылки на сноски/концевые сноски в основном тексте в активные гиперссылки. При щелчке гиперссылка приведёт к соответствующей сноске/концевой сноске. По умолчанию **false**. |
| [set_CustomPropertiesExport](./set_custompropertiesexport/)(Aspose::Words::Saving::PdfCustomPropertiesExport) | Сеттер для [Aspose::Words::Saving::PdfSaveOptions::get_CustomPropertiesExport](./get_custompropertiesexport/). |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_DigitalSignatureDetails](./set_digitalsignaturedetails/)(const System::SharedPtr\<Aspose::Words::Saving::PdfDigitalSignatureDetails\>\&) | Сеттер для [Aspose::Words::Saving::PdfSaveOptions::get_DigitalSignatureDetails](./get_digitalsignaturedetails/). |
| [set_DisplayDocTitle](./set_displaydoctitle/)(bool) | Сеттер для [Aspose::Words::Saving::PdfSaveOptions::get_DisplayDocTitle](./get_displaydoctitle/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Устанавливает значение, определяющее, как рендерятся 3D‑эффекты. |
| [set_DmlEffectsRenderingMode](./set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) override | Сеттер для [Aspose::Words::Saving::PdfSaveOptions::get_DmlEffectsRenderingMode](./get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_DownsampleOptions](./set_downsampleoptions/)(const System::SharedPtr\<Aspose::Words::Saving::DownsampleOptions\>\&) | Позволяет указать параметры понижения дискретизации. |
| [set_EmbedFullFonts](./set_embedfullfonts/)(bool) | Сеттер для [Aspose::Words::Saving::PdfSaveOptions::get_EmbedFullFonts](./get_embedfullfonts/). |
| [set_EncryptionDetails](./set_encryptiondetails/)(const System::SharedPtr\<Aspose::Words::Saving::PdfEncryptionDetails\>\&) | Сеттер для [Aspose::Words::Saving::PdfSaveOptions::get_EncryptionDetails](./get_encryptiondetails/). |
| [set_ExportDocumentStructure](./set_exportdocumentstructure/)(bool) | Сеттер для [Aspose::Words::Saving::PdfSaveOptions::get_ExportDocumentStructure](./get_exportdocumentstructure/). |
| [set_ExportFloatingShapesAsInlineTag](./set_exportfloatingshapesasinlinetag/)(bool) | Сеттер для [Aspose::Words::Saving::PdfSaveOptions::get_ExportFloatingShapesAsInlineTag](./get_exportfloatingshapesasinlinetag/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_ExportLanguageToSpanTag](./set_exportlanguagetospantag/)(bool) | Сеттер для [Aspose::Words::Saving::PdfSaveOptions::get_ExportLanguageToSpanTag](./get_exportlanguagetospantag/). |
| [set_ExportParagraphGraphicsToArtifact](./set_exportparagraphgraphicstoartifact/)(bool) | Сеттер для [Aspose::Words::Saving::PdfSaveOptions::get_ExportParagraphGraphicsToArtifact](./get_exportparagraphgraphicstoartifact/). |
| [set_FontEmbeddingMode](./set_fontembeddingmode/)(Aspose::Words::Saving::PdfFontEmbeddingMode) | Сеттер для [Aspose::Words::Saving::PdfSaveOptions::get_FontEmbeddingMode](./get_fontembeddingmode/). |
| [set_GenerateFormFieldScripts](./set_generateformfieldscripts/)(bool) | Сеттер для [Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts](./get_generateformfieldscripts/). |
| [set_HeaderFooterBookmarksExportMode](./set_headerfooterbookmarksexportmode/)(Aspose::Words::Saving::HeaderFooterBookmarksExportMode) | Сеттер для [Aspose::Words::Saving::PdfSaveOptions::get_HeaderFooterBookmarksExportMode](./get_headerfooterbookmarksexportmode/). |
| [set_ImageColorSpaceExportMode](./set_imagecolorspaceexportmode/)(Aspose::Words::Saving::PdfImageColorSpaceExportMode) | Сеттер для [Aspose::Words::Saving::PdfSaveOptions::get_ImageColorSpaceExportMode](./get_imagecolorspaceexportmode/). |
| [set_ImageCompression](./set_imagecompression/)(Aspose::Words::Saving::PdfImageCompression) | Сеттер для [Aspose::Words::Saving::PdfSaveOptions::get_ImageCompression](./get_imagecompression/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_InterpolateImages](./set_interpolateimages/)(bool) | Сеттер для [Aspose::Words::Saving::PdfSaveOptions::get_InterpolateImages](./get_interpolateimages/). |
| [set_JpegQuality](./set_jpegquality/)(int32_t) | Сеттер для [Aspose::Words::Saving::PdfSaveOptions::get_JpegQuality](./get_jpegquality/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Устанавливает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойства — **false**. |
| [set_MetafileRenderingOptions](../fixedpagesaveoptions/set_metafilerenderingoptions/)(const System::SharedPtr\<Aspose::Words::Saving::MetafileRenderingOptions\>\&) | Позволяет указать параметры рендеринга метафайлов. |
| [set_NumeralFormat](../fixedpagesaveoptions/set_numeralformat/)(Aspose::Words::Saving::NumeralFormat) | Устанавливает [NumeralFormat](../numeralformat/), используемый для отображения цифр. По умолчанию используются европейские цифры. |
| [set_OpenHyperlinksInNewWindow](./set_openhyperlinksinnewwindow/)(bool) | Сеттер для [Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow](./get_openhyperlinksinnewwindow/). |
| virtual [set_OptimizeOutput](../fixedpagesaveoptions/set_optimizeoutput/)(bool) | Сеттер для [Aspose::Words::Saving::FixedPageSaveOptions::get_OptimizeOutput](../fixedpagesaveoptions/get_optimizeoutput/). |
| [set_PageLayout](./set_pagelayout/)(Aspose::Words::Saving::PdfPageLayout) | Указывает макет страницы, который будет использоваться при открытии документа в PDF‑читалке. |
| [set_PageMode](./set_pagemode/)(Aspose::Words::Saving::PdfPageMode) | Указывает, как PDF‑документ должен отображаться при открытии в PDF‑просмотрщике. |
| [set_PageSavingCallback](../fixedpagesaveoptions/set_pagesavingcallback/)(const System::SharedPtr\<Aspose::Words::Saving::IPageSavingCallback\>\&) | Позволяет управлять тем, как отдельные страницы сохраняются при экспорте документа в фиксированный формат страниц. |
| [set_PageSet](../fixedpagesaveoptions/set_pageset/)(const System::SharedPtr\<Aspose::Words::Saving::PageSet\>\&) | Сеттер для [Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet](../fixedpagesaveoptions/get_pageset/). |
| [set_PreblendImages](./set_preblendimages/)(bool) | Сеттер для [Aspose::Words::Saving::PdfSaveOptions::get_PreblendImages](./get_preblendimages/). |
| [set_PreserveFormFields](./set_preserveformfields/)(bool) | Сеттер для [Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields](./get_preserveformfields/). |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_RenderChoiceFormFieldBorder](./set_renderchoiceformfieldborder/)(bool) | Сеттер для [Aspose::Words::Saving::PdfSaveOptions::get_RenderChoiceFormFieldBorder](./get_renderchoiceformfieldborder/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Указывает формат, в котором будет сохранён документ, если используется этот объект параметров сохранения. Может быть только [Pdf](../../aspose.words/saveformat/). |
| [set_TempFolder](../saveoptions/set_tempfolder/)(const System::String\&) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_TempFolder](../saveoptions/get_tempfolder/). |
| [set_TextCompression](./set_textcompression/)(Aspose::Words::Saving::PdfTextCompression) | Сеттер для [Aspose::Words::Saving::PdfSaveOptions::get_TextCompression](./get_textcompression/). |
| [set_UpdateAmbiguousTextFont](../saveoptions/set_updateambiguoustextfont/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](../saveoptions/get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](../saveoptions/set_updatecreatedtimeproperty/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](../saveoptions/get_updatecreatedtimeproperty/). |
| [set_UpdateFields](../saveoptions/set_updatefields/)(bool) | Устанавливает значение, определяющее, следует ли обновлять поля определённых типов перед сохранением документа в фиксированный формат страниц. Значение по умолчанию для этого свойства — **true**. |
| [set_UpdateLastPrintedProperty](../saveoptions/set_updatelastprintedproperty/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](../saveoptions/get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](../saveoptions/set_updatelastsavedtimeproperty/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](../saveoptions/get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](../saveoptions/set_updateolecontrolimages/)(bool) | Устанавливает значение, определяющее, будет ли обновлено изображение представления OLE‑элементов управления. |
| [set_UseAntiAliasing](../saveoptions/set_useantialiasing/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](../saveoptions/get_useantialiasing/). |
| [set_UseBookFoldPrintingSettings](./set_usebookfoldprintingsettings/)(bool) | Сеттер для [Aspose::Words::Saving::PdfSaveOptions::get_UseBookFoldPrintingSettings](./get_usebookfoldprintingsettings/). |
| [set_UseCoreFonts](./set_usecorefonts/)(bool) | Сеттер для [Aspose::Words::Saving::PdfSaveOptions::get_UseCoreFonts](./get_usecorefonts/). |
| [set_UseHighQualityRendering](../saveoptions/set_usehighqualityrendering/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](../saveoptions/get_usehighqualityrendering/). |
| [set_UseSdtTagAsFormFieldName](./set_usesdttagasformfieldname/)(bool) | Сеттер для [Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName](./get_usesdttagasformfieldname/). |
| [set_ZoomBehavior](./set_zoombehavior/)(Aspose::Words::Saving::PdfZoomBehavior) | Устанавливает значение, определяющее, какой тип масштабирования следует применять при открытии документа в просмотрщике PDF. |
| [set_ZoomFactor](./set_zoomfactor/)(int32_t) | Устанавливает значение, определяющее коэффициент масштабирования (в процентах) для документа. |
| static [Type](./type/)() |  |
## См. также

* Class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
