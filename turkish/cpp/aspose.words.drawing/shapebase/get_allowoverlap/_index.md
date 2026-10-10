---
title: "Aspose::Words::Drawing::ShapeBase::get_AllowOverlap metodu"
linktitle: "get_AllowOverlap"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::ShapeBase::get_AllowOverlap metodu. C++'ta bu şeklin diğer şekillerin üzerine gelip gelemeyeceğini belirten bir değeri alır veya ayarlar."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.drawing/shapebase/get_allowoverlap/
---
## ShapeBase::get_AllowOverlap method


Bu şeklin diğer şekillerin üzerine çıkıp çıkamayacağını belirten bir değeri alır veya ayarlar.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_AllowOverlap()
```

## Açıklamalar


Bu özellik, şeklin Microsoft Word'deki davranışını etkiler. Aspose.Words bu özelliğin değerini yok sayar.

Bu özellik yalnızca üst düzey şekiller için geçerlidir.

Varsayılan değer **true**'dır.

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

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
