---
title: "Aspose::Words::Story::get_StoryType Methode"
linktitle: "get_StoryType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Story::get_StoryType Methode. Gibt den Typ dieser Story in C++ zurück."
type: docs
weight: 7000
url: /de/cpp/aspose.words/story/get_storytype/
---
## Story::get_StoryType method


Ermittelt den Typ dieser Geschichte.

```cpp
Aspose::Words::StoryType Aspose::Words::Story::get_StoryType() override
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

* Enum [StoryType](../../storytype/)
* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
