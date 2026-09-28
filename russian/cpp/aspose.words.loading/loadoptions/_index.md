---
title: "Класс Aspose::Words::Loading::LoadOptions"
linktitle: "LoadOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Loading::LoadOptions. Позволяет указать дополнительные параметры (например, пароль или базовый URI) при загрузке документа в объект Document. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.loading/loadoptions/
---
## LoadOptions class


Позволяет указать дополнительные параметры (например, пароль или базовый URI) при загрузке документа в объект [Document](../../aspose.words/document/). Чтобы узнать больше, посетите статью документации [Specify Load Options](https://docs.aspose.com/words/cpp/specify-load-options/).

```cpp
class LoadOptions : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [Equals](./equals/)(System::SharedPtr\<System::Object\>) override | Определяет, равен ли указанный объект по значению текущему объекту. |
| [get_BaseUri](./get_baseuri/)() const | Получает или задает строку, которая будет использоваться для преобразования относительных URI, найденных в документе, в абсолютные URI при необходимости. Может быть **null** или пустой строкой. По умолчанию **null**. |
| [get_ConvertMetafilesToPng](./get_convertmetafilestopng/)() const | Получает или задает, следует ли конвертировать метафайлы ([Wmf](../) или [Emf](../)) в формат изображения [Png](../). |
| [get_ConvertShapeToOfficeMath](./get_convertshapetoofficemath/)() const | Получает или задает, следует ли конвертировать фигуры с EquationXML в объекты Office [Math](../../aspose.words.math/). |
| [get_Encoding](./get_encoding/)() const | Получает или задает кодировку, которая будет использоваться для загрузки HTML, TXT или CHM‑документа, если кодировка не указана внутри документа. Может быть **null**. По умолчанию **null**. |
| [get_FontSettings](./get_fontsettings/)() const | Позволяет задавать параметры шрифтов документа. |
| [get_IgnoreOleData](./get_ignoreoledata/)() const | Указывает, следует ли игнорировать данные OLE. |
| [get_LanguagePreferences](./get_languagepreferences/)() const | Получает предпочтения языка, которые будут использоваться при загрузке документа. |
| [get_LoadFormat](./get_loadformat/)() const | Указывает формат загружаемого документа. По умолчанию — [Auto](../../aspose.words/loadformat/). |
| [get_MswVersion](./get_mswversion/)() const | Позволяет указать, что процесс загрузки документа должен соответствовать определённой версии MS Word. Значение по умолчанию — [Word2019](../../aspose.words.settings/mswordversion/) |
| [get_Password](./get_password/)() const | Получает или задает пароль для открытия зашифрованного документа. Может быть **null** или пустой строкой. По умолчанию — **null**. |
| [get_PreserveIncludePictureField](./get_preserveincludepicturefield/)() const | Получает или задает, сохранять ли поле INCLUDEPICTURE при чтении форматов Microsoft Word. Значение по умолчанию — **false**. |
| [get_ProgressCallback](./get_progresscallback/)() const | Вызывается во время загрузки документа и принимает данные о прогрессе загрузки. |
| [get_RecoveryMode](./get_recoverymode/)() const | Определяет, как следует обрабатывать документ при возникновении ошибок во время загрузки. Используйте это свойство, чтобы указать, должна ли система пытаться восстановить документ или следовать другому определённому поведению. Значение по умолчанию — [TryRecover](../documentrecoverymode/). |
| [get_ResourceLoadingCallback](./get_resourceloadingcallback/)() const | Позволяет управлять тем, как внешние ресурсы (изображения, таблицы стилей) загружаются при импорте документа из HTML, MHTML. |
| [get_TempFolder](./get_tempfolder/)() const | Позволяет использовать временные файлы при чтении документа. По умолчанию это свойство равно **null**, и временные файлы не используются. |
| [get_UpdateDirtyFields](./get_updatedirtyfields/)() const | Указывает, следует ли обновлять поля с атрибутом **dirty**. |
| [get_UseSystemLcid](./get_usesystemlcid/)() const | Получает или задает, использовать ли значение LCID, полученное из реестра Windows, для определения полей страницы по умолчанию. |
| [get_WarningCallback](./get_warningcallback/)() const | Вызывается во время операции загрузки, когда обнаружена проблема, которая может привести к потере точности данных или форматирования. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LoadOptions](./loadoptions/)() | Инициализирует новый экземпляр этого класса со значениями по умолчанию. |
| [LoadOptions](./loadoptions/)(const System::String\&) | Сокращение для инициализации нового экземпляра этого класса с указанным паролем для загрузки зашифрованного документа. |
| [LoadOptions](./loadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | Сокращение для инициализации нового экземпляра этого класса со свойствами, установленными в указанные значения. |
| [set_BaseUri](./set_baseuri/)(const System::String\&) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_BaseUri](./get_baseuri/). |
| [set_ConvertMetafilesToPng](./set_convertmetafilestopng/)(bool) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng](./get_convertmetafilestopng/). |
| [set_ConvertShapeToOfficeMath](./set_convertshapetoofficemath/)(bool) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath](./get_convertshapetoofficemath/). |
| [set_Encoding](./set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_Encoding](./get_encoding/). |
| [set_FontSettings](./set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_FontSettings](./get_fontsettings/). |
| [set_IgnoreOleData](./set_ignoreoledata/)(bool) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_IgnoreOleData](./get_ignoreoledata/). |
| [set_LoadFormat](./set_loadformat/)(Aspose::Words::LoadFormat) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_LoadFormat](./get_loadformat/). |
| [set_MswVersion](./set_mswversion/)(Aspose::Words::Settings::MsWordVersion) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_MswVersion](./get_mswversion/). |
| [set_Password](./set_password/)(const System::String\&) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_Password](./get_password/). |
| [set_PreserveIncludePictureField](./set_preserveincludepicturefield/)(bool) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField](./get_preserveincludepicturefield/). |
| [set_ProgressCallback](./set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Loading::IDocumentLoadingCallback\>\&) | Вызывается во время загрузки документа и принимает данные о прогрессе загрузки. |
| [set_RecoveryMode](./set_recoverymode/)(Aspose::Words::Loading::DocumentRecoveryMode) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_RecoveryMode](./get_recoverymode/). |
| [set_ResourceLoadingCallback](./set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Позволяет управлять тем, как внешние ресурсы (изображения, таблицы стилей) загружаются при импорте документа из HTML, MHTML. |
| [set_TempFolder](./set_tempfolder/)(const System::String\&) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_TempFolder](./get_tempfolder/). |
| [set_UpdateDirtyFields](./set_updatedirtyfields/)(bool) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields](./get_updatedirtyfields/). |
| [set_UseSystemLcid](./set_usesystemlcid/)(bool) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_UseSystemLcid](./get_usesystemlcid/). |
| [set_WarningCallback](./set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Вызывается во время операции загрузки, когда обнаружена проблема, которая может привести к потере точности данных или форматирования. |
| static [Type](./type/)() |  |

## Примеры



Показывает, как загрузить зашифрованный документ Microsoft Word.
```cpp
System::SharedPtr<Aspose::Words::Document> doc;

// Aspose.Words генерирует исключение, если попытаться открыть зашифрованный документ без пароля.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx");
})(), Aspose::Words::IncorrectPasswordException);

// При загрузке такого документа пароль передаётся конструктору документа с помощью объекта LoadOptions.
auto options = System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"docPassword");

// Существует два способа загрузить зашифрованный документ с объектом LoadOptions.
// 1 -  Загрузить документ из локальной файловой системы по имени файла:
doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Encrypted.docx", options);

// 2 -  Загрузить документ из потока:
{
    System::SharedPtr<System::IO::Stream> stream = System::IO::File::OpenRead(get_MyDir() + u"Encrypted.docx");
    doc = System::MakeObject<Aspose::Words::Document>(stream, options);
}
```

## См. также

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
