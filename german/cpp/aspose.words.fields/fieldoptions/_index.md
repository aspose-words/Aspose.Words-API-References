---
title: "Aspose::Words::Fields::FieldOptions Klasse"
linktitle: "FieldOptions"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FieldOptions Klasse. Stellt Optionen zur Steuerung der Feldverarbeitung in einem Dokument dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 77000
url: /de/cpp/aspose.words.fields/fieldoptions/
---
## FieldOptions class


Stellt Optionen zur Steuerung der Feldverarbeitung in einem Dokument dar. Weitere Informationen finden Sie im [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) Dokumentationsartikel.

```cpp
class FieldOptions : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_BarcodeGenerator](./get_barcodegenerator/)() const | Liest oder setzt benutzerdefinierten Barcode‑Generator. |
| [get_BibliographyStylesProvider](./get_bibliographystylesprovider/)() const | Liest einen Anbieter, der einen Bibliografiestil für die Felder [FieldBibliography](../fieldbibliography/) und [FieldCitation](../fieldcitation/) zurückgibt. |
| [get_BuiltInTemplatesPaths](./get_builtintemplatespaths/)() const | Liest oder setzt Pfade zu den integrierten MS‑Word‑Vorlagen. |
| [get_ComparisonExpressionEvaluator](./get_comparisonexpressionevaluator/)() const | Liest den Auswerter für Feldvergleichsausdrücke. |
| [get_CurrentUser](./get_currentuser/)() const | Liest oder setzt die aktuellen Benutzerinformationen. |
| [get_CustomTocStyleSeparator](./get_customtocstyleseparator/)() const | Liest den benutzerdefinierten Stiltrenner für den \t‑Schalter im Feld [FieldToc](../fieldtoc/). |
| [get_DefaultDocumentAuthor](./get_defaultdocumentauthor/)() const | Liest oder setzt den Standard‑Autorennamen des Dokuments. Wenn der Autorenname bereits in den integrierten Dokumenteigenschaften angegeben ist, wird diese Option nicht berücksichtigt. |
| [get_FieldDatabaseProvider](./get_fielddatabaseprovider/)() const | Liest einen Anbieter, der ein Abfrageergebnis für das Feld [FieldDatabase](../fielddatabase/) zurückgibt. |
| [get_FieldIndexFormat](./get_fieldindexformat/)() | Liest oder setzt ein [FieldIndexFormat](./get_fieldindexformat/), das die Formatierung für die [FieldIndex](../fieldindex/)-Felder im Dokument darstellt. |
| [get_FieldUpdateCultureProvider](./get_fieldupdatecultureprovider/)() const | Liest oder setzt einen Anbieter, der ein kulturspezifisches Objekt für jedes einzelne Feld zurückgibt. |
| [get_FieldUpdateCultureSource](./get_fieldupdateculturesource/)() const | Gibt an, welche Kultur zur Formatierung des Feldresultats verwendet werden soll. |
| [get_FieldUpdatingCallback](./get_fieldupdatingcallback/)() const | Liest die Implementierung von [IFieldUpdatingCallback](../ifieldupdatingcallback/). |
| [get_FieldUpdatingProgressCallback](./get_fieldupdatingprogresscallback/)() const | Liest die Implementierung von [IFieldUpdatingProgressCallback](../ifieldupdatingprogresscallback/). |
| [get_FileName](./get_filename/)() const | Liest oder setzt den Dateinamen des Dokuments. |
| [get_IsBidiTextSupportedOnUpdate](./get_isbiditextsupportedonupdate/)() const | Liest oder setzt den Wert, der angibt, ob bidirektionaler Text während der Feldaktualisierung vollständig unterstützt wird oder nicht. |
| [get_LegacyNumberFormat](./get_legacynumberformat/)() const | Liest oder setzt den Wert, der angibt, ob das veraltete (vor AW 13.10) Zahlenformat für Felder aktiviert ist oder nicht. |
| [get_PreProcessCulture](./get_preprocessculture/)() const | Liest oder setzt die Kultur zur Vorverarbeitung von Feldwerten. |
| [get_ResultFormatter](./get_resultformatter/)() const | Ermöglicht die Kontrolle, wie das Feldresultat formatiert wird. |
| [get_TemplateName](./get_templatename/)() const | Liest oder legt den Dateinamen der vom Dokument verwendeten Vorlage fest. |
| [get_ToaCategories](./get_toacategories/)() const | Liest oder legt die Tabelle der Autoritätskategorien fest. |
| [get_UseInvariantCultureNumberFormat](./get_useinvariantculturenumberformat/)() const | Liest oder legt den Wert fest, der angibt, ob das Zahlenformat mit Invariant Culture geparst wird oder nicht. |
| [get_UserPromptRespondent](./get_userpromptrespondent/)() const | Liest oder legt den Befragten für Benutzeraufforderungen während der Feldaktualisierung fest. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BarcodeGenerator](./set_barcodegenerator/)(const System::SharedPtr\<Aspose::Words::Fields::IBarcodeGenerator\>\&) | Liest oder setzt benutzerdefinierten Barcode‑Generator. |
| [set_BibliographyStylesProvider](./set_bibliographystylesprovider/)(const System::SharedPtr\<Aspose::Words::Fields::IBibliographyStylesProvider\>\&) | Legt einen Anbieter fest, der einen Bibliografiestil für die Felder [FieldBibliography](../fieldbibliography/) und [FieldCitation](../fieldcitation/) zurückgibt. |
| [set_BuiltInTemplatesPaths](./set_builtintemplatespaths/)(const System::ArrayPtr\<System::String\>\&) | Setter für [Aspose::Words::Fields::FieldOptions::get_BuiltInTemplatesPaths](./get_builtintemplatespaths/). |
| [set_ComparisonExpressionEvaluator](./set_comparisonexpressionevaluator/)(const System::SharedPtr\<Aspose::Words::Fields::IComparisonExpressionEvaluator\>\&) | Legt den Evaluator für Feldvergleichsausdrücke fest. |
| [set_CurrentUser](./set_currentuser/)(const System::SharedPtr\<Aspose::Words::Fields::UserInformation\>\&) | Setter für [Aspose::Words::Fields::FieldOptions::get_CurrentUser](./get_currentuser/). |
| [set_CustomTocStyleSeparator](./set_customtocstyleseparator/)(const System::String\&) | Legt den benutzerdefinierten Stiltrennzeichen für den \t-Schalter im Feld [FieldToc](../fieldtoc/) fest. |
| [set_DefaultDocumentAuthor](./set_defaultdocumentauthor/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldOptions::get_DefaultDocumentAuthor](./get_defaultdocumentauthor/). |
| [set_FieldDatabaseProvider](./set_fielddatabaseprovider/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldDatabaseProvider\>\&) | Legt einen Anbieter fest, der ein Abfrageergebnis für das Feld [FieldDatabase](../fielddatabase/) zurückgibt. |
| [set_FieldIndexFormat](./set_fieldindexformat/)(Aspose::Words::Fields::FieldIndexFormat) | Setter für [Aspose::Words::Fields::FieldOptions::get_FieldIndexFormat](./get_fieldindexformat/). |
| [set_FieldUpdateCultureProvider](./set_fieldupdatecultureprovider/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUpdateCultureProvider\>\&) | Setter für [Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureProvider](./get_fieldupdatecultureprovider/). |
| [set_FieldUpdateCultureSource](./set_fieldupdateculturesource/)(Aspose::Words::Fields::FieldUpdateCultureSource) | Setter für [Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureSource](./get_fieldupdateculturesource/). |
| [set_FieldUpdatingCallback](./set_fieldupdatingcallback/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUpdatingCallback\>\&) | Legt die Implementierung von [IFieldUpdatingCallback](../ifieldupdatingcallback/) fest. |
| [set_FieldUpdatingProgressCallback](./set_fieldupdatingprogresscallback/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUpdatingProgressCallback\>\&) | Legt die Implementierung von [IFieldUpdatingProgressCallback](../ifieldupdatingprogresscallback/) fest. |
| [set_FileName](./set_filename/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldOptions::get_FileName](./get_filename/). |
| [set_IsBidiTextSupportedOnUpdate](./set_isbiditextsupportedonupdate/)(bool) | Setter für [Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate](./get_isbiditextsupportedonupdate/). |
| [set_LegacyNumberFormat](./set_legacynumberformat/)(bool) | Setter für [Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat](./get_legacynumberformat/). |
| [set_PreProcessCulture](./set_preprocessculture/)(const System::SharedPtr\<System::Globalization::CultureInfo\>\&) | Setter für [Aspose::Words::Fields::FieldOptions::get_PreProcessCulture](./get_preprocessculture/). |
| [set_ResultFormatter](./set_resultformatter/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldResultFormatter\>\&) | Ermöglicht die Kontrolle, wie das Feldresultat formatiert wird. |
| [set_TemplateName](./set_templatename/)(const System::String\&) | Setter für [Aspose::Words::Fields::FieldOptions::get_TemplateName](./get_templatename/). |
| [set_ToaCategories](./set_toacategories/)(const System::SharedPtr\<Aspose::Words::Fields::ToaCategories\>\&) | Setter für [Aspose::Words::Fields::FieldOptions::get_ToaCategories](./get_toacategories/). |
| [set_UseInvariantCultureNumberFormat](./set_useinvariantculturenumberformat/)(bool) | Setter für [Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat](./get_useinvariantculturenumberformat/). |
| [set_UserPromptRespondent](./set_userpromptrespondent/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUserPromptRespondent\>\&) | Setter für [Aspose::Words::Fields::FieldOptions::get_UserPromptRespondent](./get_userpromptrespondent/). |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
