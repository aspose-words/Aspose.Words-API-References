---
title: "Aspose::Words::Fields::FieldOptions clase"
linktitle: "FieldOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::FieldOptions clase. Representa opciones para controlar el manejo de campos en un documento. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 77000
url: /es/cpp/aspose.words.fields/fieldoptions/
---
## FieldOptions class


Representa opciones para controlar el manejo de campos en un documento. Para obtener más información, visite el artículo de documentación [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/).

```cpp
class FieldOptions : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_BarcodeGenerator](./get_barcodegenerator/)() const | Obtiene o establece el generador de códigos de barras personalizado. |
| [get_BibliographyStylesProvider](./get_bibliographystylesprovider/)() const | Obtiene un proveedor que devuelve un estilo de bibliografía para los campos [FieldBibliography](../fieldbibliography/) y [FieldCitation](../fieldcitation/). |
| [get_BuiltInTemplatesPaths](./get_builtintemplatespaths/)() const | Obtiene o establece las rutas de las plantillas integradas de MS Word. |
| [get_ComparisonExpressionEvaluator](./get_comparisonexpressionevaluator/)() const | Obtiene el evaluador de expresiones de comparación de campos. |
| [get_CurrentUser](./get_currentuser/)() const | Obtiene o establece la información del usuario actual. |
| [get_CustomTocStyleSeparator](./get_customtocstyleseparator/)() const | Obtiene el separador de estilo personalizado para el interruptor \t en el campo [FieldToc](../fieldtoc/). |
| [get_DefaultDocumentAuthor](./get_defaultdocumentauthor/)() const | Obtiene o establece el nombre del autor predeterminado del documento. Si el nombre del autor ya está especificado en las propiedades integradas del documento, esta opción no se considera. |
| [get_FieldDatabaseProvider](./get_fielddatabaseprovider/)() const | Obtiene un proveedor que devuelve un resultado de consulta para el campo [FieldDatabase](../fielddatabase/). |
| [get_FieldIndexFormat](./get_fieldindexformat/)() | Obtiene o establece un [FieldIndexFormat](./get_fieldindexformat/) que representa el formato para los campos [FieldIndex](../fieldindex/) en el documento. |
| [get_FieldUpdateCultureProvider](./get_fieldupdatecultureprovider/)() const | Obtiene o establece un proveedor que devuelve un objeto de cultura específico para cada campo en particular. |
| [get_FieldUpdateCultureSource](./get_fieldupdateculturesource/)() const | Especifica qué cultura usar para formatear el resultado del campo. |
| [get_FieldUpdatingCallback](./get_fieldupdatingcallback/)() const | Obtiene la implementación de [IFieldUpdatingCallback](../ifieldupdatingcallback/). |
| [get_FieldUpdatingProgressCallback](./get_fieldupdatingprogresscallback/)() const | Obtiene la implementación de [IFieldUpdatingProgressCallback](../ifieldupdatingprogresscallback/). |
| [get_FileName](./get_filename/)() const | Obtiene o establece el nombre de archivo del documento. |
| [get_IsBidiTextSupportedOnUpdate](./get_isbiditextsupportedonupdate/)() const | Obtiene o establece el valor que indica si el texto bidireccional es totalmente compatible durante la actualización del campo o no. |
| [get_LegacyNumberFormat](./get_legacynumberformat/)() const | Obtiene o establece el valor que indica si el formato numérico heredado (anterior a AW 13.10) para los campos está habilitado o no. |
| [get_PreProcessCulture](./get_preprocessculture/)() const | Obtiene o establece la cultura para preprocesar los valores de los campos. |
| [get_ResultFormatter](./get_resultformatter/)() const | Permite controlar cómo se formatea el resultado del campo. |
| [get_TemplateName](./get_templatename/)() const | Obtiene o establece el nombre de archivo de la plantilla utilizada por el documento. |
| [get_ToaCategories](./get_toacategories/)() const | Obtiene o establece la tabla de categorías de autoridades. |
| [get_UseInvariantCultureNumberFormat](./get_useinvariantculturenumberformat/)() const | Obtiene o establece el valor que indica si el formato numérico se analiza usando la cultura invariante o no. |
| [get_UserPromptRespondent](./get_userpromptrespondent/)() const | Obtiene o establece el respondedor a los mensajes del usuario durante la actualización del campo. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BarcodeGenerator](./set_barcodegenerator/)(const System::SharedPtr\<Aspose::Words::Fields::IBarcodeGenerator\>\&) | Obtiene o establece el generador de códigos de barras personalizado. |
| [set_BibliographyStylesProvider](./set_bibliographystylesprovider/)(const System::SharedPtr\<Aspose::Words::Fields::IBibliographyStylesProvider\>\&) | Establece un proveedor que devuelve un estilo de bibliografía para los campos [FieldBibliography](../fieldbibliography/) y [FieldCitation](../fieldcitation/). |
| [set_BuiltInTemplatesPaths](./set_builtintemplatespaths/)(const System::ArrayPtr\<System::String\>\&) | Establecedor para [Aspose::Words::Fields::FieldOptions::get_BuiltInTemplatesPaths](./get_builtintemplatespaths/). |
| [set_ComparisonExpressionEvaluator](./set_comparisonexpressionevaluator/)(const System::SharedPtr\<Aspose::Words::Fields::IComparisonExpressionEvaluator\>\&) | Establece el evaluador de expresiones de comparación de campos. |
| [set_CurrentUser](./set_currentuser/)(const System::SharedPtr\<Aspose::Words::Fields::UserInformation\>\&) | Método setter para [Aspose::Words::Fields::FieldOptions::get_CurrentUser](./get_currentuser/). |
| [set_CustomTocStyleSeparator](./set_customtocstyleseparator/)(const System::String\&) | Establece el separador de estilo personalizado para el interruptor \t en el campo [FieldToc](../fieldtoc/). |
| [set_DefaultDocumentAuthor](./set_defaultdocumentauthor/)(const System::String\&) | Método setter para [Aspose::Words::Fields::FieldOptions::get_DefaultDocumentAuthor](./get_defaultdocumentauthor/). |
| [set_FieldDatabaseProvider](./set_fielddatabaseprovider/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldDatabaseProvider\>\&) | Establece un proveedor que devuelve un resultado de consulta para el campo [FieldDatabase](../fielddatabase/). |
| [set_FieldIndexFormat](./set_fieldindexformat/)(Aspose::Words::Fields::FieldIndexFormat) | Método setter para [Aspose::Words::Fields::FieldOptions::get_FieldIndexFormat](./get_fieldindexformat/). |
| [set_FieldUpdateCultureProvider](./set_fieldupdatecultureprovider/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUpdateCultureProvider\>\&) | Método setter para [Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureProvider](./get_fieldupdatecultureprovider/). |
| [set_FieldUpdateCultureSource](./set_fieldupdateculturesource/)(Aspose::Words::Fields::FieldUpdateCultureSource) | Método setter para [Aspose::Words::Fields::FieldOptions::get_FieldUpdateCultureSource](./get_fieldupdateculturesource/). |
| [set_FieldUpdatingCallback](./set_fieldupdatingcallback/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUpdatingCallback\>\&) | Establece la implementación de [IFieldUpdatingCallback](../ifieldupdatingcallback/). |
| [set_FieldUpdatingProgressCallback](./set_fieldupdatingprogresscallback/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUpdatingProgressCallback\>\&) | Establece la implementación de [IFieldUpdatingProgressCallback](../ifieldupdatingprogresscallback/). |
| [set_FileName](./set_filename/)(const System::String\&) | Método setter para [Aspose::Words::Fields::FieldOptions::get_FileName](./get_filename/). |
| [set_IsBidiTextSupportedOnUpdate](./set_isbiditextsupportedonupdate/)(bool) | Método setter para [Aspose::Words::Fields::FieldOptions::get_IsBidiTextSupportedOnUpdate](./get_isbiditextsupportedonupdate/). |
| [set_LegacyNumberFormat](./set_legacynumberformat/)(bool) | Método setter para [Aspose::Words::Fields::FieldOptions::get_LegacyNumberFormat](./get_legacynumberformat/). |
| [set_PreProcessCulture](./set_preprocessculture/)(const System::SharedPtr\<System::Globalization::CultureInfo\>\&) | Método setter para [Aspose::Words::Fields::FieldOptions::get_PreProcessCulture](./get_preprocessculture/). |
| [set_ResultFormatter](./set_resultformatter/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldResultFormatter\>\&) | Permite controlar cómo se formatea el resultado del campo. |
| [set_TemplateName](./set_templatename/)(const System::String\&) | Método setter para [Aspose::Words::Fields::FieldOptions::get_TemplateName](./get_templatename/). |
| [set_ToaCategories](./set_toacategories/)(const System::SharedPtr\<Aspose::Words::Fields::ToaCategories\>\&) | Método setter para [Aspose::Words::Fields::FieldOptions::get_ToaCategories](./get_toacategories/). |
| [set_UseInvariantCultureNumberFormat](./set_useinvariantculturenumberformat/)(bool) | Método setter para [Aspose::Words::Fields::FieldOptions::get_UseInvariantCultureNumberFormat](./get_useinvariantculturenumberformat/). |
| [set_UserPromptRespondent](./set_userpromptrespondent/)(const System::SharedPtr\<Aspose::Words::Fields::IFieldUserPromptRespondent\>\&) | Método setter para [Aspose::Words::Fields::FieldOptions::get_UserPromptRespondent](./get_userpromptrespondent/). |
| static [Type](./type/)() |  |
## Ver también

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
