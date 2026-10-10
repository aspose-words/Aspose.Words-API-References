---
title: "Classe Aspose::Words::Fields::FieldOptions"
linktitle: "FieldOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Fields::FieldOptions. Rappresenta le opzioni per controllare la gestione dei campi in un documento. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 77000
url: /it/cpp/aspose.words.fields/fieldoptions/
---
## FieldOptions class


Rappresenta le opzioni per controllare la gestione dei campi in un documento. Per saperne di più, visita l'articolo di documentazione [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) .

```cpp
class FieldOptions : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_BarcodeGenerator](./get_barcodegenerator/)() const | Ottiene o imposta il generatore di codici a barre personalizzato. |
| [get_BibliographyStylesProvider](./get_bibliographystylesprovider/)() const | Ottiene un provider che restituisce uno stile bibliografico per i campi [FieldBibliography](../fieldbibliography/) e [FieldCitation](../fieldcitation/). |
| [get_BuiltInTemplatesPaths](./get_builtintemplatespaths/)() const | Ottiene o imposta i percorsi dei modelli integrati di MS Word. |
| [get_ComparisonExpressionEvaluator](./get_comparisonexpressionevaluator/)() const | Ottiene il valutatore delle espressioni di confronto dei campi. |
| [get_CurrentUser](./get_currentuser/)() const | Ottiene o imposta le informazioni dell'utente corrente. |
| [get_CustomTocStyleSeparator](./get_customtocstyleseparator/)() const | Ottiene il separatore di stile personalizzato per l'opzione \\t nel campo [FieldToc](../fieldtoc/). |
| [get_DefaultDocumentAuthor](./get_defaultdocumentauthor/)() const | Ottiene o imposta il nome dell'autore predefinito del documento. Se il nome dell'autore è già specificato nelle proprietà integrate del documento, questa opzione non viene considerata. |
| [get_FieldDatabaseProvider](./get_fielddatabaseprovider/)() const | Ottiene un provider che restituisce il risultato di una query per il campo [FieldDatabase](../fielddatabase/). |
| [get_FieldIndexFormat](./get_fieldindexformat/)() | Ottiene o imposta un [FieldIndexFormat](./get_fieldindexformat/) che rappresenta la formattazione per i campi [FieldIndex](../fieldindex/) nel documento. |
| [get_FieldUpdateCultureProvider](./get_fieldupdatecultureprovider/)() const | Ottiene o imposta un provider che restituisce un oggetto cultura specifico per ciascun campo particolare. |
| [get_FieldUpdateCultureSource](./get_fieldupdateculturesource/)() const | Specifica quale cultura utilizzare per formattare il risultato del campo. |
| [get_FieldUpdatingCallback](./get_fieldupdatingcallback/)() const | Ottiene l'implementazione di [IFieldUpdatingCallback](../ifieldupdatingcallback/). |
| [get_FieldUpdatingProgressCallback](./get_fieldupdatingprogresscallback/)() const | Ottiene l'implementazione di [IFieldUpdatingProgressCallback](../ifieldupdatingprogresscallback/). |
| [get_FileName](./get_filename/)() const | Ottiene o imposta il nome file del documento. |
| [get_IsBidiTextSupportedOnUpdate](./get_isbiditextsupportedonupdate/)() const | Ottiene o imposta il valore che indica se il testo bidirezionale è completamente supportato durante l'aggiornamento del campo o meno. |
| [get_LegacyNumberFormat](./get_legacynumberformat/)() const | Ottiene o imposta il valore che indica se il formato numerico legacy (precedente a AW 13.10) per i campi è abilitato o meno. |
| [get_PreProcessCulture](./get_preprocessculture/)() const | Ottiene o imposta la cultura per pre-elaborare i valori dei campi. |
| [get_ResultFormatter](./get_resultformatter/)() const | Consente di controllare come viene formattato il risultato del campo. |
| [get_TemplateName](./get_templatename/)() const | Ottiene o imposta il nome file del modello utilizzato dal documento. |
| [get_ToaCategories](./get_toacategories/)() const | Ottiene o imposta la tabella delle categorie di autorità. |
| [get_UseInvariantCultureNumberFormat](./get_useinvariantculturenumberformat/)() const | Ottiene o imposta il valore che indica se il formato numerico è analizzato usando la cultura invariata o meno. |
| [get_UserPromptRespondent](./get_userpromptrespondent/)() const | Ottiene o imposta il rispondente alle richieste dell'utente durante l'aggiornamento del campo. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BarcodeGenerator](./set_barcodegenerator/)(const System::SharedPtr\<Aspose::Words::Fields::IBarcodeGenerator\>\&) | Ottiene o imposta il generatore di codici a barre personalizzato. |
| [set_BibliographyStylesProvider](./set_bibliographystylesprovider/)(const System::SharedPtr\<Aspose::Words::Fields::IBibliographyStylesProvider\>\&) | Imposta un provider che restituisce uno stile bibliografico per i campi [FieldBibliography](../fieldbibliography/) e [FieldCitation](../fieldcitation/). |
| [set_BuiltInTemplatesPaths](./set_builtintemplatespaths/)(const System::ArrayPtr\<System::String\>\&) | Impostatore per [Aspose::Words::Fields::FieldOptions::get_BuiltInTemplatesPaths](./get_builtintemplatespaths/). |
| [set_ComparisonExpressionEvaluator](./set_comparisonexpressionevaluator/)(const System::SharedPtr\<Aspose::Words::Fields::IComparisonExpressionEvaluator\>\&) | Imposta il valutatore delle espressioni di confronto dei campi. |
| [set_CurrentUser](./set_currentuser/)(const System::SharedPtr\<Aspose::Words::Fields::UserInformation\>\&) | Impostatore per [Aspose::Words::Fields::FieldOptions::get_CurrentUser](./get_currentuser/). |
| [set_CustomTocStyleSeparator](./set_customtocstyleseparator/)(const System::String\&) | Imposta il separatore di stile personalizzato per l'opzione \t nel campo [FieldToc](../fieldtoc/). |
| [set_DefaultDocumentAuthor](./set_defaultdocumentauthor/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FieldOptions::get_DefaultDocumentAuthor](./get_defaultdocumentauthor/). |
| [set_FieldDatabaseProvider](./set_fielddatabaseprovider/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldDatabaseProvider\>\&) | Imposta un provider che restituisce un risultato di query per il campo [FieldDatabase](../fielddatabase/). |
| [set_FieldIndexFormat](./set_fieldindexformat/)(Aspose::Words::Fields::FieldIndexFormat) | Impostatore per [Aspose::Words::Fields::FieldOptions::get_FieldIndexFormat](./get_fieldindexformat/). |
| [set_FieldUpdateCultureProvider](./set_fieldupdatecultureprovider/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUpdateCultureProvider\>\&) | Impostatore per [Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureProvider](./get_fieldupdatecultureprovider/). |
| [set_FieldUpdateCultureSource](./set_fieldupdateculturesource/)(Aspose::Words::Fields::FieldUpdateCultureSource) | Impostatore per [Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureSource](./get_fieldupdateculturesource/). |
| [set_FieldUpdatingCallback](./set_fieldupdatingcallback/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUpdatingCallback\>\&) | Imposta l'implementazione di [IFieldUpdatingCallback](../ifieldupdatingcallback/). |
| [set_FieldUpdatingProgressCallback](./set_fieldupdatingprogresscallback/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUpdatingProgressCallback\>\&) | Imposta l'implementazione di [IFieldUpdatingProgressCallback](../ifieldupdatingprogresscallback/). |
| [set_FileName](./set_filename/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FieldOptions::get_FileName](./get_filename/). |
| [set_IsBidiTextSupportedOnUpdate](./set_isbiditextsupportedonupdate/)(bool) | Impostatore per [Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate](./get_isbiditextsupportedonupdate/). |
| [set_LegacyNumberFormat](./set_legacynumberformat/)(bool) | Impostatore per [Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat](./get_legacynumberformat/). |
| [set_PreProcessCulture](./set_preprocessculture/)(const System::SharedPtr\<System::Globalization::CultureInfo\>\&) | Impostatore per [Aspose::Words::Fields::FieldOptions::get_PreProcessCulture](./get_preprocessculture/). |
| [set_ResultFormatter](./set_resultformatter/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldResultFormatter\>\&) | Consente di controllare come viene formattato il risultato del campo. |
| [set_TemplateName](./set_templatename/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FieldOptions::get_TemplateName](./get_templatename/). |
| [set_ToaCategories](./set_toacategories/)(const System::SharedPtr\<Aspose::Words::Fields::ToaCategories\>\&) | Impostatore per [Aspose::Words::Fields::FieldOptions::get_ToaCategories](./get_toacategories/). |
| [set_UseInvariantCultureNumberFormat](./set_useinvariantculturenumberformat/)(bool) | Impostatore per [Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat](./get_useinvariantculturenumberformat/). |
| [set_UserPromptRespondent](./set_userpromptrespondent/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUserPromptRespondent\>\&) | Impostatore per [Aspose::Words::Fields::FieldOptions::get_UserPromptRespondent](./get_userpromptrespondent/). |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
