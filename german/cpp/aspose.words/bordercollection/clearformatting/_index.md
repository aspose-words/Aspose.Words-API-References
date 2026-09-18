---
title: "Aspose::Words::BorderCollection::ClearFormatting Methode"
linktitle: "ClearFormatting"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::BorderCollection::ClearFormatting Methode. Entfernt alle Ränder eines Objekts in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words/bordercollection/clearformatting/
---
## BorderCollection::ClearFormatting method


Entfernt alle Rahmen eines Objekts.

```cpp
void Aspose::Words::BorderCollection::ClearFormatting()
```


## Beispiele



Zeigt, wie man alle Ränder aus allen Absätzen in einem Dokument entfernt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Borders.docx");

// Der erste Absatz dieses Dokuments hat sichtbare Ränder mit diesen Einstellungen.
System::SharedPtr<Aspose::Words::BorderCollection> firstParagraphBorders = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Borders();

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), firstParagraphBorders->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::LineStyle::Single, firstParagraphBorders->get_LineStyle());
ASPOSE_ASSERT_EQ(3.0, firstParagraphBorders->get_LineWidth());

// Verwenden Sie die Methode "ClearFormatting" für jeden Absatz, um alle Ränder zu entfernen.
for (auto&& paragraph : System::IterateOver<Aspose::Words::Paragraph>(doc->get_FirstSection()->get_Body()->get_Paragraphs()))
{
    paragraph->get_ParagraphFormat()->get_Borders()->ClearFormatting();

    for (auto&& border : System::IterateOver(paragraph->get_ParagraphFormat()->get_Borders()))
    {
        ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), border->get_Color().ToArgb());
        ASSERT_EQ(Aspose::Words::LineStyle::None, border->get_LineStyle());
        ASPOSE_ASSERT_EQ(0.0, border->get_LineWidth());
    }
}

doc->Save(get_ArtifactsDir() + u"BorderCollection.RemoveAllBorders.docx");
```

## Siehe auch

* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
