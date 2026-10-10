---
title: "Aspose::Words::BorderCollection::get_Count metodu"
linktitle: "get_Count"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::BorderCollection::get_Count metodu. C++'de koleksiyondaki kenarlık sayısını alır."
type: docs
weight: 6000
url: /tr/cpp/aspose.words/bordercollection/get_count/
---
## BorderCollection::get_Count method


Koleksiyondaki kenar sayısını alır.

```cpp
int32_t Aspose::Words::BorderCollection::get_Count()
```


## Örnekler



Kenarlık koleksiyonlarının öğeleri nasıl paylaşabileceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Paragraph 1.");
builder->Write(u"Paragraph 2.");

// Aynı kenarlık yapılandırmasını oluştururken kullandığımız için
// bu paragraflar, kenarlık koleksiyonları aynı öğeleri paylaşır.
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

// Sadece ikinci paragraftaki kenarlıkların çizgi stilini değiştirdikten sonra,
// kenarlık koleksiyonları artık aynı öğeleri paylaşmaz.
for (int32_t i = 0; i < firstParagraphBorders->get_Count(); i++)
{
    ASSERT_FALSE(System::ObjectExt::Equals(firstParagraphBorders->idx_get(i), secondParagraphBorders->idx_get(i)));
    ASSERT_NE(System::ObjectExt::GetHashCode(firstParagraphBorders->idx_get(i)), System::ObjectExt::GetHashCode(secondParagraphBorders->idx_get(i)));

    // Boş bir kenarlığın görünümünü değiştirmek onu görünür kılar.
    ASSERT_TRUE(secondParagraphBorders->idx_get(i)->get_IsVisible());
}

doc->Save(get_ArtifactsDir() + u"Border.SharedElements.docx");
```

## Ayrıca Bakınız

* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
