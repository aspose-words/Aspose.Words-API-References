---
title: "clase Aspose::Words::EditableRange"
linktitle: "EditableRange"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::EditableRange. Representa un rango editable único. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 24000
url: /es/cpp/aspose.words/editablerange/
---
## EditableRange class


Representa un único rango editable. Para obtener más información, visite el artículo de documentación [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class EditableRange : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_EditableRangeEnd](./get_editablerangeend/)() | Obtiene el nodo que representa el final del rango editable. |
| [get_EditableRangeStart](./get_editablerangestart/)() const | Obtiene el nodo que representa el inicio del rango editable. |
| [get_EditorGroup](./get_editorgroup/)() | Devuelve o establece un alias (o grupo de edición) que se utilizará para determinar si el usuario actual tiene permiso para editar este rango editable. |
| [get_Id](./get_id/)() | Obtiene el identificador del rango editable. |
| [get_SingleUser](./get_singleuser/)() | Devuelve o establece el usuario único para el rango editable. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)() | Elimina el rango editable del documento. No elimina el contenido dentro del rango editable. |
| [set_EditorGroup](./set_editorgroup/)(Aspose::Words::EditorType) | Método set para [Aspose::Words::EditableRange::get_EditorGroup](./get_editorgroup/). |
| [set_SingleUser](./set_singleuser/)(const System::String\&) | Método set para [Aspose::Words::EditableRange::get_SingleUser](./get_singleuser/). |
| static [Type](./type/)() |  |
## Observaciones


[EditableRange](./) is a "facade" object that encapsulates two nodes [EditableRangeStart](./get_editablerangestart/) and [EditableRangeEnd](./get_editablerangeend/) in a document tree and allows to work with an editable range as a single object.

## Ejemplos



Muestra cómo trabajar con un rango editable.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->Protect(Aspose::Words::ProtectionType::ReadOnly, u"MyPassword");

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(System::String(u"Hello world! Since we have set the document's protection level to read-only,") + u" we cannot edit this paragraph without the password.");

// Los rangos editables nos permiten dejar partes de documentos protegidos abiertas para edición.
System::SharedPtr<Aspose::Words::EditableRangeStart> editableRangeStart = builder->StartEditableRange();
builder->Writeln(u"This paragraph is inside an editable range, and can be edited.");
System::SharedPtr<Aspose::Words::EditableRangeEnd> editableRangeEnd = builder->EndEditableRange();

// Un rango editable bien formado tiene un nodo de inicio y un nodo de fin.
// Estos nodos tienen IDs coincidentes y abarcan nodos editables.
System::SharedPtr<Aspose::Words::EditableRange> editableRange = editableRangeStart->get_EditableRange();

ASSERT_EQ(editableRangeStart->get_Id(), editableRange->get_Id());
ASSERT_EQ(editableRangeEnd->get_Id(), editableRange->get_Id());

// Diferentes partes del rango editable se enlazan entre sí.
ASSERT_EQ(editableRangeStart->get_Id(), editableRange->get_EditableRangeStart()->get_Id());
ASSERT_EQ(editableRangeStart->get_Id(), editableRangeEnd->get_EditableRangeStart()->get_Id());
ASSERT_EQ(editableRange->get_Id(), editableRangeStart->get_EditableRange()->get_Id());
ASSERT_EQ(editableRangeEnd->get_Id(), editableRange->get_EditableRangeEnd()->get_Id());

// Podemos acceder a los tipos de nodo de cada parte de esta manera. El rango editable en sí no es un nodo,
// sino una entidad que consiste en un inicio, un fin y su contenido incluido.
ASSERT_EQ(Aspose::Words::NodeType::EditableRangeStart, editableRangeStart->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::EditableRangeEnd, editableRangeEnd->get_NodeType());

builder->Writeln(u"This paragraph is outside the editable range, and cannot be edited.");

doc->Save(get_ArtifactsDir() + u"EditableRange.CreateAndRemove.docx");

// Elimina un rango editable. Todos los nodos que estaban dentro del rango permanecerán intactos.
editableRange->Remove();
```

## Ver también

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
