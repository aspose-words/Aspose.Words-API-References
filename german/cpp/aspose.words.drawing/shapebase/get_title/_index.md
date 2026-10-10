---
title: "Aspose::Words::Drawing::ShapeBase::get_Title Methode"
linktitle: "get_Title"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeBase::get_Title Methode. Gibt den Titel (Beschriftung) des aktuellen Formobjekts zurück oder setzt ihn in C++."
type: docs
weight: 51000
url: /de/cpp/aspose.words.drawing/shapebase/get_title/
---
## ShapeBase::get_Title method


Ruft den Titel (Beschriftung) des aktuellen Formobjekts ab oder legt ihn fest.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_Title()
```

## Hinweise


Standard ist ein leerer String.

Darf nicht **null** sein, kann aber eine leere Zeichenkette sein.

## Beispiele



Zeigt, wie man den Titel einer Form festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Erstellen Sie eine Form, geben Sie ihr einen Titel und fügen Sie sie dann dem Dokument hinzu.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Cube);
shape->set_Width(200);
shape->set_Height(200);
shape->set_Title(u"My cube");

builder->InsertNode(shape);

// Wenn wir ein Dokument mit einer Form speichern, die einen Titel hat,
// Aspose.Words speichert diesen Titel im Alt-Text der Form.
doc->Save(get_ArtifactsDir() + u"Shape.Title.docx");

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.Title.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_EQ(System::String::Empty, shape->get_Title());
ASSERT_EQ(u"Title: My cube", shape->get_AlternativeText());
```

## Siehe auch

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
