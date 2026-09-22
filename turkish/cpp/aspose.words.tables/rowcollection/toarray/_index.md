---
title: "Aspose::Words::Tables::RowCollection::ToArray metodu"
linktitle: "ToArray"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::RowCollection::ToArray metodu. Koleksiyondaki tüm satırları C++'ta yeni bir satır dizisine kopyalar."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.tables/rowcollection/toarray/
---
## RowCollection::ToArray method


Koleksiyondaki tüm satırları yeni bir satır dizisine kopyalar.

```cpp
System::ArrayPtr<System::SharedPtr<Aspose::Words::Tables::Row>> Aspose::Words::Tables::RowCollection::ToArray()
```


### ReturnValue

Satırların bir dizisi.

## Örnekler



Belgedeki tüm tabloları dolaşmayı ve her hücrenin içeriğini yazdırmayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::TableCollection> tables = doc->get_FirstSection()->get_Body()->get_Tables();

ASSERT_EQ(2, tables->ToArray()->get_Length());

for (int32_t i = 0; i < tables->get_Count(); i++)
{
    std::cout << System::String::Format(u"Start of Table {0}", i) << std::endl;

    System::SharedPtr<Aspose::Words::Tables::RowCollection> rows = tables->idx_get(i)->get_Rows();

    // Bir satır koleksiyonunda "ToArray" metodunu kullanarak onu bir diziye kopyalayabiliriz.
    ASPOSE_ASSERT_EQ(rows, rows->ToArray());
    ASPOSE_ASSERT_NS(rows, rows->ToArray());

    for (int32_t j = 0; j < rows->get_Count(); j++)
    {
        std::cout << System::String::Format(u"\tStart of Row {0}", j) << std::endl;

        System::SharedPtr<Aspose::Words::Tables::CellCollection> cells = rows->idx_get(j)->get_Cells();

        // Bir hücre koleksiyonunda "ToArray" metodunu kullanarak onu bir diziye kopyalayabiliriz.
        ASPOSE_ASSERT_EQ(cells, cells->ToArray());
        ASPOSE_ASSERT_NS(cells, cells->ToArray());

        for (int32_t k = 0; k < cells->get_Count(); k++)
        {
            System::String cellText = cells->idx_get(k)->ToString(Aspose::Words::SaveFormat::Text).Trim();
            std::cout << System::String::Format(u"\t\tContents of Cell:{0} = \"{1}\"", k, cellText) << std::endl;
        }

        std::cout << System::String::Format(u"\tEnd of Row {0}", j) << std::endl;
    }

    std::cout << System::String::Format(u"End of Table {0}\n", i) << std::endl;
}
```

## Ayrıca Bakınız

* Class [Row](../../row/)
* Class [RowCollection](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
