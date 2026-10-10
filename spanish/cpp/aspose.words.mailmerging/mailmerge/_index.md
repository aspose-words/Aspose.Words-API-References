---
title: "Aspose::Words::MailMerging::MailMerge class"
linktitle: "MailMerge"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::MailMerging::MailMerge class. Representa la funcionalidad de combinación de correspondencia. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.mailmerging/mailmerge/
---
## MailMerge class


Representa la funcionalidad de combinación de correspondencia. Para obtener más información, visite el artículo de documentación [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class MailMerge : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [DeleteFields](./deletefields/)() | Elimina los campos relacionados con la combinación de correspondencia del documento. |
| [Execute](./execute/)(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) | Realiza una combinación de correspondencia a partir de una fuente de datos personalizada. |
| [Execute](./execute/)(const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<System::Object\>\>\&) | Realiza una operación de combinación de correspondencia para un solo registro. |
| [ExecuteWithRegions](./executewithregions/)(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) | Realiza una combinación de correspondencia a partir de una fuente de datos personalizada con regiones de combinación de correspondencia. |
| [ExecuteWithRegions](./executewithregions/)(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSourceRoot\>\&) | Realiza una combinación de correspondencia a partir de una fuente de datos personalizada con regiones de combinación de correspondencia. |
| [get_CleanupOptions](./get_cleanupoptions/)() const | Obtiene un conjunto de indicadores que especifican qué elementos deben eliminarse durante la combinación de correspondencia. |
| [get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/)() const | Obtiene o establece un valor que indica si los párrafos con signos de puntuación se consideran vacíos y deben eliminarse si se especifica la opción [RemoveEmptyParagraphs](../mailmergecleanupoptions/). |
| [get_FieldMergingCallback](./get_fieldmergingcallback/)() const | Ocurre durante la combinación de correspondencia cuando se encuentra un campo de combinación de correspondencia en el documento. |
| [get_MailMergeCallback](./get_mailmergecallback/)() const | Permite manejar eventos particulares durante la combinación de correspondencia. |
| [get_MappedDataFields](./get_mappeddatafields/)() | Devuelve una colección que representa los campos de datos mapeados para la operación de combinación de correspondencia. |
| [get_MergeDuplicateRegions](./get_mergeduplicateregions/)() const | Obtiene un valor que indica si todas las regiones de combinación de correspondencia del documento con el nombre de una fuente de datos deben fusionarse al ejecutar una combinación de correspondencia con regiones contra la fuente de datos o solo la primera. |
| [get_MergeWholeDocument](./get_mergewholedocument/)() const | Obtiene un valor que indica si los campos en todo el documento se actualizan al ejecutar una combinación de correspondencia con regiones. |
| [get_PreserveUnusedTags](./get_preserveunusedtags/)() const | Obtiene un valor que indica si las etiquetas "mustache" no utilizadas deben conservarse. |
| [get_RegionEndTag](./get_regionendtag/)() const | Obtiene la etiqueta de fin de región de combinación de correspondencia. |
| [get_RegionStartTag](./get_regionstarttag/)() const | Obtiene la etiqueta de inicio de región de combinación de correspondencia. |
| [get_RestartListsAtEachSection](./get_restartlistsateachsection/)() const | Obtiene un valor que indica si las listas se reinician en cada sección después de ejecutar una combinación de correspondencia. |
| [get_RetainFirstSectionStart](./get_retainfirstsectionstart/)() const | Obtiene un valor que indica si el [SectionStart](../../aspose.words/pagesetup/get_sectionstart/) de la primera sección del documento y sus copias para filas posteriores de la fuente de datos se conservan durante la combinación de correspondencia o se actualizan según el comportamiento de MS Word. |
| [get_TrimWhitespaces](./get_trimwhitespaces/)() const | Obtiene un valor que indica si los espacios en blanco iniciales y finales se recortan de los valores de combinación de correspondencia. |
| [get_UnconditionalMergeFieldsAndRegions](./get_unconditionalmergefieldsandregions/)() const | Obtiene un valor que indica si los campos de combinación y las regiones de combinación se fusionan sin importar la condición del campo IF padre. |
| [get_UseNonMergeFields](./get_usenonmergefields/)() const | Cuando **true**, especifica que, además de los campos MERGEFIELD, la combinación de correspondencia se realiza en algunos otros tipos de campos y también en etiquetas "{{fieldName}}". |
| [get_UseWholeParagraphAsRegion](./get_usewholeparagraphasregion/)() const | Obtiene un valor que indica si todo el párrafo con el campo **TableStart** o **TableEnd**, o un rango particular entre los campos **TableStart** y **TableEnd**, debe incluirse en la región de combinación de correspondencia. |
| [GetFieldNames](./getfieldnames/)() | Devuelve una colección de nombres de campos de combinación de correspondencia disponibles en el documento. |
| [GetFieldNamesForRegion](./getfieldnamesforregion/)(const System::String\&) | Devuelve una colección de nombres de campos de combinación de correspondencia disponibles en la región. |
| [GetFieldNamesForRegion](./getfieldnamesforregion/)(const System::String\&, int32_t) | Devuelve una colección de nombres de campos de combinación de correspondencia disponibles en la región. |
| [GetRegionsByName](./getregionsbyname/)(const System::String\&) | Devuelve una colección de regiones de combinación de correspondencia con el nombre especificado. |
| [GetRegionsHierarchy](./getregionshierarchy/)() | Devuelve una jerarquía completa de regiones (con campos) disponibles en el documento. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_CleanupOptions](./set_cleanupoptions/)(Aspose::Words::MailMerging::MailMergeCleanupOptions) | Establece un conjunto de indicadores que especifican qué elementos deben eliminarse durante la combinación de correspondencia. |
| [set_CleanupParagraphsWithPunctuationMarks](./set_cleanupparagraphswithpunctuationmarks/)(bool) | Método set para [Aspose::Words::MailMerging::MailMerge::get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/). |
| [set_FieldMergingCallback](./set_fieldmergingcallback/)(const System::SharedPtr\<Aspose::Words::MailMerging::IFieldMergingCallback\>\&) | Ocurre durante la combinación de correspondencia cuando se encuentra un campo de combinación de correspondencia en el documento. |
| [set_MailMergeCallback](./set_mailmergecallback/)(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeCallback\>\&) | Permite manejar eventos particulares durante la combinación de correspondencia. |
| [set_MergeDuplicateRegions](./set_mergeduplicateregions/)(bool) | Establece un valor que indica si todas las regiones de combinación de correspondencia del documento con el nombre de una fuente de datos deben fusionarse al ejecutar una combinación de correspondencia con regiones contra la fuente de datos o solo la primera. |
| [set_MergeWholeDocument](./set_mergewholedocument/)(bool) | Establece un valor que indica si los campos en todo el documento se actualizan al ejecutar una combinación de correspondencia con regiones. |
| [set_PreserveUnusedTags](./set_preserveunusedtags/)(bool) | Establece un valor que indica si las etiquetas "mustache" no utilizadas deben conservarse. |
| [set_RegionEndTag](./set_regionendtag/)(const System::String\&) | Establece una etiqueta de fin de región de combinación de correspondencia. |
| [set_RegionStartTag](./set_regionstarttag/)(const System::String\&) | Establece una etiqueta de inicio de región de combinación de correspondencia. |
| [set_RestartListsAtEachSection](./set_restartlistsateachsection/)(bool) | Establece un valor que indica si las listas se reinician en cada sección después de ejecutar una combinación de correspondencia. |
| [set_RetainFirstSectionStart](./set_retainfirstsectionstart/)(bool) | Establece un valor que indica si el [SectionStart](../../aspose.words/pagesetup/get_sectionstart/) de la primera sección del documento y sus copias para filas posteriores de la fuente de datos se conservan durante la combinación de correspondencia o se actualizan según el comportamiento de MS Word. |
| [set_TrimWhitespaces](./set_trimwhitespaces/)(bool) | Establece un valor que indica si los espacios en blanco iniciales y finales se recortan de los valores de combinación de correspondencia. |
| [set_UnconditionalMergeFieldsAndRegions](./set_unconditionalmergefieldsandregions/)(bool) | Establece un valor que indica si los campos de combinación y las regiones de combinación se fusionan sin importar la condición del campo IF padre. |
| [set_UseNonMergeFields](./set_usenonmergefields/)(bool) | Método set para [Aspose::Words::MailMerging::MailMerge::get_UseNonMergeFields](./get_usenonmergefields/). |
| [set_UseWholeParagraphAsRegion](./set_usewholeparagraphasregion/)(bool) | Establece un valor que indica si todo el párrafo con el campo **TableStart** o **TableEnd**, o un rango particular entre los campos **TableStart** y **TableEnd**, debe incluirse en la región de combinación de correspondencia. |
| static [Type](./type/)() |  |
## Observaciones


