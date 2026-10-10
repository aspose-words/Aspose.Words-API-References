---
title: "Aspose::Words::Tables::RowCollection::idx_get-metoden"
linktitle: "idx_get"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::RowCollection::idx_get-metoden. Hämtar en Row på det angivna indexet i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.tables/rowcollection/idx_get/
---
## RowCollection::idx_get method


Hämtar en [Row](../../row/) på det angivna indexet.

```cpp
System::SharedPtr<Aspose::Words::Tables::Row> Aspose::Words::Tables::RowCollection::idx_get(int32_t index)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| index | int32_t | Ett index i samlingen. |
## Anmärkningar


Indexet är nollbaserat.

Negativa index är tillåtna och indikerar åtkomst från slutet av samlingen. Till exempel betyder -1 det sista objektet, -2 betyder det näst sista och så vidare.

Om index är större än eller lika med antalet objekt i listan, returneras en null-referens.

Om index är negativt och dess absoluta värde är större än antalet objekt i listan, returneras en null-referens.

## Exempel



Visar hur man itererar genom alla tabeller i dokumentet och skriver ut innehållet i varje cell.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::TableCollection> tables = doc->get_FirstSection()->get_Body()->get_Tables();

ASSERT_EQ(2, tables->ToArray()->get_Length());

for (int32_t i = 0; i < tables->get_Count(); i++)
{
    std::cout << System::String::Format(u"Start of Table {0}", i) << std::endl;

    System::SharedPtr<Aspose::Words::Tables::RowCollection> rows = tables->idx_get(i)->get_Rows();

    // Vi kan använda metoden "ToArray" på en rad-samling för att klona den till en array.
    ASPOSE_ASSERT_EQ(rows, rows->ToArray());
    ASPOSE_ASSERT_NS(rows, rows->ToArray());

    for (int32_t j = 0; j < rows->get_Count(); j++)
    {
        std::cout << System::String::Format(u"\tStart of Row {0}", j) << std::endl;

        System::SharedPtr<Aspose::Words::Tables::CellCollection> cells = rows->idx_get(j)->get_Cells();

        // Vi kan använda metoden "ToArray" på en cell-samling för att klona den till en array.
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

## Se även

* Class [Row](../../row/)
* Class [RowCollection](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
