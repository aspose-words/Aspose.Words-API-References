---
title: "Metodo Aspose::Words::BorderCollection::ClearFormatting"
linktitle: "ClearFormatting"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::BorderCollection::ClearFormatting. Rimuove tutti i bordi di un oggetto in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words/bordercollection/clearformatting/
---
## BorderCollection::ClearFormatting method


Rimuove tutti i bordi di un oggetto.

```cpp
void Aspose::Words::BorderCollection::ClearFormatting()
```


## Esempi



Mostra come rimuovere tutti i bordi da tutti i paragrafi in un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Borders.docx");

// Il primo paragrafo di questo documento ha bordi visibili con queste impostazioni.
System::SharedPtr<Aspose::Words::BorderCollection> firstParagraphBorders = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Borders();

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), firstParagraphBorders->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::LineStyle::Single, firstParagraphBorders->get_LineStyle());
ASPOSE_ASSERT_EQ(3.0, firstParagraphBorders->get_LineWidth());

// Usa il metodo "ClearFormatting" su ogni paragrafo per rimuovere tutti i bordi.
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

## Vedi anche

* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
