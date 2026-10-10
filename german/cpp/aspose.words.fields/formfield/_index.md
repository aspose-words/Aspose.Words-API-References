---
title: "Aspose::Words::Fields::FormField Klasse"
linktitle: "FormField"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::FormField Klasse. Stellt ein einzelnes Formularfeld dar. Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel in C++."
type: docs
weight: 112000
url: /de/cpp/aspose.words.fields/formfield/
---
## FormField class


Stellt ein einzelnes Formularfeld dar. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Form Fields](https://docs.aspose.com/words/cpp/working-with-form-fields/).

```cpp
class FormField : public Aspose::Words::SpecialChar
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Akzeptiert einen Besucher. |
| [Clone](../../aspose.words/node/clone/)(bool) | Erstellt ein Duplikat des Knotens. |
| [get_CalculateOnExit](./get_calculateonexit/)() | True, wenn Verweise auf das angegebene Formularfeld automatisch aktualisiert werden, sobald das Feld verlassen wird. |
| [get_CheckBoxSize](./get_checkboxsize/)() | Liest oder setzt die Größe des Kontrollkästchens in Punkten. Wirkt nur, wenn [IsCheckBoxExactSize](./get_ischeckboxexactsize/) **true** ist. |
| [get_Checked](./get_checked/)() | Liest oder setzt den aktivierten Status des Kontrollkästchen-Formularfelds. Der Standardwert für diese Eigenschaft ist **false**. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Legt eine benutzerdefinierte Knotenkennung fest. |
| [get_Default](./get_default/)() | Liest oder setzt den Standardwert des Kontrollkästchen-Formularfelds. Der Standardwert für diese Eigenschaft ist **false**. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Ermittelt das Dokument, zu dem dieser Knoten gehört. |
| [get_DropDownItems](./get_dropdownitems/)() | Stellt Zugriff auf die Elemente eines Dropdown-Formularfelds bereit. |
| [get_DropDownSelectedIndex](./get_dropdownselectedindex/)() | Liest den Index, der das aktuell ausgewählte Element in einem Dropdown-Formularfeld angibt. |
| [get_Enabled](./get_enabled/)() | True, wenn ein Formularfeld aktiviert ist. |
| [get_EntryMacro](./get_entrymacro/)() | Liest oder setzt einen Eingabe-Makronamen für das Formularfeld. |
| [get_ExitMacro](./get_exitmacro/)() | Liest oder setzt einen Beendigungs-Makronamen für das Formularfeld. |
| [get_Font](../../aspose.words/inline/get_font/)() | Stellt Zugriff auf die Schriftformatierung dieses Objekts bereit. |
| [get_HelpText](./get_helptext/)() | Liest oder setzt den Text, der in einer Meldungsbox angezeigt wird, wenn das Formularfeld den Fokus hat und der Benutzer F1 drückt. |
| [get_IsCheckBoxExactSize](./get_ischeckboxexactsize/)() | Liest oder setzt den booleschen Wert, der angibt, ob die Größe des Textfelds automatisch oder explizit festgelegt ist. |
| virtual [get_IsComposite](../../aspose.words/node/get_iscomposite/)() | Liefert **true**, wenn dieser Knoten andere Knoten enthalten kann. |
| [get_IsDeleteRevision](../../aspose.words/inline/get_isdeleterevision/)() | Gibt true zurück, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsverfolgung aktiviert war. |
| [get_IsFormatRevision](../../aspose.words/inline/get_isformatrevision/)() | Gibt true zurück, wenn die Formatierung des Objekts in Microsoft Word geändert wurde, während die Änderungsverfolgung aktiviert war. |
| [get_IsInsertRevision](../../aspose.words/inline/get_isinsertrevision/)() | Gibt true zurück, wenn dieses Objekt in Microsoft Word eingefügt wurde, während die Änderungsverfolgung aktiviert war. |
| [get_IsMoveFromRevision](../../aspose.words/inline/get_ismovefromrevision/)() | Gibt **true** zurück, wenn dieses Objekt in Microsoft Word verschoben (gelöscht) wurde, während die Änderungsverfolgung aktiviert war. |
| [get_IsMoveToRevision](../../aspose.words/inline/get_ismovetorevision/)() | Gibt **true** zurück, wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsverfolgung aktiviert war. |
| [get_MaxLength](./get_maxlength/)() | Maximale Länge für das Textfeld. Null, wenn die Länge nicht begrenzt ist. |
| [get_Name](./get_name/)() | Liest oder setzt den Namen des Formularfelds. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Ermittelt den Knoten, der diesem Knoten unmittelbar folgt. |
| [get_NodeType](./get_nodetype/)() const override | Gibt zurück [FormField](../../aspose.words/nodetype/). |
| [get_OwnHelp](./get_ownhelp/)() | Gibt die Quelle des Textes an, der in einer Meldungsbox angezeigt wird, wenn ein Formularfeld den Fokus hat und der Benutzer F1 drückt. |
| [get_OwnStatus](./get_ownstatus/)() | Gibt die Quelle des Textes an, der in der Statusleiste angezeigt wird, wenn ein Formularfeld den Fokus hat. |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Ermittelt den unmittelbaren Elternknoten dieses Knotens. |
| [get_ParentParagraph](../../aspose.words/inline/get_parentparagraph/)() | Ruft den übergeordneten [Paragraph](../../aspose.words/paragraph/) dieses Knotens ab. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Ermittelt den Knoten, der diesem Knoten unmittelbar vorausgeht. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Gibt ein [Range](../../aspose.words/range/)-Objekt zurück, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [get_Result](./get_result/)() | Liest oder setzt eine Zeichenkette, die das Ergebnis dieses Formularfelds darstellt. |
| [get_StatusText](./get_statustext/)() | Liest oder setzt den Text, der in der Statusleiste angezeigt wird, wenn ein Formularfeld den Fokus hat. |
| [get_TextInputDefault](./get_textinputdefault/)() | Liest oder setzt die Standardzeichenkette oder einen Berechnungsausdruck eines Text-Formularfelds. |
| [get_TextInputFormat](./get_textinputformat/)() | Liest oder setzt die Textformatierung für ein Text-Formularfeld. |
| [get_TextInputType](./get_textinputtype/)() | Liest den Typ eines Text-Formularfelds. |
| [get_Type](./get_type/)() | Gibt den Formularfeldtyp zurück. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Ermittelt den ersten Vorfahren des angegebenen [NodeType](../../aspose.words/nodetype/). |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetText](../../aspose.words/specialchar/gettext/)() override | Liefert das Sonderzeichen, das dieser Knoten darstellt. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ermittelt den nächsten Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Eine Hilfsmethode, die einen Enum‑Wert des Knotentyps in eine benutzerfreundliche Zeichenkette konvertiert. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ermittelt den vorherigen Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus. |
| [Remove](../../aspose.words/node/remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [RemoveField](./removefield/)() | Entfernt das komplette Formularfeld, nicht nur das Sonderzeichen des Formularfelds. |
| [set_CalculateOnExit](./set_calculateonexit/)(bool) | Setzer für [Aspose::Words::Fields::FormField::get_CalculateOnExit](./get_calculateonexit/). |
| [set_CheckBoxSize](./set_checkboxsize/)(double) | Setzer für [Aspose::Words::Fields::FormField::get_CheckBoxSize](./get_checkboxsize/). |
| [set_Checked](./set_checked/)(bool) | Setzer für [Aspose::Words::Fields::FormField::get_Checked](./get_checked/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Setter für [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_Default](./set_default/)(bool) | Setzer für [Aspose::Words::Fields::FormField::get_Default](./get_default/). |
| [set_DropDownSelectedIndex](./set_dropdownselectedindex/)(int32_t) | Legt den Index fest, der das aktuell ausgewählte Element in einem Dropdown-Formularfeld angibt. |
| [set_Enabled](./set_enabled/)(bool) | True, wenn ein Formularfeld aktiviert ist. |
| [set_EntryMacro](./set_entrymacro/)(const System::String\&) | Setzer für [Aspose::Words::Fields::FormField::get_EntryMacro](./get_entrymacro/). |
| [set_ExitMacro](./set_exitmacro/)(const System::String\&) | Setzer für [Aspose::Words::Fields::FormField::get_ExitMacro](./get_exitmacro/). |
| [set_HelpText](./set_helptext/)(const System::String\&) | Setzer für [Aspose::Words::Fields::FormField::get_HelpText](./get_helptext/). |
| [set_IsCheckBoxExactSize](./set_ischeckboxexactsize/)(bool) | Setzer für [Aspose::Words::Fields::FormField::get_IsCheckBoxExactSize](./get_ischeckboxexactsize/). |
| [set_MaxLength](./set_maxlength/)(int32_t) | Maximale Länge für das Textfeld. Null, wenn die Länge nicht begrenzt ist. |
| [set_Name](./set_name/)(const System::String\&) | Setzer für [Aspose::Words::Fields::FormField::get_Name](./get_name/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_OwnHelp](./set_ownhelp/)(bool) | Setzer für [Aspose::Words::Fields::FormField::get_OwnHelp](./get_ownhelp/). |
| [set_OwnStatus](./set_ownstatus/)(bool) | Setzer für [Aspose::Words::Fields::FormField::get_OwnStatus](./get_ownstatus/). |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Result](./set_result/)(const System::String\&) | Setzer für [Aspose::Words::Fields::FormField::get_Result](./get_result/). |
| [set_StatusText](./set_statustext/)(const System::String\&) | Setzer für [Aspose::Words::Fields::FormField::get_StatusText](./get_statustext/). |
| [set_TextInputDefault](./set_textinputdefault/)(const System::String\&) | Setzer für [Aspose::Words::Fields::FormField::get_TextInputDefault](./get_textinputdefault/). |
| [set_TextInputFormat](./set_textinputformat/)(const System::String\&) | Setzer für [Aspose::Words::Fields::FormField::get_TextInputFormat](./get_textinputformat/). |
| [set_TextInputType](./set_textinputtype/)(Aspose::Words::Fields::TextFormFieldType) | Legt den Typ eines Textformularfelds fest. |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTextInputValue](./settextinputvalue/)(const System::SharedPtr\<System::Object\>\&) | Wendet das im [TextInputFormat](./get_textinputformat/) angegebene Textformat an und speichert den Wert in [Result](./get_result/). |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Exportiert den Inhalt des Knotens in eine Zeichenkette im angegebenen Format. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exportiert den Inhalt des Knotens in eine Zeichenkette unter Verwendung der angegebenen Speicheroptionen. |
| static [Type](./type/)() |  |
## Hinweise


Microsoft Word stellt die folgenden Formularfelder bereit: Kontrollkästchen, Texteingabe und Dropdown (Kombinationsfeld).

[FormField](./) is an inline-node and can only be a child of [Paragraph](../../aspose.words/paragraph/).

[FormField](./) is represented in a document by a special character and positioned as a character within a line of text.

Ein komplettes Formularfeld in einem Word-Dokument ist eine komplexe Struktur, die durch mehrere Knoten dargestellt wird: Feldbeginn, Feldcode wie FORMTEXT, Formulardaten, Feldtrennzeichen, Feldresultat, Feldende und ein Lesezeichen. Um programmgesteuert Formularfelder in einem Word-Dokument zu erstellen, verwenden Sie [InsertCheckBox()](../), [InsertTextInput()](../) und [InsertComboBox()](../), die sicherstellen, dass alle Knoten des Formularfelds in der richtigen Reihenfolge und in einem geeigneten Zustand erstellt werden.

## Beispiele



Zeigt, wie man ein Kombinationsfeld einfügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Please select a fruit: ");

// Fügt ein Kombinationsfeld ein, das es einem Benutzer ermöglicht, eine Option aus einer Sammlung von Zeichenketten auszuwählen.
System::SharedPtr<Aspose::Words::Fields::FormField> comboBox = builder->InsertComboBox(u"MyComboBox", System::MakeArray<System::String>({u"Apple", u"Banana", u"Cherry"}), 0);

ASSERT_EQ(u"MyComboBox", comboBox->get_Name());
ASSERT_EQ(Aspose::Words::Fields::FieldType::FieldFormDropDown, comboBox->get_Type());
ASSERT_EQ(u"Apple", comboBox->get_Result());

// Das Formularfeld wird in Form eines "select"-HTML-Tags angezeigt.
doc->Save(get_ArtifactsDir() + u"FormFields.Create.html");
```


Zeigt, wie man das gesamte [FormField](./) formatiert, einschließlich des Feldwerts.
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

## Siehe auch

* Class [SpecialChar](../../aspose.words/specialchar/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
