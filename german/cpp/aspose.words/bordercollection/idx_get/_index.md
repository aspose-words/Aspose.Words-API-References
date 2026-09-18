---
title: "Aspose::Words::BorderCollection::idx_get Methode"
linktitle: "idx_get"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::BorderCollection::idx_get Methode. Ruft ein Border‑Objekt nach Randtyp in C++ ab."
type: docs
weight: 18000
url: /de/cpp/aspose.words/bordercollection/idx_get/
---
## BorderCollection::idx_get(Aspose::Words::BorderType) method


Ruft ein [Border](../../border/) Objekt nach Randtyp ab.

```cpp
System::SharedPtr<Aspose::Words::Border> Aspose::Words::BorderCollection::idx_get(Aspose::Words::BorderType borderType)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| borderType | Aspose::Words::BorderType | Ein [BorderType](../../bordertype/) Wert, der den Typ des abzurufenden Randes angibt. |
## Hinweise


Beachten Sie, dass nicht alle Ränder für verschiedene Dokumentelemente vorhanden sind. Diese Methode wirft eine Ausnahme, wenn Sie einen Rand anfordern, der für das aktuelle Objekt nicht zutrifft.

## Beispiele



Zeigt, wie man Text mit Rahmen und Schattierung dekoriert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::BorderCollection> borders = builder->get_ParagraphFormat()->get_Borders();
borders->set_DistanceFromText(20);
borders->idx_get(Aspose::Words::BorderType::Left)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Right)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Top)->set_LineStyle(Aspose::Words::LineStyle::Double);
borders->idx_get(Aspose::Words::BorderType::Bottom)->set_LineStyle(Aspose::Words::LineStyle::Double);

System::SharedPtr<Aspose::Words::Shading> shading = builder->get_ParagraphFormat()->get_Shading();
shading->set_Texture(Aspose::Words::TextureIndex::TextureDiagonalCross);
shading->set_BackgroundPatternColor(System::Drawing::Color::get_LightCoral());
shading->set_ForegroundPatternColor(System::Drawing::Color::get_LightSalmon());

builder->Write(u"This paragraph is formatted with a double border and shading.");
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.ApplyBordersAndShading.docx");
```

## Siehe auch

* Class [Border](../../border/)
* Enum [BorderType](../../bordertype/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## BorderCollection::idx_get(int32_t) method


Ruft ein [Border](../../border/) Objekt nach Index ab.

```cpp
System::SharedPtr<Aspose::Words::Border> Aspose::Words::BorderCollection::idx_get(int32_t index)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| index | int32_t | Nullbasierter Index des abzurufenden Randes. |

## Beispiele



Zeigt, wie Randkollektionen Elemente teilen können.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Paragraph 1.");
builder->Write(u"Paragraph 2.");

// Da wir beim Erstellen dieselbe Randkonfiguration verwendet haben
// diese Absätze, teilen ihre Randkollektionen dieselben Elemente.
System::SharedPtr<Aspose::Words::BorderCollection> firstParagraphBorders = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Borders();
System::SharedPtr<Aspose::Words::BorderCollection> secondParagraphBorders = builder->get_CurrentParagraph()->get_ParagraphFormat()->get_Borders();

for (int32_t i = 0; i < firstParagraphBorders->get_Count(); i++)
{
    ASSERT_TRUE(System::ObjectExt::Equals(firstParagraphBorders->idx_get(i), secondParagraphBorders->idx_get(i)));
    ASSERT_EQ(System::ObjectExt::GetHashCode(firstParagraphBorders->idx_get(i)), System::ObjectExt::GetHashCode(secondParagraphBorders->idx_get(i)));
    ASSERT_FALSE(firstParagraphBorders->idx_get(i)->get_IsVisible());
}

for (auto&& border : System::IterateOver(secondParagraphBorders))
{
    border->set_LineStyle(Aspose::Words::LineStyle::DotDash);
}

// Nachdem wir den Linienstil der Ränder nur im zweiten Absatz geändert haben,
// teilen die Randkollektionen nicht mehr dieselben Elemente.
for (int32_t i = 0; i < firstParagraphBorders->get_Count(); i++)
{
    ASSERT_FALSE(System::ObjectExt::Equals(firstParagraphBorders->idx_get(i), secondParagraphBorders->idx_get(i)));
    ASSERT_NE(System::ObjectExt::GetHashCode(firstParagraphBorders->idx_get(i)), System::ObjectExt::GetHashCode(secondParagraphBorders->idx_get(i)));

    // Das Ändern des Aussehens eines leeren Randes macht ihn sichtbar.
    ASSERT_TRUE(secondParagraphBorders->idx_get(i)->get_IsVisible());
}

doc->Save(get_ArtifactsDir() + u"Border.SharedElements.docx");
```

## Siehe auch

* Class [Border](../../border/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
