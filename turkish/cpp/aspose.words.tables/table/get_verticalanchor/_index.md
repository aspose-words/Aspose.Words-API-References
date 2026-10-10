---
title: "Aspose::Words::Tables::Table::get_VerticalAnchor yöntemi"
linktitle: "get_VerticalAnchor"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::Table::get_VerticalAnchor yöntemi. Yüzen tablonun dikey konumlandırmasının hesaplanacağı temel nesneyi alır. Varsayılan değer C++'ta Margin'dir."
type: docs
weight: 41000
url: /tr/cpp/aspose.words.tables/table/get_verticalanchor/
---
## Table::get_VerticalAnchor method


Yüzen tablonun dikey konumlandırmasının hesaplanacağı temel nesneyi alır. Varsayılan değer [Margin](../../../aspose.words.drawing/relativeverticalposition/)'dır.

```cpp
Aspose::Words::Drawing::RelativeVerticalPosition Aspose::Words::Tables::Table::get_VerticalAnchor()
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

* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
