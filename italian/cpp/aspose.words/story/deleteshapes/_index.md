---
title: "Metodo Aspose::Words::Story::DeleteShapes"
linktitle: "DeleteShapes"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Story::DeleteShapes. Elimina tutte le forme dal testo di questa storia in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words/story/deleteshapes/
---
## Story::DeleteShapes method


Elimina tutte le forme dal testo di questa storia.

```cpp
void Aspose::Words::Story::DeleteShapes()
```


## Esempi



Mostra come rimuovere tutte le forme da un nodo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Usa un DocumentBuilder per inserire una forma. Questa è una forma inline,
// che ha un Paragraph genitore, che è un nodo figlio del Body della prima sezione.
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 100.0, 100.0);

ASSERT_EQ(1, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());

// Possiamo eliminare tutte le forme dai paragrafi figli di questo Body.
ASSERT_EQ(Aspose::Words::StoryType::MainText, doc->get_FirstSection()->get_Body()->get_StoryType());
doc->get_FirstSection()->get_Body()->DeleteShapes();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
```

## Vedi anche

* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
