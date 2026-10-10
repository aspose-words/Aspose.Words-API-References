---
title: "Método Aspose::Words::EditableRange::get_EditorGroup"
linktitle: "get_EditorGroup"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::EditableRange::get_EditorGroup. Devuelve o establece un alias (o grupo de edición) que se utilizará para determinar si el usuario actual tiene permiso para editar este rango editable en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words/editablerange/get_editorgroup/
---
## EditableRange::get_EditorGroup method


Devuelve o establece un alias (o grupo de edición) que se utilizará para determinar si el usuario actual tiene permiso para editar este rango editable.

```cpp
Aspose::Words::EditorType Aspose::Words::EditableRange::get_EditorGroup()
```

## Observaciones


El usuario único y el grupo de editores no pueden establecerse simultáneamente para el rango editable específico; si se establece uno, el otro se borrará.

## Ejemplos



Muestra cómo crear rangos editables anidados.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"MyPassword");

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(System::String(u"Hello world! Since we have set the document's protection level to read-only, ") + u"we cannot edit this paragraph without the password.");

// Crea dos rangos editables anidados.
System::SharedPtr<Aspose::Words::EditableRangeStart> outerEditableRangeStart = builder->StartEditableRange();
builder->Writeln(u"This paragraph inside the outer editable range and can be edited.");

System::SharedPtr<Aspose::Words::EditableRangeStart> innerEditableRangeStart = builder->StartEditableRange();
builder->Writeln(u"This paragraph inside both the outer and inner editable ranges and can be edited.");

// Actualmente, el cursor de inserción de nodos del constructor de documentos está en más de un rango editable en curso.
// Cuando queremos terminar un rango editable en esta situación,
// necesitamos especificar cuál de los rangos deseamos terminar pasando su nodo EditableRangeStart.
builder->EndEditableRange(innerEditableRangeStart);

builder->Writeln(u"This paragraph inside the outer editable range and can be edited.");

builder->EndEditableRange(outerEditableRangeStart);

builder->Writeln(u"This paragraph is outside any editable ranges, and cannot be edited.");

// Si una región de texto tiene dos rangos editables superpuestos con grupos especificados,
// el grupo combinado de usuarios excluidos por ambos grupos está impedido de editarlo.
outerEditableRangeStart->get_EditableRange()->set_EditorGroup(Aspose::Words::EditorType::Everyone);
innerEditableRangeStart->get_EditableRange()->set_EditorGroup(Aspose::Words::EditorType::Contributors);

doc->Save(get_ArtifactsDir() + u"EditableRange.Nested.docx");
```

## Ver también

* Enum [EditorType](../../editortype/)
* Class [EditableRange](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
