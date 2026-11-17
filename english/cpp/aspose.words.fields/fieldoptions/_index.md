---
title: Aspose::Words::Fields::FieldOptions class
linktitle: FieldOptions
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldOptions class. Represents options to control field handling in a document. To learn more, visit the Working with Fields documentation article in C++.'
type: docs
weight: 77000
url: /cpp/aspose.words.fields/fieldoptions/
---
## FieldOptions class


Represents options to control field handling in a document. 
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) documentation article.

```cpp
class FieldOptions : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_BarcodeGenerator](./get_barcodegenerator/)() const | Gets or set custom barcode generator. |
| [get_BibliographyStylesProvider](./get_bibliographystylesprovider/)() const | Gets or sets a provider that returns a bibliography style for the [FieldBibliography](../fieldbibliography/) and [FieldCitation](../fieldcitation/) fields. |
| [get_BuiltInTemplatesPaths](./get_builtintemplatespaths/)() const | Gets or sets paths of MS Word built-in templates. |
| [get_ComparisonExpressionEvaluator](./get_comparisonexpressionevaluator/)() const | Gets or sets the field comparison expressions evaluator. |
| [get_CurrentUser](./get_currentuser/)() const | Gets or sets the current user information. |
| [get_CustomTocStyleSeparator](./get_customtocstyleseparator/)() const | Gets or sets custom style separator for the \t switch in [FieldToc](../fieldtoc/) field. |
| [get_DefaultDocumentAuthor](./get_defaultdocumentauthor/)() const | Gets or sets default document author's name. If author's name is already specified in built-in document properties, this option is not considered. |
| [get_FieldDatabaseProvider](./get_fielddatabaseprovider/)() const | Gets a provider that returns a query result for the [FieldDatabase](../fielddatabase/) field. |
| [get_FieldIndexFormat](./get_fieldindexformat/)() | Gets or sets a [FieldIndexFormat](./get_fieldindexformat/) that represents the formatting for the [FieldIndex](../fieldindex/) fields in the document. |
| [get_FieldUpdateCultureProvider](./get_fieldupdatecultureprovider/)() const | Gets or sets a provider that returns a culture object specific for each particular field. |
| [get_FieldUpdateCultureSource](./get_fieldupdateculturesource/)() const | Specifies what culture to use to format the field result. |
| [get_FieldUpdatingCallback](./get_fieldupdatingcallback/)() const | Gets [IFieldUpdatingCallback](../ifieldupdatingcallback/) implementation |
| [get_FieldUpdatingProgressCallback](./get_fieldupdatingprogresscallback/)() const | Gets [IFieldUpdatingProgressCallback](../ifieldupdatingprogresscallback/) implementation. |
| [get_FileName](./get_filename/)() const | Gets or sets the file name of the document. |
| [get_IsBidiTextSupportedOnUpdate](./get_isbiditextsupportedonupdate/)() const | Gets or sets the value indicating whether bidirectional text is fully supported during field update or not. |
| [get_LegacyNumberFormat](./get_legacynumberformat/)() const | Gets or sets the value indicating whether legacy (early than AW 13.10) number format for fields is enabled or not. |
| [get_PreProcessCulture](./get_preprocessculture/)() const | Gets or sets the culture to preprocess field values. |
| [get_ResultFormatter](./get_resultformatter/)() const | Allows to control how the field result is formatted. |
| [get_TemplateName](./get_templatename/)() const | Gets or sets the file name of the template used by the document. |
| [get_ToaCategories](./get_toacategories/)() const | Gets or sets the table of authorities categories. |
| [get_UseInvariantCultureNumberFormat](./get_useinvariantculturenumberformat/)() const | Gets or sets the value indicating that number format is parsed using invariant culture or not |
| [get_UserPromptRespondent](./get_userpromptrespondent/)() const | Gets or sets the respondent to user prompts during field update. |
| [set_BarcodeGenerator](./set_barcodegenerator/)(const System::SharedPtr\<Aspose::Words::Fields::IBarcodeGenerator\> \&) | Gets or set custom barcode generator. |
| [set_BibliographyStylesProvider](./set_bibliographystylesprovider/)(const System::SharedPtr\<Aspose::Words::Fields::IBibliographyStylesProvider\> \&) | Sets a provider that returns a bibliography style for the [FieldBibliography](../fieldbibliography/) and [FieldCitation](../fieldcitation/) fields. |
| [set_BuiltInTemplatesPaths](./set_builtintemplatespaths/)(const System::ArrayPtr\<System::String\> \&) | Sets paths of MS Word built-in templates. |
| [set_ComparisonExpressionEvaluator](./set_comparisonexpressionevaluator/)(const System::SharedPtr\<Aspose::Words::Fields::IComparisonExpressionEvaluator\> \&) | Sets the field comparison expressions evaluator. |
| [set_CurrentUser](./set_currentuser/)(const System::SharedPtr\<Aspose::Words::Fields::UserInformation\> \&) | Sets the current user information. |
| [set_CustomTocStyleSeparator](./set_customtocstyleseparator/)(const System::String \&) | Sets custom style separator for the \t switch in [FieldToc](../fieldtoc/) field. |
| [set_DefaultDocumentAuthor](./set_defaultdocumentauthor/)(const System::String \&) | Sets default document author's name. If author's name is already specified in built-in document properties, this option is not considered. |
| [set_FieldDatabaseProvider](./set_fielddatabaseprovider/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldDatabaseProvider\> \&) | Sets a provider that returns a query result for the [FieldDatabase](../fielddatabase/) field. |
| [set_FieldIndexFormat](./set_fieldindexformat/)(Aspose::Words::Fields::FieldIndexFormat) | Sets a [FieldIndexFormat](./get_fieldindexformat/) that represents the formatting for the [FieldIndex](../fieldindex/) fields in the document. |
| [set_FieldUpdateCultureProvider](./set_fieldupdatecultureprovider/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUpdateCultureProvider\> \&) | Sets a provider that returns a culture object specific for each particular field. |
| [set_FieldUpdateCultureSource](./set_fieldupdateculturesource/)(Aspose::Words::Fields::FieldUpdateCultureSource) | Specifies what culture to use to format the field result. |
| [set_FieldUpdatingCallback](./set_fieldupdatingcallback/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUpdatingCallback\> \&) | Sets [IFieldUpdatingCallback](../ifieldupdatingcallback/) implementation |
| [set_FieldUpdatingProgressCallback](./set_fieldupdatingprogresscallback/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUpdatingProgressCallback\> \&) | Sets [IFieldUpdatingProgressCallback](../ifieldupdatingprogresscallback/) implementation. |
| [set_FileName](./set_filename/)(const System::String \&) | Sets the file name of the document. |
| [set_IsBidiTextSupportedOnUpdate](./set_isbiditextsupportedonupdate/)(bool) | Sets the value indicating whether bidirectional text is fully supported during field update or not. |
| [set_LegacyNumberFormat](./set_legacynumberformat/)(bool) | Sets the value indicating whether legacy (early than AW 13.10) number format for fields is enabled or not. |
| [set_PreProcessCulture](./set_preprocessculture/)(const System::SharedPtr\<System::Globalization::CultureInfo\> \&) | Sets the culture to preprocess field values. |
| [set_ResultFormatter](./set_resultformatter/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldResultFormatter\> \&) | Allows to control how the field result is formatted. |
| [set_TemplateName](./set_templatename/)(const System::String \&) | Sets the file name of the template used by the document. |
| [set_ToaCategories](./set_toacategories/)(const System::SharedPtr\<Aspose::Words::Fields::ToaCategories\> \&) | Sets the table of authorities categories. |
| [set_UseInvariantCultureNumberFormat](./set_useinvariantculturenumberformat/)(bool) | Sets the value indicating that number format is parsed using invariant culture or not |
| [set_UserPromptRespondent](./set_userpromptrespondent/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUserPromptRespondent\> \&) | Sets the respondent to user prompts during field update. |
## See Also

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
