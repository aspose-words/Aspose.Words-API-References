---
title: "Método Aspose::Words::BorderCollection::ClearFormatting"
linktitle: "ClearFormatting"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::BorderCollection::ClearFormatting. Elimina todos los bordes de un objeto en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words/bordercollection/clearformatting/
---
## BorderCollection::ClearFormatting method


Elimina todos los bordes de un objeto.

```cpp
void Aspose::Words::BorderCollection::ClearFormatting()
```


## Ejemplos



Muestra cómo eliminar todos los bordes de todos los párrafos en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Borders.docx");

// El primer párrafo de este documento tiene bordes visibles con esta configuración.
System::SharedPtr<Aspose::Words::BorderCollection> firstParagraphBorders = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Borders();

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), firstParagraphBorders->get_Color().ToArgb());
ASSERT_EQ(Aspose::Words::LineStyle::Single, firstParagraphBorders->get_LineStyle());
ASPOSE_ASSERT_EQ(3.0, firstParagraphBorders->get_LineWidth());

// Utilice el método "ClearFormatting" en cada párrafo para eliminar todos los bordes.
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

## Ver también

* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
