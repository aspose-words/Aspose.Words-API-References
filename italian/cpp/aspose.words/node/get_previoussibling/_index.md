---
title: "Metodo Aspose::Words::Node::get_PreviousSibling"
linktitle: "get_PreviousSibling"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Node::get_PreviousSibling. Ottiene il nodo immediatamente precedente a questo nodo in C++."
type: docs
weight: 11000
url: /it/cpp/aspose.words/node/get_previoussibling/
---
## Node::get_PreviousSibling method


Ottiene il nodo immediatamente precedente a questo nodo.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::get_PreviousSibling()
```


## Esempi



Mostra come utilizzare i metodi di [Node](../) e [CompositeNode](../../compositenode/) per rimuovere una sezione prima dell'ultima sezione nel documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Section 1 text.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakContinuous);
builder->Writeln(u"Section 2 text.");

// Entrambe le sezioni sono fratelli l'una dell'altra.
auto lastSection = System::ExplicitCast<Aspose::Words::Section>(doc->get_LastChild());
auto firstSection = System::ExplicitCast<Aspose::Words::Section>(lastSection->get_PreviousSibling());

// Rimuovi una sezione in base al suo rapporto di fratellanza con un'altra sezione.
if (lastSection->get_PreviousSibling() != nullptr)
{
    doc->RemoveChild<System::SharedPtr<Aspose::Words::Section>>(firstSection);
}

// La sezione che abbiamo rimosso era la prima, lasciando il documento con solo la seconda.
ASSERT_EQ(u"Section 2 text.", doc->GetText().Trim());
```

## Vedi anche

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
