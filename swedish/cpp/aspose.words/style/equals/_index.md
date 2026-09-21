---
title: "Aspose::Words::Style::Equals metod"
linktitle: "Equals"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Style::Equals metod. Jämför med den angivna stilen. Stilar Istds jämförs endast för inbyggda stilar. Stilstandardvärden inkluderas inte i jämförelsen. Grundstil, länkad stil och nästa stycke‑stil jämförs rekursivt i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words/style/equals/
---
## Style::Equals method


Jämför med den angivna stilen. Stil-ID:n jämförs endast för inbyggda stilar. Standardvärden för stilar inkluderas inte i jämförelsen. Grundstil, länkad stil och nästa styckestil jämförs rekursivt.

```cpp
bool Aspose::Words::Style::Equals(const System::SharedPtr<Aspose::Words::Style> &style)
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
* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
