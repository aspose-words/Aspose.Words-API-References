---
title: "Aspose::Words::RevisionCollection::AcceptAll metod"
linktitle: "AcceptAll"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::RevisionCollection::AcceptAll metod. Accepterar alla revisioner i denna samling i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words/revisioncollection/acceptall/
---
## RevisionCollection::AcceptAll method


Accepterar alla revisioner i den här samlingen.

```cpp
void Aspose::Words::RevisionCollection::AcceptAll()
```


## Exempel



Visar hur man jämför dokument.
```cpp
auto docOriginal = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(docOriginal);
builder->Writeln(u"This is the original document.");

auto docEdited = System::MakeObject<Aspose::Words::Document>();
builder = System::MakeObject<Aspose::Words::DocumentBuilder>(docEdited);
builder->Writeln(u"This is the edited document.");

// Att jämföra dokument med revisioner kommer att kasta ett undantag.
if (docOriginal->get_Revisions()->get_Count() == 0 && docEdited->get_Revisions()->get_Count() == 0)
{
    docOriginal->Compare(docEdited, u"authorName", System::DateTime::get_Now());
}

// Efter jämförelsen kommer det ursprungliga dokumentet att få en ny revision
// för varje element som är annorlunda i det redigerade dokumentet.
for (auto&& r : System::IterateOver(docOriginal->get_Revisions()))
{
    std::cout << System::String::Format(u"Revision type: {0}, on a node of type \"{1}\"", r->get_RevisionType(), r->get_ParentNode()->get_NodeType()) << std::endl;
    std::cout << System::String::Format(u"\tChanged text: \"{0}\"", r->get_ParentNode()->GetText()) << std::endl;
}

// Att acceptera dessa revisioner kommer att omvandla det ursprungliga dokumentet till det redigerade dokumentet.
docOriginal->get_Revisions()->AcceptAll();

ASSERT_EQ(docOriginal->GetText(), docEdited->GetText());
```

## Se även

* Class [RevisionCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
