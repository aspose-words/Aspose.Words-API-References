---
title: "Aspose::Words::Replacing::FindReplaceOptions clase"
linktitle: "FindReplaceOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Replacing::FindReplaceOptions clase. Especifica opciones para operaciones de búsqueda/reemplazo. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 1000
url: /es/cpp/aspose.words.replacing/findreplaceoptions/
---
## FindReplaceOptions class


Especifica opciones para operaciones de búsqueda/reemplazo. Para obtener más información, visite el artículo de documentación [Find and Replace](https://docs.aspose.com/words/cpp/find-and-replace/).

```cpp
class FindReplaceOptions : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [FindReplaceOptions](./findreplaceoptions/)() | Inicializa una nueva instancia de la clase [FindReplaceOptions](./) con la configuración predeterminada. |
| [FindReplaceOptions](./findreplaceoptions/)(Aspose::Words::Replacing::FindReplaceDirection) | Inicializa una nueva instancia de la clase [FindReplaceOptions](./) con la dirección especificada. |
| [FindReplaceOptions](./findreplaceoptions/)(const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) | Inicializa una nueva instancia de la clase [FindReplaceOptions](./) con la devolución de llamada de reemplazo especificada. |
| [FindReplaceOptions](./findreplaceoptions/)(Aspose::Words::Replacing::FindReplaceDirection, const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) | Inicializa una nueva instancia de la clase [FindReplaceOptions](./) con la dirección y la devolución de llamada de reemplazo especificadas. |
| [get_ApplyFont](./get_applyfont/)() const | Formato de texto aplicado al contenido nuevo. |
| [get_ApplyParagraphFormat](./get_applyparagraphformat/)() const | Formato de [Paragraph](../../aspose.words/paragraph/) aplicado al contenido nuevo. |
| [get_Direction](./get_direction/)() const | Selecciona la dirección para el reemplazo. El valor predeterminado es [Forward](../findreplacedirection/). |
| [get_FindWholeWordsOnly](./get_findwholewordsonly/)() const | True indica que oldValue debe ser una palabra independiente. |
| [get_IgnoreDeleted](./get_ignoredeleted/)() const | Obtiene o establece un valor booleano que indica si se debe ignorar el texto dentro de revisiones de eliminación. El valor predeterminado es **false**. |
| [get_IgnoreFieldCodes](./get_ignorefieldcodes/)() const | Obtiene o establece un valor booleano que indica si se debe ignorar el texto dentro de códigos de campo. El valor predeterminado es **false**. |
| [get_IgnoreFields](./get_ignorefields/)() const | Obtiene o establece un valor booleano que indica si se debe ignorar el texto dentro de campos. El valor predeterminado es **false**. |
| [get_IgnoreFootnotes](./get_ignorefootnotes/)() const | Obtiene o establece un valor booleano que indica si se deben ignorar las notas al pie. El valor predeterminado es **false**. |
| [get_IgnoreInserted](./get_ignoreinserted/)() const | Obtiene o establece un valor booleano que indica si se debe ignorar el texto dentro de revisiones de inserción. El valor predeterminado es **false**. |
| [get_IgnoreOfficeMath](./get_ignoreofficemath/)() const | Obtiene o establece un valor booleano que indica si se debe ignorar el texto dentro de OfficeMath/>. El valor predeterminado es **true**. |
| [get_IgnoreShapes](./get_ignoreshapes/)() const | Obtiene o establece un valor booleano que indica si se deben ignorar las formas dentro de un texto. El valor predeterminado es **false**. |
| [get_IgnoreStructuredDocumentTags](./get_ignorestructureddocumenttags/)() const | Obtiene o establece un valor booleano que indica si se debe ignorar el contenido de [StructuredDocumentTag](../../aspose.words.markup/structureddocumenttag/). El valor predeterminado es **false**. |
| [get_LegacyMode](./get_legacymode/)() const | Obtiene o establece un valor booleano que indica que se utiliza el algoritmo antiguo de búsqueda/reemplazo. |
| [get_MatchCase](./get_matchcase/)() const | True indica comparación sensible a mayúsculas y minúsculas, false indica comparación insensible a mayúsculas y minúsculas. |
| [get_ReplacementFormat](./get_replacementformat/)() const | Especifica el formato del reemplazo. El valor predeterminado es [Text](../replacementformat/). |
| [get_ReplacingCallback](./get_replacingcallback/)() const | El método definido por el usuario que se llama antes de cada aparición de reemplazo. |
| [get_SmartParagraphBreakReplacement](./get_smartparagraphbreakreplacement/)() const | Obtiene o establece un valor booleano que indica si se permite reemplazar el salto de párrafo cuando no hay un párrafo hermano siguiente. El valor predeterminado es **false**. |
| [get_UseLegacyOrder](./get_uselegacyorder/)() const | True indica que una búsqueda de texto se realiza secuencialmente de arriba a abajo considerando los cuadros de texto. El valor predeterminado es **false**. |
| [get_UseSubstitutions](./get_usesubstitutions/)() const | Obtiene o establece un valor booleano que indica si se deben reconocer y usar sustituciones dentro de los patrones de reemplazo. El valor predeterminado es **false**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Direction](./set_direction/)(Aspose::Words::Replacing::FindReplaceDirection) | Selecciona la dirección para el reemplazo. El valor predeterminado es [Forward](../findreplacedirection/). |
| [set_FindWholeWordsOnly](./set_findwholewordsonly/)(bool) | Método set para [Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly](./get_findwholewordsonly/). |
| [set_IgnoreDeleted](./set_ignoredeleted/)(bool) | Método set para [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted](./get_ignoredeleted/). |
| [set_IgnoreFieldCodes](./set_ignorefieldcodes/)(bool) | Método set para [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFieldCodes](./get_ignorefieldcodes/). |
| [set_IgnoreFields](./set_ignorefields/)(bool) | Método set para [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFields](./get_ignorefields/). |
| [set_IgnoreFootnotes](./set_ignorefootnotes/)(bool) | Método set para [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes](./get_ignorefootnotes/). |
| [set_IgnoreInserted](./set_ignoreinserted/)(bool) | Método set para [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreInserted](./get_ignoreinserted/). |
| [set_IgnoreOfficeMath](./set_ignoreofficemath/)(bool) | Método set para [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreOfficeMath](./get_ignoreofficemath/). |
| [set_IgnoreShapes](./set_ignoreshapes/)(bool) | Método set para [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreShapes](./get_ignoreshapes/). |
| [set_IgnoreStructuredDocumentTags](./set_ignorestructureddocumenttags/)(bool) | Método set para [Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags](./get_ignorestructureddocumenttags/). |
| [set_LegacyMode](./set_legacymode/)(bool) | Método set para [Aspose::Words::Replacing::FindReplaceOptions::get_LegacyMode](./get_legacymode/). |
| [set_MatchCase](./set_matchcase/)(bool) | Método set para [Aspose::Words::Replacing::FindReplaceOptions::get_MatchCase](./get_matchcase/). |
| [set_ReplacementFormat](./set_replacementformat/)(Aspose::Words::Replacing::ReplacementFormat) | Especifica el formato del reemplazo. El valor predeterminado es [Text](../replacementformat/). |
| [set_ReplacingCallback](./set_replacingcallback/)(const System::SharedPtr\<Aspose::Words::Replacing::IReplacingCallback\>\&) | El método definido por el usuario que se llama antes de cada aparición de reemplazo. |
| [set_SmartParagraphBreakReplacement](./set_smartparagraphbreakreplacement/)(bool) | Método set para [Aspose::Words::Replacing::FindReplaceOptions::get_SmartParagraphBreakReplacement](./get_smartparagraphbreakreplacement/). |
| [set_UseLegacyOrder](./set_uselegacyorder/)(bool) | True indica que una búsqueda de texto se realiza secuencialmente de arriba a abajo considerando los cuadros de texto. El valor predeterminado es **false**. |
| [set_UseSubstitutions](./set_usesubstitutions/)(bool) | Método set para [Aspose::Words::Replacing::FindReplaceOptions::get_UseSubstitutions](./get_usesubstitutions/). |
| static [Type](./type/)() |  |

## Ejemplos



Muestra cómo alternar la sensibilidad a mayúsculas y minúsculas al realizar una operación de buscar y reemplazar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Ruby bought a ruby necklace.");

// Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de buscar y reemplazar.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Establezca la bandera "MatchCase" a "true" para aplicar sensibilidad a mayúsculas y minúsculas al buscar cadenas para reemplazar.
// Establezca la bandera "MatchCase" a "false" para ignorar mayúsculas y minúsculas al buscar texto para reemplazar.
options->set_MatchCase(matchCase);

doc->get_Range()->Replace(u"Ruby", u"Jade", options);

ASSERT_EQ(matchCase ? System::String(u"Jade bought a ruby necklace.") : System::String(u"Jade bought a Jade necklace."), doc->GetText().Trim());
```


Muestra cómo alternar operaciones de buscar y reemplazar que solo afectan palabras independientes.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Jackson will meet you in Jacksonville.");

// Podemos usar un objeto "FindReplaceOptions" para modificar el proceso de buscar y reemplazar.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Establezca la bandera "FindWholeWordsOnly" a "true" para reemplazar el texto encontrado si no forma parte de otra palabra.
// Establezca la bandera "FindWholeWordsOnly" a "false" para reemplazar todo el texto sin importar su contexto.
options->set_FindWholeWordsOnly(findWholeWordsOnly);

doc->get_Range()->Replace(u"Jackson", u"Louis", options);

ASSERT_EQ(findWholeWordsOnly ? System::String(u"Louis will meet you in Jacksonville.") : System::String(u"Louis will meet you in Louisville."), doc->GetText().Trim());
```

## Ver también

* Namespace [Aspose::Words::Replacing](../)
* Library [Aspose.Words for C++](../../)
