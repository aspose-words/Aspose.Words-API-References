---
title: "Aspose::Words::Bookmark::get_LastColumn méthode"
linktitle: "get_LastColumn"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Bookmark::get_LastColumn méthode. Obtient l'index basé sur zéro de la dernière colonne de la plage de colonnes du tableau associée au signet en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words/bookmark/get_lastcolumn/
---
## Bookmark::get_LastColumn method


Obtient l'index basé sur zéro de la dernière colonne de la plage de colonnes du tableau associée au signet.

```cpp
int32_t Aspose::Words::Bookmark::get_LastColumn()
```


## Exemples



Montre comment obtenir des informations sur les signets de colonnes de tableau.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table column bookmarks.doc");

for (auto&& bookmark : System::IterateOver(doc->get_Range()->get_Bookmarks()))
{
    // Si un signet englobe des colonnes d'un tableau, il s'agit d'un signet de colonne de tableau, et son drapeau IsColumn est défini sur true.
    std::cout << System::String::Format(u"Bookmark: {0}{1}", bookmark->get_Name(), (bookmark->get_IsColumn() ? System::String(u" (Column)") : System::String(u""))) << std::endl;
    if (bookmark->get_IsColumn())
    {
        auto row = System::AsCast<Aspose::Words::Tables::Row>(bookmark->get_BookmarkStart()->GetAncestor(Aspose::Words::NodeType::Row));
        if (row != nullptr && bookmark->get_FirstColumn() < row->get_Cells()->get_Count())
        {
            // Imprime le contenu des première et dernière colonnes englobées par le signet.
            std::cout << row->get_Cells()->idx_get(bookmark->get_FirstColumn())->GetText().TrimEnd(System::MakeArray<char16_t>({Aspose::Words::ControlChar::CellChar})) << std::endl;
            std::cout << row->get_Cells()->idx_get(bookmark->get_LastColumn())->GetText().TrimEnd(System::MakeArray<char16_t>({Aspose::Words::ControlChar::CellChar})) << std::endl;
        }
    }
}
```

## Voir aussi

* Class [Bookmark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
