---
title: "Класс Aspose::Words::Saving::XlsxSaveOptions"
linktitle: "XlsxSaveOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Saving::XlsxSaveOptions. Может использоваться для указания дополнительных параметров при сохранении документа в формате Xlsx. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 37500
url: /ru/cpp/aspose.words.saving/xlsxsaveoptions/
---
## XlsxSaveOptions class


Можно использовать для указания дополнительных параметров при сохранении документа в формате [Xlsx](../../aspose.words/saveformat/). Чтобы узнать больше, посетите статью документации [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class XlsxSaveOptions : public Aspose::Words::Saving::SaveOptions
```

## Методы

| Метод | Описание |
| --- | --- |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(Aspose::Words::SaveFormat) | Создаёт объект параметров сохранения класса, подходящего для указанного формата сохранения. |
| static [CreateSaveOptions](../saveoptions/createsaveoptions/)(const System::String\&) | Создаёт объект параметров сохранения класса, подходящего для расширения файла, указанного в данном имени файла. |
| [get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/)() const | Получает или задаёт логическое значение, указывающее, разрешено ли встраивание шрифтов с контурами PostScript при встраивании TrueType‑шрифтов в документ при его сохранении. Значение по умолчанию — **false**. |
| [get_CompressionLevel](./get_compressionlevel/)() const | Указывает уровень сжатия, используемый при сохранении документа. Значение по умолчанию — [Normal](../compressionlevel/). |
| [get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/)() const | Получает или задает пользовательский локальный часовой пояс, используемый для полей даты/времени. |
| [get_DateTimeParsingMode](./get_datetimeparsingmode/)() const | Получает или задает режим, который определяет, как текст документа анализируется для выявления значений даты и времени. Значение по умолчанию — [UseCurrentLocale](../xlsxdatetimeparsingmode/). |
| [get_DefaultTemplate](../saveoptions/get_defaulttemplate/)() const | Получает или задает путь к шаблону по умолчанию (включая имя файла). Значение по умолчанию для этого свойства — **empty string**. |
| [get_Dml3DEffectsRenderingMode](../saveoptions/get_dml3deffectsrenderingmode/)() const | Получает значение, определяющее, как рендерятся 3D‑эффекты. |
| virtual [get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/)() | Получает или задает значение, определяющее, как рендерятся эффекты DrawingML. |
| [get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/)() const | Получает или задает значение, определяющее, как рендерятся фигуры DrawingML. |
| [get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/)() const | Когда **true**, имя и версия Aspose.Words встраиваются в создаваемые файлы. Значение по умолчанию — **true**. |
| [get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/)() const | Получает или задает значение, определяющее, как отображаются объекты чернил (InkML). |
| [get_MemoryOptimization](../saveoptions/get_memoryoptimization/)() const | Получает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойства **false**. |
| [get_PrettyFormat](../saveoptions/get_prettyformat/)() const | Когда **true**, вывод форматируется красиво, где это применимо. Значение по умолчанию **false**. |
| [get_ProgressCallback](../saveoptions/get_progresscallback/)() const | Вызывается во время сохранения документа и принимает данные о прогрессе сохранения. |
| [get_SaveFormat](./get_saveformat/)() override | Указывает формат, в котором будет сохранён документ при использовании этого объекта параметров сохранения. Может быть только [Xlsx](../../aspose.words/saveformat/). |
| [get_SectionMode](./get_sectionmode/)() const | Получает или задает способ обработки разделов при сохранении в выходной документ XLSX. Значение по умолчанию — [MultipleWorksheets](../xlsxsectionmode/). |
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
| [set_AllowEmbeddingPostScriptFonts](../saveoptions/set_allowembeddingpostscriptfonts/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](../saveoptions/get_allowembeddingpostscriptfonts/). |
| [set_CompressionLevel](./set_compressionlevel/)(Aspose::Words::Saving::CompressionLevel) | Сеттер для [Aspose::Words::Saving::XlsxSaveOptions::get_CompressionLevel](./get_compressionlevel/). |
| [set_CustomTimeZoneInfo](../saveoptions/set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](../saveoptions/get_customtimezoneinfo/). |
| [set_DateTimeParsingMode](./set_datetimeparsingmode/)(Aspose::Words::Saving::XlsxDateTimeParsingMode) | Сеттер для [Aspose::Words::Saving::XlsxSaveOptions::get_DateTimeParsingMode](./get_datetimeparsingmode/). |
| [set_DefaultTemplate](../saveoptions/set_defaulttemplate/)(const System::String\&) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](../saveoptions/get_defaulttemplate/). |
| [set_Dml3DEffectsRenderingMode](../saveoptions/set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Устанавливает значение, определяющее, как рендерятся 3D‑эффекты. |
| virtual [set_DmlEffectsRenderingMode](../saveoptions/set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](../saveoptions/get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](../saveoptions/set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](../saveoptions/get_dmlrenderingmode/). |
| [set_ExportGeneratorName](../saveoptions/set_exportgeneratorname/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](../saveoptions/get_exportgeneratorname/). |
| [set_ImlRenderingMode](../saveoptions/set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](../saveoptions/get_imlrenderingmode/). |
| [set_MemoryOptimization](../saveoptions/set_memoryoptimization/)(bool) | Устанавливает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойства — **false**. |
| [set_PrettyFormat](../saveoptions/set_prettyformat/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](../saveoptions/get_prettyformat/). |
| [set_ProgressCallback](../saveoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](../saveoptions/get_progresscallback/). |
| [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) override | Сеттер для [Aspose::Words::Saving::XlsxSaveOptions::get_SaveFormat](./get_saveformat/). |
| [set_SectionMode](./set_sectionmode/)(Aspose::Words::Saving::XlsxSectionMode) | Сеттер для [Aspose::Words::Saving::XlsxSaveOptions::get_SectionMode](./get_sectionmode/). |
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
| [XlsxSaveOptions](./xlsxsaveoptions/)() |  |

## Примеры



Показывает, как сжать документ XLSX.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape with linked chart.docx");

auto xlsxSaveOptions = System::MakeObject<Aspose::Words::Saving::XlsxSaveOptions>();
xlsxSaveOptions->set_CompressionLevel(Aspose::Words::Saving::CompressionLevel::Maximum);
xlsxSaveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Xlsx);

doc->Save(get_ArtifactsDir() + u"XlsxSaveOptions.CompressXlsx.xlsx", xlsxSaveOptions);
```

## См. также

* Class [SaveOptions](../saveoptions/)
* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
