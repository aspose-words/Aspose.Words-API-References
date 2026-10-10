---
title: "Aspose::Words::RevisionCollection::AcceptAll metodo"
linktitle: "AcceptAll"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::RevisionCollection::AcceptAll metodo. Accetta tutte le revisioni in questa collezione in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words/revisioncollection/acceptall/
---
## RevisionCollection::AcceptAll method


Accetta tutte le revisioni in questa collezione.

```cpp
void Aspose::Words::RevisionCollection::AcceptAll()
```


## Esempi



Mostra come confrontare i documenti.
```cpp
auto docOriginal = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(docOriginal);
builder->Writeln(u"This is the original document.");

auto docEdited = System::MakeObject<Aspose::Words::Document>();
builder = System::MakeObject<Aspose::Words::DocumentBuilder>(docEdited);
builder->Writeln(u"This is the edited document.");

// Confrontare documenti con revisioni genererà un'eccezione.
if (docOriginal->get_Revisions()->get_Count() == 0 && docEdited->get_Revisions()->get_Count() == 0)
{
    docOriginal->Compare(docEdited, u"authorName", System::DateTime::get_Now());
}

// Dopo il confronto, il documento originale otterrà una nuova revisione
// per ogni elemento che è diverso nel documento modificato.
for (auto&& r : System::IterateOver(docOriginal->get_Revisions()))
{
    std::cout << System::String::Format(u"Revision type: {0}, on a node of type \"{1}\"", r->get_RevisionType(), r->get_ParentNode()->get_NodeType()) << std::endl;
    std::cout << System::String::Format(u"\tChanged text: \"{0}\"", r->get_ParentNode()->GetText()) << std::endl;
}

// Accettare queste revisioni trasformerà il documento originale nel documento modificato.
docOriginal->get_Revisions()->AcceptAll();

ASSERT_EQ(docOriginal->GetText(), docEdited->GetText());
```

## Vedi anche

* Class [RevisionCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
