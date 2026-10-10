---
title: "Aspose::Words::Drawing::ShapeBase::get_AllowOverlap Methode"
linktitle: "get_AllowOverlap"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeBase::get_AllowOverlap Methode. Gibt einen Wert zurück oder legt ihn fest, der angibt, ob diese Form andere Formen in C++ überlappen kann."
type: docs
weight: 3000
url: /de/cpp/aspose.words.drawing/shapebase/get_allowoverlap/
---
## ShapeBase::get_AllowOverlap method


Liest oder setzt einen Wert, der angibt, ob diese Form andere Formen überlappen kann.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_AllowOverlap()
```

## Hinweise


Diese Eigenschaft beeinflusst das Verhalten der Form in Microsoft Word. Aspose.Words ignoriert den Wert dieser Eigenschaft.

Diese Eigenschaft gilt nur für Formen der obersten Ebene.

Der Standardwert ist **true**.

## Beispiele



Zeigt, wie man mit den Eigenschaften schwebender Tabellen arbeitet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table wrapped by text.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

if (table->get_TextWrapping() == Aspose::Words::Tables::TextWrapping::Around)
{
    ASSERT_EQ(Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, table->get_HorizontalAnchor());
    ASSERT_EQ(Aspose::Words::Drawing::RelativeVerticalPosition::Paragraph, table->get_VerticalAnchor());
    ASPOSE_ASSERT_EQ(false, table->get_AllowOverlap());

    // Nur Margin, Page und Column sind in RelativeHorizontalPosition für den HorizontalAnchor-Setter verfügbar.
    // Eine ArgumentException wird für alle anderen Werte ausgelöst.
    table->set_HorizontalAnchor(Aspose::Words::Drawing::RelativeHorizontalPosition::Column);

    // Nur Margin, Page und Paragraph sind in RelativeVerticalPosition für den VerticalAnchor-Setter verfügbar.
    // Eine ArgumentException wird für alle anderen Werte ausgelöst.
    table->set_VerticalAnchor(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
}
```

## Siehe auch

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
