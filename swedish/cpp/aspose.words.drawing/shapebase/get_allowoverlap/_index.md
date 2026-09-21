---
title: "Aspose::Words::Drawing::ShapeBase::get_AllowOverlap metod"
linktitle: "get_AllowOverlap"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShapeBase::get_AllowOverlap‑metod. Hämtar eller anger ett värde som specificerar om den här formen kan överlappa andra former i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words.drawing/shapebase/get_allowoverlap/
---
## ShapeBase::get_AllowOverlap method


Hämtar eller anger ett värde som specificerar om denna form kan överlappa andra former.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_AllowOverlap()
```

## Anmärkningar


Denna egenskap påverkar formens beteende i Microsoft Word. Aspose.Words ignorerar värdet av denna egenskap.

Denna egenskap gäller endast för former på toppnivå.

Standardvärdet är **true**.

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

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
