---
title: "Aspose::Words::Paragraph::get_ListFormat metodo"
linktitle: "get_ListFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Paragraph::get_ListFormat metodo. Fornisce l'accesso alle proprietà di formattazione dell'elenco del paragrafo in C++."
type: docs
weight: 18000
url: /it/cpp/aspose.words/paragraph/get_listformat/
---
## Paragraph::get_ListFormat method


Fornisce l'accesso alle proprietà di formattazione dell'elenco del paragrafo.

```cpp
System::SharedPtr<Aspose::Words::Lists::ListFormat> Aspose::Words::Paragraph::get_ListFormat()
```


## Esempi



Mostra come esportare tutti i paragrafi in un documento che sono elementi di elenco.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ListFormat()->ApplyNumberDefault();
builder->Writeln(u"Numbered list item 1");
builder->Writeln(u"Numbered list item 2");
builder->Writeln(u"Numbered list item 3");
builder->get_ListFormat()->RemoveNumbers();

builder->get_ListFormat()->ApplyBulletDefault();
builder->Writeln(u"Bulleted list item 1");
builder->Writeln(u"Bulleted list item 2");
builder->Writeln(u"Bulleted list item 3");
builder->get_ListFormat()->RemoveNumbers();

System::SharedPtr<Aspose::Words::NodeCollection> paras = doc->GetChildNodes(Aspose::Words::NodeType::Paragraph, true);

for (auto&& para : paras->LINQ_OfType<System::SharedPtr<Aspose::Words::Paragraph> >()->LINQ_Where(static_cast<System::Func<System::SharedPtr<Aspose::Words::Paragraph>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Paragraph> p)>>([](System::SharedPtr<Aspose::Words::Paragraph> p) -> bool
{
    return p->get_ListFormat()->get_IsListItem();
})))->LINQ_ToList())
{
    std::cout << System::String::Format(u"This paragraph belongs to list ID# {0}, number style \"{1}\"", para->get_ListFormat()->get_List()->get_ListId(), para->get_ListFormat()->get_ListLevel()->get_NumberStyle()) << std::endl;
    std::cout << System::String::Format(u"\t\"{0}\"", para->GetText().Trim()) << std::endl;
}
```

## Vedi anche

* Class [ListFormat](../../../aspose.words.lists/listformat/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
