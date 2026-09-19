---
title: "Aspose::Words::Bookmark::get_LastColumn metodo"
linktitle: "get_LastColumn"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Bookmark::get_LastColumn metodo. Ottiene l'indice base zero dell'ultima colonna dell'intervallo di colonne della tabella associato al segnalibro in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words/bookmark/get_lastcolumn/
---
## Bookmark::get_LastColumn method


Ottiene l'indice basato su zero dell'ultima colonna dell'intervallo di colonne della tabella associato al segnalibro.

```cpp
int32_t Aspose::Words::Bookmark::get_LastColumn()
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
