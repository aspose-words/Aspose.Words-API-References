---
title: "Método Aspose::Words::RevisionCollection::AcceptAll"
linktitle: "AcceptAll"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::RevisionCollection::AcceptAll. Acepta todas las revisiones en esta colección en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words/revisioncollection/acceptall/
---
## RevisionCollection::AcceptAll method


Acepta todas las revisiones de esta colección.

```cpp
void Aspose::Words::RevisionCollection::AcceptAll()
```


## Ejemplos



Muestra cómo comparar documentos.
```cpp
auto docOriginal = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(docOriginal);
builder->Writeln(u"This is the original document.");

auto docEdited = System::MakeObject<Aspose::Words::Document>();
builder = System::MakeObject<Aspose::Words::DocumentBuilder>(docEdited);
builder->Writeln(u"This is the edited document.");

// Comparar documentos con revisiones lanzará una excepción.
if (docOriginal->get_Revisions()->get_Count() == 0 && docEdited->get_Revisions()->get_Count() == 0)
{
    docOriginal->Compare(docEdited, u"authorName", System::DateTime::get_Now());
}

// Después de la comparación, el documento original obtendrá una nueva revisión
// por cada elemento que sea diferente en el documento editado.
for (auto&& r : System::IterateOver(docOriginal->get_Revisions()))
{
    std::cout << System::String::Format(u"Revision type: {0}, on a node of type \"{1}\"", r->get_RevisionType(), r->get_ParentNode()->get_NodeType()) << std::endl;
    std::cout << System::String::Format(u"\tChanged text: \"{0}\"", r->get_ParentNode()->GetText()) << std::endl;
}

// Aceptar estas revisiones transformará el documento original en el documento editado.
docOriginal->get_Revisions()->AcceptAll();

ASSERT_EQ(docOriginal->GetText(), docEdited->GetText());
```

## Ver también

* Class [RevisionCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
