---
title: "Aspose::Words::Markup::IStructuredDocumentTag::RemoveSelfOnly méthode"
linktitle: "RemoveSelfOnly"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Markup::IStructuredDocumentTag::RemoveSelfOnly méthode. Supprime uniquement ce nœud SDT lui‑même, mais conserve son contenu dans l'arborescence du document en C++."
type: docs
weight: 17500
url: /fr/cpp/aspose.words.markup/istructureddocumenttag/removeselfonly/
---
## IStructuredDocumentTag::RemoveSelfOnly method


Supprime uniquement ce nœud SDT lui‑-même, mais conserve son contenu dans l'arborescence du document.

```cpp
virtual void Aspose::Words::Markup::IStructuredDocumentTag::RemoveSelfOnly()=0
```


## Exemples



Montre comment supprimer la balise de document structuré, mais conserve le contenu à l'intérieur.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

// Cette collection fournit une interface unifiée pour accéder aux balises structurées à portée et non à portée.
System::SharedPtr<System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Markup::IStructuredDocumentTag>>> sdts = doc->get_Range()->get_StructuredDocumentTags()->LINQ_ToList();
ASSERT_EQ(5, sdts->LINQ_Count());

// Ici, nous pouvons obtenir les nœuds enfants à partir de l'interface commune des balises structurées à portée et non à portée.
for (auto&& sdt : System::IterateOver(sdts))
{
    if (sdt->GetChildNodes(Aspose::Words::NodeType::Any, false)->get_Count() > 0)
    {
        sdt->RemoveSelfOnly();
    }
}

sdts = doc->get_Range()->get_StructuredDocumentTags()->LINQ_ToList();
ASSERT_EQ(0, sdts->LINQ_Count());
```

## Voir aussi

* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
