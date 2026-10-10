---
title: "Aspose::Words::Fields::FormField classe"
linktitle: "FormField"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Fields::FormField classe. Représente un champ de formulaire unique. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 112000
url: /fr/cpp/aspose.words.fields/formfield/
---
## FormField class


Représente un seul champ de formulaire. Pour en savoir plus, visitez l'article de documentation [Working with Form Fields](https://docs.aspose.com/words/cpp/working-with-form-fields/).

```cpp
class FormField : public Aspose::Words::SpecialChar
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accepte un visiteur. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crée un duplicata du nœud. |
| [get_CalculateOnExit](./get_calculateonexit/)() | Vrai si les références au champ de formulaire spécifié sont automatiquement mises à jour chaque fois que le champ est quitté. |
| [get_CheckBoxSize](./get_checkboxsize/)() | Obtient ou définit la taille de la case à cocher en points. N'a d'effet que lorsque [IsCheckBoxExactSize](./get_ischeckboxexactsize/) est **true**. |
| [get_Checked](./get_checked/)() | Obtient ou définit l'état coché du champ de formulaire de case à cocher. La valeur par défaut de cette propriété est **false**. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Spécifie un identifiant de nœud personnalisé. |
| [get_Default](./get_default/)() | Obtient ou définit la valeur par défaut du champ de formulaire de case à cocher. La valeur par défaut de cette propriété est **false**. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Obtient le document auquel ce nœud appartient. |
| [get_DropDownItems](./get_dropdownitems/)() | Fournit l'accès aux éléments d'un champ de formulaire déroulant. |
| [get_DropDownSelectedIndex](./get_dropdownselectedindex/)() | Obtient l'index spécifiant l'élément actuellement sélectionné dans un champ de formulaire déroulant. |
| [get_Enabled](./get_enabled/)() | Vrai si un champ de formulaire est activé. |
| [get_EntryMacro](./get_entrymacro/)() | Renvoie ou définit le nom d'une macro d'entrée pour le champ de formulaire. |
| [get_ExitMacro](./get_exitmacro/)() | Renvoie ou définit le nom d'une macro de sortie pour le champ de formulaire. |
| [get_Font](../../aspose.words/inline/get_font/)() | Fournit l'accès au format de police de cet objet. |
| [get_HelpText](./get_helptext/)() | Renvoie ou définit le texte affiché dans une boîte de dialogue lorsque le champ de formulaire a le focus et que l'utilisateur appuie sur F1. |
| [get_IsCheckBoxExactSize](./get_ischeckboxexactsize/)() | Obtient ou définit la valeur booléenne indiquant si la taille de la zone de texte est automatique ou spécifiée explicitement. |
| virtual [get_IsComposite](../../aspose.words/node/get_iscomposite/)() | Renvoie **true** si ce nœud peut contenir d'autres nœuds. |
| [get_IsDeleteRevision](../../aspose.words/inline/get_isdeleterevision/)() | Renvoie true si cet objet a été supprimé dans Microsoft Word alors que le suivi des modifications était activé. |
| [get_IsFormatRevision](../../aspose.words/inline/get_isformatrevision/)() | Renvoie vrai si le format de l'objet a été modifié dans Microsoft Word alors que le suivi des modifications était activé. |
| [get_IsInsertRevision](../../aspose.words/inline/get_isinsertrevision/)() | Renvoie true si cet objet a été inséré dans Microsoft Word alors que le suivi des modifications était activé. |
| [get_IsMoveFromRevision](../../aspose.words/inline/get_ismovefromrevision/)() | Renvoie **true** si cet objet a été déplacé (supprimé) dans Microsoft Word alors que le suivi des modifications était activé. |
| [get_IsMoveToRevision](../../aspose.words/inline/get_ismovetorevision/)() | Renvoie **true** si cet objet a été déplacé (inséré) dans Microsoft Word alors que le suivi des modifications était activé. |
| [get_MaxLength](./get_maxlength/)() | Longueur maximale pour le champ texte. Zéro lorsque la longueur n'est pas limitée. |
| [get_Name](./get_name/)() | Obtient ou définit le nom du champ de formulaire. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Obtient le nœud immédiatement suivant ce nœud. |
| [get_NodeType](./get_nodetype/)() const override | Renvoie [FormField](../../aspose.words/nodetype/). |
| [get_OwnHelp](./get_ownhelp/)() | Spécifie la source du texte affiché dans une boîte de dialogue lorsque le champ de formulaire a le focus et que l'utilisateur appuie sur F1. |
| [get_OwnStatus](./get_ownstatus/)() | Spécifie la source du texte affiché dans la barre d'état lorsque le champ de formulaire a le focus. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Obtient le parent immédiat de ce nœud. |
| [get_ParentParagraph](../../aspose.words/inline/get_parentparagraph/)() | Récupère le [Paragraph](../../aspose.words/paragraph/) parent de ce nœud. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Obtient le nœud immédiatement précédent ce nœud. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Renvoie un objet [Range](../../aspose.words/range/) qui représente la partie d'un document contenue dans ce nœud. |
| [get_Result](./get_result/)() | Obtient ou définit une chaîne qui représente le résultat de ce champ de formulaire. |
| [get_StatusText](./get_statustext/)() | Renvoie ou définit le texte affiché dans la barre d'état lorsque le champ de formulaire a le focus. |
| [get_TextInputDefault](./get_textinputdefault/)() | Obtient ou définit la chaîne par défaut ou une expression de calcul d'un champ de formulaire texte. |
| [get_TextInputFormat](./get_textinputformat/)() | Renvoie ou définit le formatage du texte pour un champ de formulaire texte. |
| [get_TextInputType](./get_textinputtype/)() | Obtient le type d'un champ de formulaire texte. |
| [get_Type](./get_type/)() | Renvoie le type de champ de formulaire. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Obtient le premier ancêtre du [NodeType](../../aspose.words/nodetype/) spécifié. |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetText](../../aspose.words/specialchar/gettext/)() override | Obtient le caractère spécial que ce nœud représente. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtient le nœud suivant selon l'algorithme de traversée d'arbre en pré-ordre. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Méthode utilitaire qui convertit une valeur d'énumération de type de nœud en une chaîne conviviale. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Obtient le nœud précédent selon l'algorithme de traversée d'arbre en pré-ordre. |
| [Remove](../../aspose.words/node/remove/)() | Se supprime du parent. |
| [RemoveField](./removefield/)() | Supprime le champ de formulaire complet, pas seulement le caractère spécial du champ de formulaire. |
| [set_CalculateOnExit](./set_calculateonexit/)(bool) | Mutateur pour [Aspose::Words::Fields::FormField::get_CalculateOnExit](./get_calculateonexit/). |
| [set_CheckBoxSize](./set_checkboxsize/)(double) | Mutateur pour [Aspose::Words::Fields::FormField::get_CheckBoxSize](./get_checkboxsize/). |
| [set_Checked](./set_checked/)(bool) | Mutateur pour [Aspose::Words::Fields::FormField::get_Checked](./get_checked/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Mutateur pour [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_Default](./set_default/)(bool) | Mutateur pour [Aspose::Words::Fields::FormField::get_Default](./get_default/). |
| [set_DropDownSelectedIndex](./set_dropdownselectedindex/)(int32_t) | Définit l'index spécifiant l'élément actuellement sélectionné dans un champ de formulaire déroulant. |
| [set_Enabled](./set_enabled/)(bool) | Vrai si un champ de formulaire est activé. |
| [set_EntryMacro](./set_entrymacro/)(const System::String\&) | Mutateur pour [Aspose::Words::Fields::FormField::get_EntryMacro](./get_entrymacro/). |
| [set_ExitMacro](./set_exitmacro/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::FormField::get_ExitMacro](./get_exitmacro/). |
| [set_HelpText](./set_helptext/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::FormField::get_HelpText](./get_helptext/). |
| [set_IsCheckBoxExactSize](./set_ischeckboxexactsize/)(bool) | Définisseur pour [Aspose::Words::Fields::FormField::get_IsCheckBoxExactSize](./get_ischeckboxexactsize/). |
| [set_MaxLength](./set_maxlength/)(int32_t) | Longueur maximale pour le champ texte. Zéro lorsque la longueur n'est pas limitée. |
| [set_Name](./set_name/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::FormField::get_Name](./get_name/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_OwnHelp](./set_ownhelp/)(bool) | Définisseur pour [Aspose::Words::Fields::FormField::get_OwnHelp](./get_ownhelp/). |
| [set_OwnStatus](./set_ownstatus/)(bool) | Définisseur pour [Aspose::Words::Fields::FormField::get_OwnStatus](./get_ownstatus/). |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Result](./set_result/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::FormField::get_Result](./get_result/). |
| [set_StatusText](./set_statustext/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::FormField::get_StatusText](./get_statustext/). |
| [set_TextInputDefault](./set_textinputdefault/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::FormField::get_TextInputDefault](./get_textinputdefault/). |
| [set_TextInputFormat](./set_textinputformat/)(const System::String\&) | Définisseur pour [Aspose::Words::Fields::FormField::get_TextInputFormat](./get_textinputformat/). |
| [set_TextInputType](./set_textinputtype/)(Aspose::Words::Fields::TextFormFieldType) | Définit le type d'un champ de formulaire texte. |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTextInputValue](./settextinputvalue/)(const System::SharedPtr\<System::Object\>\&) | Applique le format de texte spécifié dans [TextInputFormat](./get_textinputformat/) et stocke la valeur dans [Result](./get_result/). |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exporte le contenu du nœud dans une chaîne au format spécifié. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exporte le contenu du nœud dans une chaîne en utilisant les options d'enregistrement spécifiées. |
| static [Type](./type/)() |  |
## Remarques


Microsoft Word propose les champs de formulaire suivants : case à cocher, saisie de texte et liste déroulante (combobox).

[FormField](./) is an inline-node and can only be a child of [Paragraph](../../aspose.words/paragraph/).

[FormField](./) is represented in a document by a special character and positioned as a character within a line of text.

Un champ de formulaire complet dans un document Word est une structure complexe représentée par plusieurs nœuds : début de champ, code de champ tel que FORMTEXT, données du champ de formulaire, séparateur de champ, résultat du champ, fin de champ et un signet. Pour créer programmétiquement des champs de formulaire dans un document Word, utilisez [InsertCheckBox()](../), [InsertTextInput()](../) et [InsertComboBox()](../) qui garantissent que tous les nœuds du champ de formulaire sont créés dans le bon ordre et dans un état approprié.

## Exemples



Montre comment insérer une combo box.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Please select a fruit: ");

// Insérez une combo box qui permettra à l'utilisateur de choisir une option parmi une collection de chaînes.
System::SharedPtr<Aspose::Words::Fields::FormField> comboBox = builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"Apple", u"Banana", u"Cherry"}), 0);

ASSERT_EQ(u"MyComboBox", comboBox->get_Name());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldFormDropDown, comboBox->get_Type());
ASSERT_EQ(u"Apple", comboBox->get_Result());

// Le champ de formulaire apparaîtra sous la forme d'une balise HTML "select".
doc->Save(get_ArtifactsDir() + u"FormFields.Create.html");
```


Montre comment formater l'ensemble du [FormField](./), y compris la valeur du champ.
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

## Voir aussi

* Class [SpecialChar](../../aspose.words/specialchar/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
