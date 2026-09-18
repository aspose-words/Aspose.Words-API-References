---
title: "Aspose::Words::Border::GetHashCode Methode"
linktitle: "GetHashCode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Border::GetHashCode Methode. Dient als Hash‑Funktion für diesen Typ in C++."
type: docs
weight: 12000
url: /de/cpp/aspose.words/border/gethashcode/
---
## Border::GetHashCode method


Dient als Hash-Funktion für diesen Typ.

```cpp
int32_t Aspose::Words::Border::GetHashCode() const override
```


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

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
