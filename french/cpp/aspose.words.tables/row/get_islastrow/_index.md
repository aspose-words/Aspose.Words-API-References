---
title: "Aspose::Words::Tables::Row::get_IsLastRow méthode"
linktitle: "get_IsLastRow"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Tables::Row::get_IsLastRow méthode. Vrai si c'est la dernière ligne d'un tableau ; faux sinon en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words.tables/row/get_islastrow/
---
## Row::get_IsLastRow method


Vrai si c'est la dernière ligne d'un tableau ; faux sinon.

```cpp
bool Aspose::Words::Tables::Row::get_IsLastRow()
```


## Exemples



Montre comment définir un tableau pour qu'il reste ensemble sur la même page.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table spanning two pages.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Activer KeepWithNext pour chaque paragraphe du tableau sauf pour le
// les derniers de la dernière ligne empêcheront le tableau de se diviser sur plusieurs pages.
for (auto&& cell : System::IterateOver<Aspose::Words::Tables::Cell>(table->GetChildNodes(Aspose::Words::NodeType::Cell, true)))
{
    for (auto&& para : System::IterateOver<Aspose::Words::Paragraph>(cell->get_Paragraphs()))
    {
        ASSERT_TRUE(para->get_IsInCell());

        if (!(cell->get_ParentRow()->get_IsLastRow() && para->get_IsEndOfCell()))
        {
            para->get_ParagraphFormat()->set_KeepWithNext(true);
        }
    }
}

doc->Save(get_ArtifactsDir() + u"Table.KeepTableTogether.docx");
```

## Voir aussi

* Class [Row](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
