---
title: "Aspose::Words::Style::get_Aliases Methode"
linktitle: "get_Aliases"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Style::get_Aliases Methode. Gibt alle Aliasse dieses Stils zurück. Wenn der Stil keine Aliasse hat, wird ein leeres String-Array in C++ zurückgegeben."
type: docs
weight: 3000
url: /de/cpp/aspose.words/style/get_aliases/
---
## Style::get_Aliases method


Ruft alle Aliase dieses Stils ab. Wenn der Stil keine Aliase hat, wird ein leeres String‑Array zurückgegeben.

```cpp
System::ArrayPtr<System::String> Aspose::Words::Style::get_Aliases()
```


## Beispiele



Zeigt, wie man Stil-Aliasse verwendet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Style with alias.docx");

// Dieses Dokument enthält einen Stil mit dem Namen "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
// Wenn der Name eines Stils mehrere durch Kommas getrennte Werte enthält, ist jede Angabe ein separater Alias.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->idx_get(u"MyStyle");
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"MyStyle Alias 1", u"MyStyle Alias 2"}), style->get_Aliases());
ASSERT_EQ(u"Title", style->get_BaseStyleName());
ASSERT_EQ(u"MyStyle Char", style->get_LinkedStyleName());

// Wir können einen Stil sowohl über seinen Alias als auch über seinen Namen referenzieren.
ASPOSE_ASSERT_EQ(doc->get_Styles()->idx_get(u"MyStyle Alias 1"), doc->get_Styles()->idx_get(u"MyStyle Alias 2"));

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->MoveToDocumentEnd();
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle Alias 1"));
builder->Writeln(u"Hello world!");
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"MyStyle Alias 2"));
builder->Write(u"Hello again!");

ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat()->get_Style(), doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_ParagraphFormat()->get_Style());
```

## Siehe auch

* Class [Style](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