Para que la operación de combinación de correspondencia funcione, el documento debe contener campos MERGEFIELD de Word y, opcionalmente, campos NEXT. Durante la operación de combinación de correspondencia, los campos de combinación en el documento se reemplazan con valores de su fuente de datos.

Hay dos formas distintas de usar la combinación de correspondencia: con regiones de combinación de correspondencia y sin ellas.

La combinación de correspondencia más simple es sin regiones y es muy similar a cómo funciona la combinación de correspondencia en Word. Use los métodos **Execute** para combinar información de alguna fuente de datos como **DataTable**, **DataSet** o una matriz de objetos en su documento. El objeto [MailMerge](./) procesa todos los registros de la fuente de datos y copia y agrega el contenido de todo el documento para cada registro.

Tenga en cuenta que cuando el objeto [MailMerge](./) encuentra un campo NEXT, selecciona el siguiente registro en la fuente de datos y continúa la combinación sin copiar ningún contenido.

Use [ExecuteWithRegions()](../) y otras sobrecargas para combinar información en un documento con regiones de combinación de correspondencia definidas. Puede utilizarlas como fuentes de datos para esta operación.

Necesita usar regiones de combinación de correspondencia si desea ampliar dinámicamente secciones dentro del documento. Sin regiones de combinación de correspondencia, todo el documento se repetirá para cada registro de la fuente de datos.

## Ver también

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
