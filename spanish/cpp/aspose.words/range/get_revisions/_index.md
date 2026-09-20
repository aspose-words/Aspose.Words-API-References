---
title: "Método Aspose::Words::Range::get_Revisions"
linktitle: "get_Revisions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Range::get_Revisions. Obtiene una colección de revisiones (cambios controlados) que existen en este rango en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words/range/get_revisions/
---
## Range::get_Revisions method


Obtiene una colección de revisiones (cambios controlados) que existen en este rango.

```cpp
System::SharedPtr<Aspose::Words::RevisionCollection> Aspose::Words::Range::get_Revisions()
```

## Observaciones


La colección devuelta es una colección "en vivo", lo que significa que si elimina partes de un documento que contienen revisiones, las revisiones eliminadas desaparecerán automáticamente de esta colección.

## Ejemplos



Muestra cómo trabajar con revisiones en el rango.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
for (auto&& revision : System::IterateOver(paragraph->get_Range()->get_Revisions()))
{
    if (revision->get_RevisionType() == Aspose::Words::RevisionType::Deletion)
    {
        revision->Accept();
    }
}

// Rechace las revisiones de la primera sección.
doc->get_FirstSection()->get_Range()->get_Revisions()->RejectAll();
```

## Ver también

* Class [RevisionCollection](../../revisioncollection/)
* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
