---
title: "Aspose::Words::Style::get_LinkedStyleName method"
linktitle: "get_LinkedStyleName"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Style::get_LinkedStyleName metodu. Bu stile bağlı Stil'in adını alır/ayar. Stil bağlı değilse C++'ta boş dize döndürür."
type: docs
weight: 11000
url: /tr/cpp/aspose.words/style/get_linkedstylename/
---
## Style::get_LinkedStyleName method


Bu stile bağlı [Style](../) adını alır/ayar. Stil bağlı değilse boş dize döndürür.

```cpp
System::String Aspose::Words::Style::get_LinkedStyleName()
```

## Açıklamalar


Paragraf stilini karakter stiline ve tersine bağlamak yalnızca izin verilir.

Mevcut stil için LinkedStyleName ayarlandığında, bağlı stil için LinkedStyleName otomatik olarak ayarlanır.

Boş dize atamak, daha önce bağlı olan stilin bağlantısını kaldırmaya eşdeğerdir.

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


Stillerin birbirleriyle nasıl bağlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::Style> styleHeading1 = doc->get_Styles()->idx_get(Aspose::Words::StyleIdentifier::Heading1);

System::SharedPtr<Aspose::Words::Style> styleHeading1Char = doc->get_Styles()->Add(Aspose::Words::StyleType::Character, u"Heading 1 Char");
styleHeading1Char->get_Font()->set_Name(u"Verdana");
styleHeading1Char->get_Font()->set_Bold(true);
styleHeading1Char->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::Dot);
styleHeading1Char->get_Font()->get_Border()->set_LineWidth(15);

styleHeading1->set_LinkedStyleName(u"Heading 1 Char");

ASSERT_EQ(u"Heading 1 Char", styleHeading1->get_LinkedStyleName());
ASSERT_EQ(u"Heading 1", styleHeading1Char->get_LinkedStyleName());
```

## Ayrıca Bakınız

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
