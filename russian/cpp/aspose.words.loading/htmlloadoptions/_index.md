---
title: "Aspose::Words::Loading::HtmlLoadOptions class"
linktitle: "HtmlLoadOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Loading::HtmlLoadOptions class. Позволяет указать дополнительные параметры при загрузке HTML‑документа в объект Document. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.loading/htmlloadoptions/
---
## HtmlLoadOptions class


Позволяет указать дополнительные параметры при загрузке HTML‑документа в объект [Документ](../../aspose.words/document/). Чтобы узнать больше, посетите статью документации [Указать параметры загрузки](https://docs.aspose.com/words/cpp/specify-load-options/).

```cpp
class HtmlLoadOptions : public Aspose::Words::Loading::LoadOptions
```

## Методы

| Метод | Описание |
| --- | --- |
| [Equals](../loadoptions/equals/)(System::SharedPtr\<System::Object\>) override | Определяет, равен ли указанный объект по значению текущему объекту. |
| [get_BaseUri](../loadoptions/get_baseuri/)() const | Получает или задает строку, которая будет использоваться для преобразования относительных URI, найденных в документе, в абсолютные URI при необходимости. Может быть **null** или пустой строкой. По умолчанию **null**. |
| [get_BlockImportMode](./get_blockimportmode/)() const | Получает или задает значение, указывающее, как свойства блочных элементов импортируются. Значение по умолчанию — [Объединить](../blockimportmode/). |
| [get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/)() const | Получает или задает, следует ли конвертировать метафайлы ([Wmf](../) или [Emf](../)) в формат изображения [Png](../). |
| [get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/)() const | Получает или задает, следует ли конвертировать фигуры с EquationXML в объекты Office [Math](../../aspose.words.math/). |
| [get_ConvertSvgToEmf](./get_convertsvgtoemf/)() const | Получает или задает значение, указывающее, следует ли конвертировать загруженные SVG‑изображения в формат EMF. Значение по умолчанию — **false**, и, если возможно, загруженные SVG‑изображения сохраняются без изменения. |
| [get_Encoding](../loadoptions/get_encoding/)() const | Получает или задает кодировку, которая будет использоваться для загрузки HTML, TXT или CHM‑документа, если кодировка не указана внутри документа. Может быть **null**. По умолчанию **null**. |
| [get_FontSettings](../loadoptions/get_fontsettings/)() const | Позволяет задавать параметры шрифтов документа. |
| [get_IgnoreNoscriptElements](./get_ignorenoscriptelements/)() const | Получает или задает значение, указывающее, следует ли игнорировать элементы HTML <noscript>. Значение по умолчанию — **false**. |
| [get_IgnoreOleData](../loadoptions/get_ignoreoledata/)() const | Указывает, следует ли игнорировать данные OLE. |
| [get_LanguagePreferences](../loadoptions/get_languagepreferences/)() const | Получает предпочтения языка, которые будут использоваться при загрузке документа. |
| [get_LoadFormat](../loadoptions/get_loadformat/)() const | Указывает формат загружаемого документа. По умолчанию — [Auto](../../aspose.words/loadformat/). |
| [get_MswVersion](../loadoptions/get_mswversion/)() const | Позволяет указать, что процесс загрузки документа должен соответствовать определённой версии MS Word. Значение по умолчанию — [Word2019](../../aspose.words.settings/mswordversion/) |
| [get_Password](../loadoptions/get_password/)() const | Получает или задает пароль для открытия зашифрованного документа. Может быть **null** или пустой строкой. По умолчанию — **null**. |
| [get_PreferredControlType](./get_preferredcontroltype/)() const | Получает или задает предпочтительный тип узлов документа, которые будут представлять импортированные элементы <input> и <select>. Значение по умолчанию — [FormField](../htmlcontroltype/). |
| [get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/)() const | Получает или задает, сохранять ли поле INCLUDEPICTURE при чтении форматов Microsoft Word. Значение по умолчанию — **false**. |
| [get_ProgressCallback](../loadoptions/get_progresscallback/)() const | Вызывается во время загрузки документа и принимает данные о прогрессе загрузки. |
| [get_RecoveryMode](../loadoptions/get_recoverymode/)() const | Определяет, как следует обрабатывать документ при возникновении ошибок во время загрузки. Используйте это свойство, чтобы указать, должна ли система пытаться восстановить документ или следовать другому определённому поведению. Значение по умолчанию — [TryRecover](../documentrecoverymode/). |
| [get_ResourceLoadingCallback](../loadoptions/get_resourceloadingcallback/)() const | Позволяет управлять тем, как внешние ресурсы (изображения, таблицы стилей) загружаются при импорте документа из HTML, MHTML. |
| [get_SupportFontFaceRules](./get_supportfontfacerules/)() const | Получает или задает значение, указывающее, поддерживать ли правила @font-face и загружать объявленные шрифты. Значение по умолчанию — **false**. |
| [get_SupportVml](./get_supportvml/)() const | Получает или задает значение, указывающее, поддерживать ли изображения VML. |
| [get_TempFolder](../loadoptions/get_tempfolder/)() const | Позволяет использовать временные файлы при чтении документа. По умолчанию это свойство равно **null**, и временные файлы не используются. |
| [get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/)() const | Указывает, следует ли обновлять поля с атрибутом **dirty**. |
| [get_UseSystemLcid](../loadoptions/get_usesystemlcid/)() const | Получает или задает, использовать ли значение LCID, полученное из реестра Windows, для определения полей страницы по умолчанию. |
| [get_WarningCallback](../loadoptions/get_warningcallback/)() const | Вызывается во время операции загрузки, когда обнаружена проблема, которая может привести к потере точности данных или форматирования. |
| [get_WebRequestTimeout](./get_webrequesttimeout/)() const | Количество миллисекунд ожидания до истечения времени запроса. Значение по умолчанию — 100000 миллисекунд (100 секунд). |
| [GetType](./gettype/)() const override |  |
| [HtmlLoadOptions](./htmlloadoptions/)() | Инициализирует новый экземпляр этого класса со значениями по умолчанию. |
| [HtmlLoadOptions](./htmlloadoptions/)(const System::String\&) | Сокращение для инициализации нового экземпляра этого класса с указанным паролем для загрузки зашифрованного документа. |
| [HtmlLoadOptions](./htmlloadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | Сокращение для инициализации нового экземпляра этого класса со свойствами, установленными в указанные значения. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [LoadOptions](../loadoptions/loadoptions/)() | Инициализирует новый экземпляр этого класса со значениями по умолчанию. |
| [LoadOptions](../loadoptions/loadoptions/)(const System::String\&) | Сокращение для инициализации нового экземпляра этого класса с указанным паролем для загрузки зашифрованного документа. |
| [LoadOptions](../loadoptions/loadoptions/)(Aspose::Words::LoadFormat, const System::String\&, const System::String\&) | Сокращение для инициализации нового экземпляра этого класса со свойствами, установленными в указанные значения. |
| [set_BaseUri](../loadoptions/set_baseuri/)(const System::String\&) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_BaseUri](../loadoptions/get_baseuri/). |
| [set_BlockImportMode](./set_blockimportmode/)(Aspose::Words::Loading::BlockImportMode) | Сеттер для [Aspose::Words::Loading::HtmlLoadOptions::get_BlockImportMode](./get_blockimportmode/). |
| [set_ConvertMetafilesToPng](../loadoptions/set_convertmetafilestopng/)(bool) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng](../loadoptions/get_convertmetafilestopng/). |
| [set_ConvertShapeToOfficeMath](../loadoptions/set_convertshapetoofficemath/)(bool) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_ConvertShapeToOfficeMath](../loadoptions/get_convertshapetoofficemath/). |
| [set_ConvertSvgToEmf](./set_convertsvgtoemf/)(bool) | Сеттер для [Aspose::Words::Loading::HtmlLoadOptions::get_ConvertSvgToEmf](./get_convertsvgtoemf/). |
| [set_Encoding](../loadoptions/set_encoding/)(const System::SharedPtr\<System::Text::Encoding\>\&) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_Encoding](../loadoptions/get_encoding/). |
| [set_FontSettings](../loadoptions/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_FontSettings](../loadoptions/get_fontsettings/). |
| [set_IgnoreNoscriptElements](./set_ignorenoscriptelements/)(bool) | Сеттер для [Aspose::Words::Loading::HtmlLoadOptions::get_IgnoreNoscriptElements](./get_ignorenoscriptelements/). |
| [set_IgnoreOleData](../loadoptions/set_ignoreoledata/)(bool) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_IgnoreOleData](../loadoptions/get_ignoreoledata/). |
| [set_LoadFormat](../loadoptions/set_loadformat/)(Aspose::Words::LoadFormat) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_LoadFormat](../loadoptions/get_loadformat/). |
| [set_MswVersion](../loadoptions/set_mswversion/)(Aspose::Words::Settings::MsWordVersion) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_MswVersion](../loadoptions/get_mswversion/). |
| [set_Password](../loadoptions/set_password/)(const System::String\&) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_Password](../loadoptions/get_password/). |
| [set_PreferredControlType](./set_preferredcontroltype/)(Aspose::Words::Loading::HtmlControlType) | Сеттер для [Aspose::Words::Loading::HtmlLoadOptions::get_PreferredControlType](./get_preferredcontroltype/). |
| [set_PreserveIncludePictureField](../loadoptions/set_preserveincludepicturefield/)(bool) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_PreserveIncludePictureField](../loadoptions/get_preserveincludepicturefield/). |
| [set_ProgressCallback](../loadoptions/set_progresscallback/)(const System::SharedPtr\<Aspose::Words::Loading::IDocumentLoadingCallback\>\&) | Вызывается во время загрузки документа и принимает данные о прогрессе загрузки. |
| [set_RecoveryMode](../loadoptions/set_recoverymode/)(Aspose::Words::Loading::DocumentRecoveryMode) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_RecoveryMode](../loadoptions/get_recoverymode/). |
| [set_ResourceLoadingCallback](../loadoptions/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Позволяет управлять тем, как внешние ресурсы (изображения, таблицы стилей) загружаются при импорте документа из HTML, MHTML. |
| [set_SupportFontFaceRules](./set_supportfontfacerules/)(bool) | Сеттер для [Aspose::Words::Loading::HtmlLoadOptions::get_SupportFontFaceRules](./get_supportfontfacerules/). |
| [set_SupportVml](./set_supportvml/)(bool) | Сеттер для [Aspose::Words::Loading::HtmlLoadOptions::get_SupportVml](./get_supportvml/). |
| [set_TempFolder](../loadoptions/set_tempfolder/)(const System::String\&) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_TempFolder](../loadoptions/get_tempfolder/). |
| [set_UpdateDirtyFields](../loadoptions/set_updatedirtyfields/)(bool) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_UpdateDirtyFields](../loadoptions/get_updatedirtyfields/). |
| [set_UseSystemLcid](../loadoptions/set_usesystemlcid/)(bool) | Сеттер для [Aspose::Words::Loading::LoadOptions::get_UseSystemLcid](../loadoptions/get_usesystemlcid/). |
| [set_WarningCallback](../loadoptions/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Вызывается во время операции загрузки, когда обнаружена проблема, которая может привести к потере точности данных или форматирования. |
| [set_WebRequestTimeout](./set_webrequesttimeout/)(int32_t) | Количество миллисекунд ожидания до истечения времени запроса. Значение по умолчанию — 100000 миллисекунд (100 секунд). |
| static [Type](./type/)() |  |

## Примеры



Показывает, как поддерживать условные комментарии при загрузке HTML‑документа.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();

// Если значение истинно, то мы учитываем код VML при разборе загруженного документа.
loadOptions->set_SupportVml(supportVml);

// Этот документ содержит JPEG‑изображение внутри тегов "<!--[if gte vml 1]>",
// и другое PNG‑изображение внутри тегов "<![if !vml]>".
// Если установить флаг "SupportVml" в значение "true", то Aspose.Words загрузит JPEG.
// Если установить этот флаг в значение "false", то Aspose.Words загрузит только PNG.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"VML conditional.htm", loadOptions);

if (supportVml)
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Jpeg, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
else
{
    ASSERT_EQ(Aspose::Words::Drawing::ImageType::Png, (System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true)))->get_ImageData()->get_ImageType());
}
```

## См. также

* Class [LoadOptions](../loadoptions/)
* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
