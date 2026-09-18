---
title: "Aspose::Words::Bookmark::get_LastColumn Methode"
linktitle: "get_LastColumn"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Bookmark::get_LastColumn Methode. Gibt den nullbasierten Index der letzten Spalte des Tabellenspaltenbereichs zurück, der dem Lesezeichen zugeordnet ist, in C++."
type: docs
weight: 6000
url: /de/cpp/aspose.words/bookmark/get_lastcolumn/
---
## Bookmark::get_LastColumn method


Gibt den nullbasierten Index der letzten Spalte des Tabellen‑Spaltenbereichs zurück, der dem Lesezeichen zugeordnet ist.

```cpp
int32_t Aspose::Words::Bookmark::get_LastColumn()
```


## Beispiele



Zeigt, wie man Informationen über Tabellenspalten-Lesezeichen erhält.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table column bookmarks.doc");

for (auto&& bookmark : System::IterateOver(doc->get_Range()->get_Bookmarks()))
{
    // Wenn ein Lesezeichen Spalten einer Tabelle umschließt, ist es ein Tabellenspalten-Lesezeichen, und sein IsColumn-Flag wird auf true gesetzt.
    std::cout << System::String::Format(u"Bookmark: {0}{1}", bookmark->get_Name(), (bookmark->get_IsColumn() ? System::String(u" (Column)") : System::String(u""))) << std::endl;
    if (bookmark->get_IsColumn())
    {
        auto row = System::AsCast<Aspose::Words::Tables::Row>(bookmark->get_BookmarkStart()->GetAncestor(Aspose::Words::NodeType::Row));
        if (row != nullptr && bookmark->get_FirstColumn() < row->get_Cells()->get_Count())
        {
            // Gibt den Inhalt der ersten und letzten vom Lesezeichen umschlossenen Spalten aus.
            std::cout << row->get_Cells()->idx_get(bookmark->get_FirstColumn())->GetText().TrimEnd(System::MakeArray<char16_t>({Aspose::Words::ControlChar::CellChar})) << std::endl;
            std::cout << row->get_Cells()->idx_get(bookmark->get_LastColumn())->GetText().TrimEnd(System::MakeArray<char16_t>({Aspose::Words::ControlChar::CellChar})) << std::endl;
        }
    }
}
```

## Siehe auch

* Class [Bookmark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
