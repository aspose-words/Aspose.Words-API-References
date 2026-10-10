---
title: "Aspose::Words::Style::get_AutomaticallyUpdate metod"
linktitle: "get_AutomaticallyUpdate"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Style::get_AutomaticallyUpdate metod. Anger om den här stilen automatiskt omdefinieras baserat på det lämpliga värdet i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words/style/get_automaticallyupdate/
---
## Style::get_AutomaticallyUpdate method


Anger om denna stil automatiskt omdefinieras baserat på det lämpliga värdet.

```cpp
bool Aspose::Words::Style::get_AutomaticallyUpdate() const
```

## Anmärkningar


Om egenskapsvärdet är satt till true, omdefinierar MS Word automatiskt den aktuella stilen när den lämpliga styckeformateringen har ändrats.

AutomaticallyUpdate‑egenskapen gäller endast för styckestilar.

Standardvärdet är **false**.

## Exempel



Visar hur man skapar och tillämpar en anpassad stil.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle");
style->get_Font()->set_Name(u"Times New Roman");
style->get_Font()->set_Size(16);
style->get_Font()->set_Color(System::Drawing::Color::get_Navy());
// Omdefiniera stil automatiskt.
style->set_AutomaticallyUpdate(true);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Tillämpa en av dokumentets stilar på stycket som dokumentbyggaren skapar.
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle"));
builder->Writeln(u"Hello world!");

System::SharedPtr<Aspose::Words::Style> firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

ASPOSE_ASSERT_EQ(style, firstParagraphStyle);

// Ta bort vår anpassade stil från dokumentets stilkollektion.
doc->get_Styles()->idx_get(u"MyStyle")->Remove();

firstParagraphStyle = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Style();

// All text som använde en borttagen stil återgår till standardformateringen.
ASSERT_FALSE(doc->get_Styles()->LINQ_Any(static_cast<System::Func<System::SharedPtr<Aspose::Words::Style>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Style> s)>>([](System::SharedPtr<Aspose::Words::Style> s) -> bool
{
    return s->get_Name() == u"MyStyle";
}))));
ASSERT_EQ(u"Times New Roman", firstParagraphStyle->get_Font()->get_Name());
ASPOSE_ASSERT_EQ(12.0, firstParagraphStyle->get_Font()->get_Size());
ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), firstParagraphStyle->get_Font()->get_Color().ToArgb());
```

## Se även

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
