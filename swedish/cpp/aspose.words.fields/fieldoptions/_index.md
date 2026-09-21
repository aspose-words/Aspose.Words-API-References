---
title: "Aspose::Words::Fields::FieldOptions klass"
linktitle: "FieldOptions"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FieldOptions klass. Representerar alternativ för att kontrollera fältbehandling i ett dokument. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 77000
url: /sv/cpp/aspose.words.fields/fieldoptions/
---
## FieldOptions class


Representerar alternativ för att kontrollera fältbehandling i ett dokument. För att lära dig mer, besök dokumentationsartikeln [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldOptions : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_BarcodeGenerator](./get_barcodegenerator/)() const | Hämtar eller anger en anpassad streckkodsgenerator. |
| [get_BibliographyStylesProvider](./get_bibliographystylesprovider/)() const | Hämtar en leverantör som returnerar en bibliografistil för fälten [FieldBibliography](../fieldbibliography/) och [FieldCitation](../fieldcitation/). |
| [get_BuiltInTemplatesPaths](./get_builtintemplatespaths/)() const | Hämtar eller anger sökvägar till MS Words inbyggda mallar. |
| [get_ComparisonExpressionEvaluator](./get_comparisonexpressionevaluator/)() const | Hämtar utvärderaren för fältjämförelseuttryck. |
| [get_CurrentUser](./get_currentuser/)() const | Hämtar eller anger den aktuella användarinformationen. |
| [get_CustomTocStyleSeparator](./get_customtocstyleseparator/)() const | Hämtar anpassad stilseparator för \t‑växeln i fältet [FieldToc](../fieldtoc/). |
| [get_DefaultDocumentAuthor](./get_defaultdocumentauthor/)() const | Hämtar eller anger standardnamnet på dokumentets författare. Om författarens namn redan är specificerat i inbyggda dokumentegenskaper beaktas inte detta alternativ. |
| [get_FieldDatabaseProvider](./get_fielddatabaseprovider/)() const | Hämtar en leverantör som returnerar ett frågeresultat för fältet [FieldDatabase](../fielddatabase/). |
| [get_FieldIndexFormat](./get_fieldindexformat/)() | Hämtar eller anger ett [FieldIndexFormat](./get_fieldindexformat/) som representerar formateringen för [FieldIndex](../fieldindex/)-fälten i dokumentet. |
| [get_FieldUpdateCultureProvider](./get_fieldupdatecultureprovider/)() const | Hämtar eller anger en leverantör som returnerar ett kulturobjekt specifikt för varje enskilt fält. |
| [get_FieldUpdateCultureSource](./get_fieldupdateculturesource/)() const | Anger vilken kultur som ska användas för att formatera fältresultatet. |
| [get_FieldUpdatingCallback](./get_fieldupdatingcallback/)() const | Hämtar implementationen av [IFieldUpdatingCallback](../ifieldupdatingcallback/). |
| [get_FieldUpdatingProgressCallback](./get_fieldupdatingprogresscallback/)() const | Hämtar implementationen av [IFieldUpdatingProgressCallback](../ifieldupdatingprogresscallback/). |
| [get_FileName](./get_filename/)() const | Hämtar eller anger filnamnet på dokumentet. |
| [get_IsBidiTextSupportedOnUpdate](./get_isbiditextsupportedonupdate/)() const | Hämtar eller anger värdet som indikerar om bidi‑text fullt stödjs under fältuppdatering eller inte. |
| [get_LegacyNumberFormat](./get_legacynumberformat/)() const | Hämtar eller anger värdet som indikerar om äldre (tidigare än AW 13.10) talformat för fält är aktiverat eller inte. |
| [get_PreProcessCulture](./get_preprocessculture/)() const | Hämtar eller anger kulturen för att förbehandla fältvärden. |
| [get_ResultFormatter](./get_resultformatter/)() const | Tillåter att kontrollera hur fältresultatet formateras. |
| [get_TemplateName](./get_templatename/)() const | Hämtar eller anger filnamnet på mallen som används av dokumentet. |
| [get_ToaCategories](./get_toacategories/)() const | Hämtar eller anger tabellen med auktoritetskategorier. |
| [get_UseInvariantCultureNumberFormat](./get_useinvariantculturenumberformat/)() const | Hämtar eller anger värdet som indikerar om talformat tolkas med invariant kultur eller inte. |
| [get_UserPromptRespondent](./get_userpromptrespondent/)() const | Hämtar eller anger svararen på användarfrågor under fältuppdatering. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BarcodeGenerator](./set_barcodegenerator/)(const System::SharedPtr\<Aspose::Words::Fields::IBarcodeGenerator\>\&) | Hämtar eller anger en anpassad streckkodsgenerator. |
| [set_BibliographyStylesProvider](./set_bibliographystylesprovider/)(const System::SharedPtr\<Aspose::Words::Fields::IBibliographyStylesProvider\>\&) | Anger en leverantör som returnerar en bibliografistil för fälten [FieldBibliography](../fieldbibliography/) och [FieldCitation](../fieldcitation/). |
| [set_BuiltInTemplatesPaths](./set_builtintemplatespaths/)(const System::ArrayPtr\<System::String\>\&) | Sättare för [Aspose::Words::Fields::FieldOptions::get_BuiltInTemplatesPaths](./get_builtintemplatespaths/). |
| [set_ComparisonExpressionEvaluator](./set_comparisonexpressionevaluator/)(const System::SharedPtr\<Aspose::Words::Fields::IComparisonExpressionEvaluator\>\&) | Anger utvärderaren för fältjämförelseuttryck. |
| [set_CurrentUser](./set_currentuser/)(const System::SharedPtr\<Aspose::Words::Fields::UserInformation\>\&) | Sättare för [Aspose::Words::Fields::FieldOptions::get_CurrentUser](./get_currentuser/). |
| [set_CustomTocStyleSeparator](./set_customtocstyleseparator/)(const System::String\&) | Anger anpassad stilseparator för \t‑växeln i fältet [FieldToc](../fieldtoc/). |
| [set_DefaultDocumentAuthor](./set_defaultdocumentauthor/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldOptions::get_DefaultDocumentAuthor](./get_defaultdocumentauthor/). |
| [set_FieldDatabaseProvider](./set_fielddatabaseprovider/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldDatabaseProvider\>\&) | Anger en leverantör som returnerar ett frågeresultat för fältet [FieldDatabase](../fielddatabase/). |
| [set_FieldIndexFormat](./set_fieldindexformat/)(Aspose::Words::Fields::FieldIndexFormat) | Sättare för [Aspose::Words::Fields::FieldOptions::get_FieldIndexFormat](./get_fieldindexformat/). |
| [set_FieldUpdateCultureProvider](./set_fieldupdatecultureprovider/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUpdateCultureProvider\>\&) | Sättare för [Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureProvider](./get_fieldupdatecultureprovider/). |
| [set_FieldUpdateCultureSource](./set_fieldupdateculturesource/)(Aspose::Words::Fields::FieldUpdateCultureSource) | Sättare för [Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureSource](./get_fieldupdateculturesource/). |
| [set_FieldUpdatingCallback](./set_fieldupdatingcallback/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUpdatingCallback\>\&) | Anger implementation av [IFieldUpdatingCallback](../ifieldupdatingcallback/). |
| [set_FieldUpdatingProgressCallback](./set_fieldupdatingprogresscallback/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUpdatingProgressCallback\>\&) | Anger implementation av [IFieldUpdatingProgressCallback](../ifieldupdatingprogresscallback/). |
| [set_FileName](./set_filename/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldOptions::get_FileName](./get_filename/). |
| [set_IsBidiTextSupportedOnUpdate](./set_isbiditextsupportedonupdate/)(bool) | Sättare för [Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate](./get_isbiditextsupportedonupdate/). |
| [set_LegacyNumberFormat](./set_legacynumberformat/)(bool) | Sättare för [Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat](./get_legacynumberformat/). |
| [set_PreProcessCulture](./set_preprocessculture/)(const System::SharedPtr\<System::Globalization::CultureInfo\>\&) | Sättare för [Aspose::Words::Fields::FieldOptions::get_PreProcessCulture](./get_preprocessculture/). |
| [set_ResultFormatter](./set_resultformatter/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldResultFormatter\>\&) | Tillåter att kontrollera hur fältresultatet formateras. |
| [set_TemplateName](./set_templatename/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FieldOptions::get_TemplateName](./get_templatename/). |
| [set_ToaCategories](./set_toacategories/)(const System::SharedPtr\<Aspose::Words::Fields::ToaCategories\>\&) | Sättare för [Aspose::Words::Fields::FieldOptions::get_ToaCategories](./get_toacategories/). |
| [set_UseInvariantCultureNumberFormat](./set_useinvariantculturenumberformat/)(bool) | Sättare för [Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat](./get_useinvariantculturenumberformat/). |
| [set_UserPromptRespondent](./set_userpromptrespondent/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUserPromptRespondent\>\&) | Sättare för [Aspose::Words::Fields::FieldOptions::get_UserPromptRespondent](./get_userpromptrespondent/). |
| static [Type](./type/)() |  |
## Se även

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
