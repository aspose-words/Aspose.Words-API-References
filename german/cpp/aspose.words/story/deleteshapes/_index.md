---
title: "Aspose::Words::Story::DeleteShapes Methode"
linktitle: "DeleteShapes"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Story::DeleteShapes Methode. Löscht alle Formen aus dem Text dieser Story in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words/story/deleteshapes/
---
## Story::DeleteShapes method


Löscht alle Formen aus dem Text dieser Geschichte.

```cpp
void Aspose::Words::Story::DeleteShapes()
```


## Beispiele



Zeigt, wie man alle Formen aus einem Knoten entfernt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Verwenden Sie einen DocumentBuilder, um eine Form einzufügen. Dies ist eine Inline-Form,
// die einen übergeordneten Absatz hat, der ein Kindknoten des Body der ersten Abschnitts ist.
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 100.0, 100.0);

ASSERT_EQ(1, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());

// Wir können alle Formen aus den Kindabsätzen dieses Body löschen.
ASSERT_EQ(Aspose::Words::StoryType::MainText, doc->get_FirstSection()->get_Body()->get_StoryType());
doc->get_FirstSection()->get_Body()->DeleteShapes();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
```

## Siehe auch

* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
