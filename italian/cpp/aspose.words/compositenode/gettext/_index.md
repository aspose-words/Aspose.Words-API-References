---
title: "Metodo Aspose::Words::CompositeNode::GetText"
linktitle: "GetText"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::CompositeNode::GetText. Ottiene il testo di questo nodo e di tutti i suoi figli in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words/compositenode/gettext/
---
## CompositeNode::GetText method


Ottiene il testo di questo nodo e di tutti i suoi figli.

```cpp
System::String Aspose::Words::CompositeNode::GetText() override
```

## Note


La stringa restituita include tutti i caratteri di controllo e speciali come descritti in [ControlChar](../../controlchar/).

## Esempi



Mostra la differenza tra la chiamata dei metodi GetText e ToString su un nodo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertField(u"MERGEFIELD Field");

// GetText recupererà il testo visibile così come i codici di campo e i caratteri speciali.
ASSERT_EQ(u"\u0013MERGEFIELD Field\u0014«Field»\u0015", doc->GetText().Trim());

// ToString ci fornirà l'aspetto del documento se salvato nel formato di salvataggio specificato.
ASSERT_EQ(u"«Field»", doc->ToString(Aspose::Words::SaveFormat::Text).Trim());
```


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

* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
