---
title: "Aspose::Words::Style::get_Aliases metod"
linktitle: "get_Aliases"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Style::get_Aliases metod. Hämtar alla alias för denna stil. Om stilen inte har några alias returneras en tom strängarray i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words/style/get_aliases/
---
## Style::get_Aliases method


Hämtar alla alias för denna stil. Om stilen inte har några alias returneras en tom strängarray.

```cpp
System::ArrayPtr<System::String> Aspose::Words::Style::get_Aliases()
```


## Exempel



Visar hur man använder stilalias.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Style with alias.docx");

// Detta dokument innehåller en stil med namnet "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
// Om en stils namn har flera värden separerade med kommatecken, är varje del ett separat alias.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->idx_get(u"MyStyle");
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"MyStyle Alias 1", u"MyStyle Alias 2"}), style->get_Aliases());
ASSERT_EQ(u"Title", style->get_BaseStyleName());
ASSERT_EQ(u"MyStyle Char", style->get_LinkedStyleName());

// Vi kan referera till en stil med dess alias, såväl som dess namn.
ASPOSE_ASSERT_EQ(doc->get_Styles()->idx_get(u"MyStyle Alias 1"), doc->get_Styles()->idx_get(u"MyStyle Alias 2"));

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle Alias 1"));
builder->Writeln(u"Hello world!");
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle Alias 2"));
builder->Write(u"Hello again!");

ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_Style(), doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_ParagraphFormat()->get_Style());
```

## Se även

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
