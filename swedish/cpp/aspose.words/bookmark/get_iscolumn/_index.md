---
title: "Aspose::Words::Bookmark::get_IsColumn metod"
linktitle: "get_IsColumn"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Bookmark::get_IsColumn metod. Returnerar true om detta bokmärke är ett tabellkolumnbokmärke i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words/bookmark/get_iscolumn/
---
## Bookmark::get_IsColumn method


Returnerar **true** om detta bokmärke är ett tabellkolumnbokmärke.

```cpp
bool Aspose::Words::Bookmark::get_IsColumn()
```


## Exempel



Visar hur man hämtar information om tabellkolumnbokmärken.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table column bookmarks.doc");

for (auto&& bookmark : System::IterateOver(doc->get_Range()->get_Bookmarks()))
{
    // Om ett bokmärke omger kolumner i en tabell är det ett tabellkolumnbokmärke, och dess IsColumn-flagga sätts till true.
    std::cout << System::String::Format(u"Bookmark: {0}{1}", bookmark->get_Name(), (bookmark->get_IsColumn() ? System::String(u" (Column)") : System::String(u""))) << std::endl;
    if (bookmark->get_IsColumn())
    {
        auto row = System::AsCast<Aspose::Words::Tables::Row>(bookmark->get_BookmarkStart()->GetAncestor(Aspose::Words::NodeType::Row));
        if (row != nullptr && bookmark->get_FirstColumn() < row->get_Cells()->get_Count())
        {
            // Skriv ut innehållet i den första och sista kolumnen som omges av bokmärket.
            std::cout << row->get_Cells()->idx_get(bookmark->get_FirstColumn())->GetText().TrimEnd(System::MakeArray<char16_t>({Aspose::Words::ControlChar::CellChar})) << std::endl;
            std::cout << row->get_Cells()->idx_get(bookmark->get_LastColumn())->GetText().TrimEnd(System::MakeArray<char16_t>({Aspose::Words::ControlChar::CellChar})) << std::endl;
        }
    }
}
```

## Se även

* Class [Bookmark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
