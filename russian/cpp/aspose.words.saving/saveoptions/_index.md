---
title: "Класс Aspose::Words::Saving::SaveOptions"
linktitle: "SaveOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Saving::SaveOptions. Это абстрактный базовый класс для классов, позволяющих пользователю задавать дополнительные параметры при сохранении документа в определённый формат. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 29000
url: /ru/cpp/aspose.words.saving/saveoptions/
---
## SaveOptions class


Это абстрактный базовый класс для классов, позволяющих пользователю указывать дополнительные параметры при сохранении документа в определённый формат. Чтобы узнать больше, посетите статью документации [Specify Save Options](https://docs.aspose.com/words/cpp/specify-save-options/).

```cpp
class SaveOptions : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| static [CreateSaveOptions](./createsaveoptions/)(Aspose::Words::SaveFormat) | Создаёт объект параметров сохранения класса, подходящего для указанного формата сохранения. |
| static [CreateSaveOptions](./createsaveoptions/)(const System::String\&) | Создаёт объект параметров сохранения класса, подходящего для расширения файла, указанного в данном имени файла. |
| [get_AllowEmbeddingPostScriptFonts](./get_allowembeddingpostscriptfonts/)() const | Получает или задаёт логическое значение, указывающее, разрешено ли встраивание шрифтов с контурами PostScript при встраивании TrueType‑шрифтов в документ при его сохранении. Значение по умолчанию — **false**. |
| [get_CustomTimeZoneInfo](./get_customtimezoneinfo/)() const | Получает или задает пользовательский локальный часовой пояс, используемый для полей даты/времени. |
| [get_DefaultTemplate](./get_defaulttemplate/)() const | Получает или задает путь к шаблону по умолчанию (включая имя файла). Значение по умолчанию для этого свойства — **empty string**. |
| [get_Dml3DEffectsRenderingMode](./get_dml3deffectsrenderingmode/)() const | Получает значение, определяющее, как рендерятся 3D‑эффекты. |
| virtual [get_DmlEffectsRenderingMode](./get_dmleffectsrenderingmode/)() | Получает или задает значение, определяющее, как рендерятся эффекты DrawingML. |
| [get_DmlRenderingMode](./get_dmlrenderingmode/)() const | Получает или задает значение, определяющее, как рендерятся фигуры DrawingML. |
| [get_ExportGeneratorName](./get_exportgeneratorname/)() const | Когда **true**, имя и версия Aspose.Words встраиваются в создаваемые файлы. Значение по умолчанию — **true**. |
| [get_ImlRenderingMode](./get_imlrenderingmode/)() const | Получает или задает значение, определяющее, как отображаются объекты чернил (InkML). |
| [get_MemoryOptimization](./get_memoryoptimization/)() const | Получает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойства **false**. |
| [get_PrettyFormat](./get_prettyformat/)() const | Когда **true**, вывод форматируется красиво, где это применимо. Значение по умолчанию **false**. |
| [get_ProgressCallback](./get_progresscallback/)() const | Вызывается во время сохранения документа и принимает данные о прогрессе сохранения. |
| virtual [get_SaveFormat](./get_saveformat/)() | Указывает формат, в котором будет сохранён документ, если используется этот объект параметров сохранения. |
| [get_TempFolder](./get_tempfolder/)() const | Указывает папку для временных файлов, используемых при сохранении в файл DOC или DOCX. По умолчанию это свойство равно **null**, и временные файлы не используются. |
| [get_UpdateAmbiguousTextFont](./get_updateambiguoustextfont/)() const | Определяет, будут ли атрибуты шрифта изменяться в соответствии с используемым кодом символа. |
| [get_UpdateCreatedTimeProperty](./get_updatecreatedtimeproperty/)() const | Получает или задаёт значение, определяющее, будет ли свойство [CreatedTime](../../aspose.words.properties/builtindocumentproperties/get_createdtime/) обновлено перед сохранением. Значение по умолчанию — **false**;. |
| [get_UpdateFields](./get_updatefields/)() const | Получает значение, определяющее, следует ли обновлять поля определённых типов перед сохранением документа в фиксированный формат страниц. Значение по умолчанию для этого свойства — **true**. |
| [get_UpdateLastPrintedProperty](./get_updatelastprintedproperty/)() const | Получает или задаёт значение, определяющее, будет ли свойство [LastPrinted](../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) обновлено перед сохранением. |
| [get_UpdateLastSavedTimeProperty](./get_updatelastsavedtimeproperty/)() const | Получает или задаёт значение, определяющее, будет ли свойство [LastSavedTime](../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) обновлено перед сохранением. |
| [get_UpdateOleControlImages](./get_updateolecontrolimages/)() const | Получает значение, определяющее, будет ли обновлено изображение представления OLE‑элементов. |
| [get_UseAntiAliasing](./get_useantialiasing/)() const | Получает или задаёт значение, определяющее, использовать ли сглаживание при рендеринге. |
| [get_UseHighQualityRendering](./get_usehighqualityrendering/)() const | Получает или задаёт значение, определяющее, использовать ли высококачественные (т.е. медленные) алгоритмы рендеринга. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllowEmbeddingPostScriptFonts](./set_allowembeddingpostscriptfonts/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_AllowEmbeddingPostScriptFonts](./get_allowembeddingpostscriptfonts/). |
| [set_CustomTimeZoneInfo](./set_customtimezoneinfo/)(const System::SharedPtr\<System::TimeZoneInfo\>\&) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_CustomTimeZoneInfo](./get_customtimezoneinfo/). |
| [set_DefaultTemplate](./set_defaulttemplate/)(const System::String\&) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_DefaultTemplate](./get_defaulttemplate/). |
| [set_Dml3DEffectsRenderingMode](./set_dml3deffectsrenderingmode/)(Aspose::Words::Saving::Dml3DEffectsRenderingMode) | Устанавливает значение, определяющее, как рендерятся 3D‑эффекты. |
| virtual [set_DmlEffectsRenderingMode](./set_dmleffectsrenderingmode/)(Aspose::Words::Saving::DmlEffectsRenderingMode) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_DmlEffectsRenderingMode](./get_dmleffectsrenderingmode/). |
| [set_DmlRenderingMode](./set_dmlrenderingmode/)(Aspose::Words::Saving::DmlRenderingMode) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_DmlRenderingMode](./get_dmlrenderingmode/). |
| [set_ExportGeneratorName](./set_exportgeneratorname/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName](./get_exportgeneratorname/). |
| [set_ImlRenderingMode](./set_imlrenderingmode/)(Aspose::Words::Saving::ImlRenderingMode) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode](./get_imlrenderingmode/). |
| [set_MemoryOptimization](./set_memoryoptimization/)(bool) | Устанавливает значение, определяющее, следует ли выполнять оптимизацию памяти перед сохранением документа. Значение по умолчанию для этого свойства — **false**. |
| [set_PrettyFormat](./set_prettyformat/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_PrettyFormat](./get_prettyformat/). |
| [set_ProgressCallback](./set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Saving::IDocumentSavingCallback\>\&) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_ProgressCallback](./get_progresscallback/). |
| virtual [set_SaveFormat](./set_saveformat/)(Aspose::Words::SaveFormat) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_SaveFormat](./get_saveformat/). |
| [set_TempFolder](./set_tempfolder/)(const System::String\&) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_TempFolder](./get_tempfolder/). |
| [set_UpdateAmbiguousTextFont](./set_updateambiguoustextfont/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_UpdateAmbiguousTextFont](./get_updateambiguoustextfont/). |
| [set_UpdateCreatedTimeProperty](./set_updatecreatedtimeproperty/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty](./get_updatecreatedtimeproperty/). |
| [set_UpdateFields](./set_updatefields/)(bool) | Устанавливает значение, определяющее, следует ли обновлять поля определённых типов перед сохранением документа в фиксированный формат страниц. Значение по умолчанию для этого свойства — **true**. |
| [set_UpdateLastPrintedProperty](./set_updatelastprintedproperty/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty](./get_updatelastprintedproperty/). |
| [set_UpdateLastSavedTimeProperty](./set_updatelastsavedtimeproperty/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty](./get_updatelastsavedtimeproperty/). |
| [set_UpdateOleControlImages](./set_updateolecontrolimages/)(bool) | Устанавливает значение, определяющее, будет ли обновлено изображение представления OLE‑элементов управления. |
| [set_UseAntiAliasing](./set_useantialiasing/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_UseAntiAliasing](./get_useantialiasing/). |
| [set_UseHighQualityRendering](./set_usehighqualityrendering/)(bool) | Сеттер для [Aspose::Words::Saving::SaveOptions::get_UseHighQualityRendering](./get_usehighqualityrendering/). |
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

## См. также

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
