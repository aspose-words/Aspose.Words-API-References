---
title: "Aspose::Words::Fields::FormField class"
linktitle: "FormField"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::FormField class. Representerar ett enskilt formulärfält. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 112000
url: /sv/cpp/aspose.words.fields/formfield/
---
## FormField class


Representerar ett enda formulärfält. För att lära dig mer, besök [Working with Form Fields](https://docs.aspose.com/words/cpp/working-with-form-fields/) dokumentationsartikel.

```cpp
class FormField : public Aspose::Words::SpecialChar
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepterar en besökare. |
| [Clone](../../aspose.words/node/clone/)(bool) | Skapar en kopia av noden. |
| [get_CalculateOnExit](./get_calculateonexit/)() | Sant om referenser till det angivna formulärfältet uppdateras automatiskt när fältet lämnas. |
| [get_CheckBoxSize](./get_checkboxsize/)() | Hämtar eller anger storleken på kryssrutan i punkter. Har effekt endast när [IsCheckBoxExactSize](./get_ischeckboxexactsize/) är **true**. |
| [get_Checked](./get_checked/)() | Hämtar eller anger den markerade statusen för kryssrutan i formulärfältet. Standardvärdet för denna egenskap är **false**. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Anger en anpassad nodidentifierare. |
| [get_Default](./get_default/)() | Hämtar eller anger standardvärdet för kryssrutan i formulärfältet. Standardvärdet för denna egenskap är **false**. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Hämtar dokumentet som denna nod tillhör. |
| [get_DropDownItems](./get_dropdownitems/)() | Tillhandahåller åtkomst till objekten i ett rullgardinsformulärfält. |
| [get_DropDownSelectedIndex](./get_dropdownselectedindex/)() | Hämtar indexet som anger det för närvarande valda objektet i ett rullgardinsformulärfält. |
| [get_Enabled](./get_enabled/)() | Sant om ett formulärfält är aktiverat. |
| [get_EntryMacro](./get_entrymacro/)() | Returnerar eller anger ett namn på inträdesmakro för formulärfältet. |
| [get_ExitMacro](./get_exitmacro/)() | Returnerar eller anger ett namn på avslutningsmakro för formulärfältet. |
| [get_Font](../../aspose.words/inline/get_font/)() | Tillhandahåller åtkomst till teckensnittsformateringen för detta objekt. |
| [get_HelpText](./get_helptext/)() | Returnerar eller anger texten som visas i en meddelanderuta när formulärfältet har fokus och användaren trycker på F1. |
| [get_IsCheckBoxExactSize](./get_ischeckboxexactsize/)() | Hämtar eller anger det booleska värdet som indikerar om storleken på textrutan är automatisk eller specificerad explicit. |
| virtual [get_IsComposite](../../aspose.words/node/get_iscomposite/)() | Returnerar **true** om denna nod kan innehålla andra noder. |
| [get_IsDeleteRevision](../../aspose.words/inline/get_isdeleterevision/)() | Returnerar true om detta objekt raderades i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_IsFormatRevision](../../aspose.words/inline/get_isformatrevision/)() | Returnerar true om formateringen av objektet ändrades i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_IsInsertRevision](../../aspose.words/inline/get_isinsertrevision/)() | Returnerar true om detta objekt infogades i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_IsMoveFromRevision](../../aspose.words/inline/get_ismovefromrevision/)() | Returnerar **true** om detta objekt flyttades (raderades) i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_IsMoveToRevision](../../aspose.words/inline/get_ismovetorevision/)() | Returnerar **true** om detta objekt flyttades (infogades) i Microsoft Word medan spårning av ändringar var aktiverad. |
| [get_MaxLength](./get_maxlength/)() | Maximal längd för textfältet. Noll när längden inte är begränsad. |
| [get_Name](./get_name/)() | Hämtar eller anger formulärfältets namn. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Hämtar noden som omedelbart följer denna nod. |
| [get_NodeType](./get_nodetype/)() const override | Returnerar [FormField](../../aspose.words/nodetype/). |
| [get_OwnHelp](./get_ownhelp/)() | Anger källan till texten som visas i en meddelanderuta när ett formulärfält har fokus och användaren trycker på F1. |
| [get_OwnStatus](./get_ownstatus/)() | Anger källan till texten som visas i statusfältet när ett formulärfält har fokus. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Hämtar den omedelbara föräldern till den här noden. |
| [get_ParentParagraph](../../aspose.words/inline/get_parentparagraph/)() | Hämtar föräldern [Paragraph](../../aspose.words/paragraph/) till denna nod. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Hämtar noden som omedelbart föregår den här noden. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Returnerar ett [Range](../../aspose.words/range/)‑objekt som representerar den del av ett dokument som finns i den här noden. |
| [get_Result](./get_result/)() | Hämtar eller anger en sträng som representerar resultatet av detta formulärfält. |
| [get_StatusText](./get_statustext/)() | Returnerar eller anger texten som visas i statusfältet när ett formulärfält har fokus. |
| [get_TextInputDefault](./get_textinputdefault/)() | Hämtar eller anger standardsträngen eller ett beräkningsuttryck för ett textformulärfält. |
| [get_TextInputFormat](./get_textinputformat/)() | Returnerar eller anger textformateringen för ett textformulärfält. |
| [get_TextInputType](./get_textinputtype/)() | Hämtar typen av ett textformulärfält. |
| [get_Type](./get_type/)() | Returnerar formulärfältets typ. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Hämtar den första förfadern av den angivna [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetText](../../aspose.words/specialchar/gettext/)() override | Hämtar det speciella tecknet som denna nod representerar. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Hämtar nästa nod enligt pre‑order‑trädtraverseringsalgoritmen. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | En hjälpfunktion som konverterar ett nodtyp‑enumvärde till en användarvänlig sträng. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Hämtar föregående nod enligt pre‑order‑trädtraverseringsalgoritmen. |
| [Remove](../../aspose.words/node/remove/)() | Tar bort sig själv från föräldern. |
| [RemoveField](./removefield/)() | Tar bort hela formulärfältet, inte bara det speciella tecknet för formulärfältet. |
| [set_CalculateOnExit](./set_calculateonexit/)(bool) | Sättare för [Aspose::Words::Fields::FormField::get_CalculateOnExit](./get_calculateonexit/). |
| [set_CheckBoxSize](./set_checkboxsize/)(double) | Sättare för [Aspose::Words::Fields::FormField::get_CheckBoxSize](./get_checkboxsize/). |
| [set_Checked](./set_checked/)(bool) | Sättare för [Aspose::Words::Fields::FormField::get_Checked](./get_checked/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Sättare för [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_Default](./set_default/)(bool) | Sättare för [Aspose::Words::Fields::FormField::get_Default](./get_default/). |
| [set_DropDownSelectedIndex](./set_dropdownselectedindex/)(int32_t) | Anger index som specificerar det för närvarande valda objektet i ett rullgardinsformulärfält. |
| [set_Enabled](./set_enabled/)(bool) | Sant om ett formulärfält är aktiverat. |
| [set_EntryMacro](./set_entrymacro/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FormField::get_EntryMacro](./get_entrymacro/). |
| [set_ExitMacro](./set_exitmacro/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FormField::get_ExitMacro](./get_exitmacro/). |
| [set_HelpText](./set_helptext/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FormField::get_HelpText](./get_helptext/). |
| [set_IsCheckBoxExactSize](./set_ischeckboxexactsize/)(bool) | Sättare för [Aspose::Words::Fields::FormField::get_IsCheckBoxExactSize](./get_ischeckboxexactsize/). |
| [set_MaxLength](./set_maxlength/)(int32_t) | Maximal längd för textfältet. Noll när längden inte är begränsad. |
| [set_Name](./set_name/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FormField::get_Name](./get_name/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_OwnHelp](./set_ownhelp/)(bool) | Sättare för [Aspose::Words::Fields::FormField::get_OwnHelp](./get_ownhelp/). |
| [set_OwnStatus](./set_ownstatus/)(bool) | Sättare för [Aspose::Words::Fields::FormField::get_OwnStatus](./get_ownstatus/). |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Result](./set_result/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FormField::get_Result](./get_result/). |
| [set_StatusText](./set_statustext/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FormField::get_StatusText](./get_statustext/). |
| [set_TextInputDefault](./set_textinputdefault/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FormField::get_TextInputDefault](./get_textinputdefault/). |
| [set_TextInputFormat](./set_textinputformat/)(const System::String\&) | Sättare för [Aspose::Words::Fields::FormField::get_TextInputFormat](./get_textinputformat/). |
| [set_TextInputType](./set_textinputtype/)(Aspose::Words::Fields::TextFormFieldType) | Anger typen av ett textformulärfält. |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTextInputValue](./settextinputvalue/)(const System::SharedPtr\<System::Object\>\&) | Tillämpar textformatet som specificerats i [TextInputFormat](./get_textinputformat/) och lagrar värdet i [Result](./get_result/). |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exporterar innehållet i noden till en sträng i det angivna formatet. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporterar innehållet i noden till en sträng med de angivna sparalternativen. |
| static [Type](./type/)() |  |
## Anmärkningar


Microsoft Word tillhandahåller följande formulärfält: kryssruta, textinmatning och rullgardin (kombinationsruta).

[FormField](./) is an inline-node and can only be a child of [Paragraph](../../aspose.words/paragraph/).

[FormField](./) is represented in a document by a special character and positioned as a character within a line of text.

Ett komplett formulärfält i ett Word-dokument är en komplex struktur som representeras av flera noder: fältstart, fältkod såsom FORMTEXT, formulärfältsdata, fältseparator, fältresultat, fältavslut och ett bokmärke. För att programatiskt skapa formulärfält i ett Word-dokument, använd [InsertCheckBox()](../), [InsertTextInput()](../) och [InsertComboBox()](../) som säkerställer att alla formulärfältsnoder skapas i rätt ordning och i ett lämpligt tillstånd.

## Exempel



Visar hur man infogar en kombinationsruta.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Please select a fruit: ");

// Infoga en kombinationsruta som låter en användare välja ett alternativ från en samling strängar.
System::SharedPtr<Aspose::Words::Fields::FormField> comboBox = builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"Apple", u"Banana", u"Cherry"}), 0);

ASSERT_EQ(u"MyComboBox", comboBox->get_Name());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldFormDropDown, comboBox->get_Type());
ASSERT_EQ(u"Apple", comboBox->get_Result());

// Formulärfältet kommer att visas i form av en "select"-HTML-tagg.
doc->Save(get_ArtifactsDir() + u"FormFields.Create.html");
```


Visar hur man formaterar hela [FormField](./), inklusive fältvärdet.
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

## Se även

* Class [SpecialChar](../../aspose.words/specialchar/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
