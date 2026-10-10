---
title: "Aspose::Words::EditableRangeStart::get_EditableRange méthode"
linktitle: "get_EditableRange"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::EditableRangeStart::get_EditableRange méthode. Obtient l'objet façade qui encapsule ce début et cette fin de plage éditable en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words/editablerangestart/get_editablerange/
---
## EditableRangeStart::get_EditableRange method


Obtient l'objet façade qui encapsule le début et la fin de cette plage modifiable.

```cpp
System::SharedPtr<Aspose::Words::EditableRange> Aspose::Words::EditableRangeStart::get_EditableRange()
```


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

* Class [EditableRange](../../editablerange/)
* Class [EditableRangeStart](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
