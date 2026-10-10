---
title: "Método Aspose::Words::EditableRangeEnd::get_NodeType"
linktitle: "get_NodeType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::EditableRangeEnd::get_NodeType. Devuelve EditableRangeEnd en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words/editablerangeend/get_nodetype/
---
## EditableRangeEnd::get_NodeType method


Devuelve [EditableRangeEnd](../../nodetype/).

```cpp
Aspose::Words::NodeType Aspose::Words::EditableRangeEnd::get_NodeType() const override
```


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

* Enum [NodeType](../../nodetype/)
* Class [EditableRangeEnd](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
