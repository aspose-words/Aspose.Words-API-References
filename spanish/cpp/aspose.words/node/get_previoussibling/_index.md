---
title: "Método Aspose::Words::Node::get_PreviousSibling"
linktitle: "get_PreviousSibling"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Node::get_PreviousSibling. Obtiene el nodo que precede inmediatamente a este nodo en C++."
type: docs
weight: 11000
url: /es/cpp/aspose.words/node/get_previoussibling/
---
## Node::get_PreviousSibling method


Obtiene el nodo que precede inmediatamente a este nodo.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::get_PreviousSibling()
```


## Ejemplos



Muestra cómo usar los métodos de [Node](../) y [CompositeNode](../../compositenode/) para eliminar una sección antes de la última sección en el documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Section 1 text.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakContinuous);
builder->Writeln(u"Section 2 text.");

// Ambas secciones son hermanas entre sí.
auto lastSection = System::ExplicitCast<Aspose::Words::Section>(doc->get_LastChild());
auto firstSection = System::ExplicitCast<Aspose::Words::Section>(lastSection->get_PreviousSibling());

// Elimina una sección basándote en su relación de hermandad con otra sección.
if (lastSection->get_PreviousSibling() != nullptr)
{
    doc->RemoveChild<System::SharedPtr<Aspose::Words::Section>>(firstSection);
}

// La sección que eliminamos era la primera, dejando el documento solo con la segunda.
ASSERT_EQ(u"Section 2 text.", doc->GetText().Trim());
```

## Ver también

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
