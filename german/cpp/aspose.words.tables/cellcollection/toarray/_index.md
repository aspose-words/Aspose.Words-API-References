---
title: "Aspose::Words::Tables::CellCollection::ToArray-Methode"
linktitle: "ToArray"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::CellCollection::ToArray-Methode. Kopiert alle Zellen aus der Sammlung in ein neues Zellen-Array in C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words.tables/cellcollection/toarray/
---
## CellCollection::ToArray method


Kopiert alle Zellen aus der Sammlung in ein neues Array von Zellen.

```cpp
System::ArrayPtr<System::SharedPtr<Aspose::Words::Tables::Cell>> Aspose::Words::Tables::CellCollection::ToArray()
```


### ReturnValue

Ein Array von Zellen.

## Beispiele



Zeigt, wie man durch alle Tabellen im Dokument iteriert und den Inhalt jeder Zelle ausgibt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::TableCollection> tables = doc->get_FirstSection()->get_Body()->get_Tables();

ASSERT_EQ(2, tables->ToArray()->get_Length());

for (int32_t i = 0; i < tables->get_Count(); i++)
{
    std::cout << System::String::Format(u"Start of Table {0}", i) << std::endl;

    System::SharedPtr<Aspose::Words::Tables::RowCollection> rows = tables->idx_get(i)->get_Rows();

    // Wir können die Methode "ToArray" auf einer Zeilensammlung verwenden, um sie in ein Array zu klonen.
    ASPOSE_ASSERT_EQ(rows, rows->ToArray());
    ASPOSE_ASSERT_NS(rows, rows->ToArray());

    for (int32_t j = 0; j < rows->get_Count(); j++)
    {
        std::cout << System::String::Format(u"\tStart of Row {0}", j) << std::endl;

        System::SharedPtr<Aspose::Words::Tables::CellCollection> cells = rows->idx_get(j)->get_Cells();

        // Wir können die Methode "ToArray" auf einer Zellsammlung verwenden, um sie in ein Array zu klonen.
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

## Siehe auch

* Class [Cell](../../cell/)
* Class [CellCollection](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
