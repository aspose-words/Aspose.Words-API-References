---
title: "Aspose::Words::Style::get_LinkedStyleName metodo"
linktitle: "get_LinkedStyleName"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Style::get_LinkedStyleName. Ottiene/imposta il nome dello Style collegato a questo. Restituisce una stringa vuota se non ci sono stili collegati in C++."
type: docs
weight: 11000
url: /it/cpp/aspose.words/style/get_linkedstylename/
---
## Style::get_LinkedStyleName method


Ottiene/imposta il nome del [Style](../) collegato a questo. Restituisce una stringa vuota se non ci sono stili collegati.

```cpp
System::String Aspose::Words::Style::get_LinkedStyleName()
```

## Note


È consentito collegare lo stile di paragrafo solo allo stile di carattere e viceversa.

Impostare LinkedStyleName per lo stile corrente porta automaticamente a impostare LinkedStyleName per lo stile collegato.

Assegnare una stringa vuota equivale a scollegare lo stile precedentemente collegato.

## Esempi



Mostra come utilizzare gli alias di stile.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Style with alias.docx");

// Questo documento contiene uno stile denominato "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
// Se il nome di uno stile ha più valori separati da virgole, ogni clausola è un alias separato.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->idx_get(u"MyStyle");
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"MyStyle Alias 1", u"MyStyle Alias 2"}), style->get_Aliases());
ASSERT_EQ(u"Title", style->get_BaseStyleName());
ASSERT_EQ(u"MyStyle Char", style->get_LinkedStyleName());

// Possiamo fare riferimento a uno stile usando il suo alias, così come il suo nome.
ASPOSE_ASSERT_EQ(doc->get_Styles()->idx_get(u"MyStyle Alias 1"), doc->get_Styles()->idx_get(u"MyStyle Alias 2"));

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle Alias 1"));
builder->Writeln(u"Hello world!");
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle Alias 2"));
builder->Write(u"Hello again!");

ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_Style(), doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_ParagraphFormat()->get_Style());
```


Mostra come collegare gli stili tra loro.
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

## Vedi anche

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
