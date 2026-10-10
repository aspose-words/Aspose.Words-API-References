---
title: "Aspose::Words::Tables::RowCollection class"
linktitle: "RowCollection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::RowCollection-klass. Tillhandahåller typad åtkomst till en samling av Row-noder. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.tables/rowcollection/
---
## RowCollection class


Tillhandahåller typad åtkomst till en samling av [Row](../row/) noder. För att lära dig mer, besök dokumentationsartikeln [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class RowCollection : public Aspose::Words::NodeCollection
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Lägger till en nod i slutet av samlingen. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Tar bort alla noder från denna samling och från dokumentet. |
| [Contains](../../aspose.words/nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Avgör om en nod finns i samlingen. |
| [get_Count](../../aspose.words/nodecollection/get_count/)() | Hämtar antalet noder i samlingen. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() override | Tillhandahåller en enkel "foreach"‑liknande iteration över samlingen av noder. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Hämtar en [Row](../row/) på det angivna indexet. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Returnerar det nollbaserade indexet för den angivna noden. |
| [Insert](../../aspose.words/nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Infogar en nod i samlingen på det angivna indexet. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../../aspose.words/nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Tar bort noden från samlingen och från dokumentet. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(int32_t) | Tar bort noden på det angivna indexet från samlingen och från dokumentet. |
| [ToArray](./toarray/)() | Kopierar alla rader från samlingen till en ny array av rader. |
| static [Type](./type/)() |  |

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

* Class [NodeCollection](../../aspose.words/nodecollection/)
* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
