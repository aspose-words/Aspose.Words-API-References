---
title: "Aspose::Words::BorderCollection::Equals метод"
linktitle: "Equals"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::BorderCollection::Equals метод. Сравнивает коллекции границ в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words/bordercollection/equals/
---
## BorderCollection::Equals method


Сравнивает коллекции границ.

```cpp
bool Aspose::Words::BorderCollection::Equals(const System::SharedPtr<Aspose::Words::BorderCollection> &brColl)
```


## Примеры



Показывает, как коллекции границ могут делить элементы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Paragraph 1.");
builder->Write(u"Paragraph 2.");

// Поскольку мы использовали одинаковую конфигурацию границы при создании
// этих абзацев, их коллекции границ делят одни и те же элементы.
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

// После изменения стиля линии границ только во втором абзаце,
// коллекции границ больше не делят одни и те же элементы.
for (int32_t i = 0; i < firstParagraphBorders->get_Count(); i++)
{
    ASSERT_FALSE(System::ObjectExt::Equals(firstParagraphBorders->idx_get(i), secondParagraphBorders->idx_get(i)));
    ASSERT_NE(System::ObjectExt::GetHashCode(firstParagraphBorders->idx_get(i)), System::ObjectExt::GetHashCode(secondParagraphBorders->idx_get(i)));

    // Изменение внешнего вида пустой границы делает её видимой.
    ASSERT_TRUE(secondParagraphBorders->idx_get(i)->get_IsVisible());
}

doc->Save(get_ArtifactsDir() + u"Border.SharedElements.docx");
```

## См. также

* Class [BorderCollection](../)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
