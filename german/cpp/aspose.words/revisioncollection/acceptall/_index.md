---
title: "Aspose::Words::RevisionCollection::AcceptAll Methode"
linktitle: "AcceptAll"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::RevisionCollection::AcceptAll Methode. Akzeptiert alle Revisionen in dieser Sammlung in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words/revisioncollection/acceptall/
---
## RevisionCollection::AcceptAll method


Akzeptiert alle Revisionen in dieser Sammlung.

```cpp
void Aspose::Words::RevisionCollection::AcceptAll()
```


## Beispiele



Zeigt, wie Dokumente verglichen werden.
```cpp
auto docOriginal = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(docOriginal);
builder->Writeln(u"This is the original document.");

auto docEdited = System::MakeObject<Aspose::Words::Document>();
builder = System::MakeObject<Aspose::Words::DocumentBuilder>(docEdited);
builder->Writeln(u"This is the edited document.");

// Der Vergleich von Dokumenten mit Revisionen löst eine Ausnahme aus.
if (docOriginal->get_Revisions()->get_Count() == 0 && docEdited->get_Revisions()->get_Count() == 0)
{
    docOriginal->Compare(docEdited, u"authorName", System::DateTime::get_Now());
}

// Nach dem Vergleich erhält das Originaldokument eine neue Revision
// für jedes Element, das im bearbeiteten Dokument unterschiedlich ist.
for (auto&& r : System::IterateOver(docOriginal->get_Revisions()))
{
    std::cout << System::String::Format(u"Revision type: {0}, on a node of type \"{1}\"", r->get_RevisionType(), r->get_ParentNode()->get_NodeType()) << std::endl;
    std::cout << System::String::Format(u"\tChanged text: \"{0}\"", r->get_ParentNode()->GetText()) << std::endl;
}

// Das Akzeptieren dieser Revisionen verwandelt das Originaldokument in das bearbeitete Dokument.
docOriginal->get_Revisions()->AcceptAll();

ASSERT_EQ(docOriginal->GetText(), docEdited->GetText());
```

## Siehe auch

* Class [RevisionCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
