---
title: "Aspose::Words::Fields::FieldOptions класс"
linktitle: "FieldOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::FieldOptions класс. Представляет параметры для управления обработкой полей в документе. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 77000
url: /ru/cpp/aspose.words.fields/fieldoptions/
---
## FieldOptions class


Представляет параметры для управления обработкой полей в документе. Чтобы узнать больше, посетите статью документации [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldOptions : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_BarcodeGenerator](./get_barcodegenerator/)() const | Получает или задает пользовательский генератор штрих‑кода. |
| [get_BibliographyStylesProvider](./get_bibliographystylesprovider/)() const | Получает поставщика, который возвращает стиль библиографии для полей [FieldBibliography](../fieldbibliography/) и [FieldCitation](../fieldcitation/). |
| [get_BuiltInTemplatesPaths](./get_builtintemplatespaths/)() const | Получает или задает пути к встроенным шаблонам MS Word. |
| [get_ComparisonExpressionEvaluator](./get_comparisonexpressionevaluator/)() const | Получает оценщик выражений сравнения полей. |
| [get_CurrentUser](./get_currentuser/)() const | Получает или задает информацию о текущем пользователе. |
| [get_CustomTocStyleSeparator](./get_customtocstyleseparator/)() const | Получает пользовательский разделитель стилей для переключателя \t в поле [FieldToc](../fieldtoc/). |
| [get_DefaultDocumentAuthor](./get_defaultdocumentauthor/)() const | Получает или задает имя автора документа по умолчанию. Если имя автора уже указано во встроенных свойствах документа, эта опция не учитывается. |
| [get_FieldDatabaseProvider](./get_fielddatabaseprovider/)() const | Получает поставщика, который возвращает результат запроса для поля [FieldDatabase](../fielddatabase/). |
| [get_FieldIndexFormat](./get_fieldindexformat/)() | Получает или задает [FieldIndexFormat](./get_fieldindexformat/), представляющий форматирование полей [FieldIndex](../fieldindex/) в документе. |
| [get_FieldUpdateCultureProvider](./get_fieldupdatecultureprovider/)() const | Получает или задает поставщика, который возвращает объект культуры, специфичный для каждого отдельного поля. |
| [get_FieldUpdateCultureSource](./get_fieldupdateculturesource/)() const | Указывает, какую культуру использовать для форматирования результата поля. |
| [get_FieldUpdatingCallback](./get_fieldupdatingcallback/)() const | Получает реализацию [IFieldUpdatingCallback](../ifieldupdatingcallback/). |
| [get_FieldUpdatingProgressCallback](./get_fieldupdatingprogresscallback/)() const | Получает реализацию [IFieldUpdatingProgressCallback](../ifieldupdatingprogresscallback/). |
| [get_FileName](./get_filename/)() const | Получает или задает имя файла документа. |
| [get_IsBidiTextSupportedOnUpdate](./get_isbiditextsupportedonupdate/)() const | Получает или задает значение, указывающее, поддерживается ли полностью двунаправленный текст во время обновления поля. |
| [get_LegacyNumberFormat](./get_legacynumberformat/)() const | Получает или задает значение, указывающее, включён ли устаревший (ранний, чем AW 13.10) числовой формат для полей. |
| [get_PreProcessCulture](./get_preprocessculture/)() const | Получает или задает культуру для предварительной обработки значений полей. |
| [get_ResultFormatter](./get_resultformatter/)() const | Позволяет управлять тем, как форматируется результат поля. |
| [get_TemplateName](./get_templatename/)() const | Получает или задает имя файла шаблона, используемого документом. |
| [get_ToaCategories](./get_toacategories/)() const | Получает или задает таблицу категорий авторитетов. |
| [get_UseInvariantCultureNumberFormat](./get_useinvariantculturenumberformat/)() const | Получает или задает значение, указывающее, разбирается ли числовой формат с использованием инвариантной культуры. |
| [get_UserPromptRespondent](./get_userpromptrespondent/)() const | Получает или задает ответчика на запросы пользователя во время обновления поля. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BarcodeGenerator](./set_barcodegenerator/)(const System::SharedPtr\<Aspose::Words::Fields::IBarcodeGenerator\>\&) | Получает или задает пользовательский генератор штрих‑кода. |
| [set_BibliographyStylesProvider](./set_bibliographystylesprovider/)(const System::SharedPtr\<Aspose::Words::Fields::IBibliographyStylesProvider\>\&) | Задаёт поставщика, который возвращает стиль библиографии для полей [FieldBibliography](../fieldbibliography/) и [FieldCitation](../fieldcitation/). |
| [set_BuiltInTemplatesPaths](./set_builtintemplatespaths/)(const System::ArrayPtr\<System::String\>\&) | Сеттер для [Aspose::Words::Fields::FieldOptions::get_BuiltInTemplatesPaths](./get_builtintemplatespaths/). |
| [set_ComparisonExpressionEvaluator](./set_comparisonexpressionevaluator/)(const System::SharedPtr\<Aspose::Words::Fields::IComparisonExpressionEvaluator\>\&) | Задаёт оценщик выражений сравнения полей. |
| [set_CurrentUser](./set_currentuser/)(const System::SharedPtr\<Aspose::Words::Fields::UserInformation\>\&) | Установщик для [Aspose::Words::Fields::FieldOptions::get_CurrentUser](./get_currentuser/). |
| [set_CustomTocStyleSeparator](./set_customtocstyleseparator/)(const System::String\&) | Устанавливает пользовательский разделитель стилей для переключателя \t в поле [FieldToc](../fieldtoc/). |
| [set_DefaultDocumentAuthor](./set_defaultdocumentauthor/)(const System::String\&) | Установщик для [Aspose::Words::Fields::FieldOptions::get_DefaultDocumentAuthor](./get_defaultdocumentauthor/). |
| [set_FieldDatabaseProvider](./set_fielddatabaseprovider/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldDatabaseProvider\>\&) | Устанавливает поставщика, который возвращает результат запроса для поля [FieldDatabase](../fielddatabase/). |
| [set_FieldIndexFormat](./set_fieldindexformat/)(Aspose::Words::Fields::FieldIndexFormat) | Установщик для [Aspose::Words::Fields::FieldOptions::get_FieldIndexFormat](./get_fieldindexformat/). |
| [set_FieldUpdateCultureProvider](./set_fieldupdatecultureprovider/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUpdateCultureProvider\>\&) | Установщик для [Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureProvider](./get_fieldupdatecultureprovider/). |
| [set_FieldUpdateCultureSource](./set_fieldupdateculturesource/)(Aspose::Words::Fields::FieldUpdateCultureSource) | Установщик для [Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureSource](./get_fieldupdateculturesource/). |
| [set_FieldUpdatingCallback](./set_fieldupdatingcallback/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUpdatingCallback\>\&) | Устанавливает реализацию [IFieldUpdatingCallback](../ifieldupdatingcallback/). |
| [set_FieldUpdatingProgressCallback](./set_fieldupdatingprogresscallback/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUpdatingProgressCallback\>\&) | Устанавливает реализацию [IFieldUpdatingProgressCallback](../ifieldupdatingprogresscallback/). |
| [set_FileName](./set_filename/)(const System::String\&) | Установщик для [Aspose::Words::Fields::FieldOptions::get_FileName](./get_filename/). |
| [set_IsBidiTextSupportedOnUpdate](./set_isbiditextsupportedonupdate/)(bool) | Установщик для [Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate](./get_isbiditextsupportedonupdate/). |
| [set_LegacyNumberFormat](./set_legacynumberformat/)(bool) | Установщик для [Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat](./get_legacynumberformat/). |
| [set_PreProcessCulture](./set_preprocessculture/)(const System::SharedPtr\<System::Globalization::CultureInfo\>\&) | Установщик для [Aspose::Words::Fields::FieldOptions::get_PreProcessCulture](./get_preprocessculture/). |
| [set_ResultFormatter](./set_resultformatter/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldResultFormatter\>\&) | Позволяет управлять тем, как форматируется результат поля. |
| [set_TemplateName](./set_templatename/)(const System::String\&) | Установщик для [Aspose::Words::Fields::FieldOptions::get_TemplateName](./get_templatename/). |
| [set_ToaCategories](./set_toacategories/)(const System::SharedPtr\<Aspose::Words::Fields::ToaCategories\>\&) | Установщик для [Aspose::Words::Fields::FieldOptions::get_ToaCategories](./get_toacategories/). |
| [set_UseInvariantCultureNumberFormat](./set_useinvariantculturenumberformat/)(bool) | Установщик для [Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat](./get_useinvariantculturenumberformat/). |
| [set_UserPromptRespondent](./set_userpromptrespondent/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUserPromptRespondent\>\&) | Установщик для [Aspose::Words::Fields::FieldOptions::get_UserPromptRespondent](./get_userpromptrespondent/). |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
