---
title: "Clase Aspose::Words::LowCode::MailMergeOptions"
linktitle: "MailMergeOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::LowCode::MailMergeOptions. Representa opciones para la funcionalidad de combinación de correspondencia en C++."
type: docs
weight: 750
url: /es/cpp/aspose.words.lowcode/mailmergeoptions/
---
## MailMergeOptions class


Representa opciones para la funcionalidad de combinación de correspondencia.

```cpp
class MailMergeOptions : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_CleanupOptions](./get_cleanupoptions/)() const | Obtiene un conjunto de indicadores que especifican qué elementos deben eliminarse durante la combinación de correspondencia. |
| [get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/)() const | Obtiene o establece un valor que indica si los párrafos con signos de puntuación se consideran vacíos y deben eliminarse si se especifica la opción [RemoveEmptyParagraphs](../../aspose.words.mailmerging/mailmergecleanupoptions/). |
| [get_MergeDuplicateRegions](./get_mergeduplicateregions/)() const | Obtiene un valor que indica si todas las regiones de combinación de correspondencia del documento con el nombre de una fuente de datos deben fusionarse al ejecutar una combinación de correspondencia con regiones contra la fuente de datos o solo la primera. |
| [get_MergeWholeDocument](./get_mergewholedocument/)() const | Obtiene un valor que indica si los campos en todo el documento se actualizan al ejecutar una combinación de correspondencia con regiones. |
| [get_PreserveUnusedTags](./get_preserveunusedtags/)() const | Obtiene un valor que indica si las etiquetas "mustache" no utilizadas deben conservarse. |
| [get_RegionEndTag](./get_regionendtag/)() const | Obtiene la etiqueta de fin de región de combinación de correspondencia. |
| [get_RegionStartTag](./get_regionstarttag/)() const | Obtiene la etiqueta de inicio de región de combinación de correspondencia. |
| [get_RestartListsAtEachSection](./get_restartlistsateachsection/)() const | Obtiene un valor que indica si las listas se reinician en cada sección después de ejecutar una combinación de correspondencia. |
| [get_RetainFirstSectionStart](./get_retainfirstsectionstart/)() const | Obtiene un valor que indica si el inicio de sección de la primera sección del documento y sus copias para filas posteriores de la fuente de datos se conservan durante la combinación de correspondencia o se actualizan según el comportamiento de MS Word. |
| [get_TrimWhitespaces](./get_trimwhitespaces/)() const | Obtiene un valor que indica si los espacios en blanco iniciales y finales se recortan de los valores de combinación de correspondencia. |
| [get_UnconditionalMergeFieldsAndRegions](./get_unconditionalmergefieldsandregions/)() const | Obtiene un valor que indica si los campos de combinación y las regiones de combinación se fusionan sin importar la condición del campo IF padre. |
| [get_UseNonMergeFields](./get_usenonmergefields/)() const | Cuando **true**, especifica que, además de los campos MERGEFIELD, la combinación de correspondencia se realiza en algunos otros tipos de campos y también en etiquetas "{{fieldName}}". |
| [get_UseWholeParagraphAsRegion](./get_usewholeparagraphasregion/)() const | Obtiene un valor que indica si todo el párrafo con el campo **TableStart** o **TableEnd**, o un rango particular entre los campos **TableStart** y **TableEnd**, debe incluirse en la región de combinación de correspondencia. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MailMergeOptions](./mailmergeoptions/)() |  |
| [set_CleanupOptions](./set_cleanupoptions/)(Aspose::Words::MailMerging::MailMergeCleanupOptions) | Establece un conjunto de indicadores que especifican qué elementos deben eliminarse durante la combinación de correspondencia. |
| [set_CleanupParagraphsWithPunctuationMarks](./set_cleanupparagraphswithpunctuationmarks/)(bool) | Método set para [Aspose::Words::LowCode::MailMergeOptions::get_CleanupParagraphsWithPunctuationMarks](./get_cleanupparagraphswithpunctuationmarks/). |
| [set_MergeDuplicateRegions](./set_mergeduplicateregions/)(bool) | Establece un valor que indica si todas las regiones de combinación de correspondencia del documento con el nombre de una fuente de datos deben fusionarse al ejecutar una combinación de correspondencia con regiones contra la fuente de datos o solo la primera. |
| [set_MergeWholeDocument](./set_mergewholedocument/)(bool) | Establece un valor que indica si los campos en todo el documento se actualizan al ejecutar una combinación de correspondencia con regiones. |
| [set_PreserveUnusedTags](./set_preserveunusedtags/)(bool) | Establece un valor que indica si las etiquetas "mustache" no utilizadas deben conservarse. |
| [set_RegionEndTag](./set_regionendtag/)(const System::String\&) | Establece una etiqueta de fin de región de combinación de correspondencia. |
| [set_RegionStartTag](./set_regionstarttag/)(const System::String\&) | Establece una etiqueta de inicio de región de combinación de correspondencia. |
| [set_RestartListsAtEachSection](./set_restartlistsateachsection/)(bool) | Establece un valor que indica si las listas se reinician en cada sección después de ejecutar una combinación de correspondencia. |
| [set_RetainFirstSectionStart](./set_retainfirstsectionstart/)(bool) | Establece un valor que indica si el inicio de sección de la primera sección del documento y sus copias para filas posteriores de la fuente de datos se conservan durante la combinación de correspondencia o se actualizan según el comportamiento de MS Word. |
| [set_TrimWhitespaces](./set_trimwhitespaces/)(bool) | Establece un valor que indica si los espacios en blanco iniciales y finales se recortan de los valores de combinación de correspondencia. |
| [set_UnconditionalMergeFieldsAndRegions](./set_unconditionalmergefieldsandregions/)(bool) | Establece un valor que indica si los campos de combinación y las regiones de combinación se fusionan sin importar la condición del campo IF padre. |
| [set_UseNonMergeFields](./set_usenonmergefields/)(bool) | Método set para [Aspose::Words::LowCode::MailMergeOptions::get_UseNonMergeFields](./get_usenonmergefields/). |
| [set_UseWholeParagraphAsRegion](./set_usewholeparagraphasregion/)(bool) | Establece un valor que indica si todo el párrafo con el campo **TableStart** o **TableEnd**, o un rango particular entre los campos **TableStart** y **TableEnd**, debe incluirse en la región de combinación de correspondencia. |
| static [Type](./type/)() |  |
## Ver también

* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
