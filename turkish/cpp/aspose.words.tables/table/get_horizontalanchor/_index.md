---
title: "Aspose::Words::Tables::Table::get_HorizontalAnchor method"
linktitle: "get_HorizontalAnchor"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::Table::get_HorizontalAnchor yöntemi. Yüzen tablonun yatay konumlandırmasının hesaplanacağı temel nesneyi alır. Varsayılan değer C++'da Column'dur."
type: docs
weight: 24000
url: /tr/cpp/aspose.words.tables/table/get_horizontalanchor/
---
## Table::get_HorizontalAnchor method


Yüzen tablonun yatay konumlandırmasının hesaplanacağı temel nesneyi alır. Varsayılan değer [Column](../../../aspose.words.drawing/relativehorizontalposition/).

```cpp
Aspose::Words::Drawing::RelativeHorizontalPosition Aspose::Words::Tables::Table::get_HorizontalAnchor()
```


## Örnekler



Yüzen tabloların özellikleriyle nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table wrapped by text.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

if (table->get_TextWrapping() == Aspose::Words::Tables::TextWrapping::Around)
{
    ASSERT_EQ(Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, table->get_HorizontalAnchor());
    ASSERT_EQ(Aspose::Words::Drawing::RelativeVerticalPosition::Paragraph, table->get_VerticalAnchor());
    ASPOSE_ASSERT_EQ(false, table->get_AllowOverlap());

    // HorizontalAnchor ayarlayıcısı için RelativeHorizontalPosition içinde yalnızca Margin, Page, Column kullanılabilir.
    // Diğer tüm değerler için ArgumentException fırlatılacaktır.
    table->set_HorizontalAnchor(Aspose::Words::Drawing::RelativeHorizontalPosition::Column);

    // VerticalAnchor ayarlayıcısı için RelativeVerticalPosition içinde yalnızca Margin, Page, Paragraph kullanılabilir.
    // Diğer tüm değerler için ArgumentException fırlatılacaktır.
    table->set_VerticalAnchor(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
}
```

## Ayrıca Bakınız

* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
