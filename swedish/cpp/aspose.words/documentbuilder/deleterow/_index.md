---
title: "Aspose::Words::DocumentBuilder::DeleteRow‑metod"
linktitle: "DeleteRow"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBuilder::DeleteRow‑metod. Tar bort en rad från en tabell i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words/documentbuilder/deleterow/
---
## DocumentBuilder::DeleteRow method


Tar bort en rad från en tabell.

```cpp
System::SharedPtr<Aspose::Words::Tables::Row> Aspose::Words::DocumentBuilder::DeleteRow(int32_t tableIndex, int32_t rowIndex)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| tableIndex | int32_t | Tabellens index. |
| rowIndex | int32_t | Index för raden i tabellen. |

### ReturnValue

Radnoden som just togs bort.
## Anmärkningar


Om markören är inne i raden som tas bort, flyttas markören ut till nästa rad eller till nästa stycke efter tabellen.

Om du tar bort en rad från en tabell som bara innehåller en rad, tas hela tabellen bort.

För indexparametrarna, när index är större än eller lika med 0, anger det ett index från början där 0 är det första elementet. När index är mindre än 0, anger det ett index från slutet där -1 är det sista elementet.

## Exempel



Visar hur man tar bort en rad från en tabell.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, cell 1.");
builder->InsertCell();
builder->Write(u"Row 2, cell 2.");
builder->EndTable();

ASSERT_EQ(2, table->get_Rows()->get_Count());

// Ta bort den första raden i den första tabellen i dokumentet.
builder->DeleteRow(0, 0);

ASSERT_EQ(1, table->get_Rows()->get_Count());
ASSERT_EQ(u"Row 2, cell 1.\aRow 2, cell 2.\a\a", table->GetText().Trim());
```

## Se även

* Class [Row](../../../aspose.words.tables/row/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
