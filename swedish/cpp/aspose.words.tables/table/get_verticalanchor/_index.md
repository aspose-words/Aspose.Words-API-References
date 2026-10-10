---
title: "Aspose::Words::Tables::Table::get_VerticalAnchor metod"
linktitle: "get_VerticalAnchor"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::Table::get_VerticalAnchor metod. Hämtar basobjektet som den vertikala positioneringen av den flytande tabellen ska beräknas från. Standardvärdet är Margin i C++."
type: docs
weight: 41000
url: /sv/cpp/aspose.words.tables/table/get_verticalanchor/
---
## Table::get_VerticalAnchor method


Hämtar basobjektet som den vertikala positioneringen av den flytande tabellen ska beräknas från. Standardvärdet är [Margin](../../../aspose.words.drawing/relativeverticalposition/).

```cpp
Aspose::Words::Drawing::RelativeVerticalPosition Aspose::Words::Tables::Table::get_VerticalAnchor()
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

* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
