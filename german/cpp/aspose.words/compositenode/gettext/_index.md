---
title: "Aspose::Words::CompositeNode::GetText-Methode"
linktitle: "GetText"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::CompositeNode::GetText-Methode. Gibt den Text dieses Knotens und aller seiner Kinder in C++ zurück."
type: docs
weight: 12000
url: /de/cpp/aspose.words/compositenode/gettext/
---
## CompositeNode::GetText method


Ermittelt den Text dieses Knotens und aller seiner Kindknoten.

```cpp
System::String Aspose::Words::CompositeNode::GetText() override
```

## Hinweise


Der zurückgegebene String enthält alle Steuer- und Sonderzeichen wie in [ControlChar](../../controlchar/) beschrieben.

## Beispiele



Zeigt den Unterschied zwischen dem Aufruf der GetText- und ToString-Methoden an einem Knoten.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->InsertField(u"MERGEFIELD Field");

// GetText ruft den sichtbaren Text sowie Feldcodes und Sonderzeichen ab.
ASSERT_EQ(u"\u0013MERGEFIELD Field\u0014«Field»\u0015", doc->GetText().Trim());

// ToString liefert das Aussehen des Dokuments, wenn es in ein übergebenes Speicherformat gespeichert wird.
ASSERT_EQ(u"«Field»", doc->ToString(Aspose::Words::SaveFormat::Text).Trim());
```


Zeigt, wie man alle Absätze in einem Dokument ausgibt, die Listenelemente sind.
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

## Siehe auch

* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
