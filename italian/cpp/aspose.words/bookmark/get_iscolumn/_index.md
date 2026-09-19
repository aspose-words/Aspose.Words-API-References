---
title: "Metodo Aspose::Words::Bookmark::get_IsColumn"
linktitle: "get_IsColumn"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Bookmark::get_IsColumn. Restituisce true se questo segnalibro è un segnalibro di colonna di tabella in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words/bookmark/get_iscolumn/
---
## Bookmark::get_IsColumn method


Restituisce **true** se questo segnalibro è un segnalibro di colonna di tabella.

```cpp
bool Aspose::Words::Bookmark::get_IsColumn()
```


## Esempi



Mostra come ottenere informazioni sui segnalibri di colonne di tabella.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table column bookmarks.doc");

for (auto&& bookmark : System::IterateOver(doc->get_Range()->get_Bookmarks()))
{
    // Se un segnalibro racchiude colonne di una tabella, è un segnalibro di colonna di tabella e il suo flag IsColumn è impostato su true.
    std::cout << System::String::Format(u"Bookmark: {0}{1}", bookmark->get_Name(), (bookmark->get_IsColumn() ? System::String(u" (Column)") : System::String(u""))) << std::endl;
    if (bookmark->get_IsColumn())
    {
        auto row = System::AsCast<Aspose::Words::Tables::Row>(bookmark->get_BookmarkStart()->GetAncestor(Aspose::Words::NodeType::Row));
        if (row != nullptr && bookmark->get_FirstColumn() < row->get_Cells()->get_Count())
        {
            // Stampa il contenuto della prima e dell'ultima colonna racchiuse dal segnalibro.
            std::cout << row->get_Cells()->idx_get(bookmark->get_FirstColumn())->GetText().TrimEnd(System::MakeArray<char16_t>({Aspose::Words::ControlChar::CellChar})) << std::endl;
            std::cout << row->get_Cells()->idx_get(bookmark->get_LastColumn())->GetText().TrimEnd(System::MakeArray<char16_t>({Aspose::Words::ControlChar::CellChar})) << std::endl;
        }
    }
}
```

## Vedi anche

* Class [Bookmark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
