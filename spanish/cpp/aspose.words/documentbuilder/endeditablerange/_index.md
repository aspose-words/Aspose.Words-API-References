---
title: "Aspose::Words::DocumentBuilder::EndEditableRange método"
linktitle: "EndEditableRange"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::DocumentBuilder::EndEditableRange. Marca la posición actual en el documento como el final de un rango editable en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words/documentbuilder/endeditablerange/
---
## DocumentBuilder::EndEditableRange() method


Marca la posición actual en el documento como el final de un rango editable.

```cpp
System::SharedPtr<Aspose::Words::EditableRangeEnd> Aspose::Words::DocumentBuilder::EndEditableRange()
```


### ReturnValue

El nodo de fin de rango editable que se acaba de crear.
## Observaciones


Un rango editable en un documento puede superponerse y abarcar cualquier rango. Para crear un rango editable válido necesitas llamar a los métodos [StartEditableRange](../starteditablerange/) y [EndEditableRange](./) o [EndEditableRange()](../).

Los rangos editables mal formados se ignorarán al guardar el documento.

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

* Class [EditableRangeEnd](../../editablerangeend/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::EndEditableRange(const System::SharedPtr\<Aspose::Words::EditableRangeStart\>\&) method


Marca la posición actual en el documento como el final de un rango editable.

```cpp
System::SharedPtr<Aspose::Words::EditableRangeEnd> Aspose::Words::DocumentBuilder::EndEditableRange(const System::SharedPtr<Aspose::Words::EditableRangeStart> &start)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inicio | const System::SharedPtr\<Aspose::Words::EditableRangeStart\>\& | Este inicio de rango editable. |

### ReturnValue

El nodo de fin de rango editable que se acaba de crear.
## Observaciones


Utiliza esta sobrecarga al crear rangos editables anidados.

Un rango editable en un documento puede superponerse y abarcar cualquier rango. Para crear un rango editable válido necesitas llamar a los métodos [StartEditableRange](../starteditablerange/) y [EndEditableRange](./) o [EndEditableRange()](../).

Los rangos editables mal formados se ignorarán al guardar el documento.

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

* Class [EditableRangeEnd](../../editablerangeend/)
* Class [EditableRangeStart](../../editablerangestart/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
