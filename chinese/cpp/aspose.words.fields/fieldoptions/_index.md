---
title: "Aspose::Words::Fields::FieldOptions 类"
linktitle: "FieldOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldOptions 类。表示用于控制文档中字段处理的选项。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 77000
url: /zh/cpp/aspose.words.fields/fieldoptions/
---
## FieldOptions class


表示用于控制文档中字段处理的选项。要了解更多，请访问 [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) 文档文章。

```cpp
class FieldOptions : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_BarcodeGenerator](./get_barcodegenerator/)() const | 获取或设置自定义条形码生成器。 |
| [get_BibliographyStylesProvider](./get_bibliographystylesprovider/)() const | 获取一个提供程序，为 [FieldBibliography](../fieldbibliography/) 和 [FieldCitation](../fieldcitation/) 字段返回参考文献样式。 |
| [get_BuiltInTemplatesPaths](./get_builtintemplatespaths/)() const | 获取或设置 MS Word 内置模板的路径。 |
| [get_ComparisonExpressionEvaluator](./get_comparisonexpressionevaluator/)() const | 获取字段比较表达式求值器。 |
| [get_CurrentUser](./get_currentuser/)() const | 获取或设置当前用户信息。 |
| [get_CustomTocStyleSeparator](./get_customtocstyleseparator/)() const | 获取 [FieldToc](../fieldtoc/) 字段中 \\t 开关的自定义样式分隔符。 |
| [get_DefaultDocumentAuthor](./get_defaultdocumentauthor/)() const | 获取或设置默认文档作者姓名。如果作者姓名已在内置文档属性中指定，则此选项不予考虑。 |
| [get_FieldDatabaseProvider](./get_fielddatabaseprovider/)() const | 获取一个提供程序，为 [FieldDatabase](../fielddatabase/) 字段返回查询结果。 |
| [get_FieldIndexFormat](./get_fieldindexformat/)() | 获取或设置一个 [FieldIndexFormat](./get_fieldindexformat/)，表示文档中 [FieldIndex](../fieldindex/) 字段的格式。 |
| [get_FieldUpdateCultureProvider](./get_fieldupdatecultureprovider/)() const | 获取或设置一个提供程序，为每个特定字段返回特定的文化对象。 |
| [get_FieldUpdateCultureSource](./get_fieldupdateculturesource/)() const | 指定用于格式化字段结果的文化。 |
| [get_FieldUpdatingCallback](./get_fieldupdatingcallback/)() const | 获取 [IFieldUpdatingCallback](../ifieldupdatingcallback/) 实现。 |
| [get_FieldUpdatingProgressCallback](./get_fieldupdatingprogresscallback/)() const | 获取 [IFieldUpdatingProgressCallback](../ifieldupdatingprogresscallback/) 实现。 |
| [get_FileName](./get_filename/)() const | 获取或设置文档的文件名。 |
| [get_IsBidiTextSupportedOnUpdate](./get_isbiditextsupportedonupdate/)() const | 获取或设置指示在字段更新期间是否完全支持双向文本的值。 |
| [get_LegacyNumberFormat](./get_legacynumberformat/)() const | 获取或设置指示是否启用旧版（早于 AW 13.10）字段数字格式的值。 |
| [get_PreProcessCulture](./get_preprocessculture/)() const | 获取或设置用于预处理字段值的区域性。 |
| [get_ResultFormatter](./get_resultformatter/)() const | 允许控制字段结果的格式化方式。 |
| [get_TemplateName](./get_templatename/)() const | 获取或设置文档使用的模板文件名。 |
| [get_ToaCategories](./get_toacategories/)() const | 获取或设置权威类别表。 |
| [get_UseInvariantCultureNumberFormat](./get_useinvariantculturenumberformat/)() const | 获取或设置指示是否使用不变区域性解析数字格式的值。 |
| [get_UserPromptRespondent](./get_userpromptrespondent/)() const | 获取或设置在字段更新期间对用户提示的响应者。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BarcodeGenerator](./set_barcodegenerator/)(const System::SharedPtr\<Aspose::Words::Fields::IBarcodeGenerator\>\&) | 获取或设置自定义条形码生成器。 |
| [set_BibliographyStylesProvider](./set_bibliographystylesprovider/)(const System::SharedPtr\<Aspose::Words::Fields::IBibliographyStylesProvider\>\&) | 设置一个提供程序，为 [FieldBibliography](../fieldbibliography/) 和 [FieldCitation](../fieldcitation/) 字段返回参考文献样式。 |
| [set_BuiltInTemplatesPaths](./set_builtintemplatespaths/)(const System::ArrayPtr\<System::String\>\&) | 用于 [Aspose::Words::Fields::FieldOptions::get_BuiltInTemplatesPaths](./get_builtintemplatespaths/) 的设置器。 |
| [set_ComparisonExpressionEvaluator](./set_comparisonexpressionevaluator/)(const System::SharedPtr\<Aspose::Words::Fields::IComparisonExpressionEvaluator\>\&) | 设置字段比较表达式评估器。 |
| [set_CurrentUser](./set_currentuser/)(const System::SharedPtr\<Aspose::Words::Fields::UserInformation\>\&) | 用于 [Aspose::Words::Fields::FieldOptions::get_CurrentUser](./get_currentuser/) 的设置器。 |
| [set_CustomTocStyleSeparator](./set_customtocstyleseparator/)(const System::String\&) | 为 [FieldToc](../fieldtoc/) 字段中的 \t 开关设置自定义样式分隔符。 |
| [set_DefaultDocumentAuthor](./set_defaultdocumentauthor/)(const System::String\&) | 用于 [Aspose::Words::Fields::FieldOptions::get_DefaultDocumentAuthor](./get_defaultdocumentauthor/) 的设置器。 |
| [set_FieldDatabaseProvider](./set_fielddatabaseprovider/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldDatabaseProvider\>\&) | 设置一个提供程序，为 [FieldDatabase](../fielddatabase/) 字段返回查询结果。 |
| [set_FieldIndexFormat](./set_fieldindexformat/)(Aspose::Words::Fields::FieldIndexFormat) | 用于 [Aspose::Words::Fields::FieldOptions::get_FieldIndexFormat](./get_fieldindexformat/) 的设置器。 |
| [set_FieldUpdateCultureProvider](./set_fieldupdatecultureprovider/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUpdateCultureProvider\>\&) | 用于 [Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureProvider](./get_fieldupdatecultureprovider/) 的设置器。 |
| [set_FieldUpdateCultureSource](./set_fieldupdateculturesource/)(Aspose::Words::Fields::FieldUpdateCultureSource) | 用于 [Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureSource](./get_fieldupdateculturesource/) 的设置器。 |
| [set_FieldUpdatingCallback](./set_fieldupdatingcallback/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUpdatingCallback\>\&) | 设置 [IFieldUpdatingCallback](../ifieldupdatingcallback/) 实现。 |
| [set_FieldUpdatingProgressCallback](./set_fieldupdatingprogresscallback/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUpdatingProgressCallback\>\&) | 设置 [IFieldUpdatingProgressCallback](../ifieldupdatingprogresscallback/) 实现。 |
| [set_FileName](./set_filename/)(const System::String\&) | 用于 [Aspose::Words::Fields::FieldOptions::get_FileName](./get_filename/) 的设置器。 |
| [set_IsBidiTextSupportedOnUpdate](./set_isbiditextsupportedonupdate/)(bool) | 用于 [Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate](./get_isbiditextsupportedonupdate/) 的设置器。 |
| [set_LegacyNumberFormat](./set_legacynumberformat/)(bool) | 用于 [Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat](./get_legacynumberformat/) 的设置器。 |
| [set_PreProcessCulture](./set_preprocessculture/)(const System::SharedPtr\<System::Globalization::CultureInfo\>\&) | 用于设置 [Aspose::Words::Fields::FieldOptions::get_PreProcessCulture](./get_preprocessculture/). |
| [set_ResultFormatter](./set_resultformatter/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldResultFormatter\>\&) | 允许控制字段结果的格式化方式。 |
| [set_TemplateName](./set_templatename/)(const System::String\&) | 用于设置 [Aspose::Words::Fields::FieldOptions::get_TemplateName](./get_templatename/). |
| [set_ToaCategories](./set_toacategories/)(const System::SharedPtr\<Aspose::Words::Fields::ToaCategories\>\&) | 用于设置 [Aspose::Words::Fields::FieldOptions::get_ToaCategories](./get_toacategories/). |
| [set_UseInvariantCultureNumberFormat](./set_useinvariantculturenumberformat/)(bool) | 用于设置 [Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat](./get_useinvariantculturenumberformat/). |
| [set_UserPromptRespondent](./set_userpromptrespondent/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUserPromptRespondent\>\&) | 用于设置 [Aspose::Words::Fields::FieldOptions::get_UserPromptRespondent](./get_userpromptrespondent/). |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
