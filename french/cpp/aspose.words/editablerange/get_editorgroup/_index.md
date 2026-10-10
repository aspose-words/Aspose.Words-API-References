---
title: "Aspose::Words::EditableRange::get_EditorGroup méthode"
linktitle: "get_EditorGroup"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::EditableRange::get_EditorGroup méthode. Retourne ou définit un alias (ou groupe d'édition) qui sera utilisé pour déterminer si l'utilisateur actuel est autorisé à modifier cette plage modifiable en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words/editablerange/get_editorgroup/
---
## EditableRange::get_EditorGroup method


Renvoie ou définit un alias (ou groupe d'édition) qui sera utilisé pour déterminer si l'utilisateur actuel est autorisé à modifier cette plage éditable.

```cpp
Aspose::Words::EditorType Aspose::Words::EditableRange::get_EditorGroup()
```

## Remarques


L'utilisateur unique et le groupe d'éditeurs ne peuvent pas être définis simultanément pour la plage modifiable spécifique ; si l'un est défini, l'autre sera effacé.

## Exemples



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

* Enum [EditorType](../../editortype/)
* Class [EditableRange](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
