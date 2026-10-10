---
title: "Méthode Aspose::Words::ParagraphFormat::get_KeepWithNext"
linktitle: "get_KeepWithNext"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::ParagraphFormat::get_KeepWithNext méthode. Vrai si le paragraphe doit rester sur la même page que le paragraphe qui le suit en C++."
type: docs
weight: 18000
url: /fr/cpp/aspose.words/paragraphformat/get_keepwithnext/
---
## ParagraphFormat::get_KeepWithNext method


Vrai si le paragraphe doit rester sur la même page que le paragraphe qui le suit.

```cpp
bool Aspose::Words::ParagraphFormat::get_KeepWithNext()
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

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
