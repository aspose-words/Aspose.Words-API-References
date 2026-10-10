---
title: "Aspose::Words::RevisionGroupCollection::GetEnumerator método"
linktitle: "GetEnumerator"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::RevisionGroupCollection::GetEnumerator método. Devuelve un objeto enumerador en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words/revisiongroupcollection/getenumerator/
---
## RevisionGroupCollection::GetEnumerator method


Devuelve un objeto enumerador.

```cpp
System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::RevisionGroup>>> Aspose::Words::RevisionGroupCollection::GetEnumerator() override
```


## Ejemplos



Muestra cómo trabajar con la colección de revisiones de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");
System::SharedPtr<Aspose::Words::RevisionCollection> revisions = doc->get_Revisions();

// Esta colección en sí tiene una colección de grupos de revisiones.
// Cada grupo es una secuencia de revisiones adyacentes.
std::cout << System::String::Format(u"{0} revision groups:", revisions->get_Groups()->get_Count()) << std::endl;

// Itera sobre la colección de grupos e imprime el texto al que se refiere la revisión.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::RevisionGroup>>> e = revisions->get_Groups()->GetEnumerator();
    while (e->MoveNext())
    {
        std::cout << (System::String::Format(u"\tGroup type \"{0}\", ", e->get_Current()->get_RevisionType()) + System::String::Format(u"author: {0}, contents: [{1}]", e->get_Current()->get_Author(), e->get_Current()->get_Text().Trim())) << std::endl;
    }
}

// Cada Run que afecta una revisión obtiene un objeto Revision correspondiente.
// La colección de revisiones es considerablemente más grande que la forma condensada que imprimimos arriba,
// dependiendo de cuántos Runs hayamos segmentado el documento durante la edición en Microsoft Word.
std::cout << System::String::Format(u"\n{0} revisions:", revisions->get_Count()) << std::endl;

{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Revision>>> e = revisions->GetEnumerator();
    while (e->MoveNext())
    {
        // Un StyleDefinitionChange afecta estrictamente a los estilos y no a los nodos del documento. Esto significa que la "ParentStyle"
        // propiedad siempre estará en uso, mientras que ParentNode siempre será nulo.
        // Dado que todos los demás cambios afectan a los nodos, ParentNode estará en uso, y ParentStyle será nulo.
        if (e->get_Current()->get_RevisionType() == Aspose::Words::RevisionType::StyleDefinitionChange)
        {
            std::cout << (System::String::Format(u"\tRevision type \"{0}\", ", e->get_Current()->get_RevisionType()) + System::String::Format(u"author: {0}, style: [{1}]", e->get_Current()->get_Author(), e->get_Current()->get_ParentStyle()->get_Name())) << std::endl;
        }
        else
        {
            std::cout << (System::String::Format(u"\tRevision type \"{0}\", ", e->get_Current()->get_RevisionType()) + System::String::Format(u"author: {0}, contents: [{1}]", e->get_Current()->get_Author(), e->get_Current()->get_ParentNode()->GetText().Trim())) << std::endl;
        }
    }
}

// Rechaza todas las revisiones mediante la colección, devolviendo el documento a su forma original.
revisions->RejectAll();

ASSERT_EQ(0, revisions->get_Count());
```

## Ver también

* Class [RevisionGroup](../../revisiongroup/)
* Class [RevisionGroupCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
