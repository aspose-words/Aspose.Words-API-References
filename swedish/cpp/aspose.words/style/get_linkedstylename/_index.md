---
title: "Aspose::Words::Style::get_LinkedStyleName-metod"
linktitle: "get_LinkedStyleName"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Style::get_LinkedStyleName-metod. Hämtar/sätter namnet på den Style som är länkad till den här. Returnerar en tom sträng om inga stilar är länkade i C++."
type: docs
weight: 11000
url: /sv/cpp/aspose.words/style/get_linkedstylename/
---
## Style::get_LinkedStyleName method


Hämtar/sätter namnet på den [Style](../) som är länkad till den här. Returnerar en tom sträng om inga stilar är länkade.

```cpp
System::String Aspose::Words::Style::get_LinkedStyleName()
```

## Anmärkningar


Det är endast tillåtet att länka stycke-stilen till tecken-stilen och vice versa.

Att sätta LinkedStyleName för den aktuella stilen leder automatiskt till att sätta LinkedStyleName för den länkade stilen.

Att tilldela en tom sträng är ekvivalent med att avlänka den tidigare länkade stilen.

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


Visar hur man länkar stilar med varandra.
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

## Se även

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
