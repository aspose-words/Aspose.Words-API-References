---
title: "Méthode Aspose::Words::DocumentBuilder::StartEditableRange"
linktitle: "StartEditableRange"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::DocumentBuilder::StartEditableRange. Marque la position actuelle dans le document comme le début d'une plage modifiable en C++."
type: docs
weight: 70000
url: /fr/cpp/aspose.words/documentbuilder/starteditablerange/
---
## DocumentBuilder::StartEditableRange method


Marque la position actuelle dans le document comme le début d'une plage modifiable.

```cpp
System::SharedPtr<Aspose::Words::EditableRangeStart> Aspose::Words::DocumentBuilder::StartEditableRange()
```


### ReturnValue

Le nœud de début de plage modifiable qui vient d'être créé.
## Remarques


Une plage modifiable dans un document peut se chevaucher et couvrir n'importe quelle étendue. Pour créer une plage modifiable valide, vous devez appeler à la fois les méthodes [StartEditableRange](./) et [EndEditableRange](../endeditablerange/) ou [EndEditableRange()](../).

Une plage modifiable mal formée sera ignorée lors de l'enregistrement du document.

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


Montre comment créer des plages modifiables imbriquées.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"MyPassword");

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(System::String(u"Hello world! Since we have set the document's protection level to read-only, ") + u"we cannot edit this paragraph without the password.");

// Créez deux plages modifiables imbriquées.
System::SharedPtr<Aspose::Words::EditableRangeStart> outerEditableRangeStart = builder->StartEditableRange();
builder->Writeln(u"This paragraph inside the outer editable range and can be edited.");

System::SharedPtr<Aspose::Words::EditableRangeStart> innerEditableRangeStart = builder->StartEditableRange();
builder->Writeln(u"This paragraph inside both the outer and inner editable ranges and can be edited.");

// Actuellement, le curseur d'insertion de nœuds du constructeur de document se trouve dans plus d'une plage modifiable en cours.
// Lorsque nous voulons terminer une plage modifiable dans cette situation,
// nous devons spécifier laquelle des plages nous souhaitons terminer en transmettant son nœud EditableRangeStart.
builder->EndEditableRange(innerEditableRangeStart);

builder->Writeln(u"This paragraph inside the outer editable range and can be edited.");

builder->EndEditableRange(outerEditableRangeStart);

builder->Writeln(u"This paragraph is outside any editable ranges, and cannot be edited.");

// Si une région de texte possède deux plages modifiables qui se chevauchent avec des groupes spécifiés,
// le groupe combiné d'utilisateurs exclus par les deux groupes est empêché de le modifier.
outerEditableRangeStart->get_EditableRange()->set_EditorGroup(Aspose::Words::EditorType::Everyone);
innerEditableRangeStart->get_EditableRange()->set_EditorGroup(Aspose::Words::EditorType::Contributors);

doc->Save(get_ArtifactsDir() + u"EditableRange.Nested.docx");
```

## Voir aussi

* Class [EditableRangeStart](../../editablerangestart/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
