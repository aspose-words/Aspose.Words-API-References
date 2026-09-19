---
title: "Metodo Aspose::Words::Style::Equals"
linktitle: "Equals"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Style::Equals. Confronta con lo stile specificato. Gli Istd degli stili sono confrontati solo per gli stili incorporati. I valori predefiniti degli stili non sono inclusi nel confronto. Lo stile base, lo stile collegato e lo stile del paragrafo successivo sono confrontati ricorsivamente in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words/style/equals/
---
## Style::Equals method


Confronta con lo stile specificato. Gli Istd degli stili sono confrontati solo per gli stili integrati. I valori predefiniti degli stili non sono inclusi nel confronto. Lo stile base, lo stile collegato e lo stile del paragrafo successivo sono confrontati ricorsivamente.

```cpp
bool Aspose::Words::Style::Equals(const System::SharedPtr<Aspose::Words::Style> &style)
```


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

## Vedi anche

* Class [Style](../)
* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
