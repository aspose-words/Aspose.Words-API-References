---
title: "Aspose::Words::Style::get_Aliases method"
linktitle: "get_Aliases"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Style::get_Aliases method. Bu stilin tüm takma adlarını alır. Stilin takma adı yoksa C++'ta boş dizi (string) döndürülür."
type: docs
weight: 3000
url: /tr/cpp/aspose.words/style/get_aliases/
---
## Style::get_Aliases method


Bu stilin tüm takma adlarını alır. Stil takma ada sahip değilse boş bir dize dizisi döndürülür.

```cpp
System::ArrayPtr<System::String> Aspose::Words::Style::get_Aliases()
```


## Örnekler



Stil takma adlarının nasıl kullanılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Style with alias.docx");

// Bu belge "MyStyle,MyStyle Alias 1,MyStyle Alias 2" adlı bir stil içerir.
// Bir stilin adı virgüllerle ayrılmış birden fazla değere sahipse, her bölüm ayrı bir takma addır.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->idx_get(u"MyStyle");
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"MyStyle Alias 1", u"MyStyle Alias 2"}), style->get_Aliases());
ASSERT_EQ(u"Title", style->get_BaseStyleName());
ASSERT_EQ(u"MyStyle Char", style->get_LinkedStyleName());

// Bir stili hem takma adıyla hem de adıyla başvurabiliriz.
ASPOSE_ASSERT_EQ(doc->get_Styles()->idx_get(u"MyStyle Alias 1"), doc->get_Styles()->idx_get(u"MyStyle Alias 2"));

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle Alias 1"));
builder->Writeln(u"Hello world!");
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle Alias 2"));
builder->Write(u"Hello again!");

ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_Style(), doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_ParagraphFormat()->get_Style());
```

## Ayrıca Bakınız

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
