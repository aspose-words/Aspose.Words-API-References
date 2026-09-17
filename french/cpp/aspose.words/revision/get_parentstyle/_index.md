---
title: "Aspose::Words::Revision::get_ParentStyle méthode"
linktitle: "get_ParentStyle"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Revision::get_ParentStyle méthode. Obtient le style parent immédiat (propriétaire) de cette révision. Cette propriété ne fonctionnera que pour le type de révision StyleDefinitionChange en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words/revision/get_parentstyle/
---
## Revision::get_ParentStyle method


Obtient le style parent immédiat (propriétaire) de cette révision. Cette propriété ne fonctionnera que pour le type de révision [StyleDefinitionChange](../../revisiontype/).

```cpp
System::SharedPtr<Aspose::Words::Style> Aspose::Words::Revision::get_ParentStyle()
```


## Exemples



Montre comment travailler avec la collection de révisions d'un document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");
System::SharedPtr<Aspose::Words::RevisionCollection> revisions = doc->get_Revisions();

// Cette collection possède elle-même une collection de groupes de révisions.
// Chaque groupe est une séquence de révisions adjacentes.
std::cout << System::String::Format(u"{0} revision groups:", revisions->get_Groups()->get_Count()) << std::endl;

// Itérez sur la collection de groupes et affichez le texte concerné par la révision.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::RevisionGroup>>> e = revisions->get_Groups()->GetEnumerator();
    while (e->MoveNext())
    {
        std::cout << (System::String::Format(u"\tGroup type \"{0}\", ", e->get_Current()->get_RevisionType()) + System::String::Format(u"author: {0}, contents: [{1}]", e->get_Current()->get_Author(), e->get_Current()->get_Text().Trim())) << std::endl;
    }
}

// Chaque Run qu'une révision affecte obtient un objet Revision correspondant.
// La collection de révisions est considérablement plus grande que la forme condensée que nous avons affichée ci‑dessus,
// en fonction du nombre de Runs que nous avons segmentés dans le document lors de l'édition avec Microsoft Word.
std::cout << System::String::Format(u"\n{0} revisions:", revisions->get_Count()) << std::endl;

{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::Revision>>> e = revisions->GetEnumerator();
    while (e->MoveNext())
    {
        // Un StyleDefinitionChange affecte strictement les styles et non les nœuds du document. Cela signifie que le "ParentStyle"
        // la propriété sera toujours utilisée, tandis que ParentNode sera toujours nul.
        // Puisque toutes les autres modifications affectent les nœuds, ParentNode sera au contraire utilisé, et ParentStyle sera nul.
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

// Rejetez toutes les révisions via la collection, rétablissant le document à sa forme originale.
revisions->RejectAll();

ASSERT_EQ(0, revisions->get_Count());
```

## Voir aussi

* Class [Style](../../style/)
* Class [Revision](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
