---
title: "Aspose::Words::BorderCollection::idx_get metodu"
linktitle: "idx_get"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::BorderCollection::idx_get metodu. C++'de kenarlık tipine göre bir Border nesnesi alır."
type: docs
weight: 18000
url: /tr/cpp/aspose.words/bordercollection/idx_get/
---
## BorderCollection::idx_get(Aspose::Words::BorderType) method


Kenarlık tipine göre bir [Border](../../border/) nesnesi alır.

```cpp
System::SharedPtr<Aspose::Words::Border> Aspose::Words::BorderCollection::idx_get(Aspose::Words::BorderType borderType)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| borderType | Aspose::Words::BorderType | Alınacak kenarlığın tipini belirten bir [BorderType](../../bordertype/) değeri. |
## Açıklamalar


Farklı belge öğeleri için tüm kenarlıkların mevcut olmadığını unutmayın. Bu metod, mevcut nesneye uygulanamayan bir kenarlık talep ederseniz bir istisna fırlatır.

## Örnekler



Metni kenarlıklar ve gölgelendirme ile nasıl süsleneceğini gösterir.
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

## Ayrıca Bakınız

* Class [Border](../../border/)
* Enum [BorderType](../../bordertype/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## BorderCollection::idx_get(int32_t) method


İndexe göre bir [Border](../../border/) nesnesi alır.

```cpp
System::SharedPtr<Aspose::Words::Border> Aspose::Words::BorderCollection::idx_get(int32_t index)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| index | int32_t | Alınacak kenarlığın sıfır tabanlı indeksi. |

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

* Class [Border](../../border/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
