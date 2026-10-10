---
title: "Aspose::Words::Style::get_AutomaticallyUpdate yöntemi"
linktitle: "get_AutomaticallyUpdate"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Style::get_AutomaticallyUpdate yöntemi. Bu stilin C++'ta uygun değere göre otomatik olarak yeniden tanımlanıp tanımlanmayacağını belirtir."
type: docs
weight: 4000
url: /tr/cpp/aspose.words/style/get_automaticallyupdate/
---
## Style::get_AutomaticallyUpdate method


Bu stilin uygun değere göre otomatik olarak yeniden tanımlanıp tanımlanmayacağını belirtir.

```cpp
bool Aspose::Words::Style::get_AutomaticallyUpdate() const
```

## Açıklamalar


Özellik değeri true olarak ayarlanırsa, MS Word uygun paragraf biçimlendirmesi değiştiğinde mevcut stili otomatik olarak yeniden tanımlar.

AutomaticallyUpdate özelliği yalnızca paragraf stillerine uygulanabilir.

Varsayılan değer **false**'tur.

## Örnekler



Özel bir stilin nasıl oluşturulup uygulanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
style->get_Font()->set_Name(u"Times New Roman");
style->get_Font()->set_Size(16);
style->get_Font()->set_Color(System::Drawing::Color::get_Navy());
// Stili otomatik olarak yeniden tanımlar.
style->set_AutomaticallyUpdate(true);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Belgeden bir stili, belge oluşturucunun oluşturduğu paragrafa uygular.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle"));
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Style> firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

ASPOSE_ASSERT_EQ(style, firstParagraphStyle);

// Özel stilimizi belgenin stil koleksiyonundan kaldırın.
doc->get_Styles()->idx_get(u"MyStyle")->Remove();

firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

// Kaldırılan bir stil kullanan tüm metinler varsayılan biçimlendirmeye geri döner.
ASSERT_FALSE(doc->get_Styles()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Style>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Style> s)>>([](System::SharedPtr<Aspose::Words::Style> s) -> bool
{
    return s->get_Name() == u"MyStyle";
}))));
ASSERT_EQ(u"Times New Roman", firstParagraphStyle->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(12.0, firstParagraphStyle->get_Font()->get_Size());
ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), firstParagraphStyle->get_Font()->get_Color().ToArgb());
```

## Ayrıca Bakınız

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
