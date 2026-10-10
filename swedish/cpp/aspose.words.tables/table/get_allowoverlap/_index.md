---
title: "Aspose::Words::Tables::Table::get_AllowOverlap metod"
linktitle: "get_AllowOverlap"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::Table::get_AllowOverlap metod. Hämtar om en flytande tabell ska tillåta andra flytande objekt i dokumentet att överlappa dess omfattning när den visas. Standardvärdet är true i C++."
type: docs
weight: 14000
url: /sv/cpp/aspose.words.tables/table/get_allowoverlap/
---
## Table::get_AllowOverlap method


Hämtar om en flytande tabell ska tillåta andra flytande objekt i dokumentet att överlappa dess omfång när den visas. Standardvärdet är **true**.

```cpp
bool Aspose::Words::Tables::Table::get_AllowOverlap()
```


## Exempel



Visar hur man arbetar med egenskaper för flytande tabeller.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table wrapped by text.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

if (table->get_TextWrapping() == Aspose::Words::Tables::TextWrapping::Around)
{
    ASSERT_EQ(Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, table->get_HorizontalAnchor());
    ASSERT_EQ(Aspose::Words::Drawing::RelativeVerticalPosition::Paragraph, table->get_VerticalAnchor());
    ASPOSE_ASSERT_EQ(false, table->get_AllowOverlap());

    // Endast Margin, Page, Column är tillgängliga i RelativeHorizontalPosition för HorizontalAnchor‑setter.
    // ArgumentException kommer att kastas för alla andra värden.
    table->set_HorizontalAnchor(Aspose::Words::Drawing::RelativeHorizontalPosition::Column);

    // Endast Margin, Page, Paragraph är tillgängliga i RelativeVerticalPosition för VerticalAnchor‑setter.
    // ArgumentException kommer att kastas för alla andra värden.
    table->set_VerticalAnchor(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
}
```

## Se även

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
