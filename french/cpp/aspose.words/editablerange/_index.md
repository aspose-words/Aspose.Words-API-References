---
title: "Classe Aspose::Words::EditableRange"
linktitle: "EditableRange"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::EditableRange class. Représente une plage éditable unique. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 24000
url: /fr/cpp/aspose.words/editablerange/
---
## EditableRange class


Représente une seule plage modifiable. Pour en savoir plus, consultez l'article de documentation [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class EditableRange : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_EditableRangeEnd](./get_editablerangeend/)() | Obtient le nœud qui représente la fin de la plage éditable. |
| [get_EditableRangeStart](./get_editablerangestart/)() const | Obtient le nœud qui représente le début de la plage éditable. |
| [get_EditorGroup](./get_editorgroup/)() | Renvoie ou définit un alias (ou groupe d'édition) qui sera utilisé pour déterminer si l'utilisateur actuel est autorisé à modifier cette plage éditable. |
| [get_Id](./get_id/)() | Obtient l'identifiant de la plage éditable. |
| [get_SingleUser](./get_singleuser/)() | Renvoie ou définit l'utilisateur unique pour la plage éditable. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Supprime la plage éditable du document. Ne supprime pas le contenu à l'intérieur de la plage éditable. |
| [set_EditorGroup](./set_editorgroup/)(Aspose::Words::EditorType) | Définisseur pour [Aspose::Words::EditableRange::get_EditorGroup](./get_editorgroup/). |
| [set_SingleUser](./set_singleuser/)(const System::String\&) | Définisseur pour [Aspose::Words::EditableRange::get_SingleUser](./get_singleuser/). |
| static [Type](./type/)() |  |
## Remarques


[EditableRange](./) is a "facade" object that encapsulates two nodes [EditableRangeStart](./get_editablerangestart/) and [EditableRangeEnd](./get_editablerangeend/) in a document tree and allows to work with an editable range as a single object.

## Exemples



Montre comment travailler avec une plage éditable.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"MyPassword");

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(System::String(u"Hello world! Since we have set the document's protection level to read-only,") + u" we cannot edit this paragraph without the password.");

// Les plages éditables nous permettent de laisser des parties de documents protégés ouvertes à l'édition.
System::SharedPtr<Aspose::Words::EditableRangeStart> editableRangeStart = builder->StartEditableRange();
builder->Writeln(u"This paragraph is inside an editable range, and can be edited.");
System::SharedPtr<Aspose::Words::EditableRangeEnd> editableRangeEnd = builder->EndEditableRange();

// Une plage éditable bien formée possède un nœud de début et un nœud de fin.
// Ces nœuds ont des ID correspondants et englobent des nœuds éditables.
System::SharedPtr<Aspose::Words::EditableRange> editableRange = editableRangeStart->get_EditableRange();

ASSERT_EQ(editableRangeStart->get_Id(), editableRange->get_Id());
ASSERT_EQ(editableRangeEnd->get_Id(), editableRange->get_Id());

// Différentes parties de la plage éditable sont liées entre elles.
ASSERT_EQ(editableRangeStart->get_Id(), editableRange->get_EditableRangeStart()->get_Id());
ASSERT_EQ(editableRangeStart->get_Id(), editableRangeEnd->get_EditableRangeStart()->get_Id());
ASSERT_EQ(editableRange->get_Id(), editableRangeStart->get_EditableRange()->get_Id());
ASSERT_EQ(editableRangeEnd->get_Id(), editableRange->get_EditableRangeEnd()->get_Id());

// Nous pouvons accéder aux types de nœuds de chaque partie ainsi. La plage éditable elle-même n'est pas un nœud,
// mais une entité qui consiste en un début, une fin et leurs contenus inclus.
ASSERT_EQ(Aspose::Words::NodeType::EditableRangeStart, editableRangeStart->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::EditableRangeEnd, editableRangeEnd->get_NodeType());

builder->Writeln(u"This paragraph is outside the editable range, and cannot be edited.");

doc->Save(get_ArtifactsDir() + u"EditableRange.CreateAndRemove.docx");

// Supprimez une plage éditable. Tous les nœuds qui étaient à l'intérieur de la plage resteront intacts.
editableRange->Remove();
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
