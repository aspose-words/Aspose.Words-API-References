---
title: "Aspose::Words::Tables::PreferredWidth::get_Value metodo"
linktitle: "get_Value"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::PreferredWidth::get_Value metodo. Ottiene il valore della larghezza preferita. L'unità di misura è specificata nella proprietà Type in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.tables/preferredwidth/get_value/
---
## PreferredWidth::get_Value method


Ottiene il valore della larghezza preferita. L'unità di misura è specificata nella proprietà [Type](../get_type/).

```cpp
double Aspose::Words::Tables::PreferredWidth::get_Value() const
```


## Esempi



Mostra come verificare il tipo e il valore della larghezza preferita di una cella di tabella.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::Tables::Cell> firstCell = table->get_FirstRow()->get_FirstCell();

ASSERT_EQ(Aspose::Words::Tables::PreferredWidthType::Percent, firstCell->get_CellFormat()->get_PreferredWidth()->get_Type());
ASPOSE_ASSERT_EQ(11.16, firstCell->get_CellFormat()->get_PreferredWidth()->get_Value());
```

## Vedi anche

* Class [PreferredWidth](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
