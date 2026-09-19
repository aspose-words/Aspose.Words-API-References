---
title: "Aspose::Words::Fields::FormField classe"
linktitle: "FormField"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FormField classe. Rappresenta un singolo campo modulo. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 112000
url: /it/cpp/aspose.words.fields/formfield/
---
## FormField class


Rappresenta un singolo campo modulo. Per saperne di più, visita l'articolo di documentazione [Working with Form Fields](https://docs.aspose.com/words/cpp/working-with-form-fields/).

```cpp
class FormField : public Aspose::Words::SpecialChar
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accetta un visitatore. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicato del nodo. |
| [get_CalculateOnExit](./get_calculateonexit/)() | Vero se i riferimenti al campo modulo specificato vengono aggiornati automaticamente ogni volta che il campo viene abbandonato. |
| [get_CheckBoxSize](./get_checkboxsize/)() | Ottiene o imposta la dimensione della casella di controllo in punti. Ha effetto solo quando [IsCheckBoxExactSize](./get_ischeckboxexactsize/) è **true**. |
| [get_Checked](./get_checked/)() | Ottiene o imposta lo stato selezionato del campo modulo casella di controllo. Il valore predefinito per questa proprietà è **false**. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Specifica un identificatore personalizzato per il nodo. |
| [get_Default](./get_default/)() | Ottiene o imposta il valore predefinito del campo modulo casella di controllo. Il valore predefinito per questa proprietà è **false**. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Ottiene il documento a cui appartiene questo nodo. |
| [get_DropDownItems](./get_dropdownitems/)() | Fornisce l'accesso agli elementi di un campo modulo a discesa. |
| [get_DropDownSelectedIndex](./get_dropdownselectedindex/)() | Ottiene l'indice che specifica l'elemento attualmente selezionato in un campo modulo a discesa. |
| [get_Enabled](./get_enabled/)() | Vero se un campo modulo è abilitato. |
| [get_EntryMacro](./get_entrymacro/)() | Restituisce o imposta il nome della macro di ingresso per il campo modulo. |
| [get_ExitMacro](./get_exitmacro/)() | Restituisce o imposta il nome della macro di uscita per il campo modulo. |
| [get_Font](../../aspose.words/inline/get_font/)() | Fornisce l'accesso alla formattazione del carattere di questo oggetto. |
| [get_HelpText](./get_helptext/)() | Restituisce o imposta il testo visualizzato in una finestra di messaggio quando il campo modulo ha il focus e l'utente preme F1. |
| [get_IsCheckBoxExactSize](./get_ischeckboxexactsize/)() | Ottiene o imposta il valore booleano che indica se la dimensione della casella di testo è automatica o specificata esplicitamente. |
| virtual [get_IsComposite](../../aspose.words/node/get_iscomposite/)() | Restituisce **true** se questo nodo può contenere altri nodi. |
| [get_IsDeleteRevision](../../aspose.words/inline/get_isdeleterevision/)() | Restituisce true se questo oggetto è stato eliminato in Microsoft Word mentre il tracciamento delle modifiche era abilitato. |
| [get_IsFormatRevision](../../aspose.words/inline/get_isformatrevision/)() | Restituisce true se la formattazione dell'oggetto è stata modificata in Microsoft Word mentre il tracciamento delle modifiche era abilitato. |
| [get_IsInsertRevision](../../aspose.words/inline/get_isinsertrevision/)() | Restituisce true se questo oggetto è stato inserito in Microsoft Word mentre il tracciamento delle modifiche era abilitato. |
| [get_IsMoveFromRevision](../../aspose.words/inline/get_ismovefromrevision/)() | Restituisce **true** se questo oggetto è stato spostato (eliminato) in Microsoft Word mentre il tracciamento delle modifiche era abilitato. |
| [get_IsMoveToRevision](../../aspose.words/inline/get_ismovetorevision/)() | Restituisce **true** se questo oggetto è stato spostato (inserito) in Microsoft Word mentre il tracciamento delle modifiche era abilitato. |
| [get_MaxLength](./get_maxlength/)() | Lunghezza massima per il campo di testo. Zero quando la lunghezza non è limitata. |
| [get_Name](./get_name/)() | Ottiene o imposta il nome del campo modulo. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Ottiene il nodo immediatamente successivo a questo nodo. |
| [get_NodeType](./get_nodetype/)() const override | Restituisce [FormField](../../aspose.words/nodetype/). |
| [get_OwnHelp](./get_ownhelp/)() | Specifica l'origine del testo visualizzato in una finestra di messaggio quando un campo modulo ha il focus e l'utente preme F1. |
| [get_OwnStatus](./get_ownstatus/)() | Specifica l'origine del testo visualizzato nella barra di stato quando un campo modulo ha il focus. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Ottiene il genitore immediato di questo nodo. |
| [get_ParentParagraph](../../aspose.words/inline/get_parentparagraph/)() | Recupera il [Paragraph](../../aspose.words/paragraph/) genitore di questo nodo. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Ottiene il nodo immediatamente precedente a questo nodo. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Restituisce un oggetto [Range](../../aspose.words/range/) che rappresenta la porzione di un documento contenuta in questo nodo. |
| [get_Result](./get_result/)() | Ottiene o imposta una stringa che rappresenta il risultato di questo campo modulo. |
| [get_StatusText](./get_statustext/)() | Restituisce o imposta il testo visualizzato nella barra di stato quando un campo modulo ha il focus. |
| [get_TextInputDefault](./get_textinputdefault/)() | Ottiene o imposta la stringa predefinita o un'espressione di calcolo di un campo modulo di testo. |
| [get_TextInputFormat](./get_textinputformat/)() | Restituisce o imposta la formattazione del testo per un campo modulo di testo. |
| [get_TextInputType](./get_textinputtype/)() | Ottiene il tipo di un campo modulo di testo. |
| [get_Type](./get_type/)() | Restituisce il tipo di campo modulo. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Ottiene il primo antenato del [NodeType](../../aspose.words/nodetype/) specificato. |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetText](../../aspose.words/specialchar/gettext/)() override | Ottiene il carattere speciale che questo nodo rappresenta. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ottiene il nodo successivo secondo l'algoritmo di attraversamento dell'albero in pre-ordine. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Un metodo di utilità che converte un valore enum di tipo nodo in una stringa leggibile dall'utente. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ottiene il nodo precedente secondo l'algoritmo di attraversamento dell'albero in pre-ordine. |
| [Remove](../../aspose.words/node/remove/)() | Rimuove se stesso dal genitore. |
| [RemoveField](./removefield/)() | Rimuove l'intero campo modulo, non solo il carattere speciale del campo modulo. |
| [set_CalculateOnExit](./set_calculateonexit/)(bool) | Impostatore per [Aspose::Words::Fields::FormField::get_CalculateOnExit](./get_calculateonexit/). |
| [set_CheckBoxSize](./set_checkboxsize/)(double) | Impostatore per [Aspose::Words::Fields::FormField::get_CheckBoxSize](./get_checkboxsize/). |
| [set_Checked](./set_checked/)(bool) | Impostatore per [Aspose::Words::Fields::FormField::get_Checked](./get_checked/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Setter per [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_Default](./set_default/)(bool) | Impostatore per [Aspose::Words::Fields::FormField::get_Default](./get_default/). |
| [set_DropDownSelectedIndex](./set_dropdownselectedindex/)(int32_t) | Imposta l'indice che specifica l'elemento attualmente selezionato in un campo modulo a discesa. |
| [set_Enabled](./set_enabled/)(bool) | Vero se un campo modulo è abilitato. |
| [set_EntryMacro](./set_entrymacro/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FormField::get_EntryMacro](./get_entrymacro/). |
| [set_ExitMacro](./set_exitmacro/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FormField::get_ExitMacro](./get_exitmacro/). |
| [set_HelpText](./set_helptext/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FormField::get_HelpText](./get_helptext/). |
| [set_IsCheckBoxExactSize](./set_ischeckboxexactsize/)(bool) | Impostatore per [Aspose::Words::Fields::FormField::get_IsCheckBoxExactSize](./get_ischeckboxexactsize/). |
| [set_MaxLength](./set_maxlength/)(int32_t) | Lunghezza massima per il campo di testo. Zero quando la lunghezza non è limitata. |
| [set_Name](./set_name/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FormField::get_Name](./get_name/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_OwnHelp](./set_ownhelp/)(bool) | Impostatore per [Aspose::Words::Fields::FormField::get_OwnHelp](./get_ownhelp/). |
| [set_OwnStatus](./set_ownstatus/)(bool) | Impostatore per [Aspose::Words::Fields::FormField::get_OwnStatus](./get_ownstatus/). |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Result](./set_result/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FormField::get_Result](./get_result/). |
| [set_StatusText](./set_statustext/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FormField::get_StatusText](./get_statustext/). |
| [set_TextInputDefault](./set_textinputdefault/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FormField::get_TextInputDefault](./get_textinputdefault/). |
| [set_TextInputFormat](./set_textinputformat/)(const System::String\&) | Impostatore per [Aspose::Words::Fields::FormField::get_TextInputFormat](./get_textinputformat/). |
| [set_TextInputType](./set_textinputtype/)(Aspose::Words::Fields::TextFormFieldType) | Imposta il tipo di un campo modulo di testo. |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTextInputValue](./settextinputvalue/)(const System::SharedPtr\<System::Object\>\&) | Applica il formato di testo specificato in [TextInputFormat](./get_textinputformat/) e memorizza il valore in [Result](./get_result/). |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Esporta il contenuto del nodo in una stringa usando le opzioni di salvataggio specificate. |
| static [Type](./type/)() |  |
## Note


Microsoft Word fornisce i seguenti campi modulo: casella di controllo, input di testo e elenco a discesa (combobox).

[FormField](./) is an inline-node and can only be a child of [Paragraph](../../aspose.words/paragraph/).

[FormField](./) is represented in a document by a special character and positioned as a character within a line of text.

Un campo modulo completo in un documento Word è una struttura complessa rappresentata da diversi nodi: inizio campo, codice campo come FORMTEXT, dati del campo modulo, separatore di campo, risultato del campo, fine campo e un segnalibro. Per creare programmaticamente campi modulo in un documento Word usa [InsertCheckBox()](../), [InsertTextInput()](../) e [InsertComboBox()](../) che garantiscono che tutti i nodi del campo modulo siano creati nell'ordine corretto e in uno stato appropriato.

## Esempi



Mostra come inserire una casella combinata.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Please select a fruit: ");

// Inserisci una casella combinata che consentirà all'utente di scegliere un'opzione da una raccolta di stringhe.
System::SharedPtr<Aspose::Words::Fields::FormField> comboBox = builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"Apple", u"Banana", u"Cherry"}), 0);

ASSERT_EQ(u"MyComboBox", comboBox->get_Name());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldFormDropDown, comboBox->get_Type());
ASSERT_EQ(u"Apple", comboBox->get_Result());

// Il campo modulo apparirà sotto forma di tag html "select".
doc->Save(get_ArtifactsDir() + u"FormFields.Create.html");
```


Mostra come formattare l'intero [FormField](./), incluso il valore del campo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Form fields.docx");

System::SharedPtr<Aspose::Words::Fields::FormField> formField = doc->get_Range()->get_FormFields()->idx_get(0);
formField->get_Font()->set_Bold(true);
formField->get_Font()->set_Size(24);
formField->get_Font()->set_Color(System::Drawing::Color::get_Red());

formField->set_Result(u"Aspose.FormField");

doc = Aspose::Words::ApiExamples::DocumentHelper::SaveOpen(doc);

System::SharedPtr<Aspose::Words::Run> formFieldRun = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(1);

ASSERT_EQ(u"Aspose.FormField", formFieldRun->get_Text());
ASPOSE_ASSERT_EQ(true, formFieldRun->get_Font()->get_Bold());
ASPOSE_ASSERT_EQ(24, formFieldRun->get_Font()->get_Size());
ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), formFieldRun->get_Font()->get_Color().ToArgb());
```

## Vedi anche

* Class [SpecialChar](../../aspose.words/specialchar/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
