---
title: Aspose::Words::BorderCollection::ClearFormatting method
linktitle: ClearFormatting
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::BorderCollection::ClearFormatting method. Removes all borders of an object in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words/bordercollection/clearformatting/
---
## BorderCollection::ClearFormatting method


Removes all borders of an object.

```cpp
void Aspose::Words::BorderCollection::ClearFormatting()
```


## Examples



Shows how to remove all borders from all paragraphs in a document. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Borders.docx");

// The first paragraph of this document has visible borders with these settings.
SharedPtr<BorderCollection> firstParagraphBorders = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Borders();

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), firstParagraphBorders->get_Color().ToArgb());
ASSERT_EQ(LineStyle::Single, firstParagraphBorders->get_LineStyle());
ASPOSE_ASSERT_EQ(3.0, firstParagraphBorders->get_LineWidth());

// Use the "ClearFormatting" method on each paragraph to remove all borders.
for (const auto& paragraph : System::IterateOver<Paragraph>(doc->get_FirstSection()->get_Body()->get_Paragraphs()))
{
    paragraph->get_ParagraphFormat()->get_Borders()->ClearFormatting();

    for (const auto& border : System::IterateOver(paragraph->get_ParagraphFormat()->get_Borders()))
    {
        ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), border->get_Color().ToArgb());
        ASSERT_EQ(LineStyle::None, border->get_LineStyle());
        ASPOSE_ASSERT_EQ(0.0, border->get_LineWidth());
    }
}

doc->Save(ArtifactsDir + u"BorderCollection.RemoveAllBorders.docx");
```

## See Also

* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
