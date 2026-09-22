---
title: "Aspose::Words::Bookmark::get_IsColumn yöntemi"
linktitle: "get_IsColumn"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Bookmark::get_IsColumn yöntemi. Bu yer işareti bir tablo sütunu yer işareti ise C++'da true döndürür."
type: docs
weight: 5000
url: /tr/cpp/aspose.words/bookmark/get_iscolumn/
---
## Bookmark::get_IsColumn method


Bu yer imi bir tablo sütun yer imi ise **true** döndürür.

```cpp
bool Aspose::Words::Bookmark::get_IsColumn()
```


## Örnekler



Tablo sütun yer imleri hakkında bilgi almanın nasıl yapılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table column bookmarks.doc");

for (auto&& bookmark : System::IterateOver(doc->get_Range()->get_Bookmarks()))
{
    // Bir yer imi bir tablonun sütunlarını kapsıyorsa, bu bir tablo sütun yer imidir ve IsColumn bayrağı true olarak ayarlanır.
    std::cout << System::String::Format(u"Bookmark: {0}{1}", bookmark->get_Name(), (bookmark->get_IsColumn() ? System::String(u" (Column)") : System::String(u""))) << std::endl;
    if (bookmark->get_IsColumn())
    {
        auto row = System::AsCast<Aspose::Words::Tables::Row>(bookmark->get_BookmarkStart()->GetAncestor(Aspose::Words::NodeType::Row));
        if (row != nullptr && bookmark->get_FirstColumn() < row->get_Cells()->get_Count())
        {
            // Yer iminin kapsadığı ilk ve son sütunların içeriğini yazdır.
            std::cout << row->get_Cells()->idx_get(bookmark->get_FirstColumn())->GetText().TrimEnd(System::MakeArray<char16_t>({Aspose::Words::ControlChar::CellChar})) << std::endl;
            std::cout << row->get_Cells()->idx_get(bookmark->get_LastColumn())->GetText().TrimEnd(System::MakeArray<char16_t>({Aspose::Words::ControlChar::CellChar})) << std::endl;
        }
    }
}
```

## Ayrıca Bakınız

* Class [Bookmark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
