---
title: "Aspose::Words::Style::Equals yöntemi"
linktitle: "Equals"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Style::Equals yöntemi. Belirtilen stil ile karşılaştırır. Stil Istds yalnızca yerleşik stiller için karşılaştırılır. Stil varsayılanları karşılaştırmaya dahil edilmez. Temel stil, bağlantılı stil ve sonraki paragraf stili C++'ta özyinelemeli olarak karşılaştırılır."
type: docs
weight: 2000
url: /tr/cpp/aspose.words/style/equals/
---
## Style::Equals method


Belirtilen stil ile karşılaştırır. Styles Istds yalnızca yerleşik stiller için karşılaştırılır. Stil varsayılanları karşılaştırmaya dahil edilmez. Temel stil, bağlı stil ve sonraki paragraf stili özyinelemeli olarak karşılaştırılır.

```cpp
bool Aspose::Words::Style::Equals(const System::SharedPtr<Aspose::Words::Style> &style)
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
* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
