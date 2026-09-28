---
title: "Aspose::Words::Loading::ChmLoadOptions class"
linktitle: "ChmLoadOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Loading::ChmLoadOptions class. Позволяет указать дополнительные параметры при загрузке CHM‑документа в объект Document. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 1000
url: /ru/cpp/aspose.words.loading/chmloadoptions/
---
## ChmLoadOptions class


Позволяет указать дополнительные параметры при загрузке CHM‑документа в объект [Document](../../aspose.words/document/). Чтобы узнать больше, посетите статью документации [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/).

```cpp
class ChmLoadOptions : public Aspose::Words::Loading::LoadOptions
```

## Методы

| Метод | Описание |
| --- | --- |
| [ChmLoadOptions](./chmloadoptions/)() | Инициализирует новый экземпляр этого класса со значениями по умолчанию. |
| [Equals](../loadoptions/equals/)(System::SharedPtr\<System::Object\>) override | Определяет, равен ли указанный объект по значению текущему объекту. |
| [get_BaseUri](../loadoptions/get_baseuri/)() const | Получает или задает строку, которая будет использоваться для преобразования относительных URI, найденных в документе, в абсолютные URI при необходимости. Может быть **null** или пустой строкой. По умолчанию **null**. |
| [get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/)() const | Получает или задает, следует ли конвертировать метафайлы ([Wmf](../) или [Emf](../)) в формат изображения [Png](../). |
| [get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/)() const | Получает или задает, следует ли конвертировать фигуры с EquationXML в объекты Office [Math](../../aspose.words.math/). |
| [get_Encoding](../loadoptions/get_encoding/)() const | Получает или задает кодировку, которая будет использоваться для загрузки HTML, TXT или CHM‑документа, если кодировка не указана внутри документа. Может быть **null**. По умолчанию **null**. |
| [get_FontSettings](../loadoptions/get_fontsettings/)() const | Позволяет задавать параметры шрифтов документа. |
| [get_IgnoreOleData](../loadoptions/get_ignoreoledata/)() const | Указывает, следует ли игнорировать данные OLE. |
| [get_LanguagePreferences](../loadoptions/get_languagepreferences/)() const | Получает предпочтения языка, которые будут использоваться при загрузке документа. |
| [get_LoadFormat](../loadoptions/get_loadformat/)() const | Указывает формат загружаемого документа. По умолчанию — [Auto](../../aspose.words/loadformat/). |
| [get_MswVersion](../loadoptions/get_mswversion/)() const | Позволяет указать, что процесс загрузки документа должен соответствовать определённой версии MS Word. Значение по умолчанию — [Word2019](../../aspose.words.settings/mswordversion/) |
| [get_OriginalFileName](./get_originalfilename/)() const | Имя CHM‑файла. Значение по умолчанию — **null**. |
| [get_Password](../loadoptions/get_password/)() const | Получает или задает пароль для открытия зашифрованного документа. Может быть **null** или пустой строкой. По умолчанию — **null**. |
| [get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/)() const | Получает или задает, сохранять ли поле INCLUDEPICTURE при чтении форматов Microsoft Word. Значение по умолчанию — **false**. |
| [get_ProgressCallback](../loadoptions/get_progresscallback/)() const | Вызывается во время загрузки документа и принимает данные о прогрессе загрузки. |
| [get_RecoveryMode](../loadoptions/get_recoverymode/)() const | Определяет, как следует обрабатывать документ при возникновении ошибок во время загрузки. Используйте это свойство, чтобы указать, должна ли система пытаться восстановить документ или следовать другому определённому поведению. Значение по умолчанию — [TryRecover](../documentrecoverymode/). |
| [get_ResourceLoadingCallback](../loadoptions/get_resourceloadingcallback/)() const | Позволяет управлять тем, как внешние ресурсы (изображения, таблицы стилей) загружаются при импорте документа из HTML, MHTML. |
| [get_TempFolder](../loadoptions/get_tempfolder/)() const | Позволяет использовать временные файлы при чтении документа. По умолчанию это свойство равно **null**, и временные файлы не используются. |
| [get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/)() const | Указывает, следует ли обновлять поля с атрибутом **dirty**. |
| [get_UseSystemLcid](../loadoptions/get_usesystemlcid/)() const | Получает или задает, использовать ли значение LCID, полученное из реестра Windows, для определения полей страницы по умолчанию. |
| [get_WarningCallback](../loadoptions/get_warningcallback/)() const | Вызывается во время операции загрузки, когда обнаружена проблема, которая может привести к потере точности данных или форматирования. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LoadOptions](../loadoptions/loadoptions/)() | Инициализирует новый экземпляр этого класса со значениями по умолчанию. |
| [LoadOptions](../loadoptions/loadoptions/)(const System::String\&) | Сокращение для инициализации нового экземпляра этого класса с указанным паролем для загрузки зашифрованного документа. |
| [LoadOptions](../loadoptions/loadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | Сокращение для инициализации нового экземпляра этого класса со свойствами, установленными в указанные значения. |
| [set_BaseUri](../loadoptions/set_baseuri/)(const System::String\&) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_BaseUri](../loadoptions/get_baseuri/). |
| [set_ConvertMetafilesToPng](../loadoptions/set_convertmetafilestopng/)(bool) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/). |
| [set_ConvertShapeToOfficeMath](../loadoptions/set_convertshapetoofficemath/)(bool) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/). |
| [set_Encoding](../loadoptions/set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_Encoding](../loadoptions/get_encoding/). |
| [set_FontSettings](../loadoptions/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_FontSettings](../loadoptions/get_fontsettings/). |
| [set_IgnoreOleData](../loadoptions/set_ignoreoledata/)(bool) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_IgnoreOleData](../loadoptions/get_ignoreoledata/). |
| [set_LoadFormat](../loadoptions/set_loadformat/)(Aspose::Words::LoadFormat) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_LoadFormat](../loadoptions/get_loadformat/). |
| [set_MswVersion](../loadoptions/set_mswversion/)(Aspose::Words::Settings::MsWordVersion) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_MswVersion](../loadoptions/get_mswversion/). |
| [set_OriginalFileName](./set_originalfilename/)(const System::String\&) | Сеттер для [Aspose::Words::Loading::ChmLoadOptions::get_OriginalFileName](./get_originalfilename/). |
| [set_Password](../loadoptions/set_password/)(const System::String\&) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_Password](../loadoptions/get_password/). |
| [set_PreserveIncludePictureField](../loadoptions/set_preserveincludepicturefield/)(bool) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/). |
| [set_ProgressCallback](../loadoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Loading::IDocumentLoadingCallback\>\&) | Вызывается во время загрузки документа и принимает данные о прогрессе загрузки. |
| [set_RecoveryMode](../loadoptions/set_recoverymode/)(Aspose::Words::Loading::DocumentRecoveryMode) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_RecoveryMode](../loadoptions/get_recoverymode/). |
| [set_ResourceLoadingCallback](../loadoptions/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Позволяет управлять тем, как внешние ресурсы (изображения, таблицы стилей) загружаются при импорте документа из HTML, MHTML. |
| [set_TempFolder](../loadoptions/set_tempfolder/)(const System::String\&) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_TempFolder](../loadoptions/get_tempfolder/). |
| [set_UpdateDirtyFields](../loadoptions/set_updatedirtyfields/)(bool) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/). |
| [set_UseSystemLcid](../loadoptions/set_usesystemlcid/)(bool) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_UseSystemLcid](../loadoptions/get_usesystemlcid/). |
| [set_WarningCallback](../loadoptions/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Вызывается во время операции загрузки, когда обнаружена проблема, которая может привести к потере точности данных или форматирования. |
| static [Type](./type/)() |  |

## Примеры



Показывает, как разрешать URL‑адреса вида "ms-its:myfile.chm::/index.htm".
```cpp
// Наш документ содержит URL-адреса, такие как "ms-its:amhelp.chm::....htm", но у него другое имя,
// поэтому ссылки на файлы не работают после сохранения в HTML.
// Нужно задать исходное имя файла в 'ChmLoadOptions', чтобы избежать этого поведения.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::ChmLoadOptions>();
loadOptions->set_OriginalFileName(u"amhelp.chm");

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::IO::File::ReadAllBytes(get_MyDir() + u"Document with ms-its links.chm")), loadOptions);

doc->Save(get_ArtifactsDir() + u"ExChmLoadOptions.OriginalFileName.html");
```

## См. также

* Class [LoadOptions](../loadoptions/)
* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
