---
title: "Aspose::Words::Border::get_IsVisible metodu"
linktitle: "get_IsVisible"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Border::get_IsVisible metodu. C++'ta LineStyle None değilse true döndürür."
type: docs
weight: 6000
url: /tr/cpp/aspose.words/border/get_isvisible/
---
## Border::get_IsVisible method


LineStyle [LineStyle](../get_linestyle/) None [None](../../linestyle/) değilse **true** döndürür.

```cpp
bool Aspose::Words::Border::get_IsVisible()
```


## Örnekler



Bir paragraftan kenarların nasıl kaldırılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Borders.docx");

// Her paragrafın ayrı bir kenar seti vardır.
// Bu kenarların görünüm ayarlarına paragraf biçim nesnesi aracılığıyla erişebiliriz.
System::SharedPtr<Aspose::Words::BorderCollection> borders = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Borders();

ASSERT_EQ(System::Drawing::Color::get_Red().ToArgb(), borders->idx_get(0)->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(3.0, borders->idx_get(0)->get_LineWidth());
ASSERT_EQ(Aspose::Words::LineStyle::Single, borders->idx_get(0)->get_LineStyle());
ASSERT_TRUE(borders->idx_get(0)->get_IsVisible());

// ClearFormatting metodunu çalıştırarak bir kenarı bir anda kaldırabiliriz.
// Bu yöntemi bir paragraftaki her kenara uygulamak, tüm kenarlarını kaldıracaktır.
for (auto&& border : System::IterateOver(borders))
{
    border->ClearFormatting();
}

ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), borders->idx_get(0)->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(0.0, borders->idx_get(0)->get_LineWidth());
ASSERT_EQ(Aspose::Words::LineStyle::None, borders->idx_get(0)->get_LineStyle());
ASSERT_FALSE(borders->idx_get(0)->get_IsVisible());

doc->Save(get_ArtifactsDir() + u"Border.ClearFormatting.docx");
```

## Ayrıca Bakınız

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
