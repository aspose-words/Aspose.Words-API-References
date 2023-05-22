---
title: Aspose::Words::Border::Equals method
linktitle: Equals
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Border::Equals method. Determines whether the specified border is equal in value to the current border in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words/border/equals/
---
## Border::Equals(const System::SharedPtr\<Aspose::Words::Border\>\&) method


Determines whether the specified border is equal in value to the current border.

```cpp
bool Aspose::Words::Border::Equals(const System::SharedPtr<Aspose::Words::Border> &rhs)
```


## Examples



Shows how border collections can share elements. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"Paragraph 1.");
builder->Write(u"Paragraph 2.");

// Since we used the same border configuration while creating
// these paragraphs, their border collections share the same elements.
SharedPtr<BorderCollection> firstParagraphBorders = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Borders();
SharedPtr<BorderCollection> secondParagraphBorders = builder->get_CurrentParagraph()->get_ParagraphFormat()->get_Borders();

for (int i = 0; i < firstParagraphBorders->get_Count(); i++)
{
    ASSERT_TRUE(System::ObjectExt::Equals(firstParagraphBorders->idx_get(i), secondParagraphBorders->idx_get(i)));
    ASSERT_EQ(System::ObjectExt::GetHashCode(firstParagraphBorders->idx_get(i)), System::ObjectExt::GetHashCode(secondParagraphBorders->idx_get(i)));
    ASSERT_FALSE(firstParagraphBorders->idx_get(i)->get_IsVisible());
}

for (const auto& border : System::IterateOver(secondParagraphBorders))
{
    border->set_LineStyle(LineStyle::DotDash);
}

// After changing the line style of the borders in just the second paragraph,
// the border collections no longer share the same elements.
for (int i = 0; i < firstParagraphBorders->get_Count(); i++)
{
    ASSERT_FALSE(System::ObjectExt::Equals(firstParagraphBorders->idx_get(i), secondParagraphBorders->idx_get(i)));
    ASSERT_NE(System::ObjectExt::GetHashCode(firstParagraphBorders->idx_get(i)), System::ObjectExt::GetHashCode(secondParagraphBorders->idx_get(i)));

    // Changing the appearance of an empty border makes it visible.
    ASSERT_TRUE(secondParagraphBorders->idx_get(i)->get_IsVisible());
}

doc->Save(ArtifactsDir + u"Border.SharedElements.docx");
```

## See Also

* Class [Border](../)
* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Border::Equals(System::SharedPtr\<System::Object\>) method


Determines whether the specified object is equal in value to the current object.

```cpp
bool Aspose::Words::Border::Equals(System::SharedPtr<System::Object> obj) override
```


## Examples



Shows how border collections can share elements. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"Paragraph 1.");
builder->Write(u"Paragraph 2.");

// Since we used the same border configuration while creating
// these paragraphs, their border collections share the same elements.
SharedPtr<BorderCollection> firstParagraphBorders = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Borders();
SharedPtr<BorderCollection> secondParagraphBorders = builder->get_CurrentParagraph()->get_ParagraphFormat()->get_Borders();

for (int i = 0; i < firstParagraphBorders->get_Count(); i++)
{
    ASSERT_TRUE(System::ObjectExt::Equals(firstParagraphBorders->idx_get(i), secondParagraphBorders->idx_get(i)));
    ASSERT_EQ(System::ObjectExt::GetHashCode(firstParagraphBorders->idx_get(i)), System::ObjectExt::GetHashCode(secondParagraphBorders->idx_get(i)));
    ASSERT_FALSE(firstParagraphBorders->idx_get(i)->get_IsVisible());
}

for (const auto& border : System::IterateOver(secondParagraphBorders))
{
    border->set_LineStyle(LineStyle::DotDash);
}

// After changing the line style of the borders in just the second paragraph,
// the border collections no longer share the same elements.
for (int i = 0; i < firstParagraphBorders->get_Count(); i++)
{
    ASSERT_FALSE(System::ObjectExt::Equals(firstParagraphBorders->idx_get(i), secondParagraphBorders->idx_get(i)));
    ASSERT_NE(System::ObjectExt::GetHashCode(firstParagraphBorders->idx_get(i)), System::ObjectExt::GetHashCode(secondParagraphBorders->idx_get(i)));

    // Changing the appearance of an empty border makes it visible.
    ASSERT_TRUE(secondParagraphBorders->idx_get(i)->get_IsVisible());
}

doc->Save(ArtifactsDir + u"Border.SharedElements.docx");
```

## See Also

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
