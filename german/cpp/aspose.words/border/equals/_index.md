---
title: "Aspose::Words::Border::Equals Methode"
linktitle: "Equals"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Border::Equals Methode. Bestimmt, ob der angegebene Rand im Wert dem aktuellen Rand in C++ entspricht."
type: docs
weight: 3000
url: /de/cpp/aspose.words/border/equals/
---
## Border::Equals(const System::SharedPtr\<Aspose::Words::Border\>\&) method


Bestimmt, ob der angegebene Rahmen im Wert dem aktuellen Rahmen entspricht.

```cpp
bool Aspose::Words::Border::Equals(const System::SharedPtr<Aspose::Words::Border> &rhs)
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
* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Border::Equals(System::SharedPtr\<System::Object\>) method


Bestimmt, ob das angegebene Objekt im Wert dem aktuellen Objekt entspricht.

```cpp
bool Aspose::Words::Border::Equals(System::SharedPtr<System::Object> obj) override
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
