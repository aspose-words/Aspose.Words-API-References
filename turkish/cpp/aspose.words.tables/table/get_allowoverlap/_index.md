---
title: "Aspose::Words::Tables::Table::get_AllowOverlap yöntemi"
linktitle: "get_AllowOverlap"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::Table::get_AllowOverlap yöntemi. Yüzen bir tablonun, belgede diğer yüzen nesnelerin görüntülendiğinde tablo sınırlarıyla çakışmasına izin verip vermediğini alır. Varsayılan değer C++'da true'dur."
type: docs
weight: 14000
url: /tr/cpp/aspose.words.tables/table/get_allowoverlap/
---
## Table::get_AllowOverlap method


Bir yüzen tablonun, belgede diğer yüzen nesnelerin görüntülendiğinde kapsamının üstüne gelmesine izin verip vermeyeceğini alır. Varsayılan değer **true**'dır.

```cpp
bool Aspose::Words::Tables::Table::get_AllowOverlap()
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

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
